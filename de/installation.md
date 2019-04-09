# Installation

## Wenn du dieses Tutorial zu Hause bearbeitest

Wenn du das Tutorial zu Hause bearbeitest und bereits alles auf deinem Rechner eingerichtet ist, kannst du dieses Kapitel komplett überspringen und direkt mit dem Kapitel [Wie funktioniert das Internet?](how_the_internet_works.md) fortfahren. Ansonsten findest du hier eine Sammlung aller Installationshinweise, die ansonsten in den einzelnen Kapiteln versteckt sind. Folge den Anweisungen hier so gut, wie du kannst. Wenn du am Workshoptag dann im Tutorial auf einen Installationsschritt triffst, der dir zu Hause nicht gelungen ist, frage deinen Coach um Hilfe.

Wenn du mit dem Lernen beginnen willst, bevor du eine Hand voll Sachen auf deinem Computer installierst, kannst du dieses Kapitel auch überspringen und unsere Erklärungen zur Installation später im Tutorial aufgreifen

Viel Erfolg!

## Installation

In diesem Tutorial wirst du einen Blog bauen. Dafür wirst du während des Tutorials aufgefordert, verschiedene Software auf deinem Computer zu installieren und auch einige Online-Konten anzulegen, wenn sie gebraucht werden. Diese Seite fasst alle Installations- und Kontoeinrichtungs-Anweisungen an einer Stelle zusammen \(das ist für einige Workshopformate sinnvoll\).

## Kurze Einführung in die Kommandozeile

Viele der folgenden Schritte beziehen sich auf die "Konsole", das "Terminal", das "Kommandozeilen-Fenster" oder die "Kommandozeile" -- all diese Begriffe bezeichnen dasselbe: Ein Fenster auf deinem Computer, in das du Kommandos eingeben kannst. Im Hauptteil des Tutorials wirst du mehr über die Kommandozeile lernen. Vorerst musst du nur wissen, wie du ein Kommandozeilenfester öffnen kannst und wie eines aussieht:

## Python installieren



> Für Leserinnen zuhause: Dieses Kapitel wird auch im Video [Installing Python & Code Editor](https://www.youtube.com/watch?v=pVTaqzKZCdA) behandelt.
>
> Dieses Kapital basiert auf einem Tutorial der Geek Girls Carrots \([https://github.com/ggcarrots/django-carrots](https://github.com/ggcarrots/django-carrots)\).

Django ist in Python geschrieben. Wir brauchen Python für alles in Django. Fangen wir mit der Installation an! Wir möchten, dass du Python 3 installierst. Solltest du also bereits eine ältere Version installiert haben, musst du diese aktualisieren. Wenn du schon Version 3.4 oder höher besitzt, ist das in Ordnung.

### Windows

Bitte schau zuerst auf der "Systemtyp"-Zeile der Systeminformationsseite nach, ob auf deinem Computer eine 32-Bit-Version oder eine 64-Bit-Version von Windows läuft. Um diese Seite zu finden, versuche eine der folgenden Methoden:

* Drücke die Windows-Taste und die Pause/Break-Taste zur selben Zeit
* Öffne dein Control Panel über das Windows Menü und navigiere dann zu System & Sicherheit, dann System
* Drücke die Windows-Taste und navigiere dann zu Einstellungen &gt; System &gt; Über

Du kannst Python für Windows von der Webseite [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/) herunterladen. Klicke auf den "Latest Python 3 Release - Python x.x.x" Link. Wenn du eine **64-bit**-Version von Windows benutzt, lade die Datei **Windows x86-64 executable installer** herunter. Andernfalls lade den **Windows x86 executable installer** herunter. Führe den Installer nach dem Download \(per Doppelklick\) aus und folge den Anweisungen des Installationsprogramms.

Auf eine Sache solltest du achten: Während der Installation wird ein Setup-Fenster auftauchen. Stell sicher, dass du die Checkbox mit "Add Python 3.6 to PATH" oder "Add Python to your environment variables" aktiviert hast und klicke dann auf "Install Now" wie hier gezeigt \(es kann bei dir etwas anders aussehen, wenn du eine andere Version installierst\):

[![Vergiss nicht, Python zum Pfad hinzuzuf&#xFC;gen](https://github.com/hannesrothe/tutorial/raw/master/de/python_installation/images/python-installation-options.png)](https://github.com/hannesrothe/tutorial/blob/master/de/python_installation/images/python-installation-options.png)

Wenn die Installation abgeschlossen ist, siehst du vielleicht ein Dialogfeld mit einem Link, wo du mehr über Python oder über die Version lernen kannst. Schließe es oder brich den Dialog ab -- du wirst darüber mehr in diesem Tutorial lernen!

Hinweis: Falls du eine ältere Version von Windows verwendest \(7, Vista oder älter\) und die Installation von Python 3.6.x mit einer Fehlermeldung fehlschlägt, kannst du Folgendes versuchen:

1. Installiere alle Windows-Updates und versuche erneut, Python zu installieren; oder
2. Installiere eine [ältere Version von Python](https://www.python.org/downloads/windows/), z. B. [3.4.6](https://www.python.org/downloads/release/python-346/).

Wenn du eine ältere Version von Python installierst, kann es sein, dass die Installationsanzeige etwas anders aussieht als oben gezeigt. Stell sicher, dass du nach unten scrollst bis du "Add python.exe to Path" siehst, klicke den Button und wähle "Will be installed on local hard drive":

[![Python zum Pfad hinzuf&#xFC;gen \(Installer von &#xE4;lterer Python-Version\)](https://github.com/hannesrothe/tutorial/raw/master/de/python_installation/images/add_python_to_windows_path.png)](https://github.com/hannesrothe/tutorial/blob/master/de/python_installation/images/add_python_to_windows_path.png)

### **Install Python: OS X**

> **Hinweis** Bevor du Python auf Mac OS X installierst, musst du sicherstellen, dass deine Mac-Einstellungen es erlauben, Pakete zu installieren, die nicht aus dem App Store stammen. Geh auf Systemeinstellungen \(im Ordner "Programme"\), klicke auf "Sicherheit", und dann auf die Registerkarte "Allgemein". Wenn "Apps-Download erlauben von:" auf "Mac App Store" gestellt ist, ändere die Einstellung auf "Mac App Store und verifizierte Entwickler".

Auf der Website [https://www.python.org/downloads/release/python-361/](https://www.python.org/downloads/release/python-361/) findest du den passenden Python-Installer:

* Lade die Datei _Mac OS X 64-bit/32-bit installer_ herunter,
* Doppelklicke auf _python-3.6.1-macosx10.6.pkg_, um die Installation zu starten.

### **Install Python: Linux**

Es ist ziemlich wahrscheinlich, dass du Python schon automatisch installiert hast. Um herauszufinden, ob das so ist \(und wenn ja, welche Version du hast\), öffne eine Konsole und gib das folgende Kommando ein:

{% code-tabs %}
{% code-tabs-item title="in der Kommandozeile" %}
```text
$ python3 --version
Python 3.6.1
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Wenn du eine andere 'Mikroversion' von Python installiert hast, z.B. 3.6.0, dann musst du die Version nicht aktualisieren. Wenn Python bei dir nicht installiert ist, oder du eine neuere Version willst, kannst du das folgendermaßen tun:**Install Python: Debian or Ubuntu**

Gib diesen Befehl in die Konsole ein:

{% code-tabs %}
{% code-tabs-item title="in der Kommandozeile" %}
```text
$ sudo apt install python3
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### **Install Python: Fedora**

Gib diesen Befehl in die Konsole ein:

{% code-tabs %}
{% code-tabs-item title="in der Kommandozeile" %}
```text
$ sudo dnf install python3
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Auf älteren Fedora-Versionen kann es sein, dass du eine Fehlermeldung bekommst, dass das Kommando `dnf` nicht gefunden wird. Falls das passiert, musst du stattdessen `yum` verwenden.

### **Install Python: openSUSE**

Gib diesen Befehl in die Konsole ein:

{% code-tabs %}
{% code-tabs-item title="in der Kommandozeile" %}
```text
$ sudo zypper install python3
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Prüfe, ob die Installation erfolgreich war, indem du ein Kommandozeilenfenster öffnest und den `python3`-Befehl ausführst:

{% code-tabs %}
{% code-tabs-item title="in der Kommandozeile" %}
```text
$ python3 --version
Python 3.6.1
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Die angezeigte Version kann bei dir eine andere sein als 3.6.1 -- sie sollte aber der entsprechen, die du installiert hast.

**Hinweis:** Wenn du unter Windows eine Fehlermeldung bekommst, dass `python3` nicht gefunden wurde, versuche es mit `python` \(ohne die `3`\) und prüfe, ob es dennoch eine Version von Python 3.4.0 oder höher ist.

Wenn es Unklarheiten gibt oder wenn etwas schief ging und du nicht weiter weißt, frage bitte deinen Coach! Manchmal laufen die Dinge einfach nicht so glatt und dann ist es besser, jemanden mit mehr Erfahrung um Hilfe zu bitten.

## Einen Code-Editor installieren

Es gibt viele verschiedene Editoren. Welcher für dich am besten ist, ist weitestgehend Geschmackssache. Die meisten Python-Programmiererinnen verwenden komplexe, aber extrem leistungsfähige IDEs \(Integrated Development Environments\), z. B. PyCharm. Für Anfängerinnen sind diese jedoch weniger gut geeignet. Unsere Empfehlungen sind ebenso leistungsfähig, aber viel einfacher zu bedienen.

Unsere Vorschläge siehst du unten. Aber fühl dich ganz frei, deine Trainerin zu fragen, was ihre Vorlieben sind - wenn sie sich mit dem Editor auskennt, wird es leichter sein, Hilfe zu erhalten.

### Visual Studio Code \(empfohlen\)

Code ist ein mittlerweile sehr beliebter Editor. Es gibt ihn für alle Betriebssysteme. Code wird von Microsoft entwickelt.

[Du kannst ihn hier herunterladen](https://code.visualstudio.com/)

### Gedit

Gedit ist ein kostenloser Open-Source-Editor. Es gibt ihn für alle Betriebssysteme.

[Du kannst ihn hier herunterladen](https://wiki.gnome.org/Apps/Gedit#Download)

### Atom

Atom ist ein weiterer beliebter Editor. Er ist gratis, Open-Source und für Windows, OS X und Linux verfügbar. Atom wird von [GitHub](https://github.com/) entwickelt.

[Du kannst ihn hier herunterladen](https://atom.io/)

### Sublime Text 3

Sublime Text ist ein sehr beliebter Editor, nutzbar für einen kostenlosen Testzeitraum. Er ist einfach zu installieren und zu verwenden, und er ist für alle Betriebssysteme verfügbar.

[Du kannst ihn hier herunterladen](https://www.sublimetext.com/3)

### Warum installieren wir einen Code-Editor?

Vielleicht wunderst du dich, warum wir so spezielle Code-Editor-Software installieren, statt einfach etwas wie Word oder Notepad zu benutzen.

Erstens muss Code "plain text" \(unformatierter Text\) sein. Das Problem mit Programmen wie Word und Textedit ist, dass sie nicht "plain text" sondern "rich text" \(mit Schriftarten und Formatierungen\) produzieren und besondere Formate wie RTF \(Rich Text Format\) verwenden.

Ein weiterer Grund ist, dass Code-Editoren \(bisweilen auch Programmier- oder Text-Editoren genannt\) auf das Bearbeiten von Programm-Code spezialisiert sind und Funktionen aufweisen, die normale Textverarbeitungen nicht haben. Beispielsweise sogenanntes "Syntax-Highlighting", also farbliches Hervorheben bestimmter Code-Stellen, oder auch das automatische Schließen von Klammern und vieles mehr.

Einiges davon werden wir später in Aktion sehen. Glaub uns: es wird nicht lange dauern, bis du deinen Code-Editor nicht mehr missen möchtest. :\)

## Virtuelle Umgebung

Bevor wir mit der Installation von Django beginnen, lernen wir ein sehr hilfreiches Tool kennen, das uns hilft, unsere Arbeitsumgebung zum Coden sauber zu halten. Es ist möglich, diesen Schritt zu überspringen, aber wir legen ihn dir dennoch besonders ans Herz. Mit dem bestmöglichen Setup zu starten, wird dir in der Zukunft eine Menge Frust ersparen!

Wir erzeugen eine virtuelle Arbeitsumgebung - ein **virtual environment** oder auch _virtualenv_. Das isoliert die Python-/Django-Setups verschiedener Projekte voneinander. Das bedeutet, dass deine Änderungen an einem Website-Projekt keine anderen Projekte beeinträchtigen, an welchen du sonst noch entwickelst. Klingt nützlich, oder?

Du musst nur das Verzeichnis festlegen, in dem du das `virtualenv` erstellen willst; zum Beispiel dein Home-Verzeichnis. Auf Windows ist dies `C:\Users\Name` \(`Name` ist dein Anmeldename/Login\).

> **HINWEIS:** Stelle auf Windows sicher, dass dieser Verzeichnisname keine Umlaute oder Sonderzeichen enthält. Falls dein Benutzername Umlaute enthält, verwende ein anderes Verzeichnis, zum Beispiel `C:\djangogirls`.

In diesem Tutorial erstellen wir darin ein neues Verzeichnis `djangogirls`:

command-line

```text
$ mkdir djangogirls
$ cd djangogirls
```

Wir erstellen eine virtuelle Umgebung namens `myvenv`. Das Kommando dazu lautet dann:

command-line

```text
$ python3 -m venv myvenv
```

**Virtual environment: Windows**

Um ein neues `virtualenv` zu erzeugen, musst du auf der Kommandozeile von Windows `python -m venv myvenv` ausführen. Das wird so aussehen:

command-line

```text
C:\Users\Name\djangogirls> python -m venv myvenv
```

wobei `myvenv` der Name deines `virtualenv` ist. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen, Umlaute oder Sonderzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!**Virtual environment: Linux and OS X**

Auf Linux oder OS X kann ein `virtualenv` durch das Ausführen von `python3 -m venv myvenv`erzeugt werden. Das wird so aussehen:

command-line

```text
$ python3 -m venv myvenv
```

`myvenv` ist der Name deiner neuen virtuellen Arbeitsumgebung, deines neuen `virtualenv`. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!

> **Hinweis:** Bei manchen Versionen von Debian/Unbuntu kann folgender Fehler auftreten:
>
> command-line
>
> ```text
> The virtual environment was not created successfully because ensurepip is not available.  On Debian/Ubuntu systems, you need to install the python3-venv package using the following command.
>    apt install python3-venv
> You may need to use sudo with that command.  After installing the python3-venv package, recreate your virtual environment.
> ```
>
> Falls das auftritt, folge den Anweisungen in der Fehlermeldung und installiere das `python3-venv`-Paket:
>
> command-line
>
> ```text
> $ sudo apt install python3-venv
> ```
>
> **HINWEIS:** In manchen Debian/Ubuntu-Versionen kann das zu folgendem Fehler führen:
>
> command-line
>
> ```text
> Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
> ```
>
> Falls das eintritt, verwende stattdessen den `virtualenv`-Befehl.
>
> command-line
>
> ```text
> $ sudo apt install python-virtualenv
> $ virtualenv --python=python3.6 myvenv
> ```
>
> **HINWEIS:** Wenn du einen Fehler wie
>
> command-line
>
> ```text
> E: Unable to locate package python3-venv
> ```
>
> erhältst, führe stattdessen Folgendes aus:
>
> command-line
>
> ```text
> sudo apt install python3.6-venv
> ```

### Mit der virtuellen Umgebung arbeiten <a id="mit-der-virtuellen-umgebung-arbeiten"></a>

Die obigen Kommandos erstellen ein Verzeichnis `myvenv` \(bzw. den von Dir vergebenen Namen\). Es enthält unsere virtuelle Arbeitsumgebung \(im Wesentlichen ein paar Verzeichnisse und Dateien\).**Working with virtualenv: Windows**

Starte deine virtuelle Umgebung, indem du Folgendes eingibst:

command-line

```text
C:\Users\Name\djangogirls> myvenv\Scripts\activate
```

> **HINWEIS:** Auf Windows 10 kannst du in der Windows PowerShell die Fehlermeldung `execution of scripts is disabled on this system` erhalten. Öffne in diesem Fall eine weitere Windows PowerShell über "Als Administrator ausführen". Versuche dann, das folgende Kommando einzugeben, bevor du das virtualenv noch einmal aktivierst:
>
> command-line
>
> ```text
> C:\WINDOWS\system32> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
>     Execution Policy Change
>     The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy? [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): A
> ```

**Working with virtualenv: Linux and OS X**

Starte deine virtuelle Umgebung, indem du eingibst:

command-line

```text
$ source myvenv/bin/activate
```

Der Name `myvenv` muss mit dem von Dir gewählten Namen des `virtualenv` übereinstimmen!

> **Anmerkung:** Manchmal ist das Kommando `source` nicht verfügbar. In diesen Fällen geht es auch so:
>
> command-line
>
> ```text
> $ . myvenv/bin/activate
> ```

Du erkennst, dass dein `virtualenv` gestartet ist, wenn du vor der Eingabeaufforderung eine Klammer mit dem Namen deiner Umgebung siehst, `(myvenv)`.

In deiner neuen virtuellen Umgebung wird automatisch die richtige Version von `python` verwendet. Du kannst also `python` statt `python3` eingeben.

Ok, jetzt ist die erforderliche Umgebung startklar und wir können endlich Django installieren!

## Django-Installation

Da du nun dein `virtualenv` gestartet hast, kannst du Django installieren.

Bevor wir damit loslegen, sollten wir jedoch sicherstellen, dass wir die neueste Version von `pip` haben, eine Software, mit Hilfe derer wir Django installieren werden:

command-line

```text
(myvenv) ~$ python -m pip install --upgrade pip
```

#### Pakete mittels requirements-Datei installieren

Eine requirements-Datei enthält eine Liste von Abhängigkeiten, die von `pip install` installiert werden sollen:

Erstelle mit dem zuvor installierten Code-Editor eine Datei namens `requirements.txt` im Verzeichnis `djangogirls/`. Das machst du, indem du eine neue Datei in deinem Code-Editor öffnest und als `requirements.txt` im Ordner `djangogirls/` abspeicherst. Dein Ordner sieht jetzt so aus:

```text
djangogirls
└───requirements.txt
```

Schreibe in die Datei `djangogirls/requirements.txt` folgenden Text:

djangogirls/requirements.txt

```text
Django~=2.0.6
```

Führe nun `pip install -r requirements.txt` aus, um Django zu installieren.

command-line

```text
(myvenv) ~$ pip install -r requirements.txt
Collecting Django~=2.0.6 (from -r requirements.txt (line 1))
  Downloading Django-2.0.6-py3-none-any.whl (7.1MB)
Installing collected packages: Django
Successfully installed Django-2.0.6
```

#### **Installing Django: Windows**

> Wenn du einen Fehler auf einem Windowsrechner bekommst, überprüfe, ob der Pfadname deines Projekts Leerzeichen, Umlaute oder Sonderzeichen enthält \(z.B. `C:\Users\User Name\djangogirls`\). Ist das der Fall, dann verwende bitte einen anderen Ordner ohne Sonderzeichen, Umlaute oder Leerzeichen. \(Vorschlag: `C:\djangogirls`\). Erstelle ein neues virtualenv in einem neuen Verzeichnis, lösche danach das alte und wiederhohle den oben genannten Befehl. \(Das Verzeichnis des virtualenv zu verschieben funktioniert dabei nicht, da virtualenv absolute Pfade verwendet.\)

#### **Installing Django: Windows 8 and Windows 10**

> Es kann sein, dass deine Befehlszeile einfriert, wenn du versuchst Django zu installieren. Sollte das passieren, nutze folgenden Befehl anstelle des oben angegebenen:
>
> command-line
>
> ```text
> C:\Users\Name\djangogirls> python -m pip install -r requirements.txt
> ```

#### **Installing Django: Linux**

> Falls der pip-Aufruf auf Ubuntu 12.04 zu einer Fehlermeldung führt, rufe `python -m pip install -U --force-reinstall pip` auf, um die Installation von pip im virtualenv zu reparieren.

Das war's! Du bist nun \(endlich\) bereit, deine erste Django-Anwendung zu starten!

## Git

> **Hinweis:** Falls du die Installationsschritte bereits durchgeführt hast, kannst du mit dem nächsten Abschnitt fortfahren und anfangen, dein Git-Repository zu erstellen.

Git ist ein "Versionsverwaltungssystem" für Dateien und Code, das von vielen Programmierern benutzt wird. Diese Software kann Änderungen an Dateien über die Zeit verfolgen, so dass du bestimmte Versionen im Nachhinein wieder aufrufen kannst. Sie hat Ähnlichkeit mit der Funktion "Änderungen nachverfolgen" in Textverarbeitungsprogrammen \(z. B. Microsoft Word oder LibreOffice Writer\), ist jedoch weitaus leistungsfähiger.Git installieren

#### **Installing Git: Windows**

Du kannst Git von [git-scm.com](https://git-scm.com/) herunterladen. Du kannst bei allen Schritten außer zweien "next" klicken: Wähle im Schritt, in dem du einen Editor aussuchen sollst, "Nano"; und bei der Anweisung "Adjusting your PATH environment", wähle die Einstellung "Run Git and associated Unix tools from the Windows command-line" \(die letzte Option\). Die anderen Voreinstellungen sind ok. "Checkout"-Stil "Windows" und "Commit" mit "Unix line endings" \(Zeilenende im Unix-Format\) sind die richtigen Einstellungen.

Nach Abschluss der Installation musst du deine Command-Shell oder Powershell neu starten, damit die Einstellungen aktiv sind.

#### **Installing Git: OS X**

Lade Git von [git-scm.com](https://git-scm.com/) herunter und folge dann den Anweisungen.

> **Hinweis:** Falls du OS X 10.6, 10.7, oder 10.8 verwendest, muss du die Git-Version unter folgendem Link installieren: [Git installer for OS X Snow Leopard](https://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download)

#### **Installing Git: Debian or Ubuntu**

command-line

```text
$ sudo apt install git
```

#### **Installing Git: Fedora**

command-line

```text
$ sudo dnf install git
```

#### **Installing Git: openSUSE**

command-line

```text
$ sudo zypper install git
```

### Einen GitHub-Account erstellen

Gehe zu [GitHub.com](https://www.github.com) und registriere dich für ein neues, kostenfreies Benutzerkonto. Achte darauf, dass du dein Passwort nicht vergisst \(füge es deinem Passwortmanager hinzu, wenn du einen benutzt\).

## Chromebook

Du kannst [diesen Abschnitt einfach](http://tutorial.djangogirls.org/en/installation/#install-python) überspringen, falls du kein Chromebook benutzt. Wenn du eins benutzt, wird deine Installation ein wenig anders sein. Du kannst den Rest der Installationsanweisungen ignorieren.

#### Cloud IDE \(PaizaCloud Cloud IDE, AWS Cloud9\)

Mit dem Tool Cloud IDE erhältst du Zugang zu einem Code-Editor und einem Rechner, der im Internet läuft und auf dem du die Software installieren, schreiben und ausführen kannst. Für die Dauer des Tutorials wird Cloud IDE zu deinem _lokalen Rechner_. Auch du wirst Befehle in einer Kommandozeilen-Oberfläche ausführen können, genau wie die anderen Teilnehmerinnen, die mit OS X, Ubuntu oder Windows arbeiten. Dein Terminal wird jedoch mit einem Rechner verbunden sein, den Cloud IDE dir bereitstellt. Hier ist die Anleitung für die Cloud IDEs \(PaizaCloud, Cloud IDE, AWS Cloud9\). Wähle eine der Cloud IDEs aus und folge den Anweisungen der gewählten Cloud IDE.

**PaizaCloud Cloud IDE**

1. Gehe zu [PaizaCloud Cloud IDE](https://paiza.cloud/)
2. Lege dir dort ein Benutzerkonto an
3. Klicke auf _New Server_
4. Klicke auf die Schaltfläche "Terminal" \(links im Browserfenster\)

Jetzt solltest du links eine Schnittstelle mit einer Seitenleiste und Schaltflächen sehen. Klicke auf den "Terminal"-Button und öffne das Terminal-Fenster mit einer Eingabeaufforderung wie folgt:

{% code-tabs %}
{% code-tabs-item title="im Browser" %}
```text
$
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Das Terminal auf der PaizaCloud Cloud IDE steht für deine Anweisungen bereit. Du kannst die Größe des Fensters frei einstellen.

**AWS Cloud9**

1. Gehe zu [AWS Cloud9](https://aws.amazon.com/cloud9/)
2. Lege dir dort ein Benutzerkonto an
3. Klicke auf _Create Environment_

Jetzt solltest du eine Benutzeroberfläche mit Seitenleiste, ein grosses Fenster mit Text und am unteren Rand ein Feld sehen, das wie folgt aussieht:

{% code-tabs %}
{% code-tabs-item title="Im Bash" %}
```text
deinbenutzername:~/workspace $
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Dieser untere Bereich ist dein Terminal. Dort kannst du Kommandos für den Computer eingeben, den dir Cloud 9 zur Verfügung stellt. Du kannst dieses Fenster vergrößern oder verkleinern.

#### Virtuelle Umgebung

Eine virtuelle Umgebung \(auch virtualenv genannt\) ist wie ein privater Behälter, in den wir nützlichen Code für ein Projekt packen können, an dem wir arbeiten. Wir benutzen sie, um Code für verschiedene Projekte getrennt aufzubewahren, damit dieser nicht vermischt wird.

Führe im Terminal den folgenden Code aus \(das Terminal befindet sich am unteren Rand des Cloud 9-Interfaces\):

{% code-tabs %}
{% code-tabs-item title="Cloud 9" %}
```text
sudo apt update
sudo apt install python3.6-venv
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Falls das nicht funktioniert, frag' deinen Coach um Hilfe.

Führe dann die folgenden Befehle aus:

{% code-tabs %}
{% code-tabs-item title="Cloud 9" %}
```text
mkdir djangogirls
cd djangogirls python3.6 -mvenv myvenv
source myvenv/bin/activate
pip install django~={{ book.django_version }}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

\(Beachte, dass wir im letzten Befehl eine Tilde gefolgt von einem Gleichheitssymbol benutzen: `~=`\).

#### GitHub

Erstelle einen [GitHub](https://github.com/)-Account.

## Einen PythonAnywhere-Account erstellen \(optional\)

PythonAnywhere ist ein Dienst, mittels dem Python auf Servern "in der Cloud" ausgeführt werden kann. Wir werden ihn verwenden, um unsere Seite zu hosten, live und im Internet.

Wir werden den Blog, den wir bauen, auf PythonAnywhere hosten. Registriere dich auf PythonAnywhere für ein "Beginner"-Konto \(die kostenfreie Stufe ist ausreichend, du brauchst keine Kreditkarte\).

* [www.pythonanywhere.com](https://www.pythonanywhere.com/)

[![Die PythonAnywhere-Anmelde-Seite mit einem Knopf, um ein kostenloses &apos;Beginner&apos;-Benutzerkonto anzulegen](https://github.com/hannesrothe/tutorial/raw/master/de/deploy/images/pythonanywhere_beginner_account_button.png)](https://github.com/hannesrothe/tutorial/blob/master/de/deploy/images/pythonanywhere_beginner_account_button.png)

> **Hinweis** Beachte bei der Wahl deines PythonAnywhere-Benutzernamens, dass die URL deines Blogs die Form `deinbenutzername.pythonanywhere.com` haben wird. Wähle also einen Namen, unter dem du veröffentlichen willst, oder einen Namen, der den Inhalt deines Blogs beschreibt. Und vergiss dein Passwort nicht \(füge es deinem Passwortmanager hinzu, wenn du einen benutzt\).

### Erstellen eines PythonAnywhere API-Tokens

Das Folgende musst du nur einmal machen. Wenn du dich auf PythonAnywhere angemeldet hast, kommst du aufs "Dashboard". Oben rechts findest du den Link zu deiner "Account"-Seite:

[![&quot;Account&quot;-Link oben rechts auf der Seite](https://github.com/hannesrothe/tutorial/raw/master/de/deploy/images/pythonanywhere_account.png)](https://github.com/hannesrothe/tutorial/blob/master/de/deploy/images/pythonanywhere_account.png)

Klicke dort auf den Reiter namens "API token" und dann auf den Knopf, der mit "Create new API token" beschriftet ist.

[![Der API-Token-Reiter auf der &quot;Account&quot;-Seite](https://github.com/hannesrothe/tutorial/raw/master/de/deploy/images/pythonanywhere_create_api_token.png)](https://github.com/hannesrothe/tutorial/blob/master/de/deploy/images/pythonanywhere_create_api_token.png)

## Fang an zu lesen!

Herzlichen Glückwunsch, du hast alles eingerichtet und bist nun bereit loszulegen! Wenn du vor dem Workshop noch etwas Zeit hast, wäre es hilfreich, einige der einführenden Kapitel zu lesen:

* [Wie das Internet funktioniert](how_the_internet_works.md)
* [Einführung in die Kommandozeile](intro_to_command_line.md)
* [Einführung in Python](python_introduction.md)
* [Django - Was ist das?](django.md)

## Viel Spaß beim Workshop!

Wenn du mit dem Workshop anfängst, kannst du direkt zum Kapitel [Dein erstes Django-Projekt!](django_start_project.md) gehen, weil du den Inhalt der vorhergehenden Kapitel schon bearbeitet hast.

