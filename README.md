# cap-scraper
A simple Discord scraper bot for Solana

## Features
- Scrapes token-related content from Discord
- Encrypted private-key support (`--encrypt-key`)
- Simple setup via `config.toml` and `ignored_tokens.txt`

## Quick Start

1. **Give the executable permission to run**
   ```bash
   chmod +x *
   ```

2. **Encrypt your private key**
   ```bash
   ./cap-scraper --encrypt-key [your_private_key]
   ```

3. **Set your ignored pubkeys**
   ```bash
   nano ignored_tokens.txt
   ```
   Add **one mint pubkey per line** to ignore it (no names or symbols).

4. **Configure your settings**
   ```bash
   nano config.toml
   ```
   Use the minimal config below.

5. **Run the bot**
   ```bash
   ./cap-scraper
   ```

## Files
- `cap-scraper` — main executable  
- `config.toml` — runtime configuration  
- `ignored_tokens.txt` — **pubkeys only**, one per line  

## Example Templates

**ignored_tokens.txt** (pubkeys only)
```
# One pubkey per line. Lines starting with # are comments.
So11111111111111111111111111111111111111112
EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v
Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB
```

**config.toml**
```toml
# Minimal config for cap-scraper

# Discord bot token (keep secret; do not commit)
discord_token = ""

# Allowed Discord channel IDs (as strings)
discord_channels = [
  "1409939729771925545",
]

# Amount threshold or unit (project-specific meaning)
amount = 1_000_000

# Retry attempts for transient operations
retries = 3
```


## License
MIT License
