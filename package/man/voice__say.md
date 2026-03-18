#### Description

The `say` command speaks text aloud using text-to-speech. It accepts text as a positional argument, via the `--message` flag, or piped from stdin.

When no message is provided, the command reads from stdin, allowing it to be chained with other commands using pipes.

Run `aux4 voice list` to see all available voices on your system.

#### Usage

```bash
aux4 voice say [<message>] [--voice <voice>]
```

--message  The text to speak. Can also be passed as a positional argument. If omitted, reads from stdin
--voice    The voice to use (default: Samantha on macOS, en on Linux)

#### Example

```bash
aux4 voice say "Hello, World!"
```

```bash
aux4 voice say --voice Daniel "Good morning"
```

```bash
echo "Text from a pipe" | aux4 voice say
```
