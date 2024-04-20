# Chapter 3 The Cortex-M4 Instruction Set

### 3.3.6 PC-relative expressions

- A PC-relative expression or *label* is a symbol that represents the address of an instruction or literal data.

- It is represented in the instruction as the PC value plus or minus a numeric offset.

- Ther assembler calculates the required offset from the label and the address of the current instruction.

- If the offset is too big, the assembler produces an error.

> ##### Note
>
> - For `B`, `BL`, `CBNZ`, and `CBZ` instructions, the value of the PC is the address of the current instruction plus 4 bytes.
>
> - For all other instructions that use labels, the value of the PC is the address of the current instruction plus 4 bytes, with bit[1] of the result cleared to 0 to make it word-aligned.
>
> - Your assembler might permit other syntaxes for PC-relative expressions, such as label plus or minus a number, or an expression of the form `[PC, #number]`.
