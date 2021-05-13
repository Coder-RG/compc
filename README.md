# compc
**This will only work in linux terminal**

Compiling C program using `gcc` creates an output file, which needs
to be run separately.  
This really annoyed me hence, I wrote this
bash file so the C file runs after compilation.

There still are some features that need to be introduced.  
Please contribute if you may be willing to or raise an issue.


### How to make it work
- Open the terminal and write
```bash
echo $HOME
```
- Check if `$HOME/.local/bin` exists in the path.

- If it doesn't then do the following (not permanent)
```bash
export $PATH=$PATH:$HOME/.local/bin
```
- Copy `compc` to the `$HOME/.local/bin` directory.

Now this should work without any hassle.


### Trying it out!

```bash
compc <file_name>
```
- If you file_name is test.c then,
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

If everything is set up correctly, then it should show _Hello, World!_  
as output.

### You reached here!

The bash file works somewhat like,
1. It uses `gcc <file_name>.c -o file_name`
2. It then simply runs the file using `./file_name`

**Explore the file and contribute since this lacks many features.**
