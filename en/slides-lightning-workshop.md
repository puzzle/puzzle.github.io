![Puzzle ITC Logo](../assets/reveal.js-3.6.0/lib/img/puzzle_tagline_bg_rgb.svg)
<!-- .slide: class="master01" -->


<!-- section -->
### Workshop: The Lightning Network
Oliver Gugger

[@gugol](https://twitter.com/gugol),<br/>
[github.com/guggero](https://github.com/guggero)

Part of the Lightning Network team at<br/>
Puzzle ITC, contributor to LND

<!-- .slide: class="master02" -->


<!-- slide -->
Puzzle ITC GmbH: Open Source software company in Berne, Switzerland.

* Involved in Lightning Network since Oct. 2017
* Team of 5 people working on Bitcoin/Lightning
* Part of salary in Bitcoin since Aug. 2018
* Showcase project with Energy Kitchen in Sep. 2018
* Lightning enabled Beer Tap in Oct. 2018

<!-- .slide: class="master03" -->

<!-- section -->
### Workshop: The Lightning Network

Notes at:

[beta.etherpad.org/p/lightning-workshop](https://beta.etherpad.org/p/lightning-workshop)

Slides at:

[puzzle.github.io](https://puzzle.github.io)

<!-- .slide: class="master04" -->


<!-- section -->
### The current state of Bitcoin (2018-11-12)
 - SegWit is enabled and scaling
   ![SegWit transactions percentage](../assets/img/slides-lightning-workshop/segwit-tx-percentage.png)
   <small>from: http://charts.woobull.com/bitcoin-segwit-adoption</small>
<!-- .slide: class="master03" -->


<!-- slide -->
### The current state of Bitcoin (2018-11-12)
 - Mempool is pretty empty, fees low
   ![Mempool transaction count](../assets/img/slides-lightning-workshop/mempool-tx-count.png)
   <!-- .element width="85%" -->
   <small>from: https://jochen-hoenicke.de/queue</small>
<!-- .slide: class="master04" -->


<!-- section -->
### Problem?
 - When demand is high, the fees fluctuate even more than price <br/>
   ![SegWit transactions percentage](../assets/img/slides-lightning-workshop/mempool-tx-fees-december-17.png)
   <!-- .element width="75%" -->
   <small>from: https://jochen-hoenicke.de/queue</small>
<!-- .slide: class="master03" -->


<!-- slide -->
### Problem?
 - Even with SegWit the block size is limited (1'000 vkB, 4'000 kWU)
 - Average transactions per block went up as far as 2'723 (~4.5 tx/s)
 - How do we get to Visa which can process up to 24'000 tx/s at peak?
<!-- .slide: class="master04" -->



<!-- section -->
### Solution?

## Bigger blocks!
Sure, because downloading 5.3 GB every 10 minutes is no problem!
<!-- .slide: class="master03" -->


<!-- slide -->
### Better solution
 - Scale off-chain
 - Add a layer 2
 - For example: The Lightning Network
<!-- .slide: class="master04" -->



<!-- section -->
### The Lightning Network
 - Smart Contracts create Payment Channels
 - Funding transaction is in blockchain
 - Payment Channel updates happen at "speed of light"
<!-- .slide: class="master03" -->


<!-- slide -->
### The Lightning Network
 - Payments can be routed through multiple hops/channels, creating a network
 - Protected by onion routing/multi layer encryption
 - No trust required, cheating made impossible by cryptography
<!-- .slide: class="master04" -->


<!-- slide -->
### The Lightning Network
 - Layer 2 on top of Bitcoin
 - Routing payments like TCP/IP

![network](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/17_node_mesh_network.png/300px-17_node_mesh_network.png)

 - Visualisation: [puzzle.github.io/beadnet/](https://puzzle.github.io/beadnet/)
<!-- .slide: class="master05" -->


<!-- slide -->
### Workshop: Task 1
 - Install any Lightning Network wallet for Bitcoin testnet as
   described on [https://gugger.guru/lightning-workshop/](https://gugger.guru/lightning-workshop/)
 - Send yourself some testnet Bitcoin
 - Wait for the balance to be confirmed (usually 3 confirmations)
<!-- .slide: class="master01" -->



<!-- section -->
### How it works
Technologies used:
 - Multisignatures
 - Timelocks
   - CheckLockTimeVerify (absolute)
   - CheckSequenceVerify (relative)
 - Hashlocks
<!-- .slide: class="master01" -->


<!-- slide -->
### How it works
![Funding Transaction](../assets/img/slides-lightning-workshop/lightning-channels-01-funding-tx.png)
<small>from: https://www.youtube.com/watch?v=7tHD9Gj9UNg</small>
<!-- .slide: class="master02" -->


<!-- slide -->
### How it works
![Bi-Directional Channels](../assets/img/slides-lightning-workshop/lightning-channels-02-bi-directional.png)
<small>from: https://www.youtube.com/watch?v=7tHD9Gj9UNg</small>
<!-- .slide: class="master03" -->


<!-- slide -->
### How it works
![Second update](../assets/img/slides-lightning-workshop/lightning-channels-03-second-update.png)
<small>from: https://www.youtube.com/watch?v=7tHD9Gj9UNg</small>
<!-- .slide: class="master04" -->


<!-- slide -->
### How it works
![Closing a channel](../assets/img/slides-lightning-workshop/lightning-channels-04-channel-closing.png)
<small>from: https://www.youtube.com/watch?v=7tHD9Gj9UNg</small>
<!-- .slide: class="master05" -->


<!-- slide -->
### How it works
![Multi hop](../assets/img/slides-lightning-workshop/lightning-channels-05-multi-hop.png)
<!-- .element: width="75%" -->
![Multi hop tx](../assets/img/slides-lightning-workshop/lightning-channels-06-multi-hop-tx.png)
<!-- .element: width="49%" -->
![Multi hop tx](../assets/img/slides-lightning-workshop/lightning-channels-07-multi-hop-tx2.png)
<!-- .element: width="49%" -->
<small>from: https://www.youtube.com/watch?v=k-bXIZOMNyA</small>
<!-- .slide: class="master01" -->


<!-- slide -->
### Workshop: Task 2
 - Open a channel to [lightning-test.puzzle.ch](https://lightning-test.puzzle.ch)
 - Wait for the funding transaction to be confirmed (usually 3 confirmations)
<!-- .slide: class="master03" -->



<!-- section -->
### When will it be ready?
![mainnet on 2018-01-30](../assets/img/slides-lightning-workshop/lightning-channels-08-mainnet.png)
<small>from: https://lnmainnet.gaben.win/</small>
<!-- .slide: class="master04" -->


<!-- slide -->
### How will we use it?
![single-funded channel](../assets/img/slides-lightning-workshop/lightning-channels-09-single-funded-channel.png)
<!-- .slide: class="master05" -->


<!-- slide -->
### How will we use it?
![dual-funded channel](../assets/img/slides-lightning-workshop/lightning-channels-10-dual-funded-channel.png)
<!-- .slide: class="master01" -->


<!-- slide -->
### Workshop: Task 3
Discussion: <br/>assume Puzzle ITC has a Lightning Network Hub and channels with merchants:
 - What considerations would you make when choosing a Hub?
 - How big of a channel would you want to open?
 - How big would the channels to the merchants need to be?
<!-- .slide: class="master02" -->
