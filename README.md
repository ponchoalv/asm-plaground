## Testing Assembly arm64 in macOs

This is a little project I'm playing with for the first time.


### some useful commands I used (maybe worth to have them in a Makefile)


#### compile to table object

```bash
as -o func.o func.s
```

#### Linking the object table created by as command

```bash
ld -o func func.o -lSystem -syslibroot `xcrun -sdk macosx --show-sdk-path` -e _start -arch arm64
```

