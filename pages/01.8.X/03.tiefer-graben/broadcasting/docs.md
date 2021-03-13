---
title: Broadcasting
taxonomy:
    category:
        - docs
aura:
    pagetype: website
metadata:
    'og:url': 'https://laravel-docs.aldrahastur.io/8.x/tiefer-graben/broadcasting'
    'og:type': website
    'og:title': 'Broadcasting | Laravel Docs in Deutsch'
    'og:author': aldrahastur
    'twitter:card': summary_large_image
    'twitter:title': 'Broadcasting | Laravel Docs in Deutsch'
    'twitter:site': '@aldrahastur'
    'twitter:creator': '@aldrahastur'
    'article:published_time': '2021-03-13T17:24:39+01:00'
    'article:modified_time': '2021-03-13T17:24:39+01:00'
    'article:author': aldrahastur
---

# Einführung

In vielen modernen Webanwendungen werden WebSockets verwendet, um Echtzeit-Benutzeroberflächen mit Live-Aktualisierung zu implementieren. Wenn einige Daten auf dem Server aktualisiert werden, wird typischerweise eine Nachricht über eine WebSocket-Verbindung gesendet, um vom Client verarbeitet zu werden. WebSockets bieten eine effizientere Alternative zum ständigen Abfragen des Servers Ihrer Anwendung nach Datenänderungen, die in Ihrer Benutzeroberfläche widergespiegelt werden sollen.

Stellen Sie sich zum Beispiel vor, dass Ihre Anwendung in der Lage ist, die Daten eines Benutzers in eine CSV-Datei zu exportieren und diese per E-Mail zu versenden. Das Erstellen dieser CSV-Datei dauert jedoch mehrere Minuten, sodass Sie sich dafür entscheiden, die CSV-Datei innerhalb eines Warteschlangen-Jobs zu erstellen und zu versenden. Wenn die CSV-Datei erstellt und an den Benutzer gesendet wurde, können wir mithilfe von Event-Broadcasting ein Ereignis App\Events\UserDataExported versenden, das vom JavaScript unserer Anwendung empfangen wird. Sobald das Ereignis empfangen wird, können wir dem Benutzer eine Nachricht anzeigen, dass seine CSV-Datei per E-Mail an ihn gesendet wurde, ohne dass er die Seite aktualisieren muss.

Um Sie bei der Erstellung dieser Art von Funktionen zu unterstützen, macht es Laravel einfach, Ihre serverseitigen Laravel-Ereignisse über eine WebSocket-Verbindung zu "senden". Durch das Broadcasting Ihrer Laravel-Ereignisse können Sie dieselben Ereignisnamen und Daten zwischen Ihrer serverseitigen Laravel-Anwendung und Ihrer clientseitigen JavaScript-Anwendung austauschen.