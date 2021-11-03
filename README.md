# Hagelschutz über Meteo Schweiz
Fragt bei Meteo Schweiz nach dem Hagelstatus ab.

### Inhaltverzeichnis

1. [Funktionsumfang](#1-funktionsumfang)
2. [Voraussetzungen](#2-voraussetzungen)
3. [Einrichten der Instanz](#3-einrichten-der-instanz)
4. [Statusvariablen und Profile](#4-statusvariablen-und-profile)

### 1. Funktionsumfang

* Fragt im zwei Miunten Takt nach dem Hagelstatus ab.

### 2. Voraussetzungen

- IP-Symcon ab Version 1.0

### 3. Einrichten der Instanz

__Konfigurationsseite__:

Name                                 | Beschreibung
------------------------------------ | ---------------------------------
deviceID                             | Eingabe der deviceID, wird bei der Anmeldung vom VKF mitgeteilt.
hwTypeID                             | Wert wird von der VKF mitgeteilt.

### 4. Statusvariablen und Profile

Die Statusvariablen/Kategorien und Profile werden automatisch angelegt. Das Löschen einzelner kann zu Fehlfunktionen führen.

##### Statusvariablen

Es werden automatisch folgende Statusvariablen angelegt.

Bezeichnung          | Typ     | Beschreibung
-------------------- | ------- | -----------
Status               | Boolean | Zum aktivieren oder deaktivieren vom Hagelschutz. Wen deaktiviert, wird trotzdem die Abfrage bei Meteo Swiss gemacht.
Hagelmeldung         | Integer | Zeigt die aktuelle Hagelmeldung an (siehe Profile). Variable "Status" muss auf true sein.

##### Profile

Es werden automatisch folgende Profile angelegt.

Bezeichnung          | Typ     | Beschreibung
-------------------- | ------- | -----------
HailState            | Boolean | Übersetzt false = kein Hagelschutz, true = Aktiv
HailWarning          | Integer | Übersetzt 0 = kein Hagel, 1 = Hagelalarm, 2 = Testalarm