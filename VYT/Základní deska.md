# Základní deska - 09-09-2021
---
# Základní deska
- patice pro procesor
- čipovou sadu (MCH, ICH, North a South Bridge)
- čip pro vstupy a výstupy (Super I/O)
- ROM BIOS (Flash ROM)
- patice pro paměťové moduly
- sběrnice ISA, PCI, AGP, PCI-E (AMR, CNR...)
- regulátor napětí
- baterie
- integrované grafické, síťové a zvukové karty
- konektory (IDE, SATA, RAID, FDD, USB, aktivní chladiče...)
- zadní blok konektoru (PS/2, COM, LPT, USB, firewire, audio, video, RJ-45)

## Form faktor
- formát základní desky
- desky stejného formátu
	- předepsané rozměry
	- upevnění
	- napájení

### ATX
- 305x244mm

### Mini ATX
- 284x208mm

### Micro ATX
- 244x244mm

## Chipset
- umožňuje komunikaci mezi procesorem a ostatními zařízeními
- ovlivňuje stabilitu systému
- podporuje výkon procesoru a dalších komponent
- architektury
	- north/south bridge
	- hub architektura

### North/South bridge
- North Bridge (severní most) - jeho hlavním úkolem je propojení rychlejší procesorové sběrnice s pomalejšími sběrnicemi pro operační paměť a grafickou kartu
- název čipové sady bývá odvozen od názvu tohoto čipu
- sběrnice mez iCPU a north bridge je
	- FSB (frost side bus)
	- QPI (quick path interconnect)
- South Bridge (jižní most) - je pomalejší než North Bridge, spolu s čipem Super I/O umožňují připojení periferních zařízení k základní desce
- obsahují řadiče IDE, rozhraní COM, LPT, USB, most pro připojení sběrnice PCI
- oba čipy spojuje sběrnice Direct Media Interface (DMI)
- south bridge je připojen na sběrnici PCI

### Architektura rozbočovačů
- INTEL 975X
- NVIDIA nForce 4 Ultra