coe files and waveform configurations files

**new.coe contains the following instructions:**<br>
(Generic instructions)

li r1, 6   Loads the immediate value 6 into register r1.<br>
li r2, 6   Loads the immediate value 6 into register r2.<br>
add r3, r1, r2  Adds the values stored in registers r1 and r2 and stores the result in register r3.<br>
bne r1, r2, 0   Branches to offset 0 if the values in registers r1 and r2 are not equal.<br>
beq r1, r2, 0  Branches to label 0 if the values in registers r1 and r2 are equal. (since offset is 0, nothing happens)<br>
<br>
lui r8, 4  Loads the immediate value 4 shifted left by 16 bits into the upper 16 bits of register r8<br>
lui r10, 8   Loads the immediate value 8 shifted left by 16 bits into the upper 16 bits of register r10.<br>
or r8, r5, r10   Bitwise OR operation between the values in registers r5 and r10, result stored in register r8.<br>
rol r5, r6, 1  Bitwise rotate left operation on the value in register r6 by 1 bit, result stored in register r5.<br>
ror r6, r5, 1  Bitwise rotate right operation on the value in register r5 by 1 bit, result stored in register r6.<br>
sw r5, 4(r10)   Stores the value in register r5 into memory at the address formed by adding 4 to the value in register r10.<br>




mycoe.coe contains the following instructions:<br>
(Instructions to test sw, lw, lb. Although sb is not tested, it works with this implementation) <br>

li r1 , 4  Loads the immediate value 4 into register r1.<br>
addir r5, r1, 4096   Adds the immediate value 4096 to the value stored in register r1 and stores the result in register r5.<br>
sw r5, 4(r1)   Stores the value in register r5 into memory at the address formed by adding 4 to the value in register r1.<br>
lw r4, 4(r1)   Loads a word from memory at the address formed by adding 4 to the value in register r1 and stores it in register r4.<br>
lb r6 , 4(r1)  Loads a byte from memory at the address formed by adding 4 to the value in register r1 and stores it in the lower 8 bits of register r6.<br>
lb r6, 5(r1)   Loads a byte from memory at the address formed by adding 5 to the value in register r1 and stores it in the lower 8 bits of register r6.<br>
