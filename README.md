# Amstrad_CPC6128_Multi_ROM
Internal MultiROM adapter for Amstrad CPC6128

With this adapter we can have 4 ROMs in the ROMs: LowerROM+Basic (ROM0) and ROM7; and switch between ROMs as desired.

# LowerROM and ROM0

The LowerROM and ROM0 are located inside chip 40025 (40038 in the Spanish version) that corresponds to IC103. In the LowerROM the CPC OS is housed and in ROM0 the Basic, both 16Kb.

My idea is to be able to have 4 Lower ROMs without altering the Basic (you can do it if you want), so I will use an EEPROM W27C010 (128K), they would be programmed as:

- (LwROM 1 + Basic) + (LwROM 2 + Basic) + (LwROM 3 + Basic) + (LwROM 4 + Basic)

I have divided it into the 4 groups so that you can see it more clearly since we will access those ROMs in blocks of 32Kb.

# ROM7

The ROM7 is inside the 40015 chip that corresponds to the IC204 and is the one in charge of controlling the disks. It normally stores the 16Kb AMSDOS rom.

My idea is to have 4 ROMs so I will use an EEPROM W27C512 (64k) and they would be programmed as:

ROM7_1 + ROM7_2 + ROM7_3 + ROM7_4

# IMPORTANT:

* It works for v1 and v2 revision boards but NOT on v3, you can check it on CPC6128 Motherboards
* You have to desolder the two original ICs of the motherboard and put sockets or solder my PCB directly on the motherboard.
