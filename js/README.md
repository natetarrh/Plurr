JavaScript Plurr Implementation
===============================

Usage
-----

```JavaScript

var p = new Plurr(); // English locale is set by default
var s, out;

s = "{N_PLURAL:{N} file|{N} files}";
out = p.format(s, {"N": 1}); // => "1 file"
out = p.format(s, {"N": 2}); // => "2 files"
out = p.format(s, {"N": 5}); // => "5 files"

p.setLocale("ru"); // switch to Russian locale

s = "{N_PLURAL:{N} файл|{N} файла|{N} файлов}";
out = p.format(s, {"N": 1}); // => "1 файл"
out = p.format(s, {"N": 2}); // => "2 файла"
out = p.format(s, {"N": 5}); // => "5 файлов"
```