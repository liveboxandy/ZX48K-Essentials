# ZX48essentials

Sinclair ZX Spectrum 48K computer released in 1982, was not the best one in terms of features but for sure became one of the most influentials. A lot of hobbiest who collect, repair or mod Spectrum think about creating their own version. Keeping the original idea/design but replacing those sections where you could easily do better nowadays. 

For sure we leave those two things that make a Z80 system the Spectrum - ULA with its architecture, ROM and original case and keyboard. Changes.

* We leave the chip but the idea is to use modern replacement produces by vRetro Design what also has RGB output. Thus we don't need to bother with all that analogue circuity that occupies one third of the board and produces TV signal. We add mini DIN8 connector (as in Harlequin) to output signal.

* Dynamically refreshed Lower RAM can be replaced with more up to date static RAM that also allows to get rid of most of power supply section because we no longer need to have -5V amd +12V supply for 4116 chips.

* Originall upper RAM uses only one voltage hiwever we could easly replace it with one 32KB chip.

* Content of the ROM stays unchanged however when you build your ZX Spectrum you probably will not use originall IC. You probably copy content to modern EEPROM chip like W27C512. Also we can rid of of ROM type switching jumpers.

* Most of elements are marked as originals and located in the same places.

* For teh power supply we will use modern regulator like TRACO TSR-2450. Also (as in Harlequi) we will add rectifing bridge to save us from mistakenly connecting powre supply with wronmg polarity which is more likely to happen as Spectrum uses negative center while nowadays positive center is ccommon.

About the parts. I replace audio sockets with PJ-307 commonly applied to retro systems. I use small resistors, however you could squezee bigger one. After a long consideration I've decided to get rid of blue electrolitic capacitors but leave original small axial ones. 
