# První domácí úkol

Následující kód v Pythonu vytiskne pro sudá `n` vždy celý sloupec jako `x` nebo `o`. Upravte kód tak, aby byly pro jakékoliv `n` `x` a `o` naskládány jako v šachovnici.

```
n = 9
for i in range(n*n):
    if i % n == 0:
            print('')
    if i % 2 == 0:
        print('x', end="")
    else:
        print('o', end="")
```
