# Optional: Python-Aufgaben \(mit Lösung\)

Auf dieser Seite findet ihr Beispiellösungen für die zusätzlichen Python-Aufgaben.

**1.**    **Variablen definieren und ausgeben**

a\) Schreibe in einer neuen Datei ein Programm, welches vom Benutzer eine Eingabe verlangt, diese in einer Variablen speichert und anschließend wieder ausgibt.

```python
eingabe = input("Gib etwas Text ein: ")
print(eingabe)
```

b\) Schreibe ein Programm, welches vom Benutzer zwei ganze Zahlen einliest und anschließend die Summe der beiden Zahlen ausgibt.

```python
# Benutzer nach zwei Zahlen fragen und diese speichern
zahl= int(input("Gib eine Zahl ein: "))
zahl2= int(input("Gib eine weitere Zahl ein: "))

# Die erhaltenen Zahlen addieren
addition = zahl + zahl2
# Die Summe auf dem Bildschirm ausgeben
print("Die Summe der beiden Zahlen lautet: ",addition)
```

c\) Schreibe ein Programm, welches eine Zeitangabe in Stunden, Minuten und Sekunden in die Anzahl Sekunden insgesamt umrechnet.

```python
#Eingabe
stunden = int(input("Gib die Stunden ein: "))
minuten = int(input("Gib die Minuten ein: "))
sekunden = int(input("Gib die Sekunden ein: "))

#Berechnung
zeitangabe = stunden*3600 + minuten*60 + sekunden

#Ausgabe
print(stunden, "Stunden,",minuten,"Minuten,",sekunden,"Sekunden sind",zeitangabe,"Sekunden.")
```

**2.**    **If-Then-Else Statements verwenden**

a\) Schreibe ein Programm, welches vom Benutzer eine Zahl einliest und prüft, ob diese größer oder kleiner 10 ist. Es soll dann entsprechend „Die Zahl ist grösser als 10“ oder „Die Zahl ist kleiner als 10“ ausgegeben werden.

```python
zahl = int(input("Gib eine Zahl ein: "))

if zahl < 10:
    print("Die Zahl ist kleiner als 10")
else:
    print("Die Zahl ist größer als 10")
```

b\) Schreibe ein Programm, das nach Eingabe 2er Zahlen, diese miteinander vergleicht und ausgibt ob diese a &lt; b, a = b oder a &gt; b.

```python
a = int(input("Gib eine Zahl ein: "))
b = int(input("Gib eine weitere Zahl ein: "))

if b > a:
  print(b,"ist größer als",a)
elif a == b:
  print(a,"und",b,"sind gleich")
else:
  print(a,"ist größer als", b)
```

**2.**    **Funktionen definieren und aufrufen**

a\) Berechne nach Eingabe der Seitenlängen \(a,b\) die Fläche des Rechtecks. Definiere für die Berechnung der Fläche eine Funktion.

```python
#Funktiosdefinition Berechnung der Fläche eines Rechtecks
def flaeche_rechteck(a,b):
    flaeche = a*b
    print("Die Fläche des Rechtecks ist ", flaeche, ".")

#Eingabe der Seitenlängen und Aufruf der Funktion
a = int(input("Gib die Länge der ersten Seite des Rechtecks ein: "))
b = int(input("Gib die Länge der zweiten Seite des Rechtecks ein: "))
flaeche_rechteck(a,b)

```

b\) Schreibe ein Programm, dass die Fakultät einer Zahl n mithilfe einer rekursiven Funktion berechnet.

```python
#Funktionsdefinition
def fakultaet(n):
    if n == 1:
        return 1
    else:
        return n * fakultaet(n-1)

#Aufruf
n = int(input("Gib eine Zahl n ein, von welcher die Fakultät n! berechnet werden soll: "))
print(fakultaet(n))
```

**3.**    **Schleifen verwenden**

a\) Schreibe ein Programm, das mithilfe einer for-Schleife zu allen Elementen der Liste \[4,5,7,11,21\] eine zwei addiert und die Summe jeweils ausgibt.

```python
for zahl in [4,5,7,11,21]:
    summe = zahl + 2
    print("Wenn ich zu", zahl, "zwei addiere, erhalte ich", summe,".")
print("Ich bin fertig!")
```

b\) Gebe alle Zahlen von 1 bis 100 aus; von 0 bis 99 und von 0 bis 99 in 5er Schritten

```python
#Liste alle Zahlen von 1 bis 100 auf
for zahl in range(1,101):
    print(zahl)

#Liste alle Zahlen von 0 bis 99 auf
for zahl in range(100):
    print(zahl)

#Liste alle Zahlen von 0 bis 99 in 5er Schritten auf
for zahl in range(0,100,5):
    print(zahl)
```

c\) Schreibe ein Programm, welches den Benutzer mehrmals um die Eingabe eines Wortes bittet und alle diese Worte in einer Liste abspeichert. Frage den Nutzer vorher nach der Anzahl der einzugebenden Worte. Anschließend wird die neu erstellte Liste ausgegeben.

```python
anzahl = int(input("Wie viele Wörter möchtest du eingeben? "))
liste = []
for zahl in range(anzahl):
    liste.append(input("Gib ein Wort ein: "))
print(liste)
```

d\) Frage den Nutzer nach der Beantwortung einer Frage mit JA oder Nein \(J/N\). Bitte den Nutzer wiederholt um die Beantwortung der Frage, wenn die Eingabe weder \('j','J','n','N'\) ist.

```python
antwort = input('Beantworte die Frage mit Ja oder Nein (J/N): ')

while antwort not in ['j', 'J', 'n', 'N']:
    print('Eingabe ungültig!')
    antwort = input('Beantworte die Frage mit Ja oder Nein (J/N): ')

print('Vielen Dank!')
```

e\) Die Folge aus Fibonacci-Zahlen wird wie folgt gebildet: Das erste und das zweite Element sind 0 und 1. Jedes folgende Element wird gebildet, in dem die letzten zwei Elemente addiert werden. Das heißt, die Folge sieht so aus: 0,1,1,2,3,5,8,13,21,34,⋯  
Schreibe ein Programm, welches die Fibonacci-Zahlen mithilfe einer while-Schleife bis zu einer vom Benutzer gewählten Zahl ausgibt.

```python
def fibonacci(n):
    fibonacciliste=[0,1]
    i=2
    while i<=n:
        fibonacciliste.append(fibonacciliste[i-1]+fibonacciliste[i-2])
        i=i+1
    return fibonacciliste

print(fibonacci(8))
```

**4.**    **Klassen definieren und instanziieren**

a\) Definiere eine Klasse "Person" mit den Attributen "Name, Vorname, Geburtsdatum und Gewicht". Erstelle mindestens 2 Objekte der Klasse "Person".

b\) Kreiere eine Methode vorstellen\(\), die auf der Konsole für das jeweilige Obhekt folgenden Text ausgibt: „Hallo. Ich heisse \[vorname\] \[name\], wiege \[gewicht\] kg und habe am \[geb\_datum\] Geburtstag. Nice to meet you.“ Verwende die Methode für die beiden oben instanziierten Objekte.

c\) Kreiere eine zweite Methode abnehmen\(\), die als Parameter das reduzierte Gewicht erhält und dieses dann vom alten Gewicht abzieht. Das alte und neue Gewicht soll dann auf der Konsole ausgegeben werden \("Neues Gewicht: \[gewicht\] kg"\). Verwende die Methode für die beiden oben instanziierten Objekte.

```python
###Klassen definieren
class Person:
    def __init__(self, name, vorname, geb_datum, gewicht):
        self.name = name
        self.vorname = vorname
        self.geb_datum = geb_datum
        self.gewicht = gewicht

    def vorstellen(self):
        text = "Hallo.\nIch heisse " \
               + self.vorname + " " \
               + self.name + ", wiege " \
               + str(self.gewicht) + " kg und habe am " \
               + self.geb_datum + " Geburtstag.\n"\
               + "Nice to meet you."
        print(text)

    def abnehmen(self, wie_viel):
        print("Altes Gewicht:",self.gewicht,"kg")

        # Das neue Gewicht in der Instanzvariable
        # des Objektes speichern
        self.gewicht = self.gewicht - wie_viel

        print("Neues Gewicht:",self.gewicht,"kg")

##Klassen instanziieren
p1 = Person("Müller","Kurt","03.02.01", 73.5)
p2 = Person("Smith", "John", "04.04.04", 83)

p1.vorstellen()
p2.vorstellen()

p1.abnehmen(3)
p2.abnehmen(5)
```

