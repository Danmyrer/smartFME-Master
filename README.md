### Vertraulich - noch in der Entwicklung
# SmartFME
### Erhalte deine Funkmeldungen per App!
  
## Idee:
Die Alarmierung per Funkmeldeempfänger (FME) hat vor vielen Jahren die Alarmierung per Sirene abgelöst. Hierdurch konnten die Feuerwehren diskret alarmiert werden und vor allem bei Freiwilligen Feuerwehren die Einsatzteilnahme gesteigert werden, da die Alarmierung nicht mehr auf die Reichweite der Sirene beschränkt ist. In den letzten Jahren wird zunehmend in verschiedensten Landkreisen schon der nächste Schritt gewagt - die Alarmierung per Smartphone.  
... text text text ...  
Der erwähnte Übergang vom FME zur Alarmierung per Smartphone ist jedoch ein sehr langsamer. Viele - vor allem freiwillige - Feuerwehren haben diese Funktion noch nicht implementiert, da die Verbandsgemeinden noch kein System eingeführt haben. Daher versuche ich mit dieser Softwarelösung eine Möglichkeit zu bieten, datenschutzkonform die FME-Alarmierung durch die App-Alarmierungen zu erweitern, die auch von Feuerwehren Eingeführt werden kann.

---

## Umsetzung:
Die Software 'smartFME' umfasst drei Komponenten:  
1.  SmartFME-Reciever - Der Reciever liest den FME aus und sendet die Alarmierungen verschlüsselt an den Server
3.  SmartFME-Server - Der Server kann für die Nutzerverwaltung verwendet werden und dient als Verteilerzentrum für die Alarmierungen
4.  SmartFME-Client - Der Client (die Smartphone-App) empfängt die Nachricht und alarmiert den Feuerwehrmann / die Feuerwehrmannfrau

---

## Datenschutz:
Da es sich bei den Einsatzdaten um sehr vertrauliche Daten handelt, muss bei der Übertragung auf viele Standarts geachtet werden. Durch die momentane Verschlüsselungslösung können nur der Client und die berechtigten Reciever die Nachricht Entschlüsseln und Lesen. Da der Reciever die Alarmierung direkt mit den Public-Keys der zu Alarmierenden Clients verschlüsselt, ist nie eine Unverschlüsselte / für den Server entschlüsselbare Alarmierung im Internet.  
Zudem ist in den Clients keine Möglichkeit zum Speichern der Alarmdaten implementiert, wodurch die Daten nach abschließen des Einsatzes sofort gelöscht werden.

---

## Links:
Das Projekt ist zu Umfassend um in einem einzelnen Repository gespeichert zu werden, weswegen hier die dazugehörigen Repositorys gespeichert sind:
- [SmartFME-Reciever-Pi](https://github.com/Danmyrer/smartFME-Reciever)
- [SmartFME-Server-Functions](https://github.com/Danmyrer/SmartFME-Server)
- [SmartFME-Client-Android](https://github.com/Danmyrer/SmartFME-Client-Android)
