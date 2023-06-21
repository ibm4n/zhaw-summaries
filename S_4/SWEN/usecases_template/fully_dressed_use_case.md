# Fully-dressed Use-Case

**Primärakteur**: Gast (Kunde), der gerade eingetroffen ist

**Stakeholders und Interessen**
- Hotelgast: Möchte, dass Check-In korrekt und möglichst schnell abläuft
  
- Hotel wie Gast + ohne Intervention Zentrale

**Vorbedingung**: Gast ist vor dem Terminal, Terminal läuft

**Nachbedingung**: Gast ist eingebucht und seine Zimmerkarten sind erfasst und konfiguriert.

**Standardablauf**
1. Gast gibt Buchungsnummer ein.
   
2. System überprüft Buchungsnummer und zeigt die damit verbundenen Personendaten an.

3. Gast bestätigt Korrektheit.
   
4. Gast nimmt eine Zimmerkarte vom Stapel und führt sie dem Lesegerät beim Terminal zu.

5. System erhält ID der Zimmerkarte vom ZVS (oder direkt vom Leser). Darauf werden mit den Buchungsinformationen die Zimmer für diese Buchung reserviert und diese Information mit der Buchungsdauer dem ZVS mitgeteilt.

6. Schritte 4 und 5 werden solange wiederholt, bis alle Zimmer zugewiesen wurden.

7. Das Verschlusssystem bestätigt die neue Konfiguration.

8. Das System teilt dem Kunden die Zimmernummer(n) mit und dass alles korrekt abgelaufen ist.

**Erweiterungen**

*2a* Unbekannte Buchungsnummer
1. System findet keine Buchung zur eingegebenen Nummer, teilt dies dem Gast mit und fährt bei Schritt 1 weiter.

*3a* Inkorrekte Daten
1. Der Gast stellt fest, dass die Buchungsdaten fehlerhaft sind. Er ruft mit dem vorhanden Telefon die Zentrale an, um die Sache zu bereinigen.

2. Zentrale nimmt Korrekturen an den Buchungsdaten vor und erlaubt es dann dem Gast, bei Schritt 4 weiterzufahren
   
*5a* ID der Zimmerkarte ist unbekannt
1. System kennt die ID der Karte nicht. Es fordert den Gast auf, eine neue Karte vom Stapel zu nehmen.

2. Gast fährt bei Schritt 3 weiter.


*5b* Kein Zimmer verfügbar
1. System kann mit einfachem Algorithmus kein freies Zimmer gemäss den Buchungsdaten finden. Es fordert den Gast auf, mit dem Telefon die Zentrale anzurufen und das Problem so zu lösen

2. Zentrale weist von Hand ein Zimmer zu (vermutlich in einer besseren Kategorie)

3. Gast fährt bei Schritt 3 weiter.


*5c* ZVS kann nicht angesprochen werden
1. System teilt dem Gast den Fehler mit, alarmiert die Zentrale und informiert
den Gast (respektive die nächsten Gäste), dass im Moment kein Check-In 
möglich ist. 

2. Zentrale versucht Problem zu beheben und schaltet das System wieder 
aktiv, wenn dies geschehen ist.