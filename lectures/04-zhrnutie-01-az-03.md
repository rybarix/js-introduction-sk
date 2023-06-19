# 04 Zhrnutie 01-03

- Existuje viacero programovacích jazykov
- Každý program sa musí preložiť do strojového kódu (do núl a jednotiek), aby ho stroj vedel spustiť
- Počítače majú rôzne procesory a teda rozumejú inému strojovému kódu
- Programovací jazyk slúži ľuďom, aby mohli vyjadriť svoj logický postup, ktorý žiadajú od stroja
- Programovací jazyk je výtvor ľudí a ktokoľvek (ak vie ako) si môže programovací jazyk vytvoriť.

- `// je komentár a všetko za tým je ignorované`
- `let faktCokolvek = 42` nám umožní ukladať si veci do premenných
- `console.log()` služi na výpis pre nás. Do zátvoriek dávame názov premennej, ktorú chceme vypísať napr. `console.log(faktCokolvek)` vypíše 42.
- text je `string` a vieme ho ukladať do premenných ako čísla
- `string`-y vieme ščítavať a tým ich spájať dokopy
- máme 2 typy úvodzoviek, ktoré vieme použíť tzv. _single quotes_ `'` a _double quotes_ `"` pri tvorbe `string`-ov
- výsledky logických operácii sú vždy `true` alebo `false`
- vieme porovnávať ľubovoľné hodnoty aj `1000 === "halo"`
- vieme porovnávať lubovoľné premenné medzi sebou
- všetky **medzery, voľné riadky sú ignorované**, ale je dobré udržiavať kód čitateľný pre nás ľudí.

| príklad | typ |
|:--------:|:------|
|`10` a `59012.521`       |`number`|
|`"ahoj"` a `"Vonku je pekne"`       |`string`|
|`true` a `false`| `boolean` |


- spravili sme prvú užitočnú aplikáciu, ktorá reaguje na rôzne vstupy
- funkcia `prompt` vyzve používateľa na vstup
- Javascript sa používa v spojení iného jazyka, ktorý sa nazýva HTML (uvidíme neskôr). Je to hlavne vtedy, ak chceme nášmu programu dať nejakú vizuálnu podobu, s ktorou ľudia vedia interagovať.