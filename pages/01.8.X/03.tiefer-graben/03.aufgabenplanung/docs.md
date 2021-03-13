---
title: Aufgabenplanung
taxonomy:
    category:
        - docs
aura:
    pagetype: website
metadata:
    'og:url': 'https://laravel-docs.aldrahastur.io/8.x/tiefer-graben/aufgabenplanung'
    'og:type': website
    'og:title': 'Aufgabenplanung | Laravel Docs in Deutsch'
    'og:author': aldrahastur
    'twitter:card': summary_large_image
    'twitter:title': 'Aufgabenplanung | Laravel Docs in Deutsch'
    'twitter:site': '@aldrahastur'
    'twitter:creator': '@aldrahastur'
    'article:published_time': '2021-03-13T21:54:14+01:00'
    'article:modified_time': '2021-03-13T21:54:14+01:00'
    'article:author': aldrahastur
---

# Einführung
In der Vergangenheit haben Sie vielleicht einen Cron-Konfigurationseintrag für jede Aufgabe geschrieben, die Sie auf Ihrem Server planen mussten. Dies kann jedoch schnell lästig werden, da Ihr Aufgabenplan nicht mehr in der Quellcodekontrolle ist und Sie sich per SSH in Ihren Server einwählen müssen, um Ihre vorhandenen Cron-Einträge anzuzeigen oder zusätzliche Einträge hinzuzufügen.

Der Befehls-Scheduler von Laravel bietet einen neuen Ansatz für die Verwaltung von geplanten Aufgaben auf Ihrem Server. Der Scheduler ermöglicht es Ihnen, Ihren Befehlszeitplan fließend und ausdrucksstark innerhalb Ihrer Laravel-Anwendung selbst zu definieren. Wenn Sie den Scheduler verwenden, ist nur ein einziger Cron-Eintrag auf Ihrem Server erforderlich. Ihr Aufgabenplan wird in der Schedule-Methode der Datei app/Console/Kernel.php definiert. Um Ihnen den Einstieg zu erleichtern, ist ein einfaches Beispiel innerhalb der Methode defini

# Definieren von Zeitplänen
Sie können alle Ihre geplanten Aufgaben in der Schedule-Methode der App\Console\Kernel-Klasse Ihrer Anwendung definieren. Schauen wir uns für den Anfang ein Beispiel an. In diesem Beispiel werden wir eine Closure planen, die jeden Tag um Mitternacht aufgerufen wird. Innerhalb der Closure werden wir eine Datenbankabfrage ausführen, um eine Tabelle zu löschen:

