# BIOS - 23-09-2021
---
# BIOS (Basic Input Output System)
- základní souhrn instrukcí a funkcí nutných pro spuštění počítače
- Po zapnutí provádí BIOS tyto základní kroky
	- nastavení konfigurace počítače z CMOS paměti
	- provedení autonomních testů počítače (Power On Self Test, Post)
	- Inicializace komponent
	- spuštění operačního systému

## Bios - Vrstvy
- paměti ROM (pouze čtení)
	- informace, které musí být k dispozici ihned po startu počítače
		- základní detekce a používání komponent
- CMOS čip (čtení i zápis)
	- uložení jednotlivých nastavení uživatele
- Ovladače
	- zavádějí se v průběhu spouštění operačního systému

- Pro nastavování, změnu a ukládání údajů systému BIOS slouží program SETUP
- Každý druh základní desky má vlastní variantu systému BIOS
	- Různé rozmístění jednotlivých nastavení

## Aktualizace BIOSu
- Důvody update BIOSu
	- Po instalaci nového hardwaru nebo sofrwaru počítač nepracuje správně -> může být nekompatibilitou BIOSu
	- podpora nových funkcí
	- opravy funkcí starých
	- vylepšení BIOSu


