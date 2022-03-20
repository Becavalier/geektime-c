* ABI - 不遵循 ABI 的程序能否运行？ - 0x1：
```c
// sub.c
int sub(int x, int y) {
  return x - y;
}
```

* ABI - 不遵循 ABI 的程序能否运行？ - 0x2：
```asm
# main.asm
extern sub
global _start
section .text
_start:
  and   rsp, 0xfffffffffffffff0
  sub   rsp, 1
  mov   esi, 2  # the 1st param.
  mov   edi, 1  # the 2nd param.
  call  sub
  mov   edi, eax
  mov   eax, 60
  syscall
```


