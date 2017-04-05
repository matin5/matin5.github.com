---
layout     : post
title      : "語法測試"
subtitle   : "測試 Jekyll 支援 Syntax Highligh"
date       : 2017-02-11 11:01:00
author     : "Martin Wu"
tags       : Syntax
comments   : true
#signature  : true
---

#### C Language
```c
#include <stdio.h>

int main(int argc, char* argv[]) {
  char str[] = "Hello World";
  printf("%s\n", str);
  return 0;
}
```

#### Objective-C
```objective-c
NSString *str = @"Hello World";
NSLog(@"%@", str);
```
---

#### JavaScript
```javascript
var str = "Hello World";
console.log(str);
```

#### Python
```python
str = "Hello World"
print(str)
```

#### Console
```console
$ ls -l                                                                
total 48
-rw-r--r--   1 wu  staff  327  2 11 19:54 404.html
-rw-r--r--   1 wu  staff    0  2 11 20:58 CNAME
-rw-r--r--   1 wu  staff  106  2 11 21:26 README.md
-rw-r--r--   1 wu  staff  597  2 11 21:26 _config.yml
drwxr-xr-x   4 wu  staff  136  2 11 19:54 _includes
drwxr-xr-x   5 wu  staff  170  2 11 19:54 _layouts
drwxr-xr-x   3 wu  staff  102  2 11 21:49 _posts
drwxr-xr-x  10 wu  staff  340  2 11 21:45 _site
-rw-r--r--   1 wu  staff   37  2 11 21:28 about.md
-rw-r--r--   1 wu  staff  723  2 11 19:54 atom.xml
-rw-r--r--   1 wu  staff  947  2 11 19:54 index.html
drwxr-xr-x   5 wu  staff  170  2 11 19:54 public
```
