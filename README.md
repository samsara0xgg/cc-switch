# cc-switch

Claude Code API key switcher — quickly switch between multiple Anthropic API keys and proxy endpoints.

## Features

- Switch between saved API keys interactively
- Support for official Anthropic API and third-party proxies
- Per-key environment settings (model overrides, autocompact, etc.)
- Saves keys to `~/.claude/api_keys.json`, reads settings from `~/.claude/settings.json`
- Interactive TUI via `questionary`, falls back to plain CLI if not installed

## Install

```bash
pip install questionary   # optional but recommended for interactive UI
```

## Usage

```bash
python switch_api.py
```

**Options:**
- Switch to a saved key
- Switch to official Anthropic API
- Add a new API key (official or proxy)

## Key Storage

Keys are saved in `~/.claude/api_keys.json`:

```json
{
  "work": {
    "key": "sk-ant-...",
    "official": true,
    "base_url": "",
    "quota_url": "https://console.anthropic.com/settings/billing"
  },
  "proxy": {
    "key": "sk-...",
    "official": false,
    "base_url": "https://api.example.com",
    "quota_url": ""
  }
}
```
