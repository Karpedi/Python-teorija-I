## Comand line
### Osnove
Kalkulator, ki lahko izvaja aritmetične `(+, -, *, %)` in logične (and, or, not) operacije.

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
Logična vrednost oz. boolean
True
False

Operandi ki delujejo na logičnih vrednostih:
and
or
not

Primeri:
```python
>>> True and True
True
>>> True and False
False
>>> True or False
True
>>> False or False
False
>>> not False
True
>>> False or not False
True
```
Pri pogojih uporabljamo tudi naslednje operande:
```python
==
!=
<
>
<=
>=
```
Primeri:
```python
>>> 1+2 == 3
True
>>> 1+2 != 4
True
>>> 1+2 < 3
False
```
### Naloge  
* BMI kalulator

Kako se izračuna BMI?
Težo v kilogramih deliš z kvadratom višine v metrih.

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573
```
* IF stavki
Recimo da želimo povedati uporabniku, da je njegov BMI visok.

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

print("Vaš BMI je visok")
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573
Vaš BMI je visok
```
Tole ne bo šlo. Zdaj vsem povemo, da je njihov BMI visok.
To lahko popravimo.

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

if bmi > 25:
    print("Vaš BMI je visok")
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573

Teža: 90
Telesna višina: 1.75
Vaš BMI je: 29.387755102040817
Vaš BMI je visok
```
Pri pisanju if stavka je potrebno paziti na:
-	Dvopičje »:« na koncu stavka
-	Zamik – presledek/presledki ali tab. Zamaknjene vrstice spadajo pod zapisan stavek.

Te dve stvari ne veljata samo za if stavke, temveč tudi za nekaj drugih. (Katere, boš spoznal kasneje)
Zamaknjenih vrstic je lahko več

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

if bmi > 25:
    print("Vaš BMI je visok")
    print("Pridite nazaj čez en mesec")
```
Izpis:
```python
Teža: 90
Telesna višina: 1.75
Vaš BMI je: 29.387755102040817
Vaš BMI je visok
Pridite nazaj čez en mesec
```
If stavek se izvede samo, če je pogoj (v našem primeru je pogoj bmi > 25) izpolnjen.
Če želimo, da se nekaj zvede kadar pogoj ni izpolnjen uporabimo stavek else.

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

if bmi > 25:
    print("Vaš BMI je visok")
    print("Pridite nazaj čez en mesec")
else:
    print("Vaš BMI je v redu")
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573
Vaš BMI je v redu
```
If stavke lahko gnezdimo

Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

if bmi > 25:
    print("Vaš BMI je visok")
    print("Pridite nazaj čez en mesec")
else:
    if bmi < 18.5:
        print("Vaš BMI je nizek")
    else:
        print("Vaš BMI je v redu")

print("Nasvidenje")
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573
Vaš BMI je v redu
Nasvidenje

Teža: 40
Telesna višina: 1.75
Vaš BMI je: 13.061224489795919
Vaš BMI je nizek
Nasvidenje

Teža: 90
Telesna višina: 1.75
Vaš BMI je: 29.387755102040817
Vaš BMI je visok
Pridite nazaj čez en mesec
Nasvidenje
```
To lahko skrajšamo

Uporabili bomo stavek elif. Ta stavek združi else in if.
```python
else:
    if bmi < 18.5:

elif bmi < 18.5:
```
Program:
```python
teza = float(input("Teža: "))
visina = float(input("Telesna višina: "))
bmi = teza / visina ** 2
print("Vaš BMI je:", bmi)

if bmi > 25:
    print("Vaš BMI je visok")
    print("Pridite nazaj čez en mesec")
elif bmi < 18.5:
    print("Vaš BMI je nizek")
else:
    print("Vaš BMI je v redu")

print("Nasvidenje")
```
Izpis:
```python
Teža: 63
Telesna višina: 1.75
Vaš BMI je: 20.571428571428573
Vaš BMI je v redu
Nasvidenje
```
## Zanke - loop
Zanke imamo zato, da del programa ponavljamo.
Poskusimo izpisati števila od 1 do 5 brez uporabe zanke.

Program:
```python
print(1)
print(2)
print(3)
print(4)
print(5)
```
Izpis:
```python
1
2
3
4
5
```

Uporabimo lahko zanko while.
Program:
```python
x = 1
while x <= 5:
    print(x)
    x = x+1
```
Izpis:
```python
1
2
3
4
5
```
Kako deluje?
Preverjamo pogojni stavek x <= 5 in če je to enako True potem se zanka izvede.
## FizzBuzz
* Igra kjer se šteje od 1 naprej.<br>
* Kjer je število deljivo z 3 rečemo Fizz<br>
* Kjer je število deljivo z 5 rečemo Buzz<br>
* Če je število deljivo z 3 in 5 naenkrat rečemo FizzBuzz<br>

Program:
```python
i = 1
while i<=16:
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
            print("Fizz")
    elif i%5 == 0:
            print("Buzz")
    else:
            print(i)

    i += 1
```
Izpis:
```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
```




























