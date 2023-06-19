# Funkcie

Funkcie sme už použili, napríklad taký `console.log()` alebo `prompt()`.

Funkcie vieme _volať_, (z angl. _call_) a myslíme tým konkrétne to, že napíšeme jej názov a dáme zátvorky `()`.

Ale teda, čo tá funkcia vlastne je?!

Pozri si nasledujúci kód.

```js
function prvaSkusobna() {
	let x = 1;
	let y = 2;
	let z = x + y;

	console.log(z)
}

prvaSkusobna()
prvaSkusobna()
prvaSkusobna()
```

**Otázky**
- Prečo to existuje?
- Aký je rozdiel medzi `function prvaSkusobna() {...}` a `prvaSkusobna()`
- Prečo zátvorky prázdne `()` pri `function prvaSkusobna() ...`?

**Prečo to existuje?**

- **Aby sme vedeli nejaký blok kódu opakovane používať na viacerích miestach.**
- Napíšeme raz a vieme použiť viackrát.
- Bonus: ľudia si takto vedia zdielať funkcionalitu - zabalia kus logiky do funkcie a ostatní to môžu použiť.


**Aký je rozdiel medzi `function prvaSkusobna() {...}` a `prvaSkusobna()`**

- `function prvaSkusobna() {...}` je tzv. definícia, čo funkcia bude robiť
- `prvaSkusobna()` je volanie funkcie - až pri volaní sa kód spustí

**Prečo zátvorky prázdne `()` pri `function prvaSkusobna() ...`?**

- Do funkcie môžeme aj veci vkladať.
- Ako sme pracovali s funkciou `console.log()`, tak vždy sme do zátvoriek mohli vkladať premenné a tie sa vypísali - voláme to **argumenty funkcie**.
- Naša funkcia neočakáva žiadny argument preto sú zátvorky prázdne, ale hneď si ukážeme aj príklad s argumentami.
