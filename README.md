#13b Vervolg Autos

##### contructors, overloading

- Maak een klasse ```Auto``` met de volgende attributen, maar laat deze leeg
    - ```private int snelheid``` 
    - ```private String merk```
    - ```private int kilometerstand```
- Maak alleen de bijbehorende set (accessor) methoden voor alle attibuten.
- Maak een ```main``` methode en instantieer een ```Auto``` object met een variabele ```auto```.
- Vraag de snelheid, merk en kilometerstand op. Wat zijn de waarden?

De waarden van elk nieuw ```Auto``` object zijn momenteel leeg. In de vorige opgave hebben we de attributen meteen gevuld bij de declaratie. Maar het kan ook op een ander moment, namelijk in de constructor
- Maak een constructor methode `public Auto()` en vul de attributen hierin in met de waarden:
    - ```snelheid = 0 ``` 
    - ```merk = "Toyota"```
    - ```kilometerstand = 20000```
- Run nogmaals het programma, welke waarden zie je nu?  

We willen nu graag meteen bij het instantieren van ```Auto``` objecten, de mogelijkheid hebben om een auto een ander merk te geven
- Maak nog een constructor methode ```public Auto(String merk)```. Deze constructor heeft als input parameter een ```String merk```. Zorg ervoor dat de auto dit merk krijgt, i.p.v. het oorspronkelijke merk
- Instantieer nu een ```Auto``` met ```Auto tesla = new Auto("Tesla")``` en vraag alle waarden van deze auto op. Welke waarden zie je?

Zojuist hebben we *overloading* toegepast op de constructor (we hebben immers twee methoden met dezelfde naam: ```Auto()``` en ```Auto(String merk)```)

We willen nu **verplichten** om een ```Auto``` alleen te kunnen instantieren als er een merk wordt doorgegeven.
- verwijder de constructor ```Auto()``` of plaats het in commentaar
- compileert je programma nog? Waarschijnlijk niet. Pas het aan zodat alleen nog auto's aangemaakt kunnen worden door een merk door te geven (via constructor ```Auto(String merk)```) 

**Extra**  
*statische methoden*

Onze auto's hebben allemaal dezelfde motor, een "Colombo V12". Dit is dus een gemeenschappelijke eigenschap van alle auto's. Daarom stoppen we dit gegeven in een *statische* methode.
- maak in de klasse ```Auto``` een statische methode ```public static String motorgegevens()```. Deze methode heeft als output ```Motor: Colombo V12 580 pk 980 kilo 3,8 liter```
- vraag van al je geinstantieerde auto's de motorgegevens op.

- zoals je ziet kun je een *statische* methode als een *dynamische* methode aanroepen. Echter, je kunt de statische methode ook statisch aanroepen met ```Auto.motorGegevens()```. Probeer dit. 