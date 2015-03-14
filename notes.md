# Formats #
# Tools #
  * **file format** [hachoir](https://bitbucket.org/haypo/hachoir/wiki)
  * **hash** [hashcat](http://hashcat.net/hashcat/) [FsumFE](http://fsumfe.sourceforge.net/)

  * **forensics** [moonsols](http://www.moonsols.com/ressources) [volatility](https://www.volatilesystems.com/default/volatility)

  * **ASM** [x86ref](http://ref.x86asm.net/index.html) [Siyobik](http://siyobik.info/main/reference) [Sandpile](http://sandpile.org/)
  * **disasm** [XED](http://software.intel.com/en-us/articles/intel-software-development-emulator/) [diStorm](http://ragestorm.net/distorm/) (3=GPL/2=BSD) [BeaEngine](http://www.beaengine.org/)

  * **Java** [dirty JOE](http://dirty-joe.com/) [reJ](http://rejava.sourceforge.net/)
  * **Android** [kivlad](http://www.matasano.com/research/kivlad/) [smali](http://code.google.com/p/smali/) [dedexer](http://dedexer.sourceforge.net/)

  * **Office** OffVis
  * **PiNG** [tweakpng](http://entropymine.com/jason/tweakpng/) [advpng](http://advancemame.sourceforge.net/comp-readme.html)
  * **SWiF** [SWFRETools](https://github.com/sporst/SWFREtools/) ([+Buggery](https://github.com/grugq/Buggery)) [blitzableiter](http://blitzableiter.recurity.com/) [mm.cfg](http://jpauclair.net/2010/02/10/mmcfg-treasure/) [Archives](http://kb2.adobe.com/cps/142/tn_14266.html) [Alexis' SWF ref](http://www.m2osw.com/swf_alexref.html) [JPEXS Free Flash Decompiler (FFDec)](http://www.free-decompiler.com/flash/)
  * **pdf** [PDF Stream dumper](http://sandsprite.com/blogs/index.php?uid=7&pid=57) [malzilla](http://malzilla.sourceforge.net/) [pdftk](http://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/) [pdf-parser](http://blog.didierstevens.com/programs/pdf-tools/) [iText](http://itextpdf.com/) [Origami](http://esec-lab.sogeti.com/pages/Origami)

  * **DBI**
    * **[pin](http://www.pintool.org/)**  [shellcode](http://blog.zynamics.com/2010/07/28/dumping-shellcode-with-pin/) ([agustin gianni](https://github.com/agustingianni)) [TarteTatin](http://code.google.com/p/tartetatintools/) SHAN
    * **[dynamorio](http://dynamorio.org/)** [dyntrace](http://www.inreverse.net/?p=1668)

  * **unpackers** [rl!depacker](http://www.reversinglabs.com/forum/index.php?topic=11.0) [QUnpack](http://qunpack.ahteam.org/) [deroko generic unpacker](http://deroko.phearless.org/rce.html) [Fast Universal Unpacker](http://code.google.com/p/fuu/) ([TitanEngine](http://www.reversinglabs.com/products/TitanEngine.php))

  * **bochs** [images](http://bochs.sourceforge.net/diskimages.html) [mtool](http://www.frontiernet.net/~fys/mtools.htm) [disk explorer](http://hp.vector.co.jp/authors/VA013937/editdisk/index_e.html)
  * **[dosbox](http://www.dosbox.com/)** [heavy\_debug](http://vogons.zetafleet.com/viewtopic.php?t=3944)
  * **[IDA](http://www.hex-rays.com/idapro/)** [IDAPython](http://code.google.com/p/idapython/)
    * **plugins** [IDAStealth](http://newgre.net/idastealth) [optimice](http://code.google.com/p/optimice/) [Class Informer](http://www.macromonkey.com/bb/viewforum.php?f=65)
    * **doc** [binarypool](http://www.binarypool.com/idapluginwriting/)
      * **cpu** SDK\module\script\ebc.py (+[...\ebc\fat.efi](http://sourceforge.net/projects/efidevkit/files/)) [hyperunpackme](https://www.openrce.org/articles/full_view/28) [ps3spu](http://code.google.com/p/ida-spu/) [python](http://www.idabook.com/examples/chapter_19/simple_python.tgz)
  * **[WinDbg](http://msdn.microsoft.com/en-us/windows/hardware/gg463016)** [Symbols](http://msdn.microsoft.com/en-us/windows/hardware/gg463028) [VirtualKD](http://virtualkd.sysprogs.org/) [from A to Z](http://windbg.info/doc/2-windbg-a-z.html)
  * **[OllyDbg](http://www.ollydbg.de/)**
    * **plugins** OllyAdvanced OllyDump CodeDoctor FullDisasm
    * **[ImDbg](http://debugger.immunityinc.com/)** [pvefindAddr](http://redmine.corelan.be:8800/projects/pvefindaddr)
  * **[Hiew](http://hiew.ru/)** ([PyHiew](http://code.google.com/p/pyhiew/))
  * **[HT Editor](http://hte.sourceforge.net/)**

  * [sysinternals](http://www.sysinternals.com) (`net use \\live.sysinternals.com`) [nirsoft](http://www.nirsoft.net)
# Exploits #
| CVE | filetype | specific | (worthy) links |
|:----|:---------|:---------|:---------------|
| CVE-2007-5659 | PDF | collectEmailInfo |  |
| CVE-2008-2992 | PDF | util.printf |  |
| CVE-2008-5353 | Java | calendar deserialization | [Tinnes](http://blog.cr0.org/2009/05/write-once-own-everyone.html) [Koivu](http://slightlyrandombrokenthoughts.blogspot.com/2008/12/calendar-bug.html) |
| CVE-2009-0432 | PDF | media.newPlayer |  |
| CVE-2009-0658 | PDF | JBIG2 |  |
| CVE-2009-0927 | PDF | Collab.getIcon |  |
| CVE-2009-1492 | PDF | getAnnots |  |
| CVE-2009-1493 | PDF | customDictionaryOpen linux |  |
| CVE-2009-3459 | PDF | FlateDecode |  |
| CVE-2009-3867 | Java | Soundbank |  |
| CVE-2009-3953 | PDF | U3D |  |
| CVE-2010-0188 | TIFF | DotRange in PDF | [PoC @ bugix](http://bugix-security.blogspot.com/2010/03/adobe-pdf-libtiff-working-exploitcve.html) [Liu @ fortinet](http://blog.fortinet.com/cve-2010-0188-exploit-in-the-wild/) |
| CVE-2010-1297 | Flash | newfunction |  |
| CVE-2010-2065 | TIFF (pdf)| LibTIFF StripByteCount |  |
| CVE-2010-2883 | PDF | Cooltype | [bugix](http://bugix-security.blogspot.com/2010/09/cve-2010-2883-made-in-korea.html) |
| CVE-2010-3333 | RTF | (in Word) |  [Microsoft](http://blogs.technet.com/b/mmpc/archive/2010/12/29/targeted-attacks-against-recently-addressed-microsoft-office-vulnerability-cve-2010-3333-ms10-087.aspx) |
| CVE-2010-3654 | Flash | RadioButtonGroup | [Abyssec](http://www.abysssec.com/blog/2011/04/exploiting-adobe-flash-player-on-windows-7/) |
| CVE-2011-0609 | Flash |  | [Li @ fortinet](http://blog.fortinet.com/advanced-exploitation-of-the-recent-flash-zero-day-vulnerability-cve-2011-0609/) [Nicolas Joly @ Vupen](http://www.vupen.com/blog/20110326.Technical_Analysis_and_Win7_Exploitation_Adobe_Flash_0Day_CVE-2011-0609.php) |
| CVE-2011-0611 | Flash |  | [secunia](http://secunia.com/blog/210/) [microsoft](http://blogs.technet.com/b/mmpc/archive/2011/04/12/analysis-of-the-cve-2011-0611-adobe-flash-player-vulnerability-exploitation.aspx) |
| CVE-2011-0041 | GDI+ |  | [Abyssec](http://www.abysssec.com/blog/2011/07/analysis-of-cve-2011-0041-vulnerability-in-gdi/) |
| CVE-2011-0226 | Jailbreakme 3  |  | [Sogeti](http://esec-lab.sogeti.com/post/Analysis-of-the-jailbreakme-v3-font-exploit) |
| CVE-2011-2110 | Flash | array indexing| [yomuds](http://yomuds.blogspot.fr/2012/11/flash-exploit-cve-2011-2110-and-cool.html) [NCR/CRC! ARTeam](http://www.accessroot.com/arteam/site/download.php?view.331) |
| CVE-2011-2462 | U3D PDF |  |  |
| CVE-2011-3402 | TTF | Duqu MS11-087 | [lifeasageek](http://exploitshop.wordpress.com/2012/01/18/ms11-087-aka-duqu-vulnerability-in-windows-kernel-mode-drivers-could-allow-remote-code-execution/) [yomuds](http://yomuds.blogspot.fr/2012/11/cve-2011-3402-and-cool-exploit-kit_28.html) |
| CVE-2011-3544 | Java | Rhino | [shierlm](http://schierlm.users.sourceforge.net/CVE-2011-3544.html) |
| CVE-2012-0003 | Midi | midiOutPlayNextPolyEvent MS12-004| [metasploit](http://www.exploit-db.com/exploits/18426/) |
| CVE-2012-1723 | Java | Getfield | [mihi42](http://schierlm.users.sourceforge.net/CVE-2012-1723.html) |
| CVE-2012-5076 | Java | AnonymousClassLoader | [Kafeine](http://malware.dontneedcoffee.com/2012/11/cool-ek-hello-my-friend-cve-2012-5067.html) [Jeong Wook Oh](http://blogs.technet.com/b/mmpc/archive/2012/11/15/a-technical-analysis-on-new-java-vulnerability-cve-2012-5076.aspx) |
| CVE-2013-0155/0156 | Ruby on Rails |  | [Ronin](http://ronin-ruby.github.com/blog/2013/01/09/rails-pocs.html) |
| CVE-2013-0422 | Java |  |  |

# information #
  * **news** [@Ivanlef0u](https://twitter.com/#!/Ivanlef0u) [reddit](http://www.reddit.com/r/ReverseEngineering/)
  * **syscalls & structs** [Metasploit](http://dev.metasploit.com/users/opcode/syscalls.html) ([j00ru](http://j00ru.vexillium.org/win32k_syscalls/)) [Native NT Toolkit](http://code.google.com/p/native-nt-toolkit/) [undocumented](http://undocumented.ntinternals.net/) ([PEB](http://undocumented.ntinternals.net/UserMode/Undocumented%20Functions/NT%20Objects/Process/PEB.html)) [Msdn(suiche)](http://msdn.moonsols.com/)
  * **JavaScript** [Garden](http://bonsaiden.github.com/JavaScript-Garden/)
  * **Master Boot Record** [IDA debugging](http://www.hexblog.com/?p=103) [starman](http://thestarman.narod.ru/asm/mbr/index.html) [RayKnights](http://www.rayknights.org/pc_boot/pc_boot.htm)
  * **Presentations**
    * [Packer Genetics: The Selfish Code](http://blog.zynamics.com/2010/07/16/recon-slides-packer-genetics-the-selfish-code-bochspython/) Ero Carrera and Jose Duart (Recon July 10, 2010) ([video](http://www.archive.org/details/PackerGeneticsTheSelfishCode-EroCarreraAndJoseDuart))
> > like DNA sequences in genoms, small hex sequences might be found only in unpacked files, and not in packed files (such as compiler specific sequences). looking for such genes can help to determine if a file has been successfully unpacked.
    * [Java Malware](http://www.inreverse.net/?p=1687) Donato Ferrante, Caro 2011
    * [A compression scheme for code size versus performance trade-off](ftp://ftp.irisa.fr/techreports/2003/PI-1574.ps.gz)
    * virtualisation
      * Inside code virtualizer, scherzo
      * dealing with virtualization packer by Boris Lau 2008. 2nd CARO Workshop
      * how to recover virtualized x86 instructions by themida, jim wang, microsoft, vb sept 2009
      * unpacking
      * Mark Vincent Yason, [The art of unpacking](https://www.blackhat.com/presentations/bh-usa-07/Yason/Whitepaper/bh-usa-07-yason-WP.pdf), IBM ISS & X-Force, Black Hat 2007
      * Nicolas Falliere 2007-09-12, Windows Anti-Debug Reference, security focus
      * Peter Ferrie, Anti-Unpacking Tricks
    * rootkits
      * Hunting rootkits with Windbg - Frank Boldewin
# misc #
  * **hex editors** with colors
    * simple
      * [wxHexEditor](http://sourceforge.net/projects/wxhexeditor/) nice, simple, good
      * [BinID2](http://phenoelit.org/BinID/BinID2.exe) lightweight, straightforward
    * with templates
      * [010 editor](http://www.sweetscape.com/010editor/) many templates, lacks easy manual coloring, but recommended
      * [hex workshop](http://www.hexworkshop.com/) nice competitor, limited scripting and availability
      * [Hex editor Neo](http://www.hhdsoftware.com/free-hex-editor) interesting features (multiple selections) but heavy

  * **text editors** [notepad++](http://notepad-plus-plus.org/) [conTEXT](http://www.contexteditor.org/) [UniRed](http://www.esperanto.mv.ru/UniRed/ENG/index.html)
  * **audio/video** [foobar2000](http://www.foobar2000.org/) [Videocacheview](http://www.nirsoft.net/utils/video_cache_view.html) mp4box dvddecrypter flvextract dvdshrinker vobrator ifoedit vobedit virtualdub audacity eac lame wavegain

  * **orthographe** [antidote](http://www.druide.com/antidote.html) [BonPatron](http://bonpatron.com/) [Conjugueur](http://www.leconjugueur.com/)
  * **source**  [Mercurial](http://mercurial.selenic.com/) ([+tutorial](http://hginit.com/))

  * [collabedit](http://collabedit.com/) [prezi](http://prezi.com/) [Greenshot](http://greenshot.org/)
  * **screencasts** [InstantDemo](http://www.instant-demo.com/) [Wink](http://www.debugmode.com/wink/) (+[good tutorial](http://codex.gallery2.org/Codex:How_to_Create_a_Wink_Tutorial))
    * [Sizer](http://www.brianapps.net/sizer/) [ZoomIt](http://technet.microsoft.com/en-us/sysinternals/bb897434) [ShowOff](http://www.donationcoder.com/Software/Skrommel/index.html#ShowOff)
  * **fonts**
    * bitmap
      * [PalmOS](http://damieng.com/creative/typography/palmos-font) simple small bitmap font
      * [dina](http://www.donationcoder.com/Software/Jibz/Dina/) nice as well
    * vector [Envy Code R](http://damieng.com/blog/tag/envy-code-r) very nice scalable programming font **recommended**
  * **obfuscation**
    * **javascript** [jssfx](http://code.google.com/p/jssfx/) [aaencode/jjencode/jsf\*ck](http://utf-8.jp/) [p,a,c,k,e,d](http://dean.edwards.name/packer/) [doomsday](http://blog.9bplus.com/doomsday-javascript-encoder)
  * **videos**
    * [RSA Animate - Drive: The surprising truth about what motivates us](http://youtu.be/u6XAPnuFjJc)
  * **typing** [MessagEase](http://www.exideas.com/ME/index.php)
  * **checksum** [FsumFE](http://fsumfe.sourceforge.net/)
  * **shop** [inventables](http://www.inventables.com)
  * **format extractor** [QuickBMS](http://aluigi.org/papers.htm#quickbms)
  * **floppy** [dungeon master](http://dmweb.free.fr/?q=node/1429) [apple II](http://www.hackzapple.com/ORG1/MZ/PIRATESOFTS.HTM) [softpres](http://www.softpres.org/) [kryoflux](http://www.kryoflux.com/) [HxC floppy emulator](http://www.lotharek.pl/product.php?pid=12)
  * **jigsaw** [JigThings](http://www.jigthings.com/) [Wentworth](http://www.jigsaws.co.uk/) [Michele Wilson](http://www.puzzles-et-jeux.com/)

  * [Programming Languages references sheets](http://hyperpolyglot.org) [vim for programmers](http://michael.peopleofhonoronly.com/vim/)
  * [SVG cleaning](http://www.codedread.com/scour/)

###### encodings ######

| | bin | oct  | dec | hex | unicode | unicode long |
|:|:----|:-----|:----|:----|:--------|:-------------|
| WinDbg | 0y  |  | 0n | 0x |  |  |
| Python strings |     | \0 - \777 |  | \x0 - \xff | \u0000 - \uffff  | \U00000000 - \UFFFFFFFF |
| Hiew | 010i | 010 / 77o | 010t | ff / 0ffh / 0xff |  |  |