# Setup a wallet for the "Lightning Network" on Mainnet

[Die Deutsche Version ist hier.](../de/tutorial-mainnet-lightning-network-wallet.md)

Payments over the Lightning Network are as fast as lightning. But it takes
a while to set up your device to be ready to pay.

This tutorial is meant for non-technical users who want to pay with their
mobile phone. Therefore it will focus on apps for mobile platforms.

**These instructions are specific to Bitcoin Mainnet! You will deal with
real money.**
If you are looking for instructions for testnet,
[here is a tutorial.](https://gugger.guru/lightning-workshop/)

## Step 0: Disclaimer

Before we start, we want to make clear, that the Lightning Network is a
technology that is still considered to be "experimental".
This means that there is no guarantee that everything will work smoothly
and without errors.
In the worst (but rather unlikely) case, you can lose money or might not be
able to spend it for some time.

**We therefore urge you to start with small amounts!**

## Step 1: Install the app

At the time this tutorial is written (start of September 2018), there are
only Mainnet compatible apps available for Android devices. Apps for Apple iOS will
hopefully be released soon.

All the screenshots shown here are from the "Eclair" wallet. But the process
is similar in other apps, so you should be able to use this tutorial too.

1. We install the app "Eclair Wallet Mainnet" from the Google Play Store:<br/>
  <img class="shadow" src="../assets/img/lightning/store-eclair-mainnet.png" width="400">
1. At startup, the app also informs us about the "beta" state of the software:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-disclaimer.png" width="400">
1. After we acknowledge the warning, we are asked if we want to create a new wallet
  or want to import an existing one. Since we don't have one yet, we choose
  "Create New Wallet":<br/>
  <img class="shadow" src="../assets/img/lightning/create-or-import.png" width="400">
1. The next part is very very important: The 24 words, also called the mnemonic phrase.<br/>
  There is no screenshot shown here because these 24 words are very secret. They represent
  the cryptographic access code to the whole balance of Bitcoin that will be stored in
  the wallet later. Or in other words: The person who has access to them, has access
  to the money!<br/>
  Therefore:
   - **Write down the words and store them in a safe place**: If you lose your mobile
   phone or it stops working, you can restore your wallet with these words. Without
   them, everything is lost! There is no bank that can "unlock your account". So best put
   the paper with the 24 words into a safe.
   - **Never hand out these words to anyone**: A person or website asking you for the
   words is very likely a scammer who tries to steal your money. Only type your words
   into an app to restore a backup. And only into an app you know comes from a trustworthy
   source.
1. After you've written down the words, the app will check that you indeed did do so. It will
  ask for three randomly selected words out of the 24 you wrote down. You will need to type
  them, separated by a space. Once completed, the app will also ask you for a PIN.
  This PIN only protects the app itself from unauthorized access, in case your phone gets stolen.
  In contrast to the 24 mnemonic words, you can change the PIN any time.<br/>
  After setting up a PIN, you will see the main interface of the app.

You have now successfully installed the wallet. There are three main screens in the app
that you can navigate to by swiping your finger left or right:

<table border="0" cellpadding="5">
<tr>
<td><img class="shadow" src="../assets/img/lightning/mainnet-screen-left.png" width="350"></td>
<td><img class="shadow" src="../assets/img/lightning/mainnet-screen-center.png" width="350"></td>
<td><img class="shadow" src="../assets/img/lightning/mainnet-screen-right.png" width="350"></td>
</tr>
<tr>
<td>Left: Your Bitcoin Address</td>
<td>Middle: Transaction History</td>
<td>Right: Lightning Channels</td>
</tr>
</table>

Since we are going to buy Swiss Francs, it's probably a good idea to change the monetary units
the app displays. Most of the following screenshots will show CHF for fiat currencies and
Satoshi (= 0.00000001 bitcoin, BTC) as Bitcoin unit.<br/>
You find these settings in the following menu:<br/>
<img class="shadow" src="../assets/img/lightning/settings.png" width="400">
<img class="shadow" src="../assets/img/lightning/settings-units.png" width="400">

## Step 2: Buy bitcoins

Our wallet is now ready to receive some bitcoins. There are many ways to do so.
We are going to show you an option that is easy, straightforward and works at
every train station in Switzerland: Buy bitcoins at a SBB ticket machine.

All that we need is a Swiss mobile number that can receive text messages/SMS.
Bitcoin purchases at the ticket machines are limited to CHF 500.- per mobile number
and day. This is enforced by sending a mTAN as a text message to a mobile phone.

Once we are in front of the ticket machine, we select "Prepaid" and then "Top up Bitcoin" on the
touch screen. The first thing we will be asked for is our Bitcoin address.
The ticket machine can scan the QR code that is displayed in our Eclair app. So we
open the app, swipe right to show the QR code (in the tab "Your Bitcoin Address")
and hold our mobile phone screen below the camera of the ticket machine: 
<img class="shadow" src="../assets/img/lightning/mainnet-receive.png" width="400">

Depending on the ambient light and the brightness of your screen, this can be a bit tricky.
Don't put your mobile phone too close. A distance of approximately 20cm proved to be
optimal. If it doesn't work within a minute or two, it's possible that the ticket machine
reverts to its main screen. Try again by tapping "Prepaid" and then "Top up Bitcoin" once more.

As soon as the ticket machine is able to read the address, it will show it on screen.
It is always advised to check the first and last four characters of a Bitcoin address, so we
do that now too.

The machine now asks us what amount we want to exchange into bitcoins. After selecting the amount
we will need to enter the mobile number and will then receive a code in a text message.
Enter the code when the ticket machine asks for it.

Now we should see a summary of our order, the fees and the exchange rate we will get. If we agree
with everything, we can pay the order either with cash or with a bank card.
The payment will be confirmed with a paper receipt that will contain the same information again.

In our app we should see something similar to this in our "Transaction History":
<img class="shadow" src="../assets/img/lightning/mainnet-incoming-tx.png" width="400">

The transaction was registered by the Bitcoin network, but has not been confirmed yet ("0 confs").
As soon as there are at least 3 confirmations reached, the transaction is considered to be final and
the amount can be used/spent in the app.

[More information about buying bitcoins at the SBB ticket machines.](https://www.sbb.ch/en/station-services/services/further-services/bitcoin.html)

## Step 3: Open a channel to Puzzle ITC's node

After we have three confirmations on our incoming transaction, we can proceed to the last
step of our setup process: We are going to open a channel in the "Lightning Network".<br/>
This is like charging a prepaid card. The charging process can take a while but as soon
as the amount is on the card, it can be spent easily and immediately.

This last step in our tutorial will also take a moment because there will be another Bitcoin
transaction that needs to be written into the blockchain and then confirmed three times.
But this is the last step where we need to wait. As soon as the channel is open, everything
will be as fast as lightning.

1. With a swipe left, we go to the tab "Lightning Channels" in our app and click the button
  at the bottom.<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-channel-menu.png" width="400"><br/>
  If we have a PC or another device available near us, it's easiest to open the website
  [lightning.puzzle.ch](https://lightning.puzzle.ch) there and scan the QR code with our mobile
  phone. To do so, we select "Scan A Node URI" in our Eclair app and then scan the QR code
  that is displayed on the website.<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-scan-node-uri.png" width="400"><br/>
  If we only have our mobile phone with us, we open the website
  [lightning.puzzle.ch](https://lightning.puzzle.ch) in our phone's web browser and copy
  the text above the QR code. It's important to copy everything, including
  <code>...@lightning.puzzle.ch:9735</code>.
  In Eclair, we select "Paste A Node URI" and insert the text we just copied.
1. The screen of our app should look something like this now:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-open-channel.png" width="400">
1. Now we will need to choose the amount of bitcoins we are going to "charge" our channel with.
  The maximum possible amount is 16'667'000 Satoshi (=0.16 BTC) per channel. But we most likely
  bought a much smaller amount and want to use all of it for our channel. This is possible,
  we just need to subtract a small amount of approx. 1000 Satoshi (=0.00001 BTC) for the channel
  funding transaction fee.<br/>
  So if we have, for example, 5'000'000 Satoshi available (according to the balance our wallet
  shows us), we are going to enter 4'999'000 as the "Channel capacity".
1. If the amount is accepted, the channel should now be opening:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-wait-for-channel.png" width="400"><br/>
  If the selected amount was too big, there will be an error message displayed and the channel
  might disappear from the channel list. Try again by choosing a smaller amount as the channel
  capacity.<br/>
  This step might appear to be unnecessarily complicated and in fact it is. It will most likely
  be abstracted away from the user and be handled automatically. There are a lot of people working
  on the usability and user experience of these apps, so we expect this to be much easier
  in the future.
1. After three confirmations the channel should be ready:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-channel-ready.png" width="400">
1. Everything is ready for "Lightning Network" payments now!<br/>
  All you need to do is go to the tab "Transaction History", tap the button on the bottom right
  and select "Scan A Payment Request":<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-pay-menu.png" width="400">
  <br/>Scan the QR code of something you want to pay with
  the Lightning Network and confirm the payment:<br/>
  
1. Ab sofort können nun "Lightning Network"-Zahlungen ausgeführt werden!<br/>
  Dazu wählt man im Tab "Transaction History" den Button unten rechts und dann im Menü
  den Punkt "Scan A Payment Request", wonach man dann den QR-Code, den man bezahlen möchte, scannen
  kann:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-pay-menu.png" width="400"><br/>
  Die App zeigt dann die Rechnung nochmals kurz an und kann dan bezahlt werden:<br/>
  <img class="shadow" src="../assets/img/lightning/mainnet-pay-invoice.png" width="400">

Hat die Zahlung geklappt? Ja? **Dann herzlichen Glückwunsch und willkommen in der Zukunft
des Bezahlens!**

# FAQ

* Warum eröffnen wir einen Channel mit der Puzzle-Node?
  * Der Vorteil am Lightning Network (und an Bitcoin generell) ist, dass jeder einfach mitmachen
    und auch seine eigene Node aufbauen kann. Weshalb soll ich mich dann zu Puzzle verbinden und
    nicht zu irgend einer anderen Node?<br/>
    Natürlich ist das jeder Person selbst überlassen. Wir von Puzzle ITC versprechen aber, dass
    wir die Gebühren unserer Channels tief halten und uns um eine gute Liquidität kümmern werden.
    Das heisst, wir wollen gut befüllte Channels zu allen Schweizer Verkäufern aufbauen, damit
    alle Benutzer unserer Node sehr gute und kurze Routen zu allen Geschäften haben, die am
    Lightning Network mitmachen.


* Kann ich auch Geld empfangen über das Lightning Network?
  * Im Protokoll ist das natürlich grundsätzlich möglich. Die Eclair-App unterstützt dies aber aus
    technischen und sicherheitsrelevanten Gründen noch nicht. Dies wird sich aber hoffentlich
    bald ändern.<br/>
    [Mehr dazu in den FAQ von Eclair (Englisch)](https://github.com/ACINQ/eclair-wallet/wiki/FAQ). 


* Was passiert, wenn ich das Guthaben meines Channels aufgebraucht habe?
  * Ist das Guthaben eines Channels aufgebraucht, dann kann darüber nicht mehr bezahlt werden.
    Es muss also ein neuer Channel eröffnet werden. Zukünftig, wenn man mit Eclair auch Geld
    empfangen kann, dann ist es möglich, dass man im bereits eröffneten Channel wieder Guthaben zurück
    erhält, das wieder ausgeben kann. Beispielsweise, indem man
    [einen Teil seines Lohns](https://www.inside-it.ch/articles/50118) über Lightning ausbezahlt kriegt,
    oder bei einer Finanzinstitution CHF direkt gegen Lightning-Guthaben tauscht.<br/>
    Somit müsste ein Channel theoretisch nie geschlossen werden.
 
 
* Was mache ich, wenn mein Channel immer "OFFLINE" oder sonst in einem fehlerhaften Zustand stecken bleibt?
  * Die Eclair-App hat noch einige Kinderkrankheiten, die hoffentlich mit Updates bald behoben werden.<br/>
    Oft hilft es aber, die App komplett zu beenden (über das Android-Menü) und neu zu starten.<br/>
    Manchmal hilft es auch, wenn man versucht einen neuen Channel zu eröffnen, dann werden die bestehenden
    Channels auch noch einmal neu geprüft.<br/>
    Evtl. helfen auch [die FAQ von Eclair (Englisch)](https://github.com/ACINQ/eclair-wallet/wiki/FAQ) weiter.


* Wann gibt es eine App für iOS?
  * Es gibt bereits eine [beachtliche Liste](http://lightningnetworkstores.com/wallets) an Wallets,
    die auf dem Testnet für iOS verfügbar sind. Wann das erste davon für Mainnet herausgegeben wird,
    ist schwierig zu sagen. Bis Ende 2018 sollte aber spätestens auch für iOS ein Wallet erhältlich sein,
    das keine eigene "Full-Node" benötigt.<br/>
    Traut man sich technisch etwas zu, kann man natürlich auf einem Server eine Lightning-Node aufsetzen
    und dann von seinem iOS-Gerät aus diese fernsteuern. Anleitungen gibt es z.B.
    [hier](https://www.lndthinwallet.com/) und
    [hier](https://gist.github.com/bretton/0b22a0503a9eba09df86a23f3d625c13).