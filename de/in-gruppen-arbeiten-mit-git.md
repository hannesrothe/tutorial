# W5 In Gruppen arbeiten mit Git

## Deine Arbeit mit der Gruppe teilen!

Bis jetzt war deine Webseite nur auf deinem Computer verfügbar und du hast alleine für dich gearbeitet. Jetzt wirst du lernen wie du sie teilst und **gemeinsam** mit anderen an deinem Code arbeiten kannst. Dafür verwenden wir einen externen Dienst: [GitHub](https://www.github.com). Github ist ein "Code Hosting"-Dienst. Es gibt noch andere solcher Dienste, aber die meisten Programmierer haben heute ein Konto bei GitHub. Deshalb verwenden wir es auch.

Nach Einrichtung von Git werden zwei Orte für dich wichtig sein. Die Entwicklung und das Testen wirst du auf deinem lokalen Rechner durchführen. Wenn du mit deinen Änderungen zufrieden bist, wirst du eine Kopie deines Programms auf GitHub veröffentlichen.

## Git

_Was ist Git und warum brauchen wir es?_

{% embed url="https://youtu.be/BCQHnlnPusY" %}

> **Hinweis:** Falls du die Installationsschritte bereits durchgeführt hast, kannst du mit dem nächsten Abschnitt fortfahren und anfangen, dein Git-Repository zu erstellen.

### Git installieren <a id="git-installieren"></a>

#### **Installing Git: Windows**

Du kannst Git von [git-scm.com](https://git-scm.com/) herunterladen. Du kannst bei allen Schritten außer zweien "next" klicken: Wähle im Schritt, in dem du einen Editor aussuchen sollst, "Nano"; und bei der Anweisung "Adjusting your PATH environment", wähle die Einstellung "Run Git and associated Unix tools from the Windows command-line" \(die letzte Option\). Die anderen Voreinstellungen sind ok. "Checkout"-Stil "Windows" und "Commit" mit "Unix line endings" \(Zeilenende im Unix-Format\) sind die richtigen Einstellungen.

Nach Abschluss der Installation musst du deine Command-Shell oder Powershell neu starten, damit die Einstellungen aktiv sind.

#### **Installing Git: OS X**

Lade Git von [git-scm.com](https://git-scm.com/) herunter und folge dann den Anweisungen.

> **Hinweis:** Falls du OS X 10.6, 10.7, oder 10.8 verwendest, muss du die Git-Version unter folgendem Link installieren: [Git installer for OS X Snow Leopard](https://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download)

#### **Installing Git: Debian or Ubuntu**

{% code title="in der Kommandozeile" %}
```text
$ sudo apt install git
```
{% endcode %}

#### **Installing Git: Fedora**

{% code title="in der Kommandozeile" %}
```text
$ sudo dnf install git
```
{% endcode %}

#### **Installing Git: openSUSE**

{% code title="in der Kommandozeile" %}
```text
$ sudo zypper install git
```
{% endcode %}

### Unser Git-Repository

Git verwaltet die Veränderungen an einer Sammlung von Dateien in einem sogenannten Repository \(oder kurz "Repo"\). Legen wir eines für unser Projekt an. Öffne deine Konsole und gibt folgende Kommandos im `djangogirls`-Verzeichnis ein:

> **Hinweis:** Überprüfe dein aktuelles Arbeitsverzeichnis mit dem Befehl `pwd` \(OSX/Linux\) oder `cd` \(Windows\) bevor du das Repository initialisierst. Du musst dich im `djangogirls`-Verzeichnis befinden, bevor du fortfährst.

{% code title="in der Kommandozeile \(im Django-Ordner , z.B. djangogirls/\)" %}
```text
$ git init
Initialized empty Git repository in ~/djangogirls/.git/
$ git config --global user.name "Dein Name"
$ git config --global user.email du@example.com
```
{% endcode %}

Die Initialisierung des Git-Repositorys müssen wir für jedes Projekt nur einmal machen \(danach musst Du Benutzernamen und Mail-Adresse nie wieder eingeben\).

Git wird die Änderungen an all den Dateien und Ordnern in diesem Verzeichnis aufzeichnen. Wir wollen aber, dass einige Dateien ignoriert werden. Dazu legen wir eine Datei `.gitignore` im Hauptordner \(`djangogirls`\) des Repos an. Öffne deinen Editor und erstelle eine neue Datei mit dem folgenden Inhalt:

```text
*.pyc
*~
__pycache__
myvenv
db.sqlite3
/static
.DS_Store
```

Speichere die Datei mit dem Namen `.gitignore` im "djangogirls"-Root-Verzeichnis. `.gitignore` definiert, welche Dateien nicht geteilt werden sollen, z.B. weil sie persönliche Informationen enthalten oder sie nicht projektspezifisch sind.

> **Hinweis:** Der Punkt vor dem Dateinamen ist wichtig! Wenn du Schwierigkeiten beim Erstellen hast \(z.B. lassen Macs im Finder keine Dateien mit Punkt am Anfang erzeugen, Punkt-Dateien sind auf Linux und OS X "versteckte Dateien"\), dann verwende die "Speichern unter"-Funktion im Editor, das sollte immer funktionieren. Wichtig ist, dass du den Dateinamen nicht mit `.txt`, `.py` oder einer anderen Dateinamen-Erweiterung ergänzt -- die Datei wird von Git nur erkannt, wenn ihr Name exakt nur `.gitignore` ist.
>
> **Hinweis:** Eine der Dateien, die du in deiner `.gitignore`-Datei defniniert hast, ist `db.sqlite3`. Diese Datei ist deine lokale Datenbank, in welcher alle deine Benutzer und Posts gespeichert werden. Wir werden die gängige Web-Entwicklungs-Praxis befolgen, was heißt, dass wir separate Datenbanken für unsere lokale Test-Website und unsere öffentliche Website auf PythonAnywhere verwenden werden. Die Datenbank für letztere könnte SQLite sein, wie auf deiner Entwicklungsmaschine, aber normalerweise wirst du eine sogenannte MySQL-Datenbank nutzen, welche mit viel mehr Besuchern umgehen kann als SQLite. So oder so, dadurch, dass du deine SQLite-Datenbank für die GitHub-Kopie nicht verwendest, werden alle deine bisherigen Posts der Superuser nur lokal zur Verfügung stehen und du musst in der produktiven Umgebung neue hinzufügen. Betrachte deine lokale Datenbank als tollen Spielplatz, auf welchem du verschiedene Dinge ausprobieren kannst, ohne Angst zu haben, dass du deine wirklichen Post auf deinem Blog löschst.

Es ist hilfreich den Befehl `git status` vor `git add` auszuführen oder immer dann, wenn du dir unsicher bist, was geändert wurde. Das schützt vor manchen Überraschungen, wie z. B. das falsche Hinzufügen oder Übertragen von Dateien. Das `git status`-Kommando gibt Informationen über unbeobachtete/veränderte/hinzugefügte Dateien, den Status der Verzweigung und einiges mehr wieder. Deine Ausgabe sollte dem hier ähneln:

{% code title="in der Kommandozeile \(im Django-Ordner , z.B. djangogirls/\)" %}
```text
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        .gitignore
        blog/
        manage.py
        mysite/
        requirements.txt

nothing added to commit but untracked files present (use "git add" to track)
```
{% endcode %}

Nun speichern wir unsere Änderungen durch folgende Eingabe in der Konsole:

{% code title="in der Kommandozeile \(im Django-Ordner , z.B. djangogirls/\)" %}
```text
$ git add --all .
$ git commit -m "My Django Girls app, first commit"
 [...]
 13 files changed, 200 insertions(+)
 create mode 100644 .gitignore
 [...]
 create mode 100644 mysite/wsgi.py
```
{% endcode %}

### Den Code auf GitHub veröffentlichen

Gehe auf [GitHub.com](https://www.github.com) eröffne ein neues, kostenloses Nutzerkonto. \(Falls Du es bereits während der Workshop-Vorbereitung eingerichtet hast, ist das großartig!\) Stelle sicher, dass Du Dein Passwort nicht vergisst \(füge es zu zu Deinem Passwort-Manager hinzu, falls Du einen solchen verwendest\).

Erstelle dann ein neues Repository und gib ihm den Namen "my-first-blog". Lass das Kontrollkästchen "initialise with a README" deaktiviert und die Einstellung der Option .gitignore leer \(das haben wir schon von Hand gemacht\) und lass die Lizenz auf "None".

![](.gitbook/assets/new_github_repo.png)

> **Achtung:** Der Name `my-first-blog` ist wichtig -- du kannst auch einen anderen wählen, aber er wird im Folgenden noch sehr oft vorkommen und du wirst immer daran denken müssen, ihn in den Anweisungen entsprechend anzupassen. Es ist wahrscheinlich einfacher, bei `my-first-blog` zu bleiben.

In der nächsten Ansicht wirst du die clone-URL deines Repositorys sehen, die du in manchen der folgenden Kommandozeilenbefehlen verwenden wirst:

![](.gitbook/assets/github_get_repo_url_screenshot.png)

Nun müssen wir das Git-Repository auf deinem Computer mit dem auf GitHub verbinden.

Gib das Folgende auf der Kommandozeile ein \(ersetzte `<your-github-username>` mit dem Benutzernamen, den du beim Erstellen deines GitHub-Accounts gewählt hast, aber ohne die spitzen Klammern -- die URL sollte der clone-URL entsprechen, die du vorhin gerade gesehen hast\):

{% code title="in der Kommandozeile \(im Django-Ordner , z.B. djangogirls/\)" %}
```text
$ git remote add origin https://github.com/<your-github-username>/my-first-blog.git
$ git push -u origin master
```
{% endcode %}

Wenn du zu GitHub pushst, wirst du nach deinem Benutzernamen und Passwort gefragt \(entweder direkt im Kommandozeilen-Fenster oder in einem Pop-Up-Fenster\), und nach der Eingabe deiner Zugangsdaten solltest du etwas Ähnliches wie das hier sehen:

```text
Counting objects: 6, done.
Writing objects: 100% (6/6), 200 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/ola/my-first-blog.git

 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```

Hier steht nun ein neuer Begriff: _Branches_. Was sind Branches?

{% embed url="https://www.youtube.com/watch?v=oPpnCh7InLY" %}

Dein Code ist jetzt auf GitHub. Schau gleich mal nach! Dort ist dein Code in guter Gesellschaft - [Django](https://github.com/django/django), das [Django Girls Tutorial](https://github.com/DjangoGirls/tutorial) und viele andere großartige Open Source Software-Projekte haben ihren Code auf GitHub. :\)

### Ein bestehendes Git-Repository lokal nutzen

Um ein Git-Repository zu nutzen, braucht ihr als erstes die URL zum Git-Repository. Dafür ruft ihr es am besten als erstes in Github auf und klickt auf "clone". Daraufhin erhaltet ihr die URL zu eurem Repository. 

![](.gitbook/assets/image%20%282%29.png)

Die URL kopiert ihr und öffnet in der Konsole den Ordner, in dem das Repository lokal liegen soll und klont das Repository.

{% code title="in der Kommandozeile" %}
```text
$ git clone [URL zum Repository]
```
{% endcode %}

Nun liegen alle Dateien lokal im Ordner, in dem ihr den Code ausgeführt habt. Mit folgendem Befehl könnt ihr nun Aktualisierungen immer abfragen:

{% code title="in der Kommandozeile" %}
```text
$ git pull
```
{% endcode %}

### Wie können andere mitarbeiten?

Damit wir gemeinsam an einem Code arbeiten können, sind zwei Begriffe wichtig: _Pull_ und _Fork_. Wir werden insbesondere _Pull_ häufig benötigen.

{% embed url="https://www.youtube.com/watch?v=\_NrSWLQsDL4" %}

Um jedoch Änderungen durchführen zu können und hochzuladen, müssen eure Gruppenmitglieder als Collaborators eingetragen sein:

![](.gitbook/assets/image%20%281%29.png)

Anschließend können sie Änderungen lokal durchführen und hochladen. Mit "git commit" werden Änderungen zum Hochladen eingereiht und kurz kommentiert. Durch "git push" erfolgt das eigentliche Hochladen. Es empfiehlt sich vorher stets noch einmal "git pull" durchzuführen um sicherzugehen, dass lokal auch die neueste Version des Codes funktioniert.

{% code title="in der Kommandozeile \(im Django-Ordner , z.B. djangogirls/\)" %}
```text
$ git commit -m "KOMMENTAR"
 [...]
 13 files changed, 200 insertions(+)
 create mode 100644 .gitignore
 [...]
 create mode 100644 mysite/wsgi.py
$ git push
```
{% endcode %}

