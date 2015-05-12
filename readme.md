# Diffie-Hellman-Merkle key exchange demo

The Diffie Hellman Merkle (DH) key exchange is a critical component of establishing a Transport Layer Security (TLS) connection. At the conclusion of a DH key exchange, two parties will have agreed upon a symmetric key to use for encrypting and decrypting data.

The key exchange concept is important to understand when implementing TLS. This repository contains materials that are actively being developed for demoing the DH key exchange in the context of an in-person talk or workshop. The goal of the demo is to show that it is possible to securely agree on a key while communicating details over an insecure channel while avoiding distracting the audience with confusing equations and algorithms. This demo is intended for a web developer audience, which will include individuals with varying backgrounds in mathematics and computer science.

Materials and instructions in this repository will explain an effective demo for teaching the DH key exchange.

## Demo

To begin the demo, ask for two volunteers to participate in the activity. Assign one participant to be "Alice" and other to be "Bob".

Give Alice the "Alice" handout, a clipboard, and a marker. Similarly, give Bob the "Bob" handout, a clipboard, and a marker.

Annouce the value of *g* and *p* used in the [key-exchange-math.md](https://github.com/tollmanz/diffie-hellman-key-exchange-demo/blob/master/raw/key-exchange-math.md) document. Emphasize that Alice, Bob, the presenter, and all of the audience are aware of these numbers. These are public values that are purposefully available to the two parties as well as "any persons in the middle". It is important to note to the audience that they are all persons in the middle of the exchange.

Instruct Alice and Bob to complete step 1 and 2 in their respective handouts. Inform the audience that Alice and Bob are selecting a secret number that they will not reveal.

Ask Alice to complete step 3. She will announce to the audience the value of *A*. Be sure to emphasize to the audience that everyone in the room has access to this number. Instruct Bob to write down this number.

Ask Bob to complete step 3. He will announce to the audience the value of *B*. Be sure to emphasize to the audience that everyone in the room has access to this number. Instruct Alice to write down this number.

Now that *A* and *B* are public, instruct Alice and Bob to both complete step 6. Be sure to make sure they are circling the correct columns in order to make sure the key exchange works.

Instruct Alice and Bob to complete step 7, being careful to not reveal the number that they are writing. Encourage them the write the number in legible, large handwriting. Ask Alice and Bob to show their number to each other without showing the audience (and the presenter if possible). Ask them, "Are the numbers the same?" If they say yes, they have successfully agreed on a key via the DH key exchange mechanism. If they say no, make up something about packets being dropped, data being tampered with, or buggy software.

Ask the audience if they know the number that they agreed upon. If anyone attempts a guess, be sure to inquire about why they made that guess. Depending on their responses, you may have an opportunity to discuss different attack vectors or cryptanalysis methods.

Have Alice and Bob reveal their keys to the audience to show that the key exchange was successful.

Emphasize once again that 4 values were made public during the demo, while 2 values and a key remained secret. This shows that it is possible to agree on encryption keys over an insecure channel.

## Using the demo

The demo is intended to emphasize the *concepts behind key exchange* and not real world math that is used in TLS based key exchanges. Diving too deep into the math runs the risk of loosing an otherwise engaged audience. The power of the demo is to eloquently demonstrate a key exchange. 

This demo can be used to explain important TLS concepts that can otherwise be difficult to describe. For instance, after completing the demo, you can show that changing *a*, *b*, *p*, or *g* will result in the generation of different encryption keys. This information can be the basis for describing the concept of perfect forward secrecy.

This repository also includes cheat sheets for the math used in the demo. These cheats sheets are helpful for discussing the concept of "one-way functions" that power the key exchange. The included Soulver document is helpful as it is a calculator tool that supports variables allowing the presenter to easily show the effects of changing any of the variables in the equation. This effect can be achieved with other similar pieces of software. Showing this document is considered optional. The demo stands on its own and discussion of the math can be helpful for solidifying concepts depending on the audience and the amount of time given for the presentation.

## Materials

DH key exchanges are based on math. Doing a demo that requires an audience member to agree to get up in front of a crowd and do math is bound to fail. The purpose of the included materials is to allow for the math to be completed ahead of time and only require the participants to circle some numbers in a grid. What the participants don't know is that they are reaping the benefits of solved math equations.

Materials in this repo are based on *g* = 5 and *p* = 23.

*Material list*:

* alice-handout / bob-handout - Handout that Alice/Bob work through to arrive at a shared key. The handouts walk the participants through picking a private value, generating public values, and incorporating other public values to arrive at a shared key. This repo provides a Markdown, Pages.app, and PDF versions of the handouts.
* key-exchange-math - This document shows the mathematic equations that go into the key exchange demo. The Markdown file is a raw version and the Soulver file is a dynamic version.


## Contribution

Contributions are highly encouraged. In particular, I am interested in help with:

* Review of concepts for accuracy
* Accessible example based on elliptic curve mathematics
* Generator app to create handouts based on specific *g* and *p* values

## License

The MIT License (MIT)

Copyright (c) [2015] [Zack Tollman]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
