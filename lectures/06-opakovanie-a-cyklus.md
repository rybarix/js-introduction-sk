# 06 Opakovanie - cyklus

Opakovanie je ďalší kľúčový koncept v programovaní.

Čo myslím pod opakovaním?

Povedzme, že pri našom prepočte kilometrov na míle sme chceli dostať číslo, ale to sa nestalo.

Bolo by dobré, keby sa pýtame dovtedy na číslo, dokiaľ ho nedostaneme. A teda budeme opakovať našu požiadavku.

## Vylepšené míle


Poďme vylepšiť náš mini program a pýtať si vstup pokiaľ nie sme spokojný.

Predým, ako to zapracujeme, by som si rád prešiel podrobnosti, aby sme uzrejmili ako to funguje.

Máme niekoľko spôsobov ako robiť opakovanie a teda začneme s `while`.

```js
while (podmienka_ktora_plati) {
	// opakuj tento kód
}
```

**Ako to funguje?**

- určite si všimni, že tu začína byť istá podobnosť s `if` podmienkou a má podobnú štruktúru
- tento kód doslova robí nasledovné:
	- Opakuj kód v zátvorkách `{ }` **pokial** je podmienka v `( )` `true`
	- Voľný slovenský preklad: `pokial (podmienka_ktora_plati) { ...opakuj_tento_kod... }`


**Otázky**
- Prečo by sa podmienka opakovania mala zmeniť?
- Čo mám presne vložiť do `( )` zátvoriek
- Čo sa stane, keď podmienka prestane platiť?

**Prečo by sa podmienka opakovania mala zmeniť?**

```js
// malý prikád s číslami
let pocitadlo = 0

while (pocitadlo < 5) {
	pocitadlo = pocitadlo + 1
	console.log(pocitadlo)
}

console.log("koniec")
```

**Otázka**

- Prečo pri `pocitadlo = pocitadlo + 1` sme nemuseli napísať `let`?
	- Pretože `let` slúži oznámenie programu, že vytvárame premennú (pamäťovú bunku, kde si chceme uložiť hodnotu) a to robíme, **vždy len raz**.
	- Následne Javascript vie, že pod menom `pocitadlo` nájde danú premennú.


<details>
<summary><strong>Čo program vypíše?</strong></summary>

na začiatku je `pocitadlo = 0`

ideme na riadok `while (pocitadlo < 5)`

kontrola podmienky: `0 < 5` je `true`, takže

`počítadlo = pocitadlo + 1`

teraz má počítadlo hodnotu `1`, ktorú následne vypíšeme cez `console.log`

---

Vraciame naspať na riadok `while (pocitadlo < 5)`

kontrola podmienky: `1 < 5` je `true`, takže

`počítadlo = pocitadlo + 1`

teraz má počítadlo hodnotu `2`, ktorú následne vypíšeme cez `console.log`

---

(pokračujeme -  nevypíšem všetky kroky, keďže sa stále opakujú)

---

Vraciame naspať na riadok `while (pocitadlo < 5)`

(počítadlo je = 4) kontrola podmienky: `4 < 5` je `true`, takže

`počítadlo = pocitadlo + 1`

teraz má počítadlo hodnotu `5`, ktorú následne vypíšeme cez `console.log`

---

Vraciame naspať na riadok `while (pocitadlo < 5)`

(počítadlo je = 5) kontrola podmienky: `5 < 5` je `false`, takže

kočíme s opakovaním a preskakujeme `{ }` a vykoná sa ešte `console.log("koniec")`
</details>


Teraz je na čase, aby sme to využili v našom mini programe.

Postup bude taký, že pýtame si číslo pokiaľ ho nedostaneme. Využijeme rovnakú podmienku z nášho `if`.

Pozrime sa na situáciu, že ako by to mohlo prebiehať:


`let vzdialenostKm = prompt("Zadaj vzdialenosť v km")`

Vypýtame si hodnotu, ale dostaneme od človeka napríklad
`vzdialenostKm = "abc"`.

Pomocou `typeof vzdialenostKm === "number"` vieme zistiť, či máme to čo chceme - číslo.

Ak nedostaneme to čo chceme, tak si to musíme znova cez `prompt` vypýtať.


**Teraz túto myšlienku dám do kódu:**

⚠️ !! (upozorňujem, že v kóde je logická chyba) !!

A je na riadku `while (typeof vzdialenostKm === "number") {`

Vieš ju opraviť?

```js
// 1 míla je 1.60934 km
let vzdialenostKm = prompt("Zadaj vzdialenosť v km")

while (typeof vzdialenostKm === "number") {
	vzdialenostKm = prompt("Zadaj vzdialenosť v km")
}

let vzdialenostMile = vzdialenostKm / 1.60934
console.log(vzdialenostMile)
```

Urobil som zámerne chybu v tomto kóde, ako malé cvičenie.

Polož si otázku, kedy daná podmienka vo `while` platí. A čí je to tak, ako to chceme.


<details>
<summary><strong>Riešenie: kde je chyba?</strong></summary>

Na začiatku si vypýtam `vzdialenostKm` hodnotu cez `prompt`.

To je všetko dobré.

Teraz, ale máme podmienku, že ak to čo dostanem **je** číslo, tak si znova vypýtam `vzdialenostKm`.

Lenže my si chceme vypýtať hodnotu znova, keď **nedostaneme číslo**.


Preto musíme podmienku zmeniť:

```js
// 1 míla je 1.60934 km
let vzdialenostKm = prompt("Zadaj vzdialenosť v km")

while (typeof vzdialenostKm !== "number") {
	vzdialenostKm = prompt("Zadaj vzdialenosť v km")
}

let vzdialenostMile = vzdialenostKm / 1.60934
console.log(vzdialenostMile)
```

</details>