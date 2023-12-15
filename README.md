# OpenGD77-noXpresso

---
## Description

a patch kit for building OpenGD77 with standard arm-none-eabi toolchain, no f**king slow MCUXpresso required.

old OpenGD77 release has Makefile for experimental use, but it is abondoned in recent release.

this patch kit is based on that Makefile.

## Restriction

the size of newlib and picolibc is larger than redlib, so all functions of OpenGD77 cannot store into MCU's ROM. currently, international language support is disabled -- English language only.

and, *all* components are optimized with -Os option to reduce size. some objects in original OpenGD77 is compiled with -O0 (no optimization), but this is required due to improper code (I reported at https://www.opengd77.com/viewtopic.php?f=16&t=2587 but rejected). I believe -Os binary works no problem, but not well tested.

## License

WTFPL
