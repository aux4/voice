# voice say

## with message argument

### should speak text from positional argument

```execute
aux4 voice say "test"
```

## with message flag

### should speak text from message flag

```execute
aux4 voice say --message "test"
```

## with voice

### should speak text with a specific voice

```execute
aux4 voice say --voice Fred "test"
```

## with stdin

### should speak text from stdin

```execute
echo "test" | aux4 voice say
```

### should speak text from stdin with voice

```execute
echo "test" | aux4 voice say --voice Fred
```
