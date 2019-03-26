# W6 Einführung in HTML

Vielleicht fragst du dich, was ein Template \(Vorlage\) ist?

Ein Template \(zu deutsch "Vorlage"\) ist eine Textdatei und ermöglicht es uns, verschiedene Inhalte in einer einheitlichen Darstellung zu erzeugen. Eine Vorlage für z.B. einen Brief hilft uns, immer gleich aussehende Nachrichten zu versenden, in denen sich Empfänger, Betreff und Text jeweils ändern, das äußere Format jedoch bestehen bleibt.

Ein Django-Template wird mit einer Sprache namens HTML beschrieben. \(Genau das HTML aus dem ersten Kapitel: **Wie das Internet funktioniert**\).

## Was ist HTML?

HTML ist recht einfacher Code, der von deinem Browser – z.B. Chrome, Firefox oder Safari – interpretiert wird, um dem Benutzer eine Website darzustellen.

HTML steht für "HyperText Markup Language". Als **HyperText** wird Text bezeichnet, der über markierte Textstellen, den "Hyperlinks" \(die umgangssprachlichen "Links"\), auf andere \(meist ebenfalls in HTML geschriebene\) Seiten verweist. **Markup** bedeutet, dass wir ein Dokument nehmen und mit Code versehen, um einem Empfänger mitzuteilen \(in diesem Fall dem Browser\), wie diese Seite interpretiert werden muss. HTML-Code besteht aus **Tags**, wovon jeder mit `<` beginnt und mit `>` endet. Diese Tags stellen die Markup-**Elemente** dar.

## Dein erstes Template!

Ein Template zu erstellen, heißt, eine entsprechende Datei dafür zu erstellen. Alles ist eine Datei, wie du vielleicht schon bemerkt hast.

Templates werden im Verzeichnis `blog/templates/blog` gespeichert. Als Erstes erzeugen wir das Verzeichnis `templates` in deinem Blog-Verzeichnis. Im Template-Verzeichnis selbst erstellen wir ein weiteres Verzeichnis `blog`:

```text
blog
└───templates
    └───blog
```

\(Falls du dich wunderst, warum wir zwei `blog`-Verzeichnisse brauchen – das hängt mit den nützlichen Namenskonventionen von Django zusammen, die das Leben einfacher machen, wenn deine Projekte immer komplizierter und komplexer werden.\)

Als nächstes erstellen wir eine Datei `post_list.html` \(erst mal ohne Inhalt\) innerhalb des Verzeichnisses `blog/templates/blog`.

Kontrolliere deine überarbeitete Webseite unter: [http://127.0.0.1:8000](http://127.0.0.1:8000)

> Falls du die Fehlermeldung `TemplateDoesNotExist` angezeigt bekommst, versuche den Server neu zu starten. Auf der Kommandozeile drückst du dafür Strg+C bzw. Ctrl+C \(Strg-/Ctrl- und die C-Taste C zusammen\) und startest danach den Server erneut mit dem Kommando `python manage.py runserver`.

![Abbildung 11.1](.gitbook/assets/step1%20%281%29.png)

Der Fehler sollte weg sein! Toll :\) Deine Webseite ist allerdings noch leer, weil dein Template leer ist. Das müssen wir ändern.

Öffne die neue Datei im Code-Editor, und füge Folgendes hinzu:

{% code-tabs %}
{% code-tabs-item title="blog/templates/blog/post\_list.html" %}
```markup
<html>
<body>
    <p>Halli-Hallo!</p>
    <p>Es funktioniert!</p>
</body>
</html>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Hat sich die Seite geändert? Besuche [http://127.0.0.1:8000/](http://127.0.0.1:8000/), um nachzusehen.

![Abbildung 11.2](.gitbook/assets/step3%20%281%29.png)

Es funktioniert! Gute Arbeit! :\)

* Jede Webseite sollte mit dem Tag `<html>` beginnen. Und `</html>` steht immer am Ende. Zwischen den beiden Tags `<html>` und `</html>` steht der gesamte Inhalt der Webseite
* `<p>` ist der Tag für ein Absatz-Element \(paragraph\), `</p>` beendet einen Absatz

## "Head" und "body"

Jede HTML-Seite gliedert sich in zwei Teile: **head** und **body**.

* Das Element **head** speichert im "Kopf" der Seite Informationen über die Seite, die dir nicht angezeigt werden.
* Das Element **body** enthält den "Körper" - also den dargestellten Inhalt der Seite.

Im `<head>` informieren wir den Browser über Einstellungen und Konfigurationen der Webseite, z.B. wie sie dargestellt werden soll, und im `<body>` darüber, was tatsächlich dargestellt werden soll.

In den `<head>` können wir z.B. noch den Titel \(title\) der Seite mit aufnehmen:

{% code-tabs %}
{% code-tabs-item title="blog/templates/blog/post\_list.html" %}
```markup
<html>
    <head>
        <title>Olas Blog</title>
    </head>
    <body>
        <p>Halli-Hallo!</p>
        <p>Es funktioniert!</p>
    </body>
</html>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Speichere die Datei und aktualisiere die Seite im Browser.

![Abbildung 11.3](.gitbook/assets/step4.png)

Der Titel "Olas Blog" wird nun im Browser angezeigt. Hast du es bemerkt? Der Browser hat `<title>Olas Blog</title>` interpretiert und in die Titelleiste übernommen \(dieser Titel wird auch in den Lesezeichen usw. verwendet\).

Wie du vielleicht bemerkt hast, hat jedes Element zu Beginn einen öffnenden Tag und einen zugehörigen _schließenden Tag_ mit `/` und innerhalb davon sind Elemente _eingebettet_. Ein innerer Tag kann nicht außerhalb des umschließenden Tags geschlossen werden, die Reihenfolge muss immer stimmen.

Es ist, wie wenn man Sachen in Kisten steckt. Du hast eine große Kiste, `<html></html>`. In der ist als weitere, etwas kleinere Kiste `<body></body>` drin, und in der wiederum weitere kleine Kistchen: `<p></p>`.

Die Regeln und Reihenfolgen von _schließenden_ Tags und _Verschachtelung_ der Elemente musst du immer einhalten. Anderenfalls können Browser die Seite nicht richtig interpretieren und darstellen.

## Dein Template anpassen

Jetzt kannst du ein bisschen rumprobieren und dein Template umgestalten! Hier sind ein paar nützliche Tags dafür:

* `<h1>Überschrift</h1>` \(headline\) für wichtigste Überschriften
* `<h2>Unter-Überschrift</h2>` die nächst tiefere Überschiftenebene
* `<h3>Unter-Unter-Überschrift</h3>` ... und so weiter bis `<h6>`
* `<p>Ein Fliesstext-Absatz</p>`
* `<em>Text</em>` hebt deinen Text hervor
* `<strong>Text</strong>` hebt deinen Text stark hervor
* `<br>` fängt eine neue Zeile an \(du kannst nichts in das br schreiben und es gibt keinen schließenden Tag\)
* `<a href="https://djangogirls.org">link</a>` erstellt einen Link
* `<ul><li>Erster Punkt</li><li>second item</li></ul>` generiert eine Liste so wie diese hier!
* `<div></div>` definiert einen Abschnitt auf einer Seite

Hier ist ein vollständiges Beispiel eines Templates. Kopiere es und füge es in `blog/templates/blog/post_list.html` ein:

{% code-tabs %}
{% code-tabs-item title="blog/templates/blog/post\_list.html" %}
```markup
<html>
    <head>
        <title>Django Girls blog</title>
    </head>
    <body>
        <div>
            <h1><a href="/">Django Girls Blog</a></h1>
        </div>

        <div>
            <p>published: 14.06.2014, 12:14</p>
            <h2><a href="">My first post</a></h2>
            <p>Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum. Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
        </div>

        <div>
            <p>published: 14.06.2014, 12:14</p>
            <h2><a href="">My second post</a></h2>
            <p>Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum. Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut f.</p>
        </div>
    </body>
</html>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Wir haben hier drei verschiedene `div` Abschnitte erstellt.

* Das erste `div` Element enthält den Titel unseres Blogs – eine Überschrift und einen Link
* Zwei weitere `div` Elemente beinhalten unsere Blogposts und ein Publikationsdatum, `h2` mit dem Titel des Posts und zwei `p` \(paragraph\) Tags mit Text, eines für das Datum und eines für den Blogpost.

Wir bekommen das Folgende:

![Abbildung 11.4](.gitbook/assets/step6.png)

Yaaay! Bis jetzt zeigt unser Template aber immer genau die **gleichen Inhalte** – obwohl wir aber vorhin davon gesprochen haben, dass Templates uns erlauben, **verschiedene** Informationen im **gleichen Format** darzustellen.

Eigentlich wollen wir richtige Posts anzeigen, die in unserer Django-Admin-Oberfläche hinzugefügt wurden – und das wollen wir als Nächstes tun.

