# voice list

## without filter

### should list all available voices

```execute
aux4 voice list
```

```expect:partial
Samantha *?
```

## with language filter

### should filter voices by language code

```execute
aux4 voice list en_US
```

```expect:partial
Samantha *?
```

### should filter voices by partial language code

```execute
aux4 voice list pt
```

```expect:partial
Luciana *?
```

### should be case insensitive

```execute
aux4 voice list EN_US
```

```expect:partial
Samantha *?
```
