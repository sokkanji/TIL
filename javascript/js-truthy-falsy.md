```bash
# empty string
> ("")? true : false
false
```

```bash
# Number 0
> (0)? true : false
false
```
                   
```bash
# String "0"
> ("0")? true : false
true
```

```bash
# JavaScript null
> (null)? true : false
false
```

```bash
# any other String
> ("someText")? true : false
true
```

```bash
# a space character
> (" ")? true : false
true
```
