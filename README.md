# Regex 
The Regex addon adds support for Perl regular expressions
using the <a href=http://www.pcre.org/>PCRE</a> library by Philip Hazel.</p>

### Example 1
```Io
Io> re := "is.*a" asRegex
Io> "This is a test. This is also a test." \
    matchesOfRegex(" is[^.]*a") replaceAllWith(" is not a")
==> "This is not a test. This is not a test.
```

### Example 2

```Io
Io> "11aabb" matchesOfRegex("aa*")
==> list("a", "a")

Io> re := "(wom)(bat)" asRegex
Io> "wombats are cuddly" matchesOfRegex(re) replaceAllWith("$2$1!")
==> batwom!s are cuddly
```

# Installation
`pcre` should be installed and foundable in your system. Then:
```
eerie install https://github.com/IoLanguage/Regex.git
```
