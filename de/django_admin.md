# W4 Django-Administration

Wir benutzen den Django-Admin, um die soeben modellierten Posts hinzuzufügen, zu ändern oder zu löschen.

Öffne die Datei `blog/admin.py` im Code-Editor und ersetze den Inhalt wie folgt:

{% code title="blog/admin.py" %}
```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```
{% endcode %}

Wie du siehst, importieren wir hier das Model "Post", das wir im vorherigen Kapitel erstellt haben. Damit unser Model auf der Admin-Seite sichtbar wird, müssen wir es mit `admin.site.register(Post)` registrieren.

Okay, wir sehen uns nun unser Post-Model an. Denk daran, `python manage.py runserver` in die Konsole einzugeben, um den Webserver zu starten. Öffne deinen Browser und gib die Adresse [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/) ein. Du siehst eine Anmeldeseite:

![Login Seite](.gitbook/assets/login_page2.png)

Um dich einloggen zu können, musst du zunächst einen _superuser_ erstellen - einen User, der alles auf der Website steuern darf. Geh zurück zur Kommandozeile, tippe `python manage.py createsuperuser` und drücke Enter.

> Denke daran, damit du neue Kommandos eingeben kannst während der Webserver läuft, musst du ein neues Terminal öffnen und deine virtualenv aktivieren. Wie man neue Kommandos eingeben kann, haben wir im Kapitel **Dein erstes Django-Projekt!** unter **Den Webserver starten** behandelt.

{% code title="in der Kommandozeile" %}
```text
(myvenv) ~/djangogirls$ python manage.py createsuperuser
```
{% endcode %}

{% code title="in der Kommandozeile" %}
```text
(myvenv) C:\Users\Name\djangogirls> python manage.py createsuperuser
```
{% endcode %}

Wenn du dazu aufgefordert wirst, gib einen Benutzernamen \(Kleinbuchstaben, keine Leerzeichen\), eine Mailadresse und ein Passwort ein. **Mach dir keine Gedanken, wenn du das Passwort bei der Eingabe nicht sehen kannst - so soll es sein.** Tippe weiter und drücke `Enter`, um weiterzumachen. Du solltest nun Folgendes sehen \(wobei Benutzername und Email deine eigenen sein sollten\):

{% code title="in der Kommandozeile" %}
```text
Username: hannes
Email address: hannes@example.com
Password:
Password (again):
Superuser created successfully.
```
{% endcode %}

Geh nochmal in deinen Browser und log dich mit den Daten des Superusers ein, den du gerade erstellt hast. Du solltest nun das Django-Admin-Dashboard sehen.

![&quot;Django Admin&quot;-Weboberfl&#xE4;che](.gitbook/assets/django_admin3.png)

Gehe auf Posts und experimentiere ein bisschen damit. Füge fünf oder sechs Blogeinträge hinzu. Mach dir keine Sorgen wegen des Inhalts -- der ist nur auf deinem lokalen Computer sichtbar. Um Zeit zu sparen kannst du etwas Text aus diesem Tutorial kopieren und einfügen. :-\)

Achte darauf, dass bei wenigstens zwei oder drei Posts \(aber nicht bei allen\) das Veröffentlichungsdatum \(publish date\) eingetragen ist. Das werden wir später noch brauchen.

![&quot;Django Admin&quot;-Weboberfl&#xE4;che](.gitbook/assets/edit_post3.png)

Mehr zum Django-Admin-Dashboard kannst du in der Django-Dokumentation erfahren: [https://docs.djangoproject.com/en/2.0/ref/contrib/admin/](https://docs.djangoproject.com/en/2.0/ref/contrib/admin/).

Jetzt ist wahrscheinlich ein guter Moment, um dir einen Kaffee \(oder Tee\) zu gönnen und neue Kraft zu tanken. Du hast dein erstes Django-Model erstellt - du hast dir eine kleine Pause verdient!

