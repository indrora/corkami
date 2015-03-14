# x86/x64 oddities #
| **OPCODE**| **DESCRIPTION**| **EXAMPLE** |
|:----------|:---------------|:------------|
| _66 0f??:_ [bswap](http://code.google.com/p/corkami/wiki/x86oddities#bswap) `<`reg16`>` | xor `<`reg16`>`, `<`reg16`>` | _66 0fc8:_ bswap ax |
| _d5??:_ [aad](http://code.google.com/p/corkami/wiki/x86oddities#aad) `<`imm8`>` | ax = ah `*` `<`imm8`>` + al | _d507:_ aad 7 |
| _d4??:_ [aam](http://code.google.com/p/corkami/wiki/x86oddities#aam) `<`imm8`>` | ah, al = al / `<`imm8`>`, al % `<`imm8`>` | _d403:_ aam 3 |
| _f1:_ [IceBp](http://code.google.com/p/corkami/wiki/x86oddities#IceBP) | SINGLE STEP exception after execution | ... |
| _d6:_ [setalc](http://code.google.com/p/corkami/wiki/x86oddities#salc) | sbb al, al | ... |
| _0f 19-1f `*`:_ [hint nop](http://code.google.com/p/corkami/wiki/x86oddities#hint_nop) .... | nop | _0f1980 00000080:_ nop `[`eax + 8000000h`]` |
| _0f 20-24 ??:_ [mov](http://code.google.com/p/corkami/wiki/x86oddities#mov) to/from control/debug register | memory operand ignored | _0f 2000:_ mov eax, cr0 |
| _8c ??:_ [mov](http://code.google.com/p/corkami/wiki/x86oddities#mov) to/from segment | upper register cleared | _8cc8:_ mov eax, cs |
| _66 `*`:_ [jmp/retn/call](http://code.google.com/p/corkami/wiki/x86oddities#16b_flow) | jump to IP | _66 e9 fcff:_ jmp ip |
| [smsw/sidt/str/sgdt/sldt/lsl/str](http://code.google.com/p/corkami/wiki/x86oddities#os/tool/vm_detection) | OS/VM detection | ... |

## 64 bits ##
| **OPCODE**| **DESCRIPTION**| **EXAMPLE** |
|:----------|:---------------|:------------|
| [cs = 33h](http://code.google.com/p/corkami/wiki/x86oddities#switching_between_32b_and_64b_modes) (Windows) | 64b mode | _9a `<`addr32`>`3300:_ call 0033:`<`addr32`>` |
| (no REX) _63 ??:_ movsxd `<`reg64`>`, `<`reg32`>` | mov `<`reg32`>`, `<`reg32`>` | _63c8:_ movsxd ecx, eax |

###### Ange Albertini, http://corkami.com ######