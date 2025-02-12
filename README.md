# ZX48essentials

## Introduction

Sinclair ZX Spectrum 48K computer released in April 1982 was not the best one compared to its competitors but for sure became one of the most influential ones. A lot of hobbyists who nowadays collect, repair or mod Spectrum, think about creating their own version - keeping the original idea/design that makes a Z80 system The Spectrum: ULA with its architecture, content of the ROM, original case and rubber keyboard but getting rid of nonsenses where you could easily do better, even in 80’s. 

It has to be said that this is not by any means revolutionary work. There are lots of similar projects and this one could easily be called Yet Another Spectrum Clone but as mentioned before, every Spectrum lover would like to have his/her own version. I hope you like mine.

## Design

The main design decision concerns ULA. You might want to use original chip but it is difficult to get and you need to build extensive analog video circuit (that occupies one third of the board) and you still get relatively poor composite picture. On the other hand, you could use modern FPGA replacement that gives RGB output but this is not ULA architecture (on an outside) any longer. Decision was made to use [vLA82S+](https://www.vretrodesign.com/products/vla82s-spectrum-ula-replacement-with-rgb-interface-and-ay-emulator-without-interface) by vRetro Design. This is FPGA based ULA that has RGB output but is a drop-in replacement for original chip so original architecture will be preserved. Other changes are:

* Dynamically refreshed Lower RAM based on 4116 chips is replaced with more convenient static RAM which also allows to get rid of almost all of power supply section as -5V and +12V voltages are no longer needed. This is the solution commonly used in memory replacements [boards](https://www.retroleum.co.uk/spectrum-repairs-mods) – using set of flip-flops (74574) we hook new RAM to address multiplexers (74157) used in original ULA architecture.

* Dynamically refreshed Upper RAM 4132/64 chips use only one voltage, however we could easily replace them with one 32KB static RAM chip. Memory type selection jumpers are no longer needed.
  
* Content of the ROM stays unchanged however when you build your ZX Spectrum you probably will not source original PROM but instead use modern EEPROM chip like W27C512. ROM type jumpers are no longer needed. You may also consider Geoff Wearmouth's [Looking Glass ROM](https://drive.google.com/file/d/1Mf0jTW43AdGkd5ZbCQTpsrJHTxZ-JjuA/view).
  
* For the power supply section we will use switching regulator. Also (as in MAX/Harlequin) we will add rectifying bridge to save us from mistakenly connecting power supply with wrong polarity (which from experience is likely to happen if you use more machines as Spectrum uses center-negative power jack while nowadays almost everything is center-positive).

## About the parts

* Except for added components (marked with numbers 200+) all others have original markings and are located in the same places on a pcb as in ZX Spectrum 48K Issue 3B. Four unmarked small elements are additional decoupling 100nF capacitors (R=2.5mm).
  
* Standard size 0,25W resistors are used, however their length is decreased from 0.6” to 0,5”. I really hate those rows of bus separation/pullups banks so network resistors are used wherever possible.
  
* Axial capacitors are used as in original design but you can put disc ones instead. I could not resist and left blue electrolytic capacitors (only two since there are no power and video sections), however there is option to use radial as well. 
  
* Original audio sockets are replaced with PJ-307 ones, commonly used in retro systems.
  
* Mini DIN8 connector (as in Harlequin 48K) is used to output RGB signal and mono sound to TV/monitor using [RGB Scart Lead cable](https://www.ebay.com/itm/253830448917?epid=17023035733&itmmeta=01JKTFD61QHFB48BB7ZDRB7SRS&hash=item3b19794715:g:KvwAAOSwlb5nn9B-).
  
* If you think using rectifying bridge is below you, shorten pins 1-4, 2-3 and don’t use it.

* Have in mind, that [40 ohm speaker](https://www.mutant-caterpillar.co.uk/shop/product_info.php?products_id=2725) might be difficult to find.
  
## Important remarks

* Because power section is severely reduced, only +5V is available on edge connector.
  
* If you intend to put the board in ZX Spectrum 48K case, vLA82S+ must be soldered. For ZX Spectrum 48K+ case you can use socket (standard not precision).
  
* As a bonus, vLA82S+ has write-only AY-3-8910 sound generator built-in. L and R channels are mixed and output as one to TV/monitor. If you connect [divMMC interface](https://www.tfw8b.com/product/divmmc-future-sinclair-zx-spectrum/) with microSD card and Kempston joystick, you have everything you need.
  

Have fun!

Tomek

> [!NOTE]
> Disclaimer: This is my project that I’ve built and it works for me. You can do it as well but remember, you’re responsible for your doings and the consequences, not me.

