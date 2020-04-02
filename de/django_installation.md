# W3 Django-Installation

\*\*\*\*

> **Hinweis** Wenn du ein Chromebook verwendest, überspringe bitte dieses Kapitel und folge den Anweisungen im [Chromebook Setup](https://tutorial.djangogirls.org/de/chromebook_setup/).
>
> **Hinweis:** Falls du dich bereits durch die Installationsschritte gearbeitet hast, gibt es keinen Grund dies erneut zu tun - du kannst direkt zum nächsten Kapitel springen!
>
> Ein Teil dieses Kapitels basiert auf den Tutorials von Geek Girls Carrots \([https://github.com/ggcarrots/django-carrots](https://github.com/ggcarrots/django-carrots)\).
>
> Teile dieses Kapitels basieren auf dem [django-marcador Tutorial](http://django-marcador.keimlink.de/) lizenziert unter der Creative Commons Attribution-ShareAlike 4.0 International License. Für das "django-marcador Tutorial" liegt das Urheberrecht bei Markus Zapke-Gründemann et al.

### Virtuelle Umgebung <a id="virtuelle-umgebung"></a>

Bevor wir mit der Installation von Django beginnen, lernen wir ein sehr hilfreiches Tool kennen, das uns hilft, unsere Arbeitsumgebung zum Coden sauber zu halten. Es ist möglich, diesen Schritt zu überspringen, aber wir legen ihn dir dennoch besonders ans Herz. Mit dem bestmöglichen Setup zu starten, wird dir in der Zukunft eine Menge Frust ersparen!

Wir erzeugen eine virtuelle Arbeitsumgebung - ein **virtual environment** oder auch _virtualenv_. Das isoliert die Python-/Django-Setups verschiedener Projekte voneinander. Das bedeutet, dass deine Änderungen an einem Website-Projekt keine anderen Projekte beeinträchtigen, an welchen du sonst noch entwickelst. Klingt nützlich, oder?

Du musst nur das Verzeichnis festlegen, in dem du das `virtualenv` erstellen willst; zum Beispiel dein Home-Verzeichnis. Auf Windows ist dies `C:\Users\Name` \(`Name` ist dein Anmeldename/Login\).

> **HINWEIS:** Stelle auf Windows sicher, dass dieser Verzeichnisname keine Umlaute oder Sonderzeichen enthält. Falls dein Benutzername Umlaute enthält, verwende ein anderes Verzeichnis, zum Beispiel `C:\djangogirls`.

In diesem Tutorial erstellen wir darin ein neues Verzeichnis `djangogirls`:

{% code title="in der Kommandozeile" %}
```text
$ mkdir djangogirls
$ cd djangogirls
```
{% endcode %}

Wir erstellen eine virtuelle Umgebung namens `myvenv`. 

#### **Windows \(eigener PC ohne Anaconda Umgebung\)**

Um ein neues `virtualenv` zu erzeugen, musst du auf der Kommandozeile von Windows `python -m venv myvenv` ausführen. Das wird so aussehen:

{% code title="in der Kommandozeile" %}
```text
C:\Users\Name\djangogirls> python -m venv myvenv
```
{% endcode %}

wobei `myvenv` der Name deines `virtualenv` ist. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen, Umlaute oder Sonderzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!

#### **Windows \(PC Pool mit Anaconda Umgebung\)**

Um ein neues `virtualenv` zu erzeugen, musst du auf der Kommandozeile von Windows `conda install -n myvenv` ausführen. Das wird so aussehen:

{% code title="in der Kommandozeile" %}
```text
C:\Users\Name\djangogirls> conda install -n mynvenv
```
{% endcode %}

#### **Linux and OS X**

Auf Linux oder OS X kann ein `virtualenv` durch das Ausführen von `python3 -m venv myvenv`erzeugt werden. Das wird so aussehen:

{% code title="in der Kommandozeile" %}
```text
$ python3 -m venv myvenv
```
{% endcode %}

`myvenv` ist der Name deiner neuen virtuellen Arbeitsumgebung, deines neuen `virtualenv`. Du kannst auch irgend einen anderen Namen wählen, aber bleibe bei Kleinbuchstaben und verwende keine Leerzeichen. Eine Gute Idee ist, den Namen kurz zu halten. Du wirst ihn oft benutzen bzw. eingeben müssen!

> **Hinweis:** Bei manchen Versionen von Debian/Unbuntu kann folgender Fehler auftreten:
>
> {% code title="in der Kommandozeile" %}
> ```text
> The virtual environment was not created successfully because ensurepip is not available.  On Debian/Ubuntu systems, you need to install the python3-venv package using the following command.
>    apt install python3-venv
> You may need to use sudo with that command.  After installing the python3-venv package, recreate your virtual environment.
> ```
> {% endcode %}
>
> Falls das auftritt, folge den Anweisungen in der Fehlermeldung und installiere das `python3-venv`-Paket:
>
> {% code title="in der Kommandozeile" %}
> ```text
> $ sudo apt install python3-venv
> ```
> {% endcode %}
>
> **HINWEIS:** In manchen Debian/Ubuntu-Versionen kann das zu folgendem Fehler führen:
>
> {% code title="in der Kommandozeile" %}
> ```text
> Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
> ```
> {% endcode %}
>
> Falls das eintritt, verwende stattdessen den `virtualenv`-Befehl.

> {% code title="in der Kommandozeile" %}
> ```text
> $ sudo apt install python-virtualenv
> $ virtualenv --python=python3.6 myvenv
> ```
> {% endcode %}
>
> **HINWEIS:** Wenn du einen Fehler wie

> {% code title="in der Kommandozeile" %}
> ```text
> E: Unable to locate package python3-venv
> ```
> {% endcode %}
>
> erhältst, führe stattdessen Folgendes aus:

> {% code title="in der Kommandozeile" %}
> ```text
> sudo apt install python3.6-venv
> ```
> {% endcode %}

### Mit der virtuellen Umgebung arbeiten <a id="mit-der-virtuellen-umgebung-arbeiten"></a>

Die obigen Kommandos erstellen ein Verzeichnis `myvenv` \(bzw. den von Dir vergebenen Namen\). Es enthält unsere virtuelle Arbeitsumgebung \(im Wesentlichen ein paar Verzeichnisse und Dateien\).

#### **Windows \(eigener PC ohne Anaconda Umgebung\)**

Starte deine virtuelle Umgebung, indem du Folgendes eingibst:

{% code title="in der Kommandozeile" %}
```text
C:\Users\Name\djangogirls> myvenv\Scripts\activate
```
{% endcode %}

Bei Erfolg sollte in deiner Kommandozeile nun die virtuelle Umgebung in Klammern vorangestellt sein. Das sieht in etwa so aus:

{% code title="in der Kommandozeile" %}
```text
(myvenv) C:\Users\Name\djangogirls>
```
{% endcode %}

> **HINWEISE:**  
> Auf Windows 10 kannst du in der Windows PowerShell die Fehlermeldung `execution of scripts is disabled on this system` erhalten. Öffne in diesem Fall eine weitere Windows PowerShell über "Als Administrator ausführen". Versuche dann, das folgende Kommando einzugeben, bevor du das virtualenv noch einmal aktivierst:

> {% code title="in der Kommandozeile" %}
> ```text
> C:\WINDOWS\system32> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
>     Execution Policy Change
>     The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy? [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): A
> ```
> {% endcode %}

#### **Windows \(PC Pool mit Anaconda Umgebung\)**

Starte deine virtuelle Umgebung, indem du Folgendes eingibst:

{% code title="in der Kommandozeile" %}
```text
C:\Users\Name\djangogirls> activate myvenv
```
{% endcode %}

Bei Erfolg sollte in deiner Kommandozeile nun die virtuelle Umgebung in Klammern vorangestellt sein. Das sieht in etwa so aus:

{% code title="in der Kommandozeile" %}
```text
(myvenv) C:\Users\Name\djangogirls>
```
{% endcode %}

> **Anmerkung:** Um die virtuelle Umgebung zu verlassen gebe `deactivate` ein:
>
> {% code title="in der Kommandozeile" %}
> ```text
> (myvenv) C:\Users\Name\djangogirls> deactivate
> ```
> {% endcode %}

#### **Linux and OS X**

Starte deine virtuelle Umgebung, indem du eingibst:

{% code title="in der Kommandozeile" %}
```text
$ source myvenv/bin/activate
```
{% endcode %}

Der Name `myvenv` muss mit dem von Dir gewählten Namen des `virtualenv` übereinstimmen!

> **Anmerkung:** Manchmal ist das Kommando `source` nicht verfügbar. In diesen Fällen geht es auch so:

> {% code title="in der Kommandozeile" %}
> ```text
> $ . myvenv/bin/activate
> ```
> {% endcode %}

Bei Erfolg sollte in deiner Kommandozeile nun die virtuelle Umgebung in Klammern vorangestellt sein. Das sieht in etwa so aus:

{% code title="in der Kommandozeile" %}
```text
(myvenv) C:\Users\Name\djangogirls>
```
{% endcode %}

In deiner neuen virtuellen Umgebung wird automatisch die richtige Version von `python` verwendet. Du kannst also `python` statt `python3` eingeben.

Ok, jetzt ist die erforderliche Umgebung startklar und wir können endlich Django installieren!

### Django-Installation <a id="django-installation"></a>

Da du nun dein `virtualenv` gestartet hast, kannst du Django installieren.

Bevor wir damit loslegen, sollten wir jedoch sicherstellen, dass wir die neueste Version von `pip` haben, eine Software, mit Hilfe derer wir Django installieren werden:

{% code title="in der Kommandozeile" %}
```text
(myvenv) ~$ python -m pip install --upgrade pip
```
{% endcode %}

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

{% code title="in der Kommandozeile" %}
```text
(myvenv) ~$ pip install -r requirements.txt
Collecting Django~=2.0.6 (from -r requirements.txt (line 1))
  Downloading Django-2.0.6-py3-none-any.whl (7.1MB)
Installing collected packages: Django
Successfully installed Django-2.0.6
```
{% endcode %}

#### **Installing Django: Windows**

> Wenn du einen Fehler auf einem Windowsrechner bekommst, überprüfe, ob der Pfadname deines Projekts Leerzeichen, Umlaute oder Sonderzeichen enthält \(z.B. `C:\Users\User Name\djangogirls`\). Ist das der Fall, dann verwende bitte einen anderen Ordner ohne Sonderzeichen, Umlaute oder Leerzeichen. \(Vorschlag: `C:\djangogirls`\). Erstelle ein neues virtualenv in einem neuen Verzeichnis, lösche danach das alte und wiederhohle den oben genannten Befehl. \(Das Verzeichnis des virtualenv zu verschieben funktioniert dabei nicht, da virtualenv absolute Pfade verwendet.\)

#### **Installing Django: Windows 8 and Windows 10**

> Es kann sein, dass deine Befehlszeile einfriert, wenn du versuchst Django zu installieren. Sollte das passieren, nutze folgenden Befehl anstelle des oben angegebenen:

> {% code title="in der Kommandozeile" %}
> ```text
> C:\Users\Name\djangogirls> python -m pip install -r requirements.txt
> ```
> {% endcode %}

#### **Installing Django: Linux**

> Falls der pip-Aufruf auf Ubuntu 12.04 zu einer Fehlermeldung führt, rufe `python -m pip install -U --force-reinstall pip` auf, um die Installation von pip im virtualenv zu reparieren.

Das war's! Du bist nun \(endlich\) bereit, deine erste Django-Anwendung zu starten![  
](https://tutorial.djangogirls.org/de/django/)

