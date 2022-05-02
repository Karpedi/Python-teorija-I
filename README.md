## Comand line
### Osnove
Kalkulator, ki lahko izvaja aritmetične (+, -, *, %) in logične (and, or, not) operacije.

Osnovno računanje. Seštevanje, odštevanje, množenje, deljenje

Primeri:

```python
>>> 1+1
2
>>> 5-4
1
>>> 2*5
10
>>> 9/3
3.0
```
Napredno računanje. Potenciranje, ostanek

Primeri:
```python
>>> 4**2
16
>>> 2**10
1024
>>> 5%2
1
```
Oklepaji

Primeri:
```python
>>> 4 + 2*5
14
>>> (4+2) * 5
30
```
Celoštevilsko deljenje.

Primeri:
```python
>>> 5 // 2
2
>>> 4.5 // 1.2
3.0
```
Cela števila in ne cela števila.

Primeri:
```python
>>> 4+1
5
>>> 4.1+0.9
5.0
```
## Shranjevanje – spremenljivke - variable
Računalnik ima spomin.Želimo sešteti 1+2 in si to shraniti.

Primer:
```python
>>> x = 1+2
>>> x
3
```
Kaj lahko delamo z x? Lahko ga uporabljamo namesto števil. X je v našem primeru isto kot 3.

Primer:
```python
>>> x + 7
10
>>> x ** 2
9
>>> x
3
```
Definiramo lahko tudi druge spremenljivke.

Primer:
```python
>>> y = x+5
>>> y
8
```
Primerjava z matematiko. Spremenljivka se lahko poljubno spreminja. Ni enako kot pri matematiki, kje mora biti v našem primeru »x« vedno enak.

Primer:
```python
>>> x = 5
>>> x
5
>>> x = 7
>>> x
7
>>> x = x+3
>>> x
10
```
Najprej se poračuna desna stran in rezultat se zapiše v levo stran. = ne predstavlja enakosti, temveč prirejanje.

Ne se bat za imena spremenljivk uporabljati daljših imen. Ne samo x, ali y. Ampak če se računa število oseb, raje napišite »stevilo_oseb«.
## Nizi - string
Neko zaporedje znakov.
V Pythonu jih označimo z '' '' ali ' '. V drugih jezikih je to lahko drugače.

Primer:
```python
>>> "Primer niza"
'Primer niza'
>>> "Še en primer"
'Še en primer'
```
Tudi nize lahko shranimo v spremenljivke.

Primer:
```python
>>> niz = "Danes je lepo vreme."
>>> niz
'Danes je lepo vreme.'
```
Lahko jih tudi seštevamo.

Primer:
```python
>>> "Jutri " + "bo " + "snežilo"
'Jutri bo snežilo'
>>> glavno_mesto = "Ljubljana"
>>> "Glavno mesto je " + glavno_mesto
'Glavno mesto je Ljubljana'
```
glavno_mesto je spremenljivka, zato ni pod narekovaji.

## Napake
(da izbrišemo spremenljivko napišeš del spremenljivka)

Primeri:
```python
>>> a=7
>>> a+b
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'b' is not defined
```
Spremenljivka b ni definirana
```python
>>> 7=a
  File "<stdin>", line 1
SyntaxError: can't assign to literal
```
V matematiki bi to bilo čisto v redu. Pri programiranju pa to pomeni, da želimo številu 7 prirediti vrednost a-ja. To pa ne gre.

```python
>>> True = 2
  File "<stdin>", line 1
SyntaxError: can't assign to keyword
```
True je rezervirana beseda
```python
>>> if = 4
  File "<stdin>", line 1
    if = 4
       ^
SyntaxError: invalid syntax
```
Napačna sintaksa. To pomeni, da Python ne razume kaj želimo. If je spet neka rezervirana beseda po kateri morajo slediti točno dočučene stvari. Kasneje bomo videli kaj.

## Funkcije
Ni čisto enako kot pri matematiki, ampak je pa podobno.

Primeri:
```python
>>> abs(5)
5
>>> abs(-4)
4
>>> pow(2, 4)
16
```
pow(2, 4) je enako kot 2 ** 4

Funkcije lahko uporabljamo kot del izraza.

Primeri:
```python
>>> abs(-2) * 5
10
```
Argumenti funkcij so lahko izraz.

Primeri:
```python
>>> x = -4
>>> abs(pow(2, 2) * x)
16
```
## Iz nizov v števila
Primeri:
```python
>>> a = 1+1
>>> a
2
>>> b = "1 + 1"
>>> b
'1 + 1'
>>> c = "1" + "1"
>>> c
'11'
>>> d = 1 + "1"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
Integerjev (števil) in stringov (nizov) ne moremo seštevati

Recimo da imamo niza »1« in »2« in ju želimo sešteti.
Primer:
```python
>>> x = "1"
>>> y = "2"
>>> x+y
'12'
```
Dobimo niz in ne 3 kot želimo. Saj seštevamo nize
Kako to popravimo?

Primer:
```python
>>> x = "1"
>>> y = "2"
>>> xx = int(x)
>>> yy = int(y)
>>> xx+yy
3
```
Lahko tudi prepišemo stare vrednosti.
```python
>>> x = "1"
>>> y = "2"
>>> x = int(x)
>>> y = int(y)
>>> x+y
3
```
Lahko samo seštejemo brez da si shranimo številske vrednosti.

Primer:
```python
>>> x = "1"
>>> y = "2"
>>> int(x) + int(y)
3
```
Ena stvar, ki je dokaj ne pomembna za tukaj, ampak je dobro da se ve!
V Pythonu ni potrebno nastavljati tipov spremenljivk, kot je to potrebno pri nekaterih drugih jezikih. Samo za primer. V jeziku C, C++, C#, Java je potrebno napisati recimo
```c
int x = 1;
string niz = "asd";
```
1 ne moreš spraviti v String ker je 1 število in ne niz.
## Vpis in izpis
Če želimo imeti nek dejanski program je dobro, da nam program kaj izpiše. Tako bomo lahko videli kaj se dogaja in tudi pridobili neke rezultate.

Primer:
```python
>>> print("Zdravo")
Zdravo
>>> print(1+2)
3
>>> print("Jutri", "bo", 20-15, "stopinj.")
Jutri bo 5 stopinj.
```
Programu moramo tudi nekako podajati podatke.

Primer:
```python
>>> ime = input("Kako ti je ime? ")
Kako ti je ime? Jaka
>>> ime
'Jaka'
```
## Pogoji




























