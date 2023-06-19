# 05 Rozhodovanie

Rozhodovanie je ďalším kľúčovým konceptom v programovaní.


Musíme sa vedieť rozhodovať na základe hodnôt, s ktorými pracujeme, aby sme vedeli napríklad detekovať a nahlásiť nesprávnu hodnotu. Ako pri našej aplikácii na prevod kilometrov na míle, keď sme nezadali číslo.


Navrhujem, aby sme to opravili a popri tom sa naučili, ako navedieme program sa rozhodnúť, že čo má robiť.

## Ignorovanie zlého vstupu

Poďme opraviť náš predošlí program.

```js
// 1 míla je 1.60934 km
let vzdialenostKm = prompt("Zadaj vzdialenosť v km")

// ak je vzdialenostKm číslo, tak urob výpočet a vypíš pomocou console.log
if (typeof vzdialenostKm === "number") {
	let vzdialenostMile = vzdialenostKm / 1.60934
	console.log(vzdialenostMile)
}
```

Hmm, tu máme veľa otázok:

- čo je `if`
- čo je `typeof`
- prečo je kód v zátvorkách `{ }` odsadený medzerami
- čo sa znamená `typeof vzdialenostKm === "number"`?


**čo je `if`**

- `if` slúži na definovanie podmienky, ktorú cheme skontrolovať
- `if` sa rozhoduje iba podľa `true` a `false` - ak je výsledná podmienka `true`, tak sa vykoná kód v `{}`
- podmienka je umiestnená medzi zátvorky obyčajne zátvorky hned za if `if ( podmienka ) { tu_bude_kód }`

```js
if (podmienka) {
	// ak platí - ak výsledok podmienky je true, tak vykonaj to čo je medzi týmito zátvorkami {}
}
// ak podmienka neplatí - tak celé to preskoč a pokračuj ďalej...
```

**čo je `typeof`**

- spomeň si na dátové typy, že každa hodnota uložená do premennej bude mať nejaky dátový typ
- špecialnym slovom `typeof nazov_premennej` vieme dostať tento typ ako text
- `console.log(typeof 10)` by nám vypísalo `"number"`
- `console.log(typeof "ahoj")` by nám vypísalo `"string"`
- `console.log(typeof true)` by nám vypísalo `"boolean"`


**prečo je kód v zátvorkách `{ }` odsadený medzerami**

- len čisto pre prehladnosť, aby bolo jasné, že tento kód sa vykoná, ak bude daná podmienka platiť

**čo sa znamená `typeof vzdialenostKm === "number"`?**

- zisťujeme, či dátový typ `vzdialenostKm` je číslo (`number`)
- tu vidíme, ako sme nakombinovali niekoľko vecí dokopy, tak si to poďme bližšie vysvetliť


Možno nám pomôže, keď si to rozdelíme na drobnejšie, čo sme už robili:

```js
// vypýtame si vstup
let vzdialenostKm = prompt("Zadaj vzdialenosť v km")

// zistíme, čo sme dostali, buď "number" "string" alebo "boolean"
let typVzdialenostKm = typeof vzdialenostKm

// porovnáme či typVzdialenostKm je číslo
let podmienka = typVzdialenostKm === "number"

// v tomto momente je premenná podmienka buď true alebo false

if (podmienka) {
	// ... to čo chceme spraviť, ak je podmienka true
}
```


### Zhrnutie

- rozhodovanie ovplyvňuje chod programu, že čo sa bude diať
- zápis: `if ( podmienka ) { tu bude kód ak podmienka je true }`
- if podmienky budeme používať veľmi často
- jeden z najužitočnejších konceptov - každý programovací jazyk podporuje rozhodovanie
