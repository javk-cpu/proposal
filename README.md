# proposal

We intend to design an 8-bit CPU with a 16-bit data bus.  To achieve the
following, we will be making the following design decisions:


## Registers

We plan to have 10 total registers, of that, we will dedicate three
16-bit registers, two 16-bit registers that can be divided into two
8-bit registers each, two 8-bit registers, and a zero register which
acts as an 8-bit or 16-bit register depending on the use case.

The `A` register is arguably the most important as it is the accumulator
and where all arithmetic operation results will be stored.  These
operations will also set the appropriate arithmetic flags in the `F`
register.

The `BC` and `DF` are the two 16-bit registers that can be individually
addressed at the byte level as either `B`, `C`, `D`, or `F`.

The `SP` is the stack pointer.

The `FP` is the frame pointer.

The `PC` is the program counter.

The `ZR` is both an 8-bit and 16-bit register depending on the use case.
Its value is always set to the constant `0`.


```
Register Map:

+---+ +---+
| A | | F |
+---+ +---+
+---------+
|  B | C  |
+---------+
+---------+
|  D | F  |
+---------+
+---------+
|   S P   |
+---------+
+---------+
|   F P   |
+---------+
+---------+
|   P C   |
+---------+
+---------+
| ZR | ZR |
+---------+
```


## Copyright & Licensing

Copyright (C) 2022  Jacob Koziej [`<jacobkoziej@gmail.com>`]

Copyright (C) 2022  Ani Vardanyan [`<ani.var.2003@gmail.com>`]

Licensed under the [CC BY-NC-SA 4.0].


[`<jacobkoziej@gmail.com>`]: mailto:jacobkoziej@gmail.com
[`<ani.var.2003@gmail.com>`]: mailto:ani.var.2003@gmail.com
[CC BY-NC-SA 4.0]: https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode
