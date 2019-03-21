# W1 Einführung in die Kommandozeile

## Einführung in die Kommandozeile <a id="einf&#xFC;hrung-in-die-kommandozeile"></a>

Für die Leser zu Hause: Dieses Kapitel wird im Video [Your new friend: Command Line](https://www.youtube.com/watch?v=jvZLWhkzX-8) behandelt.

Aufregend, oder?! In ein paar Minuten wirst du deine erste Zeile Code schreiben! :\)

**Erstmal stellen wir dir deine neue Freundin vor: Die Konsole!**

Im Folgenden zeigen wir dir, wie du das schwarze Fenster benutzt, das alle Hackerinnen nutzen. Es sieht vielleicht erstmal etwas unheimlich aus, aber es ist nur ein Programm, das darauf wartet, Anweisungen von dir zu bekommen.

> **Hinweis:** Bitte beachte, dass wir in dem gesamten Buch die Begriffe "Verzeichnis" und "Ordner" abwechselnd gebrauchen, aber sie stehen für ein und dasselbe.

### Was ist die Konsole? <a id="was-ist-die-konsole"></a>

> Das Fenster, welches gewöhnlich die **Kommandokonsole** \(command line\) oder **Kommandozeilen-Interface** \(command-line interface\) genannt wird, ist eine textbasierte Applikation zum Betrachten, Bearbeiten und Manipulieren von Dateien auf deinem Computer. Es ist dem Windows Explorer oder Finder auf dem Mac ähnlich, aber ohne die grafische Benutzeroberfläche. Andere Bezeichnungen dafür sind: _CMD_, _CLI_, _Prompt \(Eingabeaufforderung\)_, _Konsole_ oder _Terminal_.

### Öffnen der Konsole <a id="&#xF6;ffnen-der-konsole"></a>

> Um mit unserem Tutorial zu starten, musst du als Erstes das Kommandozeilenprogramm starten.

#### **Opening: Windows**

> Abhängig von deiner Windows-Version und deiner Tastatur sollte eine der folgenden Methoden ein Kommandozeilen-Fenster öffnen \(du musst vielleicht etwas herumexperimentieren, aber du musst nicht jeden dieser Vorschläge ausprobieren\):
>
> * Gehe zum Start-Menü oder Start-Bildschirm und gib "Eingabeaufforderung" in das Suchfeld ein.
> * Klicke Start-Menü → Windows System → Eingabeaufforderung.
> * Geh ins Start Menü → Alle Programme → Zubehör → Eingabeaufforderung.
> * Gehe zum Startbildschirm, bewege deinen Mauszeiger zur unteren linken Bildschirmecke und klicke auf den nach unten zeigenden Pfeil, der erschienen ist \(auf einem Touch-Screen streichst du mit dem Finger vom unteren Bildschirmrand nach oben\). Die Apps-Seite sollte sich öffnen. Klicke auf Eingabeaufforderung im Abschnitt Windows System.
> * Drücke die Windows-Taste und gleichzeitig "x" auf deiner Tastatur. Wähle "Eingabeaufforderung" aus dem Menü aus.
> * Drücke die Windows-Taste und gleichzeitig "r", um das "Ausführen"-Fenster zu erhalten. Tippe "cmd" in das Feld und klicke OK.
>
> ![Tippe &quot;cmd&quot; in das &quot;Ausf&#xFC;hren&quot;-Fenster](https://tutorial.djangogirls.org/de/python_installation/images/windows-plus-r.png)
>
> Später im Tutorial wirst du zwei offene Kommandozeilen-Fenster gleichzeitig brauchen. Wenn du aber schon ein Kommandozeilen-Fenster offen hast, wirst du bei manchen Windows-Versionen einfach zu diesem geschickt, wenn du mit derselben Methode versuchst, ein zweites Fenster zu öffnen. Probiere das nun aus und achte darauf, was passiert! Wenn du nur ein Kommandozeilen-Fenster bekommst, versuche eine der anderen Methoden aus der Liste oben. Mindestens eine der Methoden sollte dazu führen, dass ein neues \(zweites\) Kommandozeilen-Fenster geöffnet wird.

**Opening: OS X**

> Öffne das Launchpad → Andere → Terminal.

**Opening: Linux**

> Wahrscheinlich ist es unter Programme → Zubehör → Terminal, aber das ist von deinem System abhängig. Wenn es nicht da ist, kannst du versuchen, danach zu googlen. :\)

### Eingabeaufforderung \(Prompt\) <a id="eingabeaufforderung-prompt"></a>

> Du solltest nun ein weißes oder schwarzes Fenster sehen, das auf deine Anweisungen wartet.

**Prompt: OS X and Linux**

> Auf einem Mac- oder Linux-Rechner siehst du wahrscheinlich ein `$`, also so:
>
> command-line
>
> ```text
> $
> ```

**Prompt: Windows**

> Auf einem Windows-Rechner siehst du wahrscheinlich ein `>`, so hier:
>
> command-line
>
> ```text
> >
> ```
>
> Schau 'mal in den Linux-Abschnitt hier obendrüber -- so etwas wirst du wieder im Abschnitt PythonAnywhere später im Tutorial antreffen.
>
> Vor jedem Kommando wird das Zeichen `$` oder `>` und ein Leerzeichen vorangestellt, aber du musst das nicht hinschreiben. Dein Computer macht das für dich. :\)
>
> > Ein kleiner Hinweis: Falls du etwas in der Art wie `C:\Users\ola>` oder `Olas-MacBook-Air:~ ola$`sehen solltest, ist das auch 100%ig korrekt.
>
> Der Teil bis und einschließlich `$` oder `>` heißt _Kommandozeilen-Eingabeaufforderung_ oder kurz _Eingabeaufforderung_. Sie fordert dich auf, hier etwas einzugeben.
>
> Wenn wir im Tutorial wollen, dass du einen Befehl eingibst, schreiben wir `$` oder `>` mit hin, gelegentlich auch noch die anderen Angaben links davon. Ignoriere den linken Teil und gib nur das Kommando ein, welches rechts der Eingabeaufforderung steht.

### Dein erstes Kommando \(YAY!\) <a id="dein-erstes-kommando-yay"></a>

> Lass uns mit diesem Kommando beginnen:

**Your first command: OS X and Linux**

> command-line
>
> ```text
> $ whoami
> ```

**Your first command: Windows**

> command-line
>
> ```text
> > whoami
> ```
>
> Und dann bestätige mit `Enter`. Das ist unser Ergebnis:
>
> command-line
>
> ```text
> $ whoami
> olasitarska
> ```
>
> Wie du sehen kannst, hat der Computer gerade deinen Benutzernamen ausgegeben. Toll, was? :\)
>
> > Versuch, jeden Befehl abzuschreiben und nicht zu kopieren und einzufügen. Auf diese Weise wirst du dir mehr merken!

### Grundlagen <a id="grundlagen"></a>

> Jedes Betriebssystem hat einen geringfügig anderen Bestand an Befehlen für die Kommandozeile, beachte daher die Anweisungen für dein Betriebssystem. Lass uns das ausprobieren.

#### Aktuelles Verzeichnis <a id="aktuelles-verzeichnis"></a>

> Es wäre schön zu sehen, wo wir uns befinden, oder? Lass uns nachsehen. Gib diesen Befehl in die Konsole ein und bestätige ihn mit `Enter`:

**Current directory: OS X and Linux**

> command-line
>
> ```text
> $ pwd
> /Users/olasitarska
> ```
>
> > Hinweis: 'pwd' steht für 'print working directory' \(zeige derzeitiges Arbeitsverzeichnis\).

**Current directory: Windows**

> command-line
>
> ```text
> > cd
> C:\Users\olasitarska
> ```
>
> > Hinweis: "cd" steht für "change directory". Mit Powershell kannst du auch 'pwd' verwenden, wie auf Linux oder Mac OS X.
>
> Du wirst wahrscheinlich etwas Ähnliches auf deinem Gerät sehen. Wenn du die Konsole öffnest, befindest du dich normalerweise im Heimverzeichnis deines Benutzers.

#### Mehr über ein Kommando lernen <a id="mehr-&#xFC;ber-ein-kommando-lernen"></a>

> Viele Befehle, die du in der Kommandozeile nutzen kannst, haben eine eingebaute Hilfe, die du anzeigen und lesen kannst! Zum Beispiel kannst du etwas über den eben verwendeten Befehl lernen:**Command help: OS X and Linux**
>
> OS X und Linux haben einen `man`-Befehl, mit dem du die Hilfe über die Kommandos aufrufen kannst. Gib `man pwd` ein und schau, was angezeigt wird oder setzte `man` vor andere Kommandos und sieh dir deren Hilfe an. Das Ergebnis von `man` wird in der Regel seitenweise ausgegeben. Du kannst die Leertaste benutzen, um auf die nächste Seite zu gelangen und `q` \(für engl. "quit", was "verlassen"/"rausgehen" heisst\), um die Hilfeseiten zu schließen.**Current directory: Windows**
>
> Wenn du Windows benutzt, dann wird dir der Suffix `/?` für die meisten Kommandos die Hilfeseite ausgeben. Gegebenenfalls musst du nach oben scrollen, um alles zu sehen. Versuch es mal mit `cd /?`.

#### Anzeigen von Dateien und Unterordnern <a id="anzeigen-von-dateien-und-unterordnern"></a>

> Nun, was befindet sich in deinem Verzeichnis? Es wäre toll, das herauszufinden. Lass uns mal schauen:**List files and directories: OS X and Linux**
>
> command-line
>
> ```text
> $ ls
> Anwendungen
> Desktop
> Downloads
> Musik
> ...
> ```

**List files and directories: Windows**

> command-line
>
> ```text
> > dir
>  Directory of C:\Users\olasitarska
>  05/08/2014 07:28 PM <DIR> Applications 
>  05/08/2014 07:28 PM <DIR> Desktop
>  05/08/2014 07:28 PM <DIR> Downloads
>  05/08/2014 07:28 PM <DIR> Music ...
> ```
>
> > Hinweis: Mit Powershell kannst du auch 'ls' verwenden, wie auf Linux oder Mac OS X.

#### Wechseln des Verzeichnisses <a id="wechseln-des-verzeichnisses"></a>

> Lass uns jetzt zu unserem Desktop-Verzeichnis wechseln:
>
> **Change current directory: OS X**
>
> command-line
>
> ```text
> $ cd Desktop
> ```
>
> **Change current directory: Linux**
>
> command-line
>
> ```text
> $ cd Desktop
> ```
>
> Wenn dein Linux-Benutzerkonto auf Deutsch eingestellt ist, kann es sein, dass auch der Name des Desktop-Verzeichnisses übersetzt ist. Wenn dem so ist, musst du im obigen Befehl `Desktop` durch den übersetzten Verzeichnisnamen `Schreibtisch` ersetzen.
>
> **Change current directory: Windows**
>
> command-line
>
> ```text
> > cd Desktop
> ```
>
> Schau, ob das Wechseln des Verzeichnisses funktioniert hat:

> **Check if changed: OS X and Linux**
>
> command-line
>
> ```text
> $ pwd
> /Users/olasitarska/Desktop
> ```
>
> **Check if changed: Windows**
>
> command-line
>
> ```text
> > cd
> C:\Users\olasitarska\Desktop
> ```
>
> Passt!
>
> > Profi-Tipp: Wenn du `cd D` tippst und dann `tab` auf deiner Tastatur drückst, wird die Kommandozeile automatisch den Rest des Namens vervollständigen, wodurch du schneller navigieren kannst. Wenn es mehr als einen Ordner gibt, dessen Name mit "D" beginnt, drücke die `tab`-Taste zweimal, um eine Liste der Möglichkeiten anzuzeigen.

#### Erstellen eines Verzeichnisses <a id="erstellen-eines-verzeichnisses"></a>

> Wie wär's damit, ein Übungsverzeichnis auf deinem Desktop zu erstellen? So kannst du das tun:
>
> **Create directory: OS X and Linux**
>
> command-line
>
> ```text
> $ mkdir practice
> ```
>
> **Create directory: Windows**
>
> command-line
>
> ```text
> > mkdir practice
> ```
>
> Dieser kleine Befehl erstellt einen Ordner mit dem Namen `practice` auf deinem Desktop. Du kannst nun überprüfen, ob er wirklich dort ist, indem du auf deinem Desktop nachschaust oder indem du den Befehl `ls` oder `dir` ausführst! Versuch es. :\)
>
> > Profi-Tipp: Wenn du die selben Befehle nicht immer wieder und wieder schreiben willst, verwende die `Pfeil aufwärts`- und `Pfeil abwärts`-Tasten deiner Tastatur, um durch die zuletzt verwendeten Befehle zu blättern.

#### Übung! <a id="&#xFC;bung"></a>

> Eine kleine Herausforderung für dich: Erstelle in deinem neu erstellten `practice`-Ordner ein Verzeichnis namens `test`. \(Verwende dazu die Kommandos `cd` und `mkdir`.\)
>
> **Lösung:**
>
> **Exercise solution: OS X and Linux**
>
> command-line
>
> ```text
> $ cd practice
> $ mkdir test
> $ ls
> test
> ```
>
> **Exercise solution: Windows**
>
> command-line
>
> ```text
> > cd practice
> > mkdir test
> > dir
> 05/08/2014 07:28 PM <DIR>      test
> ```
>
> Glückwunsch! :\)

#### Aufräumen <a id="aufr&#xE4;umen"></a>

> Wir wollen kein Chaos hinterlassen, also lass uns das bislang Geschaffene wieder löschen.
>
> Zuerst müssen wir zurück zum Desktop wechseln:
>
> **Clean up: OS X and Linux**
>
> command-line
>
> ```text
> $ cd ..
> ```
>
> **Clean up: Windows**
>
> command-line
>
> ```text
> > cd ..
> ```
>
> Durch Verwendung von `..` mit dem `cd`-Kommando wechselst du von deinem aktuellen Verzeichnis zum übergeordneten Verzeichnis \(dies ist das Verzeichnis, das das aktuelle Verzeichnis enthält\).
>
> Schau nach, wo du gerade bist:
>
> **Check location: OS X and Linux**
>
> command-line
>
> ```text
> $ pwd
> /Users/olasitarska/Desktop
> ```
>
> **Check location: Windows**
>
> command-line
>
> ```text
> > cd
> C:\Users\olasitarska\Desktop
> ```
>
> Jetzt ist es an der Zeit, dein `practice`-Verzeichnis zu löschen:
>
> > **Achtung**: Wenn du Daten mit `del`, `rmdir` oder `rm` löschst, kannst du das nicht mehr rückgängig machen, das bedeutet, _die gelöschten Dateien sind für immer weg_! Sei also sehr vorsichtig mit diesem Befehl.
>
> **Delete directory: Windows Powershell, OS X and Linux**
>
> command-line
>
> ```text
> $ rm -r practice
> ```
>
> **Delete directory: Windows Command Prompt**
>
> command-line
>
> ```text
> > rmdir /S practice
> practice, Are you sure <Y/N>? Y
> ```

Geschafft! Lass uns schauen, ob es wirklich gelöscht ist:

> **Check deletion: OS X and Linux**
>
> command-line
>
> ```text
> $ ls
> ```
>
> **Check deletion: Windows**
>
> command-line
>
> ```text
> > dir
> ```

#### Beenden <a id="beenden"></a>

> Das wärs fürs Erste. Du kannst nun beruhigt deine Konsole schließen. Lass es uns wie die Hacker machen, okay? :\)**Exit: OS X and Linux**
>
> command-line
>
> ```text
> $ exit
> ```
>
> **Exit: Windows**
>
> command-line
>
> ```text
> > exit
> ```
>
> Cool, was? :\)

### Zusammenfassung <a id="zusammenfassung"></a>

> Hier ist eine Zusammenfassung einiger nützlicher Kommandos:
>
> | Befehl \(Windows\) | Befehl \(Mac OS / Linux\) | Beschreibung | Beispiel |
> | :--- | :--- | :--- | :--- |
> | exit | exit | Fenster schließen | **exit** |
> | cd | cd | Verzeichnis wechseln | **cd test** |
> | cd | pwd | aktuelles Verzeichnis anzeigen | **cd** \(Windows\) oder **pwd** \(Mac OS / Linux\) |
> | dir | ls | Unterordner/Dateien zeigen | **dir** |
> | copy | cp | Datei kopieren | **copy c:\test\test.txt c:\windows\test.txt** |
> | move | mv | Datei verschieben | **move c:\test\test.txt c:\windows\test.txt** |
> | mkdir | mkdir | neues Verzeichnis erstellen | **mkdir testdirectory** |
> | rmdir \(oder del\) | rm | Datei löschen | **del c:\test\test.txt** |
> | rmdir /S | rm -r | Verzeichnis löschen | **rm -r testdirectory** |
> | \[CMD\] /? | man \[CMD\] | Hilfe für ein Kommando aufrufen | **cd /?** \(Windows\) oder **man cd**\(Mac OS / Linux\) |
>
> Das sind nur sehr wenige der Befehle, welche du in deiner Konsole verwenden kannst, aber du wirst heute nicht mehr brauchen.
>
> Falls du neugierig bist, findest du auf [ss64.com](http://ss64.com/) eine vollständige Übersicht über alle Kommandozeilen-Befehle für alle Betriebssysteme.

### Fertig? <a id="fertig"></a>

> Lass uns mit Python anfangen!

