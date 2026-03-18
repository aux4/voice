# aux4/voice

Text-to-speech CLI tool for aux4. Speak text from the command line or pipe text from other commands.

- **macOS** — uses the built-in `say` command
- **Linux** — uses `espeak` (installed automatically)

## Installation

```bash
aux4 aux4 pkger install aux4/voice
```

## Quick Start

```bash
# Speak a message
aux4 voice say "Hello, World!"

# Pipe text from another command
echo "Hello from a pipe" | aux4 voice say

# Use a specific voice
aux4 voice say --voice Fred "Welcome to aux4"

# List available voices
aux4 voice list

# Filter voices by language
aux4 voice list en
```

## Commands

### say

Speak text using text-to-speech. Accepts text as a positional argument, via `--message`, or piped from stdin.

```bash
aux4 voice say "Your text here"
aux4 voice say --message "Your text here"
echo "Hello" | aux4 voice say
aux4 voice say --voice Daniel "Good morning"
```

| Parameter | Description | Default |
|-----------|-------------|---------|
| `--message` | The text to speak (also accepts positional arg) | *(stdin)* |
| `--voice` | The voice to use | Samantha (macOS), en (Linux) |

### list

List all available text-to-speech voices. Optionally filter by language code.

```bash
aux4 voice list
aux4 voice list en
aux4 voice list pt
```

| Parameter | Description | Default |
|-----------|-------------|---------|
| `--language` | Filter by language code (e.g., en, pt, ja) | *(show all)* |
