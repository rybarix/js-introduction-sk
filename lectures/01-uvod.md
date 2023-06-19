# 01 Úvod

Predtým ako sa pustíte do učenia, si prosím prečítajte nasledovné body o tom, ako prechádzať cez lekcie.

- V každej lekcí sa naučíš vždy minimum na to, aby si mohol/a experimentovať
- Každý jeden príklad si musíš vyskúšať sám/a
- Vždy sa budem snažiť ukázať praktický príklad a následne poskytnúť ďalšie informácie
	- Tu nie je vždy potrebné sa z tvojej strany ponoriť do detailov, **vždy sa k ním môžeš neskôr vrátiť**
	- Ďalšie informácie slúžia na dokreslenie celého obrazu, ale nie sú nutné k pokračovaniu ďalej v lekcí
- Niekedy veci budem zjednodušovať, ale dám to vždy vedieť.



## Čo je programovanie?

Programovanie je proces, pri ktorom stroju dáme inštrukcie čo má urobiť.
Robíme to väčšinou s nejakým konkrétnym cieľom, ktorý chceme dosiahnuť:

- môžeme chcieť stiahnuť všetký texty z vašej obľúbenej stránky
- alebo chceme zobrať údaje z excel tabuľky a vytvoriť novú tabuľku s nejakými zmenami
- alebo chceme vytvoriť vlastnú webovú stránku pre váš blog
- alebo spraviť lekcie na učenie sa programovať :)
- možností je nekonečno...

Informatika je veľmi mladý odbor s koreňmi v 50tych rokoch, ale aj tak vzniklo množstvo
zaujímavej teórie, ktorá bude neskôr veľmi užitočná.

Poďme skočiť rovno do vody, aby sme sa naučili plávať.

## Prvý program a programovacie jazyky

Určite ste počuli o programovacích jazykoch. Java, C, C++, C#, Python, atď. sú ich stovky a síu rôzne populárne.

Ja navrhujem si na teraz vyrobiť vlastný jazyk, ktorý budeme spúštať iba v našich hlavách.
Nás mozog bude "stroj", ktorý bude robiť výpočet.

Chcem to spraviť preto, aby sme si uvedomili, že tieto programovacie jazyky sú primárne výtvory ľudí, aby sa im ľahšie vyjadrovali logické inštrukcie pre stroje.


Náš primitívny jazyk bude mať len inštrukcie:
- pamäť, kde si môžeme uložiť napr. `X=1` alebo `A=100`, akékoľvek ľubovolné písmeno
- `OPAKUJ N-krát { ... }`, kde zopakujeme niečo N-krát, čo je medzi zátvorkami `{ }`
- `PRIDAJ číslo do ktorá_pamäť`
- a ešte inštrukcia `VYSTUP`, ktorá signalizuje, aký výsledok nás zaujíma - toto chceme z nášho programu dostať von.

Tu máme náš program, ktorý sa teraz pokúsime spustiť v našej hlave.
Každý riadok signalizuje jednu instrukciu.

Inštrukcia opakuj má špecialny význam v tom, že inštrukcie vo vnútri `{  }` sa viackrát a až potom prejdeme na poslednú `inštrukciu VYSTUP X`

```
X=1
OPAKUJ 3 {
	PRIDAJ 1 do X
	PRIDAJ 2 do X
}
VYSTUP X
```

Poďme to skúsiť. Začnite od inštrukcie `X=1`, kde si v hľave vytvoríte pomyselné miesto, kde budete sledovať akú hodnotu má `X`. A choďte postupne riadok po riadku.

<details>
<summary>Riešenie</summary>

Rozbor nášho mini programu.

```
X=1

(prvé opakovanie)
PRIDAJ 1 do X          X=2
PRIDAJ 2 do X          X=4

(druhé opakovanie)
PRIDAJ 1 do X          X=5
PRIDAJ 2 do X          X=7

(tretie opakovanie)
PRIDAJ 1 do X          X=8
PRIDAJ 2 do X          X=10

VYSTUP X               X=10

X je 10 !
```

**X je nakonci 10.**

Ak ste dostali iný výsledok, vôbec nič sa nedeje!


Programovanie v hlave nie je ľahké pretože sme neni zvyknutý rozmýšlať, po inštrukciách ako stroje.

Treba sa to naučiť a najlepšie samotným programovaním.

</details>

**Týmto malým cvičením** sme ukázali, že koncept programovaciecho jazyku vieme aplikovať aj na náš mozog, ktoŕy vie simulovať akýsi stroj. Čo je veľmi zaujimavý fakt a teda samotné jazyky sú len výtvor ľudí.

## Strojový kód a strojový jazyk

Už som spomenul, že "jazyk stroja" alebo "stroj". Určite ste počuli slovo _procesor_. Predstavme si teraz za ním náš mozog, ale v mechanickej podobe.

Strojový kód je v binárnej podobe - jednotky a nuly, ktoré reprezentujú náš program.

**Do tohto kódu sa musí preložiť každý program, aby ho stroj vedel spustiť.**

Tým, že v tomto bode ešte nevieme, čo všetko treba na funkčný počítač, tak nemá moc zmysel pozerať sa na takýto kód.


## Zhrnutie

- Existuje viacero programovacích jazykov
- Každý program sa musí preložiť do strojového kódu (do núl a jednotiek), aby ho stroj vedel spustiť
- Počítače majú rôzne procesory a teda rozumejú inému strojovému kódu
- Programovací jazyk slúži ľuďom, aby mohli vyjadriť svoj logický postup, ktorý žiadajú od stroja
- Programovací jazyk je výtvor ľudí a ktokoľvek (ak vie ako) si môže programovací jazyk vytvoriť.
