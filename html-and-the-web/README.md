# Wie das Internet funktioniert

Das World Wide Web ist ein Netzwerk von Computern, die Informationen untereinander austauschen können. Es gibt viele verschiedene Protokolle, die die Regeln für die Kommunikation zwischen den Maschinen festlegen. Browser verwenden HTTP (Hypertext Transfer Protocol) zur Kommunikation mit Webservern.

- Die URL (Uniform Resource Locator) ist die eindeutige Adresse einer Ressource im Web und enthält einen für Menschen lesbaren Domänennamen, der über einen DNS (Domain Name Server) in die technische IP-Adresse (Internet Protocol) des Webservers aufgelöst werden muss.
- Der Browser sendet eine **GET- Anfrage** (eine HTTP-Methode) , um ein HTML-Dokument (Hypertext Markup Language) von einem Webserver zu laden.
- Der Webserver sendet eine **Antwort,** die das Dokument enthält.
- Häufig enthält der HTML-Code Verweise auf zusätzliche Ressourcen (CSS-Dateien, Bilder usw.), die der Browser dann ebenfalls vom Server anfordert.
- Der Browser **stellt** die empfangenen Inhalte auf dem Bildschirm dar und macht sie interaktiv.
- **Browser können später auch über nachfolgende GET-POST-** oder Anfragen zusätzliche Daten von Servern anfordern.

# Webprotokolle

Es gibt viele verschiedene Protokolle, die die Regeln für die Kommunikation zwischen zwei Maschinen definieren, zum Beispiel:

- Anfordern und Anzeigen von HTML-Dateien `http`(z. B. durch Öffnen von Webseiten mit Ihrem Browser)
- Zugriff auf die Shell eines anderen Computers `ssh`oder Klonen von Repositories von GitHub über eine SSH-Verbindung
- Senden und Empfangen von E-Mails über`TLS/SSL`
- Zugriff auf Dateien auf einem Server über das `FTP`Dateitransferprotokoll (File Transfer Protocol)

Im Moment konzentrieren wir uns auf die am häufigsten genutzte Funktion des Internets: das Anzeigen und Interagieren mit Webseiten.

Um eine bestimmte Website anzuzeigen, müssen Sie:

- Ermitteln Sie die IP- Adresse `addressIP address`des Servers, der die HTML-Datei bereitstellt, also die Internetprotokolladresse.
- sende eine `GET request`an diese Adresse
- Zusätzliche Ressourcen anfordern (CSS-Dateien, Bilder usw.).
- `render`der empfangene Inhalt (z. B. über einen Browser)

Die meisten mit dem Internet verbundenen Computer sind über eine Adresse erreichbar, `IPv4`die aus vier durch einen Punkt getrennten Zahlen im Bereich von 0 bis 255 besteht.

> 💡 Geben Sie diese IP-Adresse in die Adresszeile Ihres Browsers ein und sehen Sie, was passiert: `172.217.203.94`.

> 💡 Führen Sie folgenden Befehl in Ihrem Terminal aus, um die aktuelle IP-Adresse Ihres Computers zu erhalten: `curl ipinfo.io`.

Genauso wie es unpraktisch ist, sich alle Telefonnummern seiner Freunde zu merken, ist es nicht besonders benutzerfreundlich, sich die IP-Adressen aller Websites zu merken. Um dieses Problem zu lösen, können Websites über einen Domain Name Server ( `url`DNS ) aufgerufen werden `https://www.neuefische.de`. Der Browser fordert dann die IP-Adresse dieser Website von einem `DNS`DNS-Server an, der im Prinzip ein Telefonbuch für Domains ist.

Der Browser lädt dann alle notwendigen Inhalte für die Website, wie die HTML-Datei, CSS- und JavaScript-Dateien, Bilder, Schriftarten usw. Sobald alle Dateien heruntergeladen sind, zeigt der Browser den HTML-Inhalt an, formatiert ihn gemäß den Vorgaben im Stylesheet und führt den JavaScript-Code aus. Nun können wir mit der Website interagieren.

# HTML-Grundlagen

HTML (Hypertext Markup Language) dient dazu, Text strukturiert darzustellen. HTML-Tags geben an, welche Art von Element auf der Website angezeigt wird. Eine Überschrift wird beispielsweise so geschrieben:

```html
<h1>I am a headline!</h1>
```

Der als Überschrift definierte Inhalt wird von einem **öffnenden** und einem **schließenden Tag** umschlossen . Das Ganze wird als **Element** bezeichnet .

Die Elemente sind ineinander verschachtelt, um Struktur und Hierarchie zu schaffen.

```html
<h1>I am a <em>headline!</em></h1>
```

Manche Elemente können keine anderen Elemente enthalten und haben daher kein schließendes Tag. Sie sind selbstschließend und werden *leere Elemente* genannt .

```html
<hr />
or
<br />
```

## HTML-Tag-Attribute

Manche Elemente benötigen zusätzliche Informationen, um ordnungsgemäß zu funktionieren. Diese Informationen werden über Attribute angegeben, zum Beispiel:

- die Quelle eines Bildes
  ```html
  <img src="logo.png" alt="The logo of the company." />
  ```
- das Ziel eines Ankerelements
  ```html
  <a href="https://example.com"> click me </a>
  ```
- der Typ eines Eingabeelements
  ```html
  <input type="date" />
  ```

> 💡 Die MDN-Webdokumentation enthält detaillierte Informationen über Elemente und zugehörige Attribute.

## Layout einer HTML-Datei

Jedes HTML-Dokument beginnt mit einem Doctype , gefolgt vom `<html>`<html>-Element, das aus zwei Hauptteilen besteht:

- Es `<head>`enthält wichtige Metainformationen für den Browser, wie zum Beispiel
  - der Zeichensatz (utf-8)
  - das im Tab angezeigte Favicon
  - der Titel der Website
  - Für die Website werden CSS- und JavaScript-Dateien benötigt.
- Der `<body>`Bereich enthält den sichtbaren Inhalt der Website, strukturiert durch HTML-Elemente.

## Strukturierung einer Website

Entwicklern stehen zwei Hauptwerkzeuge zur Verfügung, um einer Website eine sinnvolle Struktur zu verleihen:

1. Verwendung semantischer HTML-Elemente
2. Verschachtelung / Gruppierung von HTML-Elementen

### **Semantisches HTML**

Semantische HTML-Elemente unterteilen nicht nur den Inhalt der Webseite in verschiedene Abschnitte, sondern beschreiben auch die Funktion oder den Zweck der Elemente. Dies hat zwei wesentliche Vorteile:

- Der HTML-Code wird für andere Entwickler verständlicher.
- Barrierefreiheitstools und Suchmaschinen können die Website interpretieren

Daher sollte man nach Möglichkeit immer semantische HTML-Elemente verwenden.

### **Verschachtelung von HTML-Elementen**

Durch Verschachtelung werden Elemente sinnvoll gruppiert. Das Element, das die anderen Elemente enthält, wird als **Elternelement** bezeichnet und enthält ein oder mehrere **Kindelemente** .
