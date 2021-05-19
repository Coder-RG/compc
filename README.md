# compc
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE) [![made-with-bash](https://img.shields.io/badge/Made%20with-Bash-1f425f.svg)](https://www.gnu.org/software/bash/) [![GitHub tag](https://img.shields.io/github/tag/Coder-RG/compc.svg)](https://GitHub.com/Coder-RG/compc/tags/)



**This may only work in bash**

Compiling C program using `gcc` creates an output file, which needs
to be run separately.  
This really annoyed me hence, I wrote this
bash file so the C file runs after compilation.

There still are some features that need to be introduced.  
Please contribute if you may be willing to or raise an issue.

### How to make it work(clone this repo first)
- First change directory to this project.

- Open the terminal and write
```bash
pwd
```
- Add this project to the PATH variable
```bash
export PATH=$PATH:<path-to-this-project>
```
If your path to this project is `/home/<username>/compc` then, use `export PATH=$PATH:/home/<username>/compc`.
- This way of exporting is not permanent. To make it permanent,
update the .bashrc file with the export command at the end of the file.

**NOTE:** .bashrc file is an integral part of bash. Please do not play with it.

### Trying it out!

```bash
compc <file_name>
```
- If your file_name is test.c then,
```bash
compc test.c
```

### Some example code

Create a new file and copy this code.(ex. test.c)

```C
#include<stdio.h>

int main()
{
  printf("Hello, World!");
  return 0;
}
```
Then run it using compc

```bash
compc test.c
```

If everything is set up correctly, then it should show _Hello, World!_ as output.

### You reached here!

The bash file works somewhat like,
1. It uses `gcc <file_name>.c -o file_name`
2. It then simply runs the file using `./file_name`

**Explore the file and contribute since this lacks many features.**
