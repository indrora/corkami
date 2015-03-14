**Preserving arcade games** was presented at Recon, T2, Area41, NuitDuHack, RaumZeitLabor, CCC and other locations.

# Abstract #
_Old-school arcade games were so protected that hacking is the only way to preserve them before all boards are dead, and the games are lost._

  * an overview of famous old-school arcade games
  * their incredible hardware
  * the permanent piracy
  * the awesome protections (designed to commit suicide !)
  * what was required to preserve some of them from being lost for ever.

This talk is a homage to Michael Steil's Ultimate Commodore 64 presentation at 25c3: you should watch it, it's inspiring in content and quality !

# Contents #
The slide deck initially started as pure b&w text, then evolved to pictures only, and lastly fully animated with custom recorded (some are tools-assisted) lossless videos, presented via a tweaked version of [AdvanceMenu](http://advancemame.sourceforge.net/menu-readme.html) (an arcade frontend) (_full deck download soon_)

Why? This talk was rejected a lot - often without even an answer despite requests - so I just kept improving it anyway :)

Please give me feedback [here](http://events.ccc.de/congress/2014/Fahrplan/events/5997.html).

The best version was presented at the CCC ([hi-res video + download](http://media.ccc.de/browse/congress/2014/31c3_-_5997_-_en_-_saal_6_-_201412282030_-_preserving_arcade_games_-_ange_albertini.html))

> <a href='http://www.youtube.com/watch?feature=player_embedded&v=vg7LPcFUxg8' target='_blank'><img src='http://img.youtube.com/vi/vg7LPcFUxg8/0.jpg' width='425' height=344 /></a>

A static version of the slides is [available as PDF](https://speakerdeck.com/ange/preserving-arcade-games-31c3), viewable online and directly downloadable.

You can download the full animated presentation (~1Gb) with extras on [archive.org](https://archive.org/details/arcade31c3).

## special versions ##
An extended version (more details) is also available
> <a href='http://www.youtube.com/watch?feature=player_embedded&v=LiRIc0LDlu4' target='_blank'><img src='http://img.youtube.com/vi/LiRIc0LDlu4/0.jpg' width='425' height=344 /></a>

**french** J'ai aussi donné cette présentation en Français
> <a href='http://www.youtube.com/watch?feature=player_embedded&v=d2X0YyxHg5Q' target='_blank'><img src='http://img.youtube.com/vi/d2X0YyxHg5Q/0.jpg' width='425' height=344 /></a>

# extra #
you can find [here](http://pics.corkami.com) some hi-res version of some of the slides (facepalm, timeline)
![http://i.imgur.com/PJbYtpB.png](http://i.imgur.com/PJbYtpB.png)

The Q&A screensaver uses AdvanceMenu and the video set from its [website](http://advancemame.sourceforge.net/menu-download.html) (6 Gb)

# tricks #
  * images
    * original slides from the first PDF version were converted to PNG via [ImageMagick + "-density parameter"](http://www.imagemagick.org/script/command-line-options.php#density)
  * video
    1. create your own video / download video via [youtube-dl](http://rg3.github.io/youtube-dl/)
    1. extract all/specific frames as PNG via [MPlayer](http://www.mplayerhq.hu/design7/news.html)
    1. manipulate frames via imagemagick (crop, colors, perspective...)
    1. reencode via [advmng](http://advancemame.sourceforge.net/doc-advmng.html)
  * mame recording
    1. save game just before recording position
    1. restart Mame and record audio & video via Mame's _mngwrite_ & _wavwrite_ option, load savegame
    1. trim start on both MNG & WAV via [this script](http://corkami.googlecode.com/svn/trunk/misc/python/trimmer.py) (only works before any advmng-specific compression)
    1. audio levelling via replaygain
  * or use AdvanceMame direct MNG + WAV recording

  * Tools assisted videos: [Mame-RR](https://code.google.com/p/mame-rr/downloads/list) with [MacroLua](https://code.google.com/p/macrolua/wiki/MacroLuaDocumentation) and my [inputs scripts](https://code.google.com/p/corkami/source/browse/trunk/misc/tas/?r=1750)

  * some videos were 'cleaned' at emulation level to prevent the display of some specific tiles (if you have a better solution, let me know!)
    * used WinKawaks Shot Factory to identify the tiles more easily (blinking state)
    * patched tiles functions in Mame & recompile.

  * compression
    * pngout, advpng, advmng

  * AdvanceMenu works better under Wine for correct playback.
    * the configuration was tweaked so that it's as big as possible on screen (it's still windowed)
    * taskbar color is set to black, W8 settings "Prevent windows from being automatically arranged when moved to the edge of the screen" mus be disabled.
    * a patch to prevent AdvanceMenu to restart at the first frame was implemented by Philippe Teuwen. Because the official build couldn't compile under Windows at the time, I did a crossplatform diff patch on the official Windows binary


# ack #
Thanks to everyone who could make this presentation possible (Raz, Andreas, Charles, Dave, Phil), and to anyone who made preservation possible, and in particular CPS2.