# Digitales Klassenbuch

## Technologien
- Python 3  
- PyQt5  
- CSS-Stylesheet
- JSON

## Was ich gelernt habe
- Das Erstellen eines Eingabefelds.  
- Das Gestalten von zwei unterschiedlich aussehenden Buttons.   
- Das Erstellen und Anwenden eines CSS-Stylesheets.  
- Das Erstellen von KI-Assistenten, die mit den manuellen Tabs verbunden sind  
  und die Verwaltung vereinfachen.

## Beschreibung
### Startseite – Stammdaten
Mein Programm besteht aus sechs manuellen Tabs; zusätzlich gibt es vier KI-Assistenten.  
Beim Start des Programms erscheint ein Fenster. Oberhalb befinden sich die Tabs  
**Stammdaten**, **Stundenplan**, **Anwesenheitsliste**, **Abwesenheitsliste**, **Notenliste**, **Unterrichtsausfall**,  
**KI-Assistent (Anwesenheit)**, **KI-Assistent (Abwesenheit)**, **KI-Assistent (Stammdaten)** und **KI-Assistent (Notenliste)**.  
Unter den Tabs steht der Name der Klasse, den man im Eingabefeld **„Neuen Klassennamen eingeben“** eingeben  
und durch Klick auf den Button **„Klassenname übernehmen“** setzen kann.  
Unter dem Button **„Klassenname übernehmen“** befindet sich ein Bereich, in dem man Schüler:innen und Lehrkräfte verwalten kann.  
Es gibt die zwei Eingabefelder **„Schüler-Name“** und **„Lehrer-Name“**.  
Gibt man den Namen einer Schülerin/eines Schülers in das Eingabefeld **„Name der Schülerin/des Schülers“** ein und klickt auf  
**„Schüler:in anlegen“**, wird die Person in der **„Aktuellen Schülerliste“** angezeigt.  
Möchte man eine:n Schüler:in entfernen, markiert man den Eintrag in der **„Aktuellen Schülerliste“** und klickt auf  
**„Ausgewählte:n Schüler:in entfernen“**.  
Nach demselben Prinzip funktioniert die Verwaltung der Lehrkräfte.

### Stundenplan
Das Tab **Stundenplan** enthält drei Buttons. Damit kann man einen Stundenplan aus einer JSON-Datei laden.  
Bei Klick auf **„Stundenplan aus JSON laden“** öffnet sich der Datei-Explorer; man wählt die entsprechende JSON-Datei.  
Beim Einlesen werden die Lehrkräfte automatisch in die **„Aktuelle Lehrkraftliste“** eingetragen.  
Der Stundenplan ist variabel und kann mit sechs oder acht Stunden geladen werden.  
Der zweite Button **„Stundenplan als JSON speichern“** exportiert den Stundenplan als JSON-Datei.  
Der dritte Button **„Stundenplan leeren“** leert den Stundenplan.

### Anwesenheitsliste
Dieses Tab zeigt die Anwesenheitsliste der Klasse. Hier werden alle Schüler:innen aus der **„Aktuellen Schülerliste“** angezeigt.  
Neben jedem Namen befindet sich ein Kästchen, in dem man die Anwesenheit abhaken kann.  
Unten befindet sich der Button **„Anwesenheit als Textdatei exportieren und Liste zurücksetzen“**.  
Damit wird eine Textdatei erzeugt; anschließend werden die Häkchen zurückgesetzt (nur die Markierungen, nicht die Liste selbst).

### Abwesenheitsliste 
Hier werden die Namen angezeigt, die in der Anwesenheitsliste **nicht** abgehakt wurden.  
Mit dem Button **„Abwesenheitsliste exportieren“** kann man die Liste als Textdatei speichern.

### Notenliste
In diesem Tab kann man eine Notenliste für Schüler:innen führen.  
Im Feld **„Aktuelles Fach:“** kann man ein Fach auswählen.  
Falls noch kein Fach angelegt wurde, befindet sich darunter der Button **„Neues Fach anlegen“**.  
Nach Klick auf **„Neues Fach anlegen“** erscheint ein Dialog, in dem man den Namen des Fachs eingibt; mit **„OK“** wird das Fach angelegt.  
Unter dem Eingabefeld **„Spaltenname“** befindet sich der Button **„Notenspalte hinzufügen“**. Gibt man einen Spaltennamen ein  
und klickt auf **„Notenspalte hinzufügen“**, wird die entsprechende Spalte angelegt.  
Möchte man eine Spalte löschen, gibt man den Namen in das Eingabefeld **„Spaltenname Noten“** ein und klickt auf  
**„Notenspalte löschen“**.  
Mit **„Noten als Textdatei exportieren und Liste zurücksetzen“** kann man die Notenliste als Textdatei speichern;  
nach dem Speichern wird die Liste geleert (die Spalten bleiben bestehen).  
Unter diesem Button befindet sich **„Fach entfernen“**; damit wird das ausgewählte Fach gelöscht.

### Unterrichtsausfall
Dieses Tab dient der Dokumentation von Unterrichtsausfällen.  
Es gibt vier Eingabefelder: **„Datum“**, **„Stunde“**, **„Fach“** und **„Grund“**.  
Nach dem Ausfüllen kann man mit **„Ausfall hinzufügen“** den Eintrag zur Liste hinzufügen.  
Zum Löschen markiert man einen Eintrag und klickt auf **„Ausgewählte Einträge löschen“**.  
Zum Archivieren exportiert man die Ausfälle über **„Ausfälle als CSV exportieren“** in eine CSV-Datei.

### KI-Assistent (Anwesenheit)
Dieser Assistent automatisiert die Verwaltung der Anwesenheit.  
**Beispiel:**  
• „Max Mustermann“ → nur den Namen eingeben, die Person wird abgehakt.  
Gibt man einen Namen ein und klickt auf **„Senden“**, wird die/der Schüler:in abgehakt.

### KI-Assistent (Ausfall)
Dieser Assistent verwaltet die Einträge im Tab **Unterrichtsausfall**.  
**Befehle:**  
• „Ausfall“ → Dialog (Datum → Stunde → Fach → Grund)  
• „Export“ → CSV exportieren und Liste leeren  
• „Liste leeren“ → alle Ausfälle löschen  
• „Lösche Zeile 2“ / „Lösche Zeilen 2–4, 6“

Die Befehle gibt man unten in das Eingabefeld ein; mit **„Senden“** wird der Befehl auf das Tab **Unterrichtsausfall** angewendet.

### KI-Assistent (Stammdaten)
Dieser Assistent verwaltet die Stammdaten.  
**Tipp:** Alles per Textbefehl.  
**Beispiele:**  
• „Importiere Schüler-CSV“ / „Importiere Lehrer-CSV“  
• „Lösche alle Schüler“ / „Lösche alle Lehrer“  
• „Füge Schüler Max Mustermann hinzu“ / „Lösche Lehrkraft Herr Weber“  
• „Setze Klasse 10b“ oder „Klasse: 10b“

Die Befehle gibt man unten in das Eingabefeld ein; mit **„Senden“** wird der Befehl auf die Stammdaten angewendet.

### KI-Assistent (Notenliste)
Dieser Assistent hilft bei der Verwaltung der Notenliste.  
**Beispiele für Befehle:**  
• „Mathe: Max Mustermann -> KA1 = 2“  
• „Max Mustermann -> Test 1 = 1,7“  
• „Fach: Mathe“ / „Wechsle Fach Mathe“ / „Fach löschen Mathe“  
• „Spalte hinzufügen Test 1“ / „Spalte löschen Test 2“

Die Befehle gibt man unten in das Eingabefeld ein; mit **„Senden“** werden sie auf die Notenliste angewendet.

```bash
# 1) venv anlegen
python -m venv .venv

# 2) aktivieren
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

# 3) Abhängigkeiten installieren
python -m pip install --upgrade pip
pip install PyQt5


##  Starten
```bash
python main.py
````

