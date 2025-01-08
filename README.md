# vsdsquadron-mini-internship
Mini internship (RISC V toolchain intro)
<details Task1>
  <summary><b>Task 1</b></summary>
  
  ### Details of `sum1ton.c` and `sum1ton.o`:

  1. **Source Code: `sum1ton.c`**
     - This is the source code file written in C, which contains a function to calculate the sum of the first `n` natural numbers.
     - Example code:
       ```c
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

  2. **Compilation Details:**
     - The source file `sum1ton.c` is compiled into an object file `sum1ton.o` using the following compilers:

       - **Using `gcc`:**
         - Command: `gcc -c sum1ton.c -o sum1ton.o`
         - Description: This generates an object file `sum1ton.o` for the host machine's architecture (x86_64).
         - Output: The object file contains machine code specific to the host architecture.

       - **Using `riscv64-unknown-elf-gcc`:**
         - Command: `riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c`
         - Description: This generates an object file `sum1ton.o` specifically for the RISC-V architecture.
         - Output: The object file contains machine code that is compatible with the RISC-V architecture.

  3. **Differences in Output Files (`sum1ton.o`):**
     - **Format**: The output file format depends on the target architecture (e.g., ELF for RISC-V, ELF for x86_64).
     - **Instruction Set**: The machine instructions in the `.o` file will differ based on the target architecture:
       - `gcc` generates instructions for the host architecture.
       - `riscv64-unknown-elf-gcc` generates instructions for the RISC-V architecture.

  4. **Further Notes:**
     - The object file `sum1ton.o` can be linked to create an executable for the corresponding architecture.
     - Cross-compilation using `riscv64-unknown-elf-gcc` is commonly used in embedded systems development for the RISC-V target.
</details>


