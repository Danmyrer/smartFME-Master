# SmartFME
### Erhalte deine Funkmeldungen per App!
  
## Idee:
Die Alarmierung per Funkmeldeempfänger (FME) hat vor vielen Jahren die Alarmierung per Sirene abgelöst. Hierdurch konnten die Feuerwehren diskret alarmiert werden und vor allem bei Freiwilligen Feuerwehren die Einsatzteilnahme gesteigert werden, da die Alarmierung nicht mehr auf die Reichweite der Sirene beschränkt ist. In den letzten Jahren wird zunehmend in verschiedensten Landkreisen schon der nächste Schritt gewagt - die Alarmierung per Smartphone.  
Der FME ist ein zusätzliches Gerät, dass jeder Feuermann / jede Feuerwehrfrau täglich neben seinem Handy mit sich führen muss. Da das Handy aber optimal die Alarmierungsfunktion des FME ersetzten kann, ist die Entwicklung einer solchen App naheliegend. Des Weiteren kann man über das Handy auch Features einbringen (Bspw. Zusage / Absage zu Einsatz), die den Führungskräften die Einsatzplanung erleichtern können.  
Der erwähnte Übergang vom FME zur Alarmierung per Smartphone ist jedoch ein sehr langsamer. Viele - vor allem freiwillige - Feuerwehren haben diese Funktion noch nicht implementiert, da die Verbandsgemeinden noch kein System eingeführt haben. Daher biete ich mit dieser Softwarelösung eine Möglichkeit, datenschutzkonform die FME-Alarmierung durch App-Alarmierungen zu erweitern, aber auch von Feuerwehren eingeführt werden kann.

---

## Umsetzung:
Die Software 'smartFME' umfasst drei Komponenten:  
1.  SmartFME-Receiver - Der Receiver liest den FME aus und sendet die Alarmierungen verschlüsselt an den Server
3.  SmartFME-Server - Der Server kann für die Nutzerverwaltung verwendet werden und dient als Verteilerzentrum für die Alarmierungen
4.  SmartFME-Client - Der Client (die Smartphone-App) empfängt die Nachricht und alarmiert den Feuerwehrmann / die Feuerwehrmannfrau

---

## Datenschutz:
Da es sich bei den Einsatzdaten um sehr vertrauliche Daten handelt, muss bei der Übertragung auf viele Standards geachtet werden. Durch die momentane Verschlüsselungslösung können nur der Client und die berechtigten Receiver die Nachricht entschlüsseln und lesen. Da der Receiver die Alarmierung direkt mit den Public-Keys der zu alarmierenden Clients verschlüsselt, ist nie eine Unverschlüsselte / für den Server entschlüsselbare Alarmierung im Internet.
Zudem ist in den Clients keine Möglichkeit zum Speichern der Alarmdaten implementiert, wodurch die Daten nach abschließen des Einsatzes sofort gelöscht werden.

## Links:
- [SmartFME-Receiver-Pi](https://github.com/Danmyrer/smartFME-Reciever-Pi)
- [SmartFME-Server-Functions](https://github.com/Danmyrer/SmartFME-Server-Functions)
- [SmartFME-Client-Android](https://github.com/Danmyrer/SmartFME-Client-Android)
