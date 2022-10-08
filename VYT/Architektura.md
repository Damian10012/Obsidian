# Architektura - 11-10-2021
Links: [[VYT]]

---
## Harvardská architektura
- Navržena Howardem Aikenem v třicátých letech minulého století na Harvardské univerzitě
- Ve své době nebyla technologie pro realizaci této architektury
- Využívají ji mikrokontrolery obsažené např. v televizích, tiskárnách klávesnicích počítačů, ale i např. tachometrech

### Harvardská architektura - využití
- Harvardská architektura se také často používá v:
	- Specializovaných DSP procesorech
		- v audio/video technice
- Převážně malé jednoúčelové mikrokontrolery
- Pro procesory charakteristické
	- svojí malou kapacitou pamětí
	- redukované instrukční sady (RISC)

### Typy procesorů
- MCU (Micro Controller Unit)
	- nejjednodušší skupina procesorů
	- nízká cena
	- malé rozměry
	- nízká spotřeba energie
	- vyráběny pro přesně určenou specifickou činnost
	- malá možnost rozšíření
	- malý výkon
- CPU (Central Processing Unit)
	- tvoří základní řídící jednotku počítače
	- vyšší výkon
	- větší rozměry
	- Dobrá rozšiřitelnost vzhledem k otevřené architektuře a velkému množství vyvedených signálů
	- vyší spotřebou
	- ztrátovým výkonem
	- cena je vyšší
- DSP (Digital Signal Processor)
	- Vyznačují se vysokým výkonem
	- Využití ve zpracování matematických výpočtů
	- Schopnost zpracovávat velké objemy dat
	- Součástí jsou často digitálně-analogové/analogově-digitální převodníky
	- Využití u měřící techniky (digitální osciloskop), ve zvukových kartách
- NPU (Network Processors Units)
	- Jsou součástí všech přepínačů, směrovačů a dalších síťových zařízení
	- Vedoučí pozici ve výrobě síťových procesorů má společnost Broadcom

### Historický vývoj CPU
- 1971: 4004 Microprocessor
	- 2300 tranzistorů
	- 60000 instrukcí za sekundu
	- pracovní frekvence 108KHz
	- 4bitová sběrnice
	- umožňoval adresovat 640 bajtů
- 1972: 8008 Microprocessor
	- 3500 tranzistorů
	- frekvence 200KHz
	- sběrnice 8bitová
	- mohl adresovat až 16KB paměti
- 1974: 8080 Microprocessor
	- 6000 tranzistorů
	- frekvence 2MHz
	- 8 bitová sběrnice
	- mohl adresovat až 64KB
	- prováděl 640 tisíc operací za sekundu
- 1978: 8086-8088 Microprocessor
	- první generace procesorů x86
	- 29 tisíc tranzistorů
	- pracovní frekvence 5-10 MHz
	- 16bitový procesor
	- může adresovat 1 MB
- 8088
	- 16bitový jen uvnitř, sběrnici má 8bitovou
	- 1981 - první osobní počítač IBM PC
	- 8086 je zhruba 10x rychlejší než 8080
- 1989: Intel 486(TM) DX CPU Microprocessor
	- Integrovaná cache
	- vestavěný matematický koprocesor
	- 1,2M tranzistorů
	- 20MHz (20MIPS)
	- 1992 DX2
		- pracovní frekvence 50 a 66 MHz (54 MIPS)
		- sběrnice pracuje na poloviční frekvenci tj. 25 nebo 33 MHz
	- 1994 DX4
		- frekvence sběrnice 75 a 100 MHz
	- verze SX jako "levná varianta" bez matematického koprocesoru
- 1993: Pentium Procesor
	- plně kompatibilní s předchůdci
	- 64bitová datová sběrnice
	- oddělené 8 KB datové a instrukční vyrovnávací paměti
	- 3,1M tranzistorů
	- pracovní frekvenci 66 MHz (112 MIPS)
	- Adresovatelný prostor 4 GB a virtuálních 64 TB
- 1997: Pentium MMX Procesor
	- rozšíření o multimediální instrukce (57 nových instrukcí)
	- MMX používá stejné registry jako matematický koprocesor
		- oba výpočty nemohou pracovat současně
	- v základní sadě instrukcí cca o 20% rychlejší
		- zvětšení vnitřní cache z 16 na 32 KB
		- algoritmus na předpovídání větvení běhu programu
	- První MMX pracovaly a 166 MHz
	- leden 1999: vydán čip pracující i na 300 MHz
		- určen především do notebooků
		- 4,5M tranzistorů
	- 1999 - Intel Celeron
		- 32bitový mikroprocesor odvozený původně od Intel Pentium II
	- 1999 - Intel Pentium III
		- 32bitový mikroprocesor nové generace s novou sadou instrukcí SIMD (9,5M tranzistorů)
	- 2000 - Intel Pentium 4
		- 32bitový mikroprocesor zaměřený na vysoké frekvence
	- 2001 - Intel Itanium
		- 64bitový mikroprocesor nové generace pro servery


### Významné parametry procesoru
- Napájecí napětí jádra procesoru
- TDP (Thermal Design Power)
	- maximální možný příkon (spotřeba při maximálním vytížení)
	- watt 
- Patice (Socket)
	- uchycení procesoru na základní desce
	- LGA, PGA
	- Jednotlivé patice nejsou ve většině případů vzájemně kompatibilní
- Počet fyzických jader uvnitř procesoru
	- více fyzických jader procesoru
-	Počet instrukčních kanálů(pipelines)
-	Velikost vyrovnávací paměti (Cache paměť)
	-	rychlost
	-	velmi krátká přístupová doba
	-	Vyrovnávací statická paměť první úrovně (L1)
		-	datová a instrukční
		-	kapacita desítky KB
	- Vyrovnávací statická paměť druhé úrovně (L2)
		- Komunikace mezi procesorem a operační pamětí
		- kapacita jednotky až desítky MB
-	Instrukční sada - CISC, RISC, EPIC
-	Účinnost mikrokódu
	-	počet kroků, které procesor musí vykonat pro provedení jedné instrukce
-	Velikost adresovatelné paměti
	-	velikost operační paměti, kterou je prrocesor schopen používat (adresovat)
	-	Maximální velikost adresovatelné paměti jsou 4 GB pro 32-bitovou adresovou sběrnici

### Režimy procesoru
-	Reálný režim
	-	Software tohoto typu je jednoúlohový bez ochranných mechanismů proti přepisování paměti jiného spuštěného programu nebo OS.
-	Chráněný režim
	-	ochrana dat jedné aplikace před přepsáním jiným programem
-	Virtuální reálný režim

### Procesory - x86
-	Architektura se nazývá x86 - končí sekvencí 86: 8086, 80186, 80286
-	32bit

### Procesory - x86-64
- 64bit kompatibilní s 32bit a 16bit
- vyvinulo AMD
- 32bit nebo 64bit systém
