# Flash, SSD - 17-02-2021
---
# Flash paměti
-	Flash paměť elektricky programovatelné (zapisovatelné) paměti s libovolným přístupem
-	Odvozeny od EEPROM, ale struktura paměťových buněk a propojovací sítě mezi paměťovými buňkami jsou odlišné
-	Podle způsobu zapojení paměťových buněk i principu jejich práce odlišujeme paměti typu NAND a NOR

## Flash paměť - NOR
-	NOR
	-	každá buňka se skládá z jediného tranzistoru s izolovanou elektrodou nad níž je umístěna bežná brána

## Flash paměť - NAND
-	Několik paměťových buněk zapojeno za sebou v "sérii"
	-	lepší využití plochy čipu
-	Nejmenší adresovatelná jednotka se nazývá stránka (page)
-	Několik stránek je sdruženo do bloku (block)
-	Čtení a zápis dat je prováděn již při zápisu

#### NAND - náhrada hdd, rychlý zápis a čtení, pomalý náhodný přístup
#### NOR - náhrada PROM, EPROM, EEPROM, pomalý zápis a čtení, dobrý náhodný přístup

# Solid State Disk (SSD)
-	pevné disky bez mechanických částí
-	založené na flash pamětech
-	Výhody
	-	rychlý start
	-	nízké latence
	-	krátký vyhledávací čas
	-	žádný hluk
	-	nízká spotřeba a produkce tepla
	-	lepší bezpečnost
	-	vysoká odolnost vůči okolí
-	velmi špatný poměr cena / 1GB dat
-	omezený počet přepisovacích cyklů
-	sníženou pravděpodobnost obnovy dat při mechanickém poškození

## RAID (Redundant Array of Inexpensive/Independent Disks)
-	vícenásobné diskové pole laciných/nezávislých disků
-	metoda zabezpečení dat proti selhání pevného disku
-	Zabezpečení je realizováno specifickým ukládáním dat na více nezávislých disků, kdy jsou uložená data zachována i při selhání některého z nich
-	RAID pole je složeno z obyčejných sériově zapojených disků

**metody:**
-	softwarově 
	-	zápis do pole RAID obsluhuje operační systém
		-	speciální mezivrstva
		-	ovladač zařízení
-	hardwarově

-	při výpadku některého disku
	-	tzv. degradovaný stav
	-	nižší výkon
	-	uložená data k dispozici
-	Výměna havarovaného disku zpět do pole (hot add)
	-	rekonstrukce pole
	-	dopočítány chybějící údaje a zapsány na nový disk
	-	synchronizace pole
	-	může být rezervní disk - automatická rekonstrukce

### Typy RAID polí
-	**RAID 0**
	-	zařízení jsou jen spojena do logického celku a vytváří tak kapacitu součtu všech členů
	-	porucha členu znamená ztrátu dat
	-	Zřetězení
		-	data postupně ukládána na několik disků
		-	jakmile se zaplní první, ukládá se na další
	-	Prokládání
		-	data ukládána na disky střídavě

-	**RAID 1 (zrcadlení)**
	-	obsah se současně zaznamenává na dva disky
	-	v případě výpadku jednoho disku se pracuje s kopií
	-	bezpečnost dat X ztráta kapacity

-	**RAID 5**
	-	vyžaduje alespoň 3 členy
	-	kapacitu jednoho členu zabírají samoopravné kódy
		-	uloženy na členech střídavě (odstraněna nevýhoda)

-	**RAID 6**
	-	vyžaduje alespoň 4 členy
	-	kapacitu dvou členů zabírají samoopravné kódy

