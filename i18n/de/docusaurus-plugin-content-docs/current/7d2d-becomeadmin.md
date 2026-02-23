---
id: 7d2d-becomeadmin
title: "7 Days to Die: So wirst du Admin für 7 Days to Die"
description: "Entdecke, wie du Administratorrechte vergibst und verwaltest für volle Serverkontrolle und individuelle Admin-Rollen → Jetzt mehr erfahren"
sidebar_label: Admin werden
services:
  - gameserver-7d2d
---

import InlineVoucher from '@site/src/components/InlineVoucher';



Test Test Test 



## Einführung
Die Vergabe von Administratorrechten ermöglicht dir eine einfache und umfassende Verwaltung mit voller Kontrolle über deinen Server. Als Administrator kannst du alle verfügbaren Optionen und Funktionen, die das Spiel bietet, direkt im Spiel nutzen. Alle Schritte, die du zur Vergabe von Administratorrechten für deinen Server durchführen musst, werden im Folgenden beschrieben.  
<InlineVoucher />

## Konfiguration
Das Hinzufügen eines Admins erfolgt über die **serveradmin.xml**-Konfig, die du im Webinterface unter Konfigurationen findest.

![](https://screensaver01.zap-hosting.com/index.php/s/wXpLL2qyZE2zCYa/preview)

Deine SteamID64 findest du, indem du dein Steam-Profil öffnest und irgendwo mit der rechten Maustaste klickst. Dort wählst du dann **Steam-URL kopieren** aus.

![](https://screensaver01.zap-hosting.com/index.php/s/Q9WJ8GwbHCmTRPx/preview)



Anschließend öffnest du eine der folgenden Seiten und fügst die URL deines Profils dort ein: 

- https://steamrep.com/
- https://steamidfinder.com/
- https://steamid.io/

Dort erhältst du allgemeine Infos sowie die Steam ID deines Accounts. Für uns relevant ist nur die SteamID64. Die SteamID64 wird dann unter ``<admins>...</admins>`` eingetragen. Das sieht dann so aus:

```
 <users>
    <user steamID="76561198021925107" name="Hinweis, wer dieser Nutzer ist" permission_level="0" />
  </users>
```

:::danger  Admin-Eintrag wird nicht erkannt? 
Stelle sicher, dass du die Kommentarzeichen `<!--` und `-->` entfernst, damit die Zeile gültig wird. Ansonsten bleibt die Zeile nur ein Kommentar und wird nicht angewendet. Entferne einfach die Zeichen am Anfang und Ende der Zeile, um sie zu aktivieren.
:::

Das Spiel bietet die Möglichkeit, verschiedene Berechtigungsstufen für Administratorrechte zu definieren. Das heißt, es können unterschiedliche Admin-Gruppen mit verschiedenen Rechten angelegt werden. Die Stufe wird über die Option ``permission_level`` definiert. Diese kann von 0 bis 1000 gesetzt werden. Je nachdem, wie das eingestellt ist, haben die Administratoren Zugriff auf die zugewiesenen Rechte. Sobald das erledigt ist, wurden die Administratorrechte erfolgreich vergeben. 



## Berechtigungen

Die Berechtigungen für alle Admin-Befehle können unter ``permissions`` definiert werden. Dafür muss der ``permission_level`` angepasst werden, genau wie beim Hinzufügen von Administratoren. Das sieht dann so aus:

```
<permissions>
	<permission cmd="dm" permission_level="0" ></permission>
	<permission cmd="kick" permission_level="1" ></permission>
	<permission cmd="say" permission_level="1000" ></permission>
    <permission cmd="chunkcache" permission_level="1000" ></permission>
    <permission cmd="debugshot" permission_level="1000" ></permission>
    <permission cmd="debugweather" permission_level="1000" ></permission>
    <permission cmd="getgamepref" permission_level="1000" ></permission>
</permissions>
```

Ein Berechtigungslevel ist ein Wert zwischen 0 und 1000 und bestimmt, welche Rechte ein Spieler hat. 1000 ist das niedrigste Level (keine Rechte) und 0 das höchste (volle Admin-Rechte). Je nachdem, wie die Rechte vergeben werden sollen, muss das entsprechend angepasst werden. 


## Fazit

Glückwunsch, du hast die Administratorrechte erfolgreich konfiguriert. Bei weiteren Fragen oder wenn du Hilfe brauchst, steht dir unser Support-Team täglich zur Verfügung! 🙂

<InlineVoucher />