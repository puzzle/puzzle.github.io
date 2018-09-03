# Einrichten eines Wallets für das "Lightning Network" auf dem Mainnet

Zahlungen mit dem Lightning Network sind blitzschnell. Doch bis man sein
Gerät soweit hat, dass man Zahlungen ausführen kann, dauert es einen Moment.

Diese Anleitung ist für technisch nicht so versierte Benutzer gedacht, die
mit dem Handy bezahlen möchten. Deshalb zeigen wir den Prozess anhand
Apps für Mobilgeräte.

**Diese Anleitung bezieht sich auf Bitcoin Mainnet, also die "produktive"
Bitcoin-Blockchain!** 
Wer eine Anleitung für das Testnet sucht,
[wird hier fündig (Englisch)](https://gugger.guru/lightning-workshop/).

## Schritt 0: Disclaimer

Bevor wir loslegen, möchten wir an dieser Stelle noch einmal ganz klar und deutlich
darauf aufmerksam machen, dass es sich beim Lightning Network um eine Technologie
handelt, die sich noch im Stadium "experimentell" befindet.
Dies bedeutet, dass nicht garantiert werden kann, dass alles fehlerfrei und reibungslos
funktioniert.
Im schlimmsten (jedoch eher unwahrscheinlichen) Fall kann Geld verloren gehen
oder für eine gewisse Zeit nicht zugänglich sein.

**Wir empfehlen deshalb ganz klar, nur mit kleinen Beträgen zu starten!**

## Schritt 1: App installieren

Zum Entstehungszeitpunkt dieses Artikels (Anfang September 2018) gibt es nur
Mainnet-Kompatible Apps für Android-Geräte. Apps für iOS werden hoffentlich sehr
bald erscheinen.

Die hier ersichtlichen Screenshots sind alle vom "Eclair" Wallet. Das Prinzip sollte aber
bei anderen Apps sehr ähnlich sein und die Anleitung sollte deshalb auch für diese
benutzt werden können.

1. Wir installieren uns nun die App "Eclair Wallet Mainnet" aus dem Google Play store:
  <img src="../assets/img/lightning/store-eclair-mainnet.png" width="300">
1. Beim Starten wird uns auch hier noch einmal mitgeteilt, dass es sich um "beta"-Software
  handelt:
  <img src="../assets/img/lightning/mainnet-disclaimer.png" width="300">
1. Nach der Bestätigung der Warnung, werden wir gefragt, ob wir ein neues Wallet
  einrichten oder ein bestehendes importieren wollen. Wir wollen ein neuer erstellen
  und wählen deshalb "Create New Wallet":
  <img src="../assets/img/lightning/create-or-import.png" width="300">
1. Nun kommt ein sehr sehr wichtiger Teil: Die 24 Wörter.<br/>
  Hier gibt es absichtlich keinen Screenshot, weil diese 24 Wörter sehr geheim sind.
  Diese Wörter widerspiegeln den kryptografischen Zugangscode auf das gesamte Guthaben,
  das später in dem Wallet sein wird. Das heisst, wer die Wörter kennt, hat Zugriff
  auf das Geld.<br/>
  Deshalb:
   - **Wörter aufgschreiben und an einem sicheren Ort aufbewahren**: Wenn das Handy
   defekt ist, oder verloren geht, dann kann mit den Wörtern das Guthaben widerhergestellt
   werden.
   - **Niemals jemandem diese Wörter anvertrauen**: Eine Person oder Webseite, die nach
   diesen Wörtern fragt, versucht sehr wahrscheinlich, das Guthaben zu stehlen. Darum sollte
   ein Backup nur bei Apps eingespielt werden, bei denen man sicher ist, dass sie
   vertrauenswürdig sind.
1. Hat man die Wörter aufgeschrieben, werden sie gleich überprüft. Die App fragt nach 3
  zufälligen Wörtern aus der Liste, die man soeben aufgeschrieben hat. Hat man diese bestätigt,
  gelangt man auf den Hauptbildschirm der App.

Die App ist nun erfolgreich installiert und die Geldbörse/das Wallet eingerichtet.
Wir können nun auf den drei Hauptbildschirmen der App herumnavigieren, in dem wir nach
links oder rechts swipen/streichen:

<table border="0" cellpadding="5">
<tr>
<td><img src="../assets/img/lightning/mainnet-screen-left.png" width="100"></td>
<td><img src="../assets/img/lightning/mainnet-screen-center.png" width="100"></td>
<td><img src="../assets/img/lightning/mainnet-screen-right.png" width="100"></td>
</tr>
<tr>
<td>Links: Bitcoin-Adresse</td>
<td>Mitte: Transaktionen</td>
<td>Rechts: Lightning Channels</td>
</tr>
</table>

## Schritt 2: Bitcoin einkaufen



* SBB-Automat
* Handy dabei wegen SMS
* Adresse im Wallet generieren
* Dauert 3 Confirmations

## Schritt 3: Channel zu Puzzle-Node eröffnen

* Darauf hinweisen, warum Puzzle-Node, Vor-/Nachteile zeigen
* Vergleich mit Prepaid-Guthaben aufstellen, aber mit Unterschied, dass
  über den Channel auch Geld zurückfliessen kann
* Dauert 3 Confirmations

# FAQ

* Geld zurück verlangen?
  * Payment Request erzeugen

* Was ist, wenn Geld im Channel aufgebraucht?
  * Channel schliessen oder Geld zurück erhalten
 
 