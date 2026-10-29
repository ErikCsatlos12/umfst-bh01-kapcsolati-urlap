# bh01 – Kapcsolati űrlap javítása

Csatlos Erik – Webfejlesztés, UMFST

| # | Hiba | Ok | Javítás |
|---|---|---|---|
| 1 | Rossz nyelvű felolvasás | Hiányzó `lang` (WCAG 3.1.1) | `<html lang="hu">` |
| 2 | A logónál a fájlnevet olvassa | Hiányzó `alt` (WCAG 1.1.1) | `alt="UMFST – Orvosi Kar"` |
| 3 | A mezőknek nincs neve | Csak placeholder, nincs `label` (WCAG 1.3.1, 4.1.2) | `<label for>` + `id` minden mezőhöz |
| 4 | Az „alma” is elfogadott e-mail | `type="text"` | `type="email"` + `autocomplete` |
| 5 | A Küldésre kétszer kell Tab-olni, validátorhiba | `<button>` egy `<a>` elemben | csak `<button type="submit">` |
| 6 | A cím nem zöld | Elgépelés: `colour` | `color` |
| 7 | Nem látszik a fókusz | `outline: none` (WCAG 2.4.7) | `:focus-visible` kék kerettel |

**Tesztelés:** W3C HTML és CSS validátor (0 hiba), Lighthouse Accessibility, Tab-bejárás.

**Tanulság:** natív HTML elemek (label, button, megfelelő input típus) használata, és a validátor + Lighthouse futtatása minden beadás előtt.

A javítások hibánként külön commitban vannak (lásd a commit-előzményeket).