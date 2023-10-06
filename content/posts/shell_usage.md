---
title: shell usage
date: 2023-09-10
---
# hello world
```bash
#!/bin/bash
echo "Hello World !"
```
# variables
```bash
user=$(whoami)
```
# functions
```bash
function hello {
    echo "hello, $(whoami)"
}
```
# other
## fancy date
```bash
date +"%A, %d %B %Y %H:%M:%S:%N %p %z %Z Week:%W Day:%j Epoch:%s %t"
```