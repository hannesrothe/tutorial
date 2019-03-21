# W3 Django-Installation

> **Hinweis** Wenn du ein Chromebook verwendest, überspringe bitte dieses Kapitel und folge den Anweisungen im [Chromebook Setup](chromebook_setup.md).
>
> **Hinweis:** Falls du dich bereits durch die Installationsschritte gearbeitet hast, gibt es keinen Grund dies erneut zu tun - du kannst direkt zum nächsten Kapitel springen!



```text
irls> python -m venv myvenv
```

wobei `myvenv` der Name deines `virtualenv` ist. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen, Umlaute oder Sonderzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!

Auf Linux oder OS X kann ein `virtualenv` durch das Ausführen von `python3 -m venv myvenv` erzeugt werden. Das wird so aussehen:

{% filename %}command-line{% endfilename %}

```text
$ python3 -m venv myvenv
```

`myvenv` ist der Name deiner neuen virtuellen Arbeitsumgebung, deines neuen `virtualenv`. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!

> **Hinweis:** Bei manchen Versionen von Debian/Unbuntu kann folgender Fehler auftreten:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> The virtual environment was not created successfully because ensurepip is not available.  On Debian/Ubuntu systems, you need to install the python3-venv package using the following command.
>    apt install python3-venv
> You may need to use sudo with that command.  After installing the python3-venv package, recreate your virtual environment.
> ```
>
> Falls das auftritt, folge den Anweisungen in der Fehlermeldung und installiere das `python3-venv`-Paket: {% filename %}command-line{% endfilename %}
>
> ```text
> $ sudo apt install python3-venv
> ```
>
> **HINWEIS:** In manchen Debian/Ubuntu-Versionen kann das zu folgendem Fehler führen:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
> ```
>
> Falls das eintritt, verwende stattdessen den `virtualenv`-Befehl.
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> $ sudo apt install python-virtualenv
> $ virtualenv --python=python3.6 myvenv
> ```
>
> **HINWEIS:** Wenn du einen Fehler wie
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> E: Unable to locate package python3-venv
> ```
>
> erhältst, führe stattdessen Folgendes aus:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> sudo apt install python3.6-venv
> ```

### Mit der virtuellen Umgebung arbeiten

Die obigen Kommandos erstellen ein Verzeichnis `myvenv` \(bzw. den von Dir vergebenen Namen\). Es enthält unsere virtuelle Arbeitsumgebung \(im Wesentlichen ein paar Verzeichnisse und Dateien\).

Starte deine virtuelle Umgebung, indem du Folgendes eingibst:

{% filename %}command-line{% endfilename %}

```text
C:\Users\Name\djangogirls> myvenv\Scripts\activate
```

> **HINWEIS:** Auf Windows 10 kannst du in der Windows PowerShell die Fehlermeldung `execution of scripts is disabled on this system` erhalten. Öffne in diesem Fall eine weitere Windows PowerShell über "Als Administrator ausführen". Versuche dann, das folgende Kommando einzugeben, bevor du das virtualenv noch einmal aktivierst:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> C:\WINDOWS\system32> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
>     Execution Policy Change
>     The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy? [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): A
> ```

Starte deine virtuelle Umgebung, indem du eingibst:

{% filename %}command-line{% endfilename %}

```text
$ source myvenv/bin/activate
```

Der Name `myvenv` muss mit dem von Dir gewählten Namen des `virtualenv` übereinstimmen!

> **Anmerkung:** Manchmal ist das Kommando `source` nicht verfügbar. In diesen Fällen geht es auch so:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> $ . myvenv/bin/activate
> ```

Du erkennst, dass dein `virtualenv` gestartet ist, wenn du vor der Eingabeaufforderung eine Klammer mit dem Namen deiner Umgebung siehst, `(myvenv)`.

In deiner neuen virtuellen Umgebung wird automatisch die richtige Version von `python` verwendet. Du kannst also `python`statt `python3` eingeben.

Ok, jetzt ist die erforderliche Umgebung startklar und wir können endlich Django installieren!

### Django-Installation

Da du nun dein `virtualenv` gestartet hast, kannst du Django installieren.

Bevor wir damit loslegen, sollten wir jedoch sicherstellen, dass wir die neueste Version von `pip` haben, eine Software, mit Hilfe derer wir Django installieren werden:

{% filename %}command-line{% endfilename %}

```text
(myvenv) ~$ python -m pip install --upgrade pip
```

#### Pakete mittels requirements-Datei installieren

Eine requirements-Datei enthält eine Liste von Abhängigkeiten, die von `pip install` installiert werden sollen:

Erstelle mit dem zuvor installierten Code-Editor eine Datei namens `requirements.txt` im Verzeichnis `djangogirls/`. Das machst du, indem du eine neue Datei in deinem Code-Editor öffnest und als `requirements.txt` im Ordner `djangogirls/`abspeicherst. Dein Ordner sieht jetzt so aus:

```text
djangogirls
└───requirements.txt
```

Schreibe in die Datei `djangogirls/requirements.txt` folgenden Text:

{% filename %}djangogirls/requirements.txt{% endfilename %}

```text
Django~={{ book.django_version }}
```

Führe nun `pip install -r requirements.txt` aus, um Django zu installieren.

{% filename %}command-line{% endfilename %}

```text
(myvenv) ~$ pip install -r requirements.txt
Collecting Django~={{ book.django_version }} (from -r requirements.txt (line 1))
  Downloading Django-{{ book.django_version }}-py3-none-any.whl (7.1MB)
Installing collected packages: Django
Successfully installed Django-{{ book.django_version }}
```

> Wenn du einen Fehler auf einem Windowsrechner bekommst, überprüfe, ob der Pfadname deines Projekts Leerzeichen, Umlaute oder Sonderzeichen enthält \(z.B. `C:\Users\User Name\djangogirls`\). Ist das der Fall, dann verwende bitte einen anderen Ordner ohne Sonderzeichen, Umlaute oder Leerzeichen. \(Vorschlag: `C:\djangogirls`\). Erstelle ein neues virtualenv in einem neuen Verzeichnis, lösche danach das alte und wiederhohle den oben genannten Befehl. \(Das Verzeichnis des virtualenv zu verschieben funktioniert dabei nicht, da virtualenv absolute Pfade verwendet.\)

> Es kann sein, dass deine Befehlszeile einfriert, wenn du versuchst Django zu installieren. Sollte das passieren, nutze folgenden Befehl anstelle des oben angegebenen:
>
> {% filename %}command-line{% endfilename %}
>
> ```text
> C:\Users\Name\djangogirls> python -m pip install -r requirements.txt
> ```

> Falls der pip-Aufruf auf Ubuntu 12.04 zu einer Fehlermeldung führt, rufe `python -m pip install -U --force-reinstall pip` auf, um die Installation von pip im virtualenv zu reparieren.

Das war's! Du bist nun \(endlich\) bereit, deine erste Django-Anwendung zu starten!

