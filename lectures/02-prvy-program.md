
# 02 Prvý program

Pri učení sa programovať sa zvykne dávať dôraz na programovací jazyk.
Dokonca v praxi sa stretnete, že sa ľudia podľa programovacieho jazyka aj zoskupujú. "Ja som Java programátor" alebo "Ja som C programátor" je bežné počuť.


Ja zvolím taký, kde aj s málo kódom vieme urobiť niečo užitočné a postupne pôjdeme do hĺbky a porozumenia, že čo sa vlastne deje na pozadí.


Budeme robiť v **Javascripte**. Javascript je čitateľný a dá nám dobrý základ pre pochopenie konceptov v programovaní.

Teraz je rad na tebe, ideme robiť príklady a trénovať prax.

Otvor si prosím tento [link](https://runjs.co/) v novom okne, kde si môžeš javascript skúšať alebo iný ekvivalent.

## Koľko míľ je 80km?

Vždy ukážem nejaký kód a následne si postupne prejdeme jednotlivé koncepty a rozdrobíme si to.


```js
// 1 míľa je 1.60934 km
let vzdialenostKm = 80
let vzdialenostMile = vzdialenostKm / 1.60934

console.log(vzdialenostMile)
```

Máme tu hneď niekoľko otázok:
- čo znamena `//` a prečo je za text `//` inej farby
- čo je `let`
- čo je `console.log` a prečo sú tam zátvorky `( )`
- aký je výsledok?

Samotný výpočet primína klasickú matematiku, vidíme tam delenie `/` a vidíme čísla. Nič prekvapujúce.


**čo znamena `//` a prečo je text tým inej farby**

- Každy programovací jazyk ma možnosť napísať komentár.
- Je to informácia čisto pre ostatných ľudí alebo pre nás.
- Všetko čo je bude za `//` bude ignorované.

**čo je `let`**

- `let` signalizuje, že teraz príde názov pamäťovej bunky do ktorej budeme chcieť niečo uložiť.
- Tieto bunky voláme po správnosti **premenné**. Teda môžu sa volať akokoľvek (písmená bez diakritiky a _) a ukladať si akúkoľvek hodnotu za znamienkom `=`.

**čo je `console.log` a prečo sú tam zátvorky `( )`**

- console.log() je  _funkcia_, do ktorej môžeme dávať premenné.
	- To čo to presne znamená budeme riešiť o chvílu.
- **console.log nám bude slúžiť ako nástroj na výpis výsledkov**
- ak by sme odstránili, tak náš program by nevypísal výsledok a nechal by si ho len pre seba.
- **Skúste odstrániť `console.log(vzdialenostMile)` a znovu program spustiť. Alebo skúste dať pred `console.log(vzdialenostMile)` komentár pomocou `//`**



<details>
<summary><strong>aký je výsledok?</strong></summary>

- `49.70981893198454`
</details>


### Zhrnutie

- `// je komentár a všetko za tým je ignorované`
- `let faktCokolvek = 42` nám umožní ukladať si veci do premenných
- `console.log()` služi na výpis pre nás. Do zátvoriek dávame názov premennej, ktorú chceme vypísať napr. `console.log(faktCokolvek)` vypíše 42.

## Pozdrav s menom

Pokračujeme v budovaní užitočných vecí.


Povedzme, že chceme posielať email a máme meno osoby a radi by sme k menu pridali aj pozdrav.

Predtým ako si spustíme tento kód sa poďme zamyslieť, čo očakávame, že sa stane. Nesústredme sa teraz na úvodzovky a ich význam, ale čo by si ako človek očakával/a, že bude výsledok, keď to vidíš.

```js
let pozdrav = "Ahoj, "
let meno = 'Janko'
let dokopy = pozdrav + meno

console.log(dokopy)
```

Máme tu hneď niekoľko otázok:

- čo znamenajú úvodzovky a majú špecialny význam?
- aký je rozdiel medzi `"` a `'` ?
- ako sa dá **šcivať text?!**
- aký je výsledok? Čo sa výpíše?


**čo znamenajú úvodzovky a majú špecialny význam?**

- všetko čo je medzi úvodzovkami je z pohľadu programu text, s ktorým vieme ďalej pracovať
- tak ako si vieme ukladať čísla, si vieme ukladať aj text
- takýto text sa nazýva `string`, "reťazec znakov"

**aký je rozdiel medzi `"` a `'` ?**

- žiadny, vieme ich používať zameniteľne, je to vec preferencie, ktoré chceme používať
- my budeme používať v lekciach `"`

**ako sa dá šcivať text?!**

- toto je jedna z vecí, ktorá sa môže meniť naprieč rôznymi programovacími jazykmi
- v Javascripte je to možné, výsledny text sa jednoducho spojí dokopy
- znova môžeme vidieť, že tvorcovia Javascriptu spravili rozhodnutie, že operátor `+`, bude fungovať aj s `string`-ami


### Zhrnutie

- text je `string` a vieme ho ukladať do premenných ako čísla
- `string`-y vieme ščítavať a tým ich spájať dokopy
- máme 2 typy úvodzoviek, ktoré vieme použíť tzv. _single quotes_ `'` a _double quotes_ `"` pri tvorbe `string`-ov


## Kontrola veku

Ďalej čo bude užitočné, bude vedieť porovnávať naše premenné.

Aby sme mohli robiť viac užitočné programy, budeme sa musieť rozhodnúť, či niečo je platné alebo nie.

Či sa niečo rovná alebo nie.



```js
let vek = 24

let siDospely = vek >= 18
let niesiDospely = !siDospely
let mas18 = vek === 18
let masViacAko30 = vek > 30

console.log(siDospely)
console.log(niesiDospely)
console.log(mas18)
console.log(masViacAko30)
```

Máme tu hneď niekoľko otázok:

Vidíme povedomé porovnácie operátor ako je `>` alebo `>=`, ale aj divnejšie `===` trojité rovná sa alebo dokonca `!`.

- čo vlastne robíme?
- aký hodnoty majú výsledky porovnávaní?
- čo znamená `!`
- čo je `===` a aký je rozdiel oproti `=`
- ako zistím, či sa dve veci nerovnajú?
- koľko máme takýchto porovnávacích/logických operatorov?
- aký sú presné výsledky nášho programu?

**čo vlastne robíme?**

- Používame _logické operátory_
- tieto logické operátory majú základ v matematike a chovajú sa tak, ako by sme očakávali pri porovnávaní čísel
- alebo pri logických operáciach - k tomu sa ešte dostaneme nižšie


**aký hodnoty majú výsledky porovnávaní?**

- po každej logickej operácii je výsledok buď áno alebo nie - tieto sú označené špecialne `true` alebo `false`
- môžeme napríklad vytvoriť premennú `let vonkuPrsi = false`

**čo znamená `!`**

- výkričník znamená negácia - obrátime hodnotu:
	- z `true` na `false`
	- a `false` na `true`
- `siDospely` je `true`, pretože platí, že `vek` je vačší alebo rovný ako `18`
- `niesiDospely` bude opak `siDospely`, takže `false`

**čo je `===` a aký je rozdiel oproti `=`**

- `===` je operátor porovnávania premenných, či majú rovnaké hodnoty
- `=` je priradovanie hodnoty premenným. To čo je na pravej strane sa uloží do toho premennej na ľavo
- `mas18` bude preto `false` lebo nie je pravda, že `24 === 18`

**ako zistím, či sa dve veci nerovnajú?**

- tak ako máme `===`, tak máme `!==`, ktorý sa vyhodnotí ako nerovnosť
- `vek !== 0` by sa vyhodnotil ako `true` pretože je pravda, že vek sa nerovná `0`

**koľko máme takýchto porovnávacích/logických operatorov?**

| operátor | význam | príklad | výsledok |
|:--------:|:------|:--------:|:---------|
|`!`       |negácia| `!true`  | `false`  |
|`>`| porovnanie väčšie ako | `vek > 19` | `true`|
|`>=`| porovnanie väčšie-rovné ako | `24 >= 35` | `false`|
|`<`| porovnanie mensie ako | `45 < 100` | `false` |
|`<=`| porovnanie menšie-rovné ako | `0 <= 0` | `true` |
|`===`| rovné | `1000 === "halo"` | `false` |
|`!==`| nerovné | `1000 !== 1001` | `true` |



<details>
<summary><strong>aký sú presné výsledky nášho programu?</strong></summary>

- siDospely: `true`
- niesiDospely: `false`
- mas18: `false`
- masViacAko30: `false`
</details>


### Zhrnutie

- výsledky logických operácii sú vždy `true` alebo `false`
- vieme porovnávať ľubovoľné hodnoty aj `1000 === "halo"`
- vieme porovnávať lubovoľné premenné medzi sebou


# Dátové typy

Všetký hodnoty, ktoré sme doteraz používali `10` - číslo, `"text"` - string, `true` - logická hodnota rozdelujeme podľa ich tzv. dátového typu.

Dátovy typ je buď číslo alebo string, alebo logická hodnota, ktorá sa taktiež nazýva `boolean`.

| príklad | typ |
|:--------:|:------|
|`10` a `59012.521`       |`number`|
|`"ahoj"` a `"Vonku je pekne"`       |`string`|
|`true` a `false`| `boolean` |


Čo to v praxi znamená?

Keď máme napríklad hodnotu `100`, ktorá je typu `number`, tak automaticky vieme robiť operácie s číslami, ktoré nám Javascript dovoluje. Napríklad `100 * 2` má zmysel, lebo `100` aj `2` sú čísla (`number`).

Ale keby sme chceli `100 * "ahoj"`, tak máme problém, lebo operácia násobenia nedáva zmysel pri typoch `number` a `string`.

Skúste teraz spustiť nasledovný program:

```
console.log(100 * "ahoj")
```

Dostaneme výsledok `NaN`, čo znamená `Not a Number` inak povedané, dostali sme neplatný výsledok a považujeme ho za chybu.

Koncept dátových typov je prítomný v každom programovaciom jazyku.

Teraz je dôležite si len uvedomiť, že dátové typy umožňujú sa stroju, ktorý náś kód spúšťa, vyznať vo všetkých premenných a zabezpečiť, aby operácie, ktoré chceme robiť boli korektné.

Dátových typov má Javascript viac, ale k tým sa dostaneme postupne, keď to bude potrebné.
