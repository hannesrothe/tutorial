# W9 Erweiterung der Templates

Eine weitere praktische Sache von Django ist das **template extending**, Erweiterungen des Templates. Was bedeutet das? Damit kannst du Teile deines HTML-Codes für andere Seiten deiner Website nutzen.

Templates helfen, wenn du die selben Informationen oder das selbe Layout an mehreren Stellen verwenden willst. Du musst dich so nicht in jeder Datei wiederholen. Und wenn du etwas ändern willst, dann musst du es nicht in jedem einzelnen Template tun, sondern nur in einem!

## Ein Basis-Template erstellen

Ein Basis-Template ist das grundlegende Template, welches dann auf jeder einzelnen Seite deiner Website erweitert wird.

Wir erstellen jetzt eine `base.html`-Datei in `blog/templates/blog/`:

```text
blog
└───templates
    └───blog
            base.html
            post_list.html
```

Öffne sie im Code-Editor, kopiere alles von `post_list.html` und füge es wie folgt in die `base.html`-Datei ein:

{% code title="blog/templates/blog/base.html" %}
```markup
{% load static %}
<html>
    <head>
        <title>Django Girls blog</title>
        <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
        <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap-theme.min.css">
        <link href='//fonts.googleapis.com/css?family=Lobster&subset=latin,latin-ext' rel='stylesheet' type='text/css'>
        <link rel="stylesheet" href="{% static 'css/blog.css' %}">
    </head>
    <body>
        <div class="page-header">
            <h1><a href="/">Django Girls Blog</a></h1>
        </div>

        <div class="content container">
            <div class="row">
                <div class="col-md-8">
                {% for post in posts %}
                    <div class="post">
                        <div class="date">
                            {{ post.published_date }}
                        </div>
                        <h2><a href="">{{ post.title }}</a></h2>
                        <p>{{ post.text|linebreaksbr }}</p>
                    </div>
                {% endfor %}
                </div>
            </div>
        </div>
    </body>
</html>
```
{% endcode %}

Dann ersetze in `base.html` den gesamten `<body>` \(alles zwischen `<body>` und `</body>`\) hiermit:

{% code title="blog/templates/blog/base.html" %}
```markup
<body>
    <div class="page-header">
        <h1><a href="/">Django Girls Blog</a></h1>
    </div>
    <div class="content container">
        <div class="row">
            <div class="col-md-8">
            {% block content %}
            {% endblock %}
            </div>
        </div>
    </div>
</body>
```
{% endcode %}

{% code title="blog/templates/blog/base.html" %}
```markup
{% block content %}
{% endblock %}
```
{% endcode %}

Aber warum? Du hast gerade einen `block` erstellt! Du hast den Template-Tag benutzt, um einen Bereich zu schaffen, der HTML aufnehmen kann. Dieses HTML kommt aus einem anderen Template, welches das Template hier \(`base.html`\) erweitert. Wir zeigen dir gleich, wie das geht.

Speichere nun die Datei `base.html` und öffne wieder `blog/templates/blog/post_list.html` im Code-Editor.

{% code title="blog/templates/blog/post\_list.html" %}
```markup
{% for post in posts %}
    <div class="post">
        <div class="date">
            {{ post.published_date }}
        </div>
        <h2><a href="">{{ post.title }}</a></h2>
        <p>{{ post.text|linebreaksbr }}</p>
    </div>
{% endfor %}
```
{% endcode %}

Dieser Teil unseres Templates soll nun das Basis-Template erweitern. Wir müssen daher Block-Tags ergänzen!

{% code title="blog/templates/blog/post\_list.html" %}
```markup
{% block content %}
    {% for post in posts %}
        <div class="post">
            <div class="date">
                {{ post.published_date }}
            </div>
            <h2><a href="">{{ post.title }}</a></h2>
            <p>{{ post.text|linebreaksbr }}</p>
        </div>
    {% endfor %}
{% endblock %}
```
{% endcode %}

Nur eine Sache noch. Wir müssen die beiden Templates miteinander verknüpfen. Darum geht es ja bei der Template-Erweiterung! Dafür ergänzen wir einen Tag für Erweiterung \(extends tag\) ganz oben in der Datei. Und zwar so:

{% code title="blog/templates/blog/post\_list.html" %}
```markup
{% extends 'blog/base.html' %}

{% block content %}
    {% for post in posts %}
        <div class="post">
            <div class="date">
                {{ post.published_date }}
            </div>
            <h2><a href="">{{ post.title }}</a></h2>
            <p>{{ post.text|linebreaksbr }}</p>
        </div>
    {% endfor %}
{% endblock %}
```
{% endcode %}

Das war's! Speichere die Datei und probier aus, ob deine Website noch richtig funktioniert. :\)

> Wenn du den Fehler `TemplateDoesNotExist` erhältst, dann heißt das, dass es die Datei `blog/base.html` nicht gibt und dass `runserver` in der Konsole läuft. Halte ihn an \(durch Drücken von Ctrl+C bzw. Strg+C – Control- und die C-Taste gleichzeitig\) und starte ihn neu, indem du den Befehl `python manage.py runserver` ausführst.

