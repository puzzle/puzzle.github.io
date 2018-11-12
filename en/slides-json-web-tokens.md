![Puzzle ITC Logo](../assets/reveal.js-3.6.0/lib/img/puzzle_tagline_bg_rgb.svg)
<!-- .slide: class="master01" -->


<!-- section -->
### JSON web tokens
Oliver Gugger

[@gugol](https://twitter.com/gugol),<br/>
[github.com/guggero](https://github.com/guggero)

Part of the Lightning Network team at<br/>
Puzzle ITC, contributor to LND

<!-- .slide: class="master02" -->


<!-- section -->
### What is JWT?

* Open industry standard, RFC 7519
* Digitally signed peace of information
* Uses HMAC or RSA/ECDSA to sign
* Can also contain encrypted information

<!-- .slide: class="master03" -->

<!-- slide -->
### Why?

* Like a cookie but with a payload
* The issuer can trust its content because it is signed
* Can be used to store the session state
* JSified version of SAML

<!-- .slide: class="master05" -->

<!-- slide -->
### Advantages

* Offload session information (authentication, authorization) to the user
* No application session or database entry needed
* A way to share session state between servers, good for load balancing
* Issuer and verifier don't need to be the same application

<!-- .slide: class="master01" -->

<!-- slide -->
### Disadvantages

* Payload is "public". Can be decoded and read (but not modified).
* Invalidating (e.g. killing a session) is harder

<!-- .slide: class="master02" -->

<!-- slide -->
### Example

Demo: [jwt.io](https://jwt.io/#debugger)

<!-- .slide: class="master03" -->

<!-- slide -->
### Discussion

* Store in local/session storage or cookie?
* What information should be added?
* Further use cases?

<!-- .slide: class="master04" -->

<!-- slide -->
### Further reading

* HMAC
* Macaroons
* [Wikipedia: JWT Standard fields](https://en.wikipedia.org/wiki/JSON_Web_Token#Standard_fields)

<!-- .slide: class="master05" -->