---
title: Testen
taxonomy:
    category: docs
---

### Chapter Number

# Chapter Title

Laravel wurde mit Blick auf das Testen entwickelt. Tatsächlich ist die Unterstützung für das Testen mit PHPUnit bereits im Lieferumfang enthalten und eine phpunit.xml-Datei ist bereits für Ihre Anwendung eingerichtet. Das Framework wird außerdem mit praktischen Hilfsmethoden ausgeliefert, mit denen Sie Ihre Anwendungen ausdrucksstark testen können.

Standardmäßig enthält das Testverzeichnis Ihrer Anwendung zwei Verzeichnisse: Feature und Unit. Unit-Tests sind Tests, die sich auf einen sehr kleinen, isolierten Teil Ihres Codes konzentrieren. In der Tat konzentrieren sich die meisten Unit-Tests wahrscheinlich auf eine einzige Methode. Tests innerhalb des Unit"-Testverzeichnisses booten Ihre Laravel-Anwendung nicht und können daher nicht auf die Datenbank Ihrer Anwendung oder andere Framework-Dienste zugreifen.

Feature-Tests können einen größeren Teil Ihres Codes testen, z. B. wie mehrere Objekte miteinander interagieren oder sogar eine vollständige HTTP-Anfrage an einen JSON-Endpunkt. Im Allgemeinen sollten die meisten Ihrer Tests Funktionstests sein. Diese Arten von Tests bieten die größte Sicherheit, dass Ihr System als Ganzes wie vorgesehen funktioniert.

Eine ExampleTest.php-Datei wird sowohl im Feature- als auch im Unit-Test-Verzeichnis bereitgestellt. Nach der Installation einer neuen Laravel-Anwendung führen Sie die Befehle vendor/bin/phpunit oder php artisan test aus, um Ihre Tests zu starten.

Übersetzt mit www.DeepL.com/Translator (kostenlose Version)