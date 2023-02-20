# ModelDopravnihoSystemu - 20-02-2023
Links: [[PRG]]

---
## Jak to bude fungovat
1. Bude 8 #Stanice + #CentralniDispecink 
2. U každé stanice bude #Auto
3. My klikneme na #Auto a ukáže se nám novej Form, kde si nějak nastavíme čas, kdy má odjet (za jak dlouho ig, nějakej numericUpDown)
4. #Auto potom pobere postupně všechny balíky (dát tam nějakej sleep při každém pickupu) #ToDo *možná dobre na vícevláknové řešení, každé auto jiné vlákno, to by nebylo špatné*
5. Až je pobere, pojede do #CentralniDispecink 
6. Tam zase začne vykládat (*nevim, jestli víc než jedno #Auto najednou může*)
7. Veme to, co má vzít zpátky, naloží a pojede do své #Stanice 
8. Když si klikneme na #StaniceBtn tak se nám ukáže Form s 2 možnostma
	1. Vyzvednout balík (asi se odečte 1 balík z toho, co už je dovezeno)
	2. Odeslat balík (otevře další Form)
		1. V tom Formu bude listbox kam to odeslat a to se přidá do KOdvezení
## How to:
- ### Vytvořit si všechny komponenty
	1. Základní #Form1.cs, kde bude picturebox s mapou a timer pro simulaci času
	2. Potom uděláme UserComponent #Stanice.cs, která bude mít picturebox, ve kterém bude kruh a uvnitř bude 3(6) labelů s informacema (Id, KVyzvednuti, KOdvezeni) a tlačítko #StaniceBtn
	3. Potom uděláme UserComponent #CentralniDispecink.cs, #ToDo *sem ještě nevim co všechno dáme*
	4. Potom uděláme UserComponent #Auto.cs, kde bude jen picturebox s nějakym obrázkem auta (kroužek)
 