---
title: 'Artisan Console'
taxonomy:
    category:
        - docs
aura:
    pagetype: website
metadata:
    'og:url': 'https://laravel-docs.aldrahastur.io/8.x/tiefer-graben/artisan-console'
    'og:type': website
    'og:title': 'Artisan Console | Laravel Docs in Deutsch'
    'og:author': aldrahastur
    'twitter:card': summary_large_image
    'twitter:title': 'Artisan Console | Laravel Docs in Deutsch'
    'twitter:site': '@aldrahastur'
    'twitter:creator': '@aldrahastur'
    'article:published_time': '2021-03-13T17:45:08+01:00'
    'article:modified_time': '2021-03-13T17:45:08+01:00'
    'article:author': aldrahastur
---

# Einführung.
Artisan ist die in Laravel enthaltene Befehlszeilenschnittstelle. Artisan ist im Stammverzeichnis Ihrer Anwendung als artisan-Skript vorhanden und bietet eine Reihe hilfreicher Befehle, die Sie bei der Erstellung Ihrer Anwendung unterstützen können. Um eine Liste aller verfügbaren Artisan-Befehle anzuzeigen, können Sie den Befehl list verwenden:
> php artisan list

Jeder Befehl enthält auch einen "Hilfe"-Bildschirm, der die verfügbaren Argumente und Optionen des Befehls anzeigt und beschreibt. Um einen Hilfebildschirm anzuzeigen, stellen Sie dem Namen des Befehls "help" voran:
> php artisan help migrate

### Laravel Sail
Wenn Sie Laravel Sail als lokale Entwicklungsumgebung verwenden, denken Sie daran, die sail-Befehlszeile zu verwenden, um Artisan-Befehle aufzurufen. Sail wird Ihre Artisan-Befehle innerhalb der Docker-Container Ihrer Anwendung ausführen:
> ./sail artisan list

## Tinker (REPL)
Laravel Tinker ist eine leistungsstarke REPL für das Laravel-Framework, die auf dem PsySH-Paket basiert.

### Installation
Alle Laravel-Anwendungen enthalten standardmäßig Tinker. Sie können Tinker jedoch mit Composer installieren, wenn Sie es zuvor aus Ihrer Anwendung entfernt haben:
> composer require laravel/tinker

### Nutzung
Mit Tinker können Sie über die Kommandozeile mit Ihrer gesamten Laravel-Anwendung interagieren, einschließlich Ihrer Eloquent-Modelle, Jobs, Ereignisse und mehr. Um die Tinker-Umgebung zu betreten, führen Sie den Befehl tinker Artisan aus:
> php artisan tinker

Sie können die Konfigurationsdatei von Tinker mit dem Befehl vendor:publish veröffentlichen:
> php artisan vendor:publish --provider="Laravel\Tinker\TinkerServiceProvider"

### 

# Commands schreiben

