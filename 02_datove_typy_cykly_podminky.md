# Datové typy, vstupy, výstupy, seznamy, cykly for a while, podmínky

## IDE

Seznámení s vývojovým prostředím Microsoft Visual Studio Code.

## Práce v interaktivním módu

Spuštění pomocí příkazu `python` v terminálu.

Opuštění pomocí klávesové zkratky `ctrl + d`.

## Výstup

`print('Hello world')`

## Numerické datové typy

`int`, `float`, `complex`

Zjištění typu pomocí `type()`

## Operátory

- sčítání +
- odčítání/negace -
- násobení *
- dělení /
- celočíselné dělení //
- zbytek po celočíselném dělení %
- mocnina **
- přiřazovací operátory +=, -=, /=, *=, atd.

## Načítání vstupu

```python
x = input('Zadejte slovo: ')
print(x)
```

## Textové řetězce

`string`

Zapisuje se buď do jednoduchých `'text 1'` nebo dvojitých `"text 2"` uvozovek.

převod textového řetězce na číslo:

```python
cele_cislo = int('64')
desetinne_cislo = float('3.14')
```

Formátování čísel a vkládání proměnných do textového řetězce:

```python
cislo = 6.66666
print(f'Vytištění proměnné na dvě desetinná místa: {cislo:.2f}')
```

## Úkoly

- Vytvořte program, který po zadání čísla vrátí hodnotu zbývající do nejbližšího vyššího násobku 20. 1 => 19, 26 => 14, 103 => 17, atd.
- Napište program, který vyzve uživatele k zadání poloos elipsy a vypočítá její obsah. (Pro pokročilé i obvod).

## Řešení

```python
x = int(input('Zadejte číslo: '))
result = 20 - (x % 20)
print(f'Do nejblližšího násobku zbývá {result}')
```

```python
a = float(input('Zadejte poloosu a: '))
b = float(input('Zadejte poloosu b: '))
result = 3.14159 * a * b
print(f'Obsah elipsy je {result:.2f}')
```

## Seznam

Datový typ list v Pythonu lze pomocí hranatých závorek (popřípadě pomocí `list()`).

Prázdný seznam:

```
seznam_a = [] 
```

Nový seznam s prvky:

```
dopravni_prostredky = ['auto', 'kolo', 'letadlo']
```

Počet prvků v seznamu:
```
print(len(dopravni_prostredky))
```

### Přistupování k prvkům pomocí indexu:
```
print(dopravni_prostredky[1])
print(dopravni_prostredky[-1])
print(dopravni_prostredky[0:2])
```

Podrobnosti: https://www.w3schools.com/python/python_lists.asp

## Cyklus for

Iterace přes pole:
```
for dp in dopravni_prostredky:
  print(dp)
```
Iterace s indexem:
```
for i in range(len(dopravni_prostredky)):
  print(dopravni_prostredky[i])
```

Iterace s indexem a prvkem:
```
for i, dp in enumerate(dopravni_prostredky):
  print(f'{i}: {dp}')
```

## Cyklus while

Využívá se hlavně, když není předem známo, kolik iterací bude.
```
i = 0
while i < len(dopravni_prostredky):
  print(dopravni_prostredky[i])
  i += 1
```

## Podmínky
```
if 'letadlo' in dopravni_prostredky:
  print('Poletíme!')
elif 'auto' in dopravni_prostredky or 'kolo' in dopravni_prostredky:
  print('Pojedeme.')
else:
  print('Půjdeme pěšky :-(')
```

## Předčasné ukončení cyklu nebo selé smyčky

```
i = 0
while i < len(dopravni_prostredky):
  if dopravni_prostredky[i] == 'kolo':
    break
  i += 1
```

## Úkoly

1. Napište program, který sečte pouze pozitivní čísla v poli. [1, -2, 3, -4] → 4
1. Napište program, který po zadání letopočtu vypíše století: 1705 → 18, 1900 → 19, 2000 → 20, 2024 → 21

## Řešení

```python
pole = [1, -2, 3, -4, 5, -6, 7]

sum = 0
for cislo in pole:
    if cislo > 0:
        sum += cislo

print(sum)
```

```python
vstup = input('Zadejte rok: ')
rok = int(vstup)
stoleti = rok // 100
if rok % 100 > 0:
    stoleti += 1
print(f'Století je {stoleti}.')
```


## Procvičování

https://www.codewars.com/
