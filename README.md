# ZX48essentials

## Introduction

Sinclair ZX Spectrum 48K computer released in April 1982 was not the best one compared to its competitors but for sure became one of the most influential ones. A lot of hobbyists who nowadays collect, repair or mod Spectrum, probably think about creating their own version - keeping the original idea/design that makes a Z80 system The Spectrum: ULA with its architecture, content of the ROM, original case and keyboard but getting rid of nonsenses where you could easily do better, even in 80’s. 

It has to be said that this is not by any means revolutionary work. There are lots of similar projects and this one could be easily called Yet Another Spectrum Clone but as said before, every Spectrum lover would like to have his/her own version. I hope you like mine.

## Design

The main design decision concerns ULA. You might want to use original chip but it is difficult to get and you need to build extensive analog video circuit (that occupies one third of the board) and you still get relatively poor composite picture. On the other hand, you could use modern FPGA replacement that gives RGB output but this is not ULA architecture (on an outside) any longer. Decision was made to use vLA82S+ version by vRetro Design. This is FPGA based ULA replacement that has RGB output but is drop-in replacement for original chip so original architecture will be retained. Other changes are:

* Dynamically refreshed Lower RAM based on 4116 chips is replaced with more convenient static RAM which also allows to get rid of most all of power supply section as -5V and +12V voltages are no longer needed. This is the solution commonly used in memory replacements boards – using set of flip-flops (74574) we hook new RAM into address multiplexers used in original ULA architecture.

* Original dynamically refreshed Upper RAM chips use only one voltage, however we could easily replace them with one 32KB static RAM chip. Memory type selection jumpers are no longer needed.
  
* Content of the ROM stays unchanged however when you build your ZX Spectrum you probably will not source original PROM but instead use modern EEPROM chip like W27C512. ROM type jumpers are no longer needed.
  
* For the power supply section we will use switching regulator 2450. Also (as in MAX/Harlequin) we will add rectifying bridge to save us from mistakenly connecting power supply with wrong polarity (which from experience is likely to happen as Spectrum uses center-negative jack while nowadays almost everything is center-positive).

## About the parts

* Except for added components all others have original markings and are located in the same places as in ZX Spectrum 48K Issue 3B.
  
* Standard size 0,25W resistors are used, however length is decreased from 0.6” to 0,5”. I really hate those rows of bus separation/pullups resistors so network ones are used wherever possible.
  
* Axial capacitors are used as in original design but you can put disc ones instead. I could not resist and left blue electrolytic capacitors, however there is option for radial ones as well. Four unmarked small elements are additional decoupling 100nF capacitors.
  
* Original audio sockets are replaced with PJ-307 ones, commonly used in retro systems.
  
* Mini DIN8 connector (as in Harlequin 48K) is used to output RGB signal and mono sound to TV/monitor.
  
* If you think using rectifying bridge is below you, shorten adequate pins and don’t use it.
  
## Important remarks

* Because power section is limited, only 5V is available on edge connector.
  
* If you intend to put the board in ZX Spectrum 48K case, vLA82S+ must be soldered. For ZX Spectrum 48K+ case you can use socket (standard not precision).
  
* As a bonus, vLA82S+ has write-only AY-3-8910 sound generator built-in. L and R channels are mixed and output as one to TV/monitor.
  

Have fun!

Tomasz

> [!NOTE]
> Disclaimer: This is my project that I’ve built and it works for me. You can do it as well but remember, you’re responsible for your doings not me.

