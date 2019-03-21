# W1 Installation \(Chromebook\)

> **Hinweis** Wenn du die Installation bereits gemacht hast, kannst du direkt zur [Einführung in Python](python_introduction.md) gehen.

Du kannst [diesen Abschnitt einfach](http://tutorial.djangogirls.org/en/installation/#install-python) überspringen, falls du kein Chromebook benutzt. Wenn du eins benutzt, wird deine Installation ein wenig anders sein. Du kannst den Rest der Installationsanweisungen ignorieren.

#### Cloud IDE \(PaizaCloud Cloud IDE, AWS Cloud9\)

Mit dem Tool Cloud IDE erhältst du Zugang zu einem Code-Editor und einem Rechner, der im Internet läuft und auf dem du die Software installieren, schreiben und ausführen kannst. Für die Dauer des Tutorials wird Cloud IDE zu deinem _lokalen Rechner_. Auch du wirst Befehle in einer Kommandozeilen-Oberfläche ausführen können, genau wie die anderen Teilnehmerinnen, die mit OS X, Ubuntu oder Windows arbeiten. Dein Terminal wird jedoch mit einem Rechner verbunden sein, den Cloud IDE dir bereitstellt. Hier ist die Anleitung für die Cloud IDEs \(PaizaCloud, Cloud IDE, AWS Cloud9\). Wähle eine der Cloud IDEs aus und folge den Anweisungen der gewählten Cloud IDE.

**PaizaCloud Cloud IDE**

1. Gehe zu [PaizaCloud Cloud IDE](https://paiza.cloud/)
2. Lege dir dort ein Benutzerkonto an
3. Klicke auf _New Server_
4. Klicke auf die Schaltfläche "Terminal" \(links im Browserfenster\)

Jetzt solltest du links eine Schnittstelle mit einer Seitenleiste und Schaltflächen sehen. Klicke auf den "Terminal"-Button und öffne das Terminal-Fenster mit einer Eingabeaufforderung wie folgt:

{% filename %}browser{% endfilename %}

```text
$
```

Das Terminal auf der PaizaCloud Cloud IDE steht für deine Anweisungen bereit. Du kannst die Größe des Fensters frei einstellen.

**AWS Cloud9**

1. Gehe zu [AWS Cloud9](https://aws.amazon.com/cloud9/)
2. Lege dir dort ein Benutzerkonto an
3. Klicke auf _Create Environment_

Jetzt solltest du eine Benutzeroberfläche mit Seitenleiste, ein grosses Fenster mit Text und am unteren Rand ein Feld sehen, das wie folgt aussieht:

{% filename %}bash{% endfilename %}

```text
deinbenutzername:~/workspace $
```

Dieser untere Bereich ist dein Terminal. Dort kannst du Kommandos für den Computer eingeben, den dir Cloud 9 zur Verfügung stellt. Du kannst dieses Fenster vergrößern oder verkleinern.

#### Virtuelle Umgebung

Eine virtuelle Umgebung \(auch virtualenv genannt\) ist wie ein privater Behälter, in den wir nützlichen Code für ein Projekt packen können, an dem wir arbeiten. Wir benutzen sie, um Code für verschiedene Projekte getrennt aufzubewahren, damit dieser nicht vermischt wird.

Führe im Terminal den folgenden Code aus \(das Terminal befindet sich am unteren Rand des Cloud 9-Interfaces\):

{% filename %}Cloud 9{% endfilename %}

```text
sudo apt update
sudo apt install python3.6-venv
```

Falls das nicht funktioniert, frag' deinen Coach um Hilfe.

Führe dann die folgenden Befehle aus:

{% filename %}Cloud 9{% endfilename %}

```text
mkdir djangogirls
cd djangogirls python3.6 -mvenv myvenv
source myvenv/bin/activate
pip install django~={{ book.django_version }}
```

\(Beachte, dass wir im letzten Befehl eine Tilde gefolgt von einem Gleichheitssymbol benutzen: `~=`\).

#### GitHub

Erstelle einen [GitHub](https://github.com/)-Account.

