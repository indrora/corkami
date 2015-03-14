[<< index](http://code.google.com/p/corkami/) [Android/Java/x86/... opcodes tables](http://opcodes.corkami.com) [PDF tricks](http://pdf.corkami.com) [Portable Executable](http://pe.corkami.com) [x86 oddities](http://x86.corkami.com) (this project is done in my spare time. **[Support ](http://code.google.com/p/corkami/wiki/About#Support_Corkami)** it!)

# Binary art - Byte-ing the PE that fails you #

#### presented the 3rd November 2012 during Hashdays, at Luzern, Switzerland ####

# abstract #
Being the standard executable format under Windows, the Portable Executable is omnipresent. Sadly, there is a huge gap between the official specs, suggestive at best, and the reality of the loader. While it's critical for analysts and software to reliably understand such binaries, it's actually almost impossible in extreme cases. After showing various examples that prove that Microsoft itself doesn't have an internal and perfect documentation, I'll explain why and how I decided to start my own way to cover the topic, introducing the various documents that I made in the process. then I'll present some of the most awkward features of the PE file format, with some of my numerous proof of concepts.

**Please note** that two slide decks are available: one [shorter](http://www.slideshare.net/ange4771/binary-art-byteing-the-pe-that-fails-you), presented at Hashdays, and one [extended](http://www.slideshare.net/ange4771/ange-albertini-hashdays2012extended), with more text explanations and more examples (the presentation one is a subset of the extended one).

Download [both slides decks](http://corkami.googlecode.com/files/ange_albertini_hashdays_2012.zip).

# live version #
<a href='http://www.youtube.com/watch?feature=player_embedded&v=kibEcaG0zCk' target='_blank'><img src='http://img.youtube.com/vi/kibEcaG0zCk/0.jpg' width='425' height=344 /></a>

&lt;wiki:gadget url="https://corkami.googlecode.com/svn/wiki/gadgets/hashdays2012\_slideshare\_live.xml" width=595 height=497 border=0/&gt;

# extended (offline) version #

&lt;wiki:gadget url="https://corkami.googlecode.com/svn/wiki/gadgets/hashdays2012\_slideshare.xml" width=595 height=497 border=0/&gt;

# links #
  * [PE 101](PE101.md) - a windows executable walkthrough
> > ![https://corkami.googlecode.com/svn/wiki/pics/pe101_thumb.jpg](https://corkami.googlecode.com/svn/wiki/pics/pe101_thumb.jpg)
  * [the PE format](PE.md)
> > <wiki:gadget url=https://corkami.googlecode.com/svn/wiki/gadgets/flash.xml up\_File=https://corkami.googlecode.com/svn/wiki/pics/wink/PE\_virtEP.swf up\_FlashHeight=268 up\_FlashWidth=358 up\_ContainerCol="#d1dae3" height=268 width=358 title="" border=0/>

[<< index](http://code.google.com/p/corkami/) [Android/Java/x86/... opcodes tables](http://opcodes.corkami.com) [PDF tricks](http://pdf.corkami.com) [Portable Executable](http://pe.corkami.com) [x86 oddities](http://x86.corkami.com) (this project is done in my spare time. **[Support ](http://code.google.com/p/corkami/wiki/About#Support_Corkami)** it!)