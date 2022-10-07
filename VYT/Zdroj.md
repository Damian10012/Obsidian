# Zdroj - 07-09-2021
---
# Napájecí zdroj
Počítačový zdroj = **měnič napětí**
Střídavé napětí ze sítě (230 V / 50 Hz) => stejnosměrné napětí (3,3V, 5V, 12V)

Komponenty v PC využívají tyto větve přímo, nebo si je dále mění. Porucha zdroje může způsobit zničení dalších komponent. Pro konkrétní počítačovou sestavu nevhodný zdroj může způsobit nestabilitu systému.

## Napájecí zdroj ATX
### AT
- napětí 5 V a 12 V
- spínač přimo napojený na síť 230 V
- nelze zapnout softwarově

### ATX
- další větev napětí 3,3 V
- 3 stavy
	- zapnuto
	- stand-by - 5 V
	- vypnutí - kabel, vypínač
- zapnutí přes základní desku, umožňuje Wake on LAN

### ATX 12V
- samostatný 4pin konektor +12V (napětí pro procesor)
- úpravy výkonu jednotlivých napěťových větví

### ATX 12V 2.0
- 24pin konektor (propojení základní desky se zdrojem)
- povinný SATA konektor
- samostatná větev +12V2 pouze pro CPU
- dvě samostané 12V větve => vyšší stabilita napájení

## Konektory
### Hlavní napájecí konektor (Main Power)
- Napájení hlavních částí desky (nutní zapojení)
- Od standartu ATX 12v rev2.0 má 24 pinů (dříve 20)

### +12 napájecí konektor
- hlavní odlišení ATX a ATX12V
- vodiče 2x 12V, 2x COM(zem)

### Floppy drive konektor (Berg)
### Peripheral konektor (Molex)
- přímý napájecí vstup (případně zredukován)
- napájení HDD, grafické karty, chlazení

### SATA