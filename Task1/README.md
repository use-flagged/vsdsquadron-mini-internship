# First week
Tasks related to compiling [riscv-tools](https://github.com/kunalg123/riscv_workshop_collaterals/blob/master/run.sh)
and compiling a bare metal `C - program` using GCC and using FOSS tools to compile the same `C - program` using `riscv64-unknown-elf-gcc`.

## sum1ton.c
```C
#include <stdio.h>

int main(){
    int i, sum = 0, n = 5;
    for ( i = 1; i <= n; ++i ){
        sum += i;
    }
    printf("Sum is %d\n", sum);
    return 0;

}
```
