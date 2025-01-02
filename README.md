# ZX48essentials

Sinclair ZX Spectrum 48K computer released in 1982, was not the best one in terms of features but for sure became one of the most influentials. A lot of hobbiest who collect, repair or mod Spectrum think about creating their own version - keeping the original idea/design but replacing those sections where you could easily do better nowadays. 

For sure we want to have those things that make a Z80 system The Spectrum - ULA with its architecture, content of the ROM and original case and keyboard. Most of elements are marked as originals and are located in the same places. 

* We leave the ULA chip but use modern replacement produces by vRetro Design that also has a RGB output. Thus, we don't need to bother with all that analogue circuity that occupies one third of the board and produces TV signal. We use mini DIN8 connector (as in Harlequin) to output signal to monitor.

* Dynamically refreshed Lower RAM based on 4116 chips can be replaced with more up to date static RAM that also allows to get rid of most of power supply section because we no longer need to have -5V and +12V supply. This is the solution commonly used in memory replacements boards.

* Originall Upper RAM chips use only one voltage however we could easly replace it with one 32KB chip.

* Content of the ROM stays unchanged however when you build your ZX Spectrum you probably will not use source original PROM. You probably copy its content to modern EEPROM chip like W27C512. Also we can rid of of ROM type switching jumpers.

* For teh power supply we will use modern regulator like TRACO TSR-2450. Also (as in Harlequi) we will add rectifing bridge to save us from mistakenly connecting powre supply with wronmg polarity which is more likely to happen as Spectrum uses negative center while nowadays positive center is ccommon.

About the parts. I replace audio sockets with PJ-307 commonly applied to retro systems. I use small resistors, however you could squezee bigger one. After a long consideration I've decided to get rid of blue electrolitic capacitors but leave original small axial ones. 
