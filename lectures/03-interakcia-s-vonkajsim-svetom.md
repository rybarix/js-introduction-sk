# 03 Interakcia s vonkajším svetom

Javascript sa používa na písanie programov aj v prehliadači, v ktorom si práve pozeráte túto lekciu.

Preto navrhujem aplikovať naše skúsenosti z predošlích lekcií a spraviť prvý plne-funkčný program, s ktorým sa dá interagovať.


Poďme vylepšiť náš prvý program. Chceli by sme robiť prepočet kilometrov na míle, tak že zadáme kilometre do nejakého okienka a následne to prepočítame.


## Interakcia s človekom

Tým, že náš kód beží v prehliadači, tak máme prístup k mnoho funkciam. Zatiaľ sme mali funkciu `console.log`, ktorú sme používali na výpis.

K samotným funkciam a ako si môžeme tvoriť vlastné sa dostaneme o trošku neskôr.

Teraz uvediem ďalšiu, ktorú môžeme použiť a volá sa `prompt()`.

Ukážka ako vieme prompt využiť.

```js
// chceme dostať kilometre od človeka
let kilometre = prompt("Zadaj prosím kilometre:")

// vypíšeme to čo nám človek zadal
console.log(kilometre)
```

Všimni me si, že do funkcie `prompt` vkladáme aj sprievodný text, ktorý sa zobrazí pre človeka, aby vedel čo od neho chceme. **Môžeme tam napísať čokoľvek** - to čokoľvek musí byť `string` teda text.


Druhý postreh je, že pri písaní nášho kódu nezáleží, či dávame prázdne riadky medzi jednotlivými riadkami kódu.

Všetky **medzery, voľné riadky sú ignorované**, ale je dobré udržiavať kód čitateľný pre nás ľudí.

Stroju je to jedno v akej podobe ho dostane, pokiaľ to čo je v kóde napísane je správne.

**Poďme kód spustiť, aby sme pochopili, čo vlastne robí.**
- vidíme, že vyskčilo okienko, do ktorého môžeme písať
- vidíme, že to čo sme tam napísali sa následne aj vypísalo

Teraz ideme upraviť náš pôvodný program z 2. lekcie:

```js
// 1 míla je 1.60934 km
let vzdialenostKm = 80
let vzdialenostMile = vzdialenostKm / 1.60934

console.log(vzdialenostMile)
```

Otázka: vieš upraviť program, tak že si program vypýta vzdialenosť v kilometroch a uloží si ju do  `vzdialenostKm` pomocou funkcie `prompt` ?


<details>
<summary><strong>Riešenie</strong></summary>

```js
// 1 míla je 1.60934 km
let vzdialenostKm = prompt("Zadaj vzdialenosť v km")
let vzdialenostMile = vzdialenostKm / 1.60934

console.log(vzdialenostMile)
```
</details>

Otázky:

- čo sa stane ak namiesto čísla napíšeme text?
- vieme detekovať a oznámiť, že sme dostali nesprávny vstup?
- čo znamená prompt?
- budem `prompt` používať často?


**čo sa stane ak namiesto čísla napíšeme text?**

- ak chceme deliť veci, ktoré nie sú obe typu `number`, tak výsledok bude `NaN` (Not a Number) teda chybný výpočet
- áno vieme. Javascript nám dáva možnosť, zistiť či to čo je v premennej uložené je typu `number`, ale ešte sme si to neukázali
	- zároveň nám chýba rozhodovanie, aj keby sme zistili, či sme dostali správny vstup, nevedeli by sme nič ovplyvniť (**zatiaľ**) pretože kód sa vykonáva riadok po riadku.


**čo znamená prompt?**

- preklad z angl. je výzva. Výzva k akcii

**budem prompt používať často?**

- Nie, pretože ak sa dostaneme ku komplikovanejším aplikáciam, kde bude na vyplnenie viacero políčok, tak na to využijeme HTML čo bude samostatný "jazyk", pre tvorbu webových stránok.
- Zatiaľ nám prompt postačí pri takýchto jednoduchých mini programoch, kde chceme jednu dve veci od používateľa.

### Zhrnutie

- spravili sme prvú užitočnú aplikáciu, ktorá reaguje na rôzne vstupy
- funkcia `prompt` vyzve používateľa na vstup
- Javascript sa používa v spojení iného jazyka, ktorý sa nazýva HTML (uvidíme neskôr). Je to hlavne vtedy, ak chceme nášmu programu dať nejakú vizuálnu podobu, s ktorou ľudia vedia interagovať.