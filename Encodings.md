[<< index](http://code.google.com/p/corkami/) [Android/Java/x86/... opcodes tables](http://opcodes.corkami.com) [PDF tricks](http://pdf.corkami.com) [Portable Executable](http://pe.corkami.com) [x86 oddities](http://x86.corkami.com) (this project is done in my spare time. **[Support ](http://code.google.com/p/corkami/wiki/About#Support_Corkami)** it!)

# Encodings #
  * This page ([printable version](http://code.google.com/p/corkami/wiki/Encodings?show=content) [wiki source](http://corkami.googlecode.com/svn/wiki/Encodings.wiki)) explains curious encodings or encoded files.


# JavaScript #
## jjencode ##
![https://corkami.googlecode.com/svn/wiki/pics/misc_jjencode.png](https://corkami.googlecode.com/svn/wiki/pics/misc_jjencode.png)

JJEncode is a JavaScript encoding by Yosuke Hasegawa that turns standard javascript into symbol-only code, including the decoder.

  * [commented source code](https://corkami.googlecode.com/svn/trunk/asm/encodings/jjencode.txt)

# COM #
Not the ActiveX thingy, but the old headerless binaries from DOS (and Windows XP or before)

## aa86 ##
![https://corkami.googlecode.com/svn/wiki/pics/misc_aa86.png](https://corkami.googlecode.com/svn/wiki/pics/misc_aa86.png)

Aa86 is a .COM file encoder by Yosuke Hasegawa that encodes binaries using only symbols characters, with a decoder.

so for example, a simple `hello world` binary is encoded as:
```
%@"%"@,~,%,!`_^[^_^]-;>`_^[^_^]%"!,^,:`_^[^_^]-@{-`{-?:`_[^_^]_-``-``-@@`_^[^_^]-`~-``-@$`_^[^_^]-``-``-@@`_^[^_^]-`~-``-@#`_^[^_^]-+~-/~-?;`_^[^_^]%!~-;-,;`_^[^_^]-"$-@~-@``_^[^_^]-{[-);-@:`_^[^_^]-/*,%`_^[^_^]`_^[^_^]`_^[^_^]`_^[^_^]%@$-@;-?;`_^[^_^]-/~-`&,#`_^[^_^]-`~-`{,*`_^[^_^]-@@-$!`_^[^_^]-:$,[,<`_^[^_^]-!|-.),!`_^[^_^]-@{-@`-/(`_^[^_^]`_^[^_^]`_^[^_^]`_^[^_^]-{!-{.,.`_^[^_^]-~/-/``_^[^_^]%""-}@$"`_^[^_^]%@@-!/,!`_^[^_^]-:*-=%`[[[[[[[[`^^^^^-%+)@@^^^!;@@_!,((,.((-$+)@*+@!!@-,!"(+@@,$-,!"($%&,&,&_&@"'%_&"',&$&!"-@*@$"
```

  * [commented assembly source](https://corkami.googlecode.com/svn/trunk/asm/encodings/aa86.asm)
  * [standalone encoder](https://corkami.googlecode.com/svn/trunk/asm/encodings/aa86.py)

### aa86-based dropper ###
![https://corkami.googlecode.com/svn/wiki/pics/misc_aa86drop.png](https://corkami.googlecode.com/svn/wiki/pics/misc_aa86drop.png)

Using Aa86 and a simple .COM dropper, it's possible to make an embedded PE not only non-null, but even typeable.

Example of an Aa86-encoded dropper with embedded PE:
```
%@"%"@,~,%,!`_^[^_^]-;>`_^[^_^]%"!,^,:`_^[^_^]-@{-`{-?:`_[^_^]_-``-``-@@`_^[^_^]-`~-``-@$`_^[^_^]-``-``-@@`_^[^_^]-`~-``-@#`_^[^_^]-+~-/~-?;`_^[^_^]%!~-;-,;`_^[^_^]-"$-@~-@``_^[^_^]-{[-);-@:`_^[^_^]-/*,%`_^[^_^]`_^[^_^]`_^[^_^]`_^[^_^]%@$-@;-?;`_^[^_^]-/~-`&,#`_^[^_^]-`~-`{,*`_^[^_^]-@@-$!`_^[^_^]-:$,[,<`_^[^_^]-!|-.),!`_^[^_^]-@{-@`-/(`_^[^_^]`_^[^_^]`_^[^_^]`_^[^_^]-{!-{.,.`_^[^_^]-~/-/``_^[^_^]%""-}@$"`_^[^_^]%@@-!/,!`_^[^_^]-:*-=%`[[[[[[[[`^^^^^-%+)@@^^^!;!@%+.@_!*+@(!@$+)@-,!"$+*$,+--"@)(#.!(#,@(@@!,+.$@-,!"$+,#)+@@@@*+&&!@-,!""'(##*"&!@+(.!"&!@.!$+@$*+)*!@)+,@!@-,!"_!"'#"$+.#+(.!"&!@-,!""')!.!'@++-&!@,(_%$@,(_%(@,(_%,@$++$@+@@*+&&!@-,!""'@@(+!@,$-,!"@@@@@@@@%$@%."%$(%%$@@@@@@@(@@@@@@,%@@@@@@,&@@@@@@@@@@@@@@@@@"#"@"$&"'_&@'@')&.&'&@"@%%$@"("&&"'_&-&@"!#&#"&)&$'@"."#$_$-$@"&&)&,&%&)"-@-@*@$"-$*%@@@@@%%$@@@@,$!@@@@@-&#'&'#&"'$'."$&,&,&@@@@@@@@"@!@+@!@(&$.@@@$@@__%!$$@@@$@@+.)@@@.!@@@@@@@@@@@@@@#($,$@#,@@@@@$@@$@@@@@@@$@@@@@@@!&@@@@@@@@@@@@@@$@@@@@@@@@@@@@@@,@!@@@@@+@!@@@@@@@@@@@@@#@@@@@@'"')&.&$'&&@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@-@@@@@@@@@@@@@@@@@@@@@@@((@@@@@@$$@@@@@@@@@@@@@@@@@@@@@@,@@@@@@@$$@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@$$@@@@@@(@@@@@@@@"#"@"$&"'_&@'@'%&$&@"@%%$@"("##"#"&@"@%%$@"&&)&,&%&)"*@@@@@@@@@@@@@@@@@@@@@@@@@
```

## EICAR ##
![https://corkami.googlecode.com/svn/wiki/pics/misc_eicar2.png](https://corkami.googlecode.com/svn/wiki/pics/misc_eicar2.png)

the EICAR file is a tiny test file that is made of printable characters and prints the eicar test string.

  * [commented assembly source](https://corkami.googlecode.com/svn/trunk/asm/encodings/eicar.asm)

```
X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
```
### EICAR2 ###
Peter Ferrie rewrote the EICAR file, smaller this time, as the test string itself is executed in this new version.
```
5T2)D4)D65Z3PZEICAR-STANDARD-ANTIVIRUS-TEST-FILE!$UX!T!S
```

  * [commented assembly source](https://corkami.googlecode.com/svn/trunk/asm/encodings/eicar2.asm)

---

# acknowledgements #
  * Peter Ferrie
  * [Yosuke Hasegawa](http://utf-8.jp/)

[<< index](http://code.google.com/p/corkami/) [Android/Java/x86/... opcodes tables](http://opcodes.corkami.com) [PDF tricks](http://pdf.corkami.com) [Portable Executable](http://pe.corkami.com) [x86 oddities](http://x86.corkami.com) (this project is done in my spare time. **[Support ](http://code.google.com/p/corkami/wiki/About#Support_Corkami)** it!)