### Normal find file:
```
find <location> -name <name you want to find>
```
e.g.,
```
find . -name README.md
```

### Sometimes you want to search within files:
```
find . -type f -exec grep -Hn "main" {} \;
```
Searches (recursively) files with the word "main" within it. `-H` prints the filename; `-n` prints the line number where the pattern is found.

### And if you want to exclude certain files:
```
find . -type f -exec grep -Hn "main" {} \; | grep -v "CMake"
```
The `-v` means "excludes". So the above command search for the word "main" in all files in this directory (recursive) and excludes ones that is in file names with "CMake".

### Cleaner output:
If `-Hn` gives you output that is too much stuff, `-l` will also work and only show you file names, like so:
```
find . -type f -exec grep -l "main" {} \; | grep -v "CMake"
```

### Additional flags:
- `-i` flag for `grep` will make the grep case insensitive.
