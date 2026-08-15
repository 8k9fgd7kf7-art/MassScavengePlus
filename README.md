# Mass Scavenge+

Mass Scavenge+ ist ein komfortables Schnellleisten-Script für **Die
Stämme**, das den Massenraubzug um eine kompakte Oberfläche, flexible
Zeitplanung und zusätzliche Hilfen bei der Verteilung von Truppen auf
Sammelaufträge erweitert.

## Funktionen

-   Auswahl und Priorisierung der verwendeten Truppentypen
-   frei einstellbare Reserven pro Truppentyp
-   Auswahl der vier Sammelkategorien
-   zwei Verteilungsstrategien:
    -   **Ausgeglichen**
    -   **Hohe Kategorien zuerst**
-   getrennte Planung für Off- und Def-Dörfer
-   Planung über **Rückkehrzeit** oder **Laufzeit in Stunden**
-   frei konfigurierbare Schnellbuttons, z. B.:
    -   `+4h`
    -   `Heute 22:30`
    -   `Morgen 09:00`
-   intelligente Empfehlungen für die passende Verteilung
-   auffällige rote Warnung, wenn die aktuelle Verteilung nicht zur
    Empfehlung eines Schnellbuttons passt
-   erneute Sicherheitsprüfung vor der Berechnung
-   Dorf-Auswahl und Filter
-   Berechnungsanalyse
-   kompakte, an Die Stämme angepasste Oberfläche
-   mobile Darstellung für die Nutzung über die Schnellleiste
-   Touch-Bedienung und verschiebbares Fenster auf Mobilgeräten

## Installation über die Schnellleiste

Mass Scavenge+ ist für die Nutzung als Schnellleisten-Script vorgesehen.

Die eigentliche Script-Datei liegt im GitHub-Repository und wird beim
Start über GitHub Pages geladen. Dadurch muss der Schnellleisten-Eintrag
bei späteren Updates nicht jedes Mal geändert werden.

### GitHub Pages

Die veröffentlichte Script-Datei wird über folgenden Pfad geladen:

`https://8k9fgd7kf7-art.github.io/MassScavengePlus/MassScavengePlus.js`

### Schnellleisten-Code

``` javascript
javascript:(()=>{const u=new URL(location.href);if(u.searchParams.get('screen')!=='place'||u.searchParams.get('mode')!=='scavenge_mass'){location.href=game_data.link_base_pure+'place&mode=scavenge_mass';return;}if(window.__MASS_SCAVENGE_PLUS_RUNNING__){return;}$.getScript('https://8k9fgd7kf7-art.github.io/MassScavengePlus/MassScavengePlus.js').fail(()=>UI.ErrorMessage('Mass Scavenge+ konnte nicht über GitHub Pages geladen werden.'));})();
```

Wird der Schnellleisten-Button außerhalb des Massenraubzugs gedrückt,
wechselt er zunächst auf die passende Seite. Auf der Massenraubzug-Seite
lädt er Mass Scavenge+.

## Bedienung

### 1. Truppen auswählen

Hier wird festgelegt, welche Truppentypen für die Berechnung verwendet
werden dürfen. Zusätzlich kann für jeden Truppentyp eine Reserve
festgelegt werden.

### 2. Sammelkategorien

Hier werden die gewünschten Sammelkategorien aktiviert oder deaktiviert.

### 3. Verteilung

**Ausgeglichen** verteilt die verfügbaren Truppen möglichst auf die
aktiven Kategorien.

**Hohe Kategorien zuerst** priorisiert die höheren Sammelstufen.

### 4. Laufzeit / Rückkehr

Es stehen zwei Planungsarten zur Verfügung:

-   **Rückkehrzeit** -- Off- und Def-Dörfer erhalten eine gewünschte
    Rückkehrzeit.
-   **Laufzeit in Stunden** -- es wird direkt eine gewünschte Laufzeit
    angegeben.

Die Werte für Off- und Def-Dörfer können getrennt eingestellt oder mit
den Buttons **Off → Def** und **Def → Off** übernommen werden.

### Schnellbuttons

Über das Zahnrad neben den Schnellbuttons können eigene Buttons
hinzugefügt, bearbeitet und entfernt werden.

Ein Schnellbutton kann beispielsweise relativ oder kalenderbezogen
arbeiten:

-   `+4h`
-   heute um eine bestimmte Uhrzeit
-   morgen um eine bestimmte Uhrzeit
-   nächster Zeitpunkt einer bestimmten Uhrzeit

Zusätzlich kann jedem Schnellbutton eine empfohlene Verteilung
zugeordnet werden:

-   **Egal**
-   **Ausgeglichen**
-   **Hohe Kategorien zuerst**

Stimmt die aktuelle Verteilung nicht mit der Empfehlung überein, zeigt
Mass Scavenge+ eine rote Warnung und bietet eine direkte Umstellung an.
Die Verteilung wird niemals ungefragt automatisch geändert.

### 5. Dörfer

Die zu berücksichtigenden Dörfer können geladen, ausgewählt und
gefiltert werden.

### 6. Berechnungsanalyse

Die Analyse zeigt zusätzliche Informationen dazu, wie die aktuelle
Planung zustande kommt.

## Mobile Nutzung

Mass Scavenge+ ist auch für Smartphones ausgelegt.

Auf kleinen Displays verwendet das Fenster nahezu die gesamte verfügbare
Bildschirmbreite. Inhalte können innerhalb des Fensters gescrollt
werden, Schnellbuttons brechen automatisch um und die Zeitsteuerung wird
für schmale Displays angepasst.

Das Fenster kann auf Touch-Geräten am Kopf verschoben werden.

## Updates

Da die Schnellleiste nur den Loader enthält, erfolgen Updates zentral
über die Datei `MassScavengePlus.js` auf GitHub.

Nach einem Update der GitHub-Datei wird beim nächsten Laden automatisch
die aktuelle Version verwendet. Der Schnellleisten-Code muss dafür
normalerweise nicht verändert werden.

## Aktueller Entwicklungsstand

**Mass Scavenge+ v2.9.4-beta**

Die aktuelle Version enthält insbesondere:

-   bereinigte und kompakte Benutzeroberfläche
-   einheitliche Statuszeile
-   konfigurierbare Schnellbuttons
-   intelligente Verteilungswarnungen
-   rote Warnanzeige
-   optimierte mobile Oberfläche

## Hinweis

Mass Scavenge+ ist ein inoffizielles Hilfsscript und kein Bestandteil
von Die Stämme bzw. InnoGames.

Die Verwendung erfolgt auf eigene Verantwortung. Vor der Nutzung sollte
geprüft werden, ob Scripts dieser Art nach den jeweils geltenden
Spielregeln des verwendeten Servers zulässig sind.
