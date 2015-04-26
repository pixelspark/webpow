# WebPoW

Prevent form spam using in-browser proof-of-work (PoW)

[Try WebPoW here](http://pixelspark.github.io/webpow/pow.html)

WebPoW page is a proof of concept of using Web Workers to calculate a so-called 'proof of work'. A proof of work is a solution to a mathematical problem that can only be solved using trial-and-error; showing that you have found the solution is proof that you have performed a certain amount of computation (in reality, sometimes you 'get lucky' and find a solution fast, and sometimes it takes much longer; the average amount of work required however can be decided upon in advance).

Proofs of work can be used to prevent spam (e.g. on form submissions, e-mails, et cetera). Traditional CAPTCHAs prevent spam by exploiting the fact that computers cannot solve a particular problem easily, and that humans that can solve them are scarce/expensive/slow (but available in the regular use case). Proof of work, by contrast, exploits the fact that computational resources are scarce. While non-spamming users will typically have the resources to perform the computation once in reasonable time, spammers will have difficulty finding the resources to compute many proofs of work required to submit their spam. By requiring a 'proof of work' from the client before accepting any data, spammers are thus effectively blocked.

Using Web Workers, the proof of work computation can be performed in standard browsers in the background, while efficiently utilizing available computing power. This demo will attempt to spawn four worker threads (most browsers seem to be able to saturate four cores with this).

Use cases include:
* Prevention of automated form spam (require a PoW on submit)
* Prevention of website crawling (require an increasingly difficult PoW on each new request)

## Contact
- Tommy van der Vorst
- Twitter: [@tommyvdv](http://twitter.com/tommyvdv)
- Web: [http://pixelspark.nl](http://pixelspark.nl)

## License

Copyright (c) 2014-2015 Tommy van der Vorst

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

This repository includes SHA-256 implementation in JavaScript (c) Chris Veness 2002-2014