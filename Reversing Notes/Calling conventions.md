

examples will be presented on this c pseudo code.
```c
int test(int x, int y, int z);
int a, b, c, ret;
ret = test(a, b, c);
```

# cdecl
- arguments are pushed on to the stack ***from right to left***
- ***caller cleans up*** the stack 
- when the function is complete the *result* is stored in **eax***

example:

```asmatmel
push c
push b
push a
call test
add esp, 12
mov ret, eax
```

# stdcall
pretty much same as [[#cdecl]] although the ***[[Words and definitions#^ca1e96|calle]]*** is required to clean up the stack

# fastcall
- usually first two arguments are being passed in **edx** and **ecx**
- additional arguments are loaded from right to left 
- caller (calling function) is usually responsible for cleaning up the stack 