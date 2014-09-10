sources:
* http://www.sitepoint.com/do-you-really-need-jquery/
* http://www.sitepoint.com/jquery-vs-raw-javascript-1-dom-forms/
* http://www.sitepoint.com/jquery-vs-raw-javascript-2-css3-animation/
* http://www.sitepoint.com/jquery-vs-raw-javascript-3-events-ajax/

* http://youmightnotneedjquery.com/

write jsperf.com tests

Introduction
============

I'm Craig Buckler. Find me at most places using that name - it's fairly unique; Twitter, Github, LinkedIn etc.


Do you really need jQuery
=========================

How many of you have used jQuery?

How many use it in every project?

Purpose of this presentation: get you to question whether you really need jQuery in that next project. Or indeed any general-purpose library.

Trendy to bash jQuery
I love jQuery - show jQuery video image and link


Why jQuery has been so successful?
----------------------------------

Ask question: what percentage of sites is jQuery used?

* Top 10K sites: 77.8% use jQuery
* Top 100K: 67.2%
* Top 1 million: 58.9%

SOURCE: http://trends.builtwith.com/javascript/jQuery

* browsers are buggy and too inconsistent
* JavaScript is too hard, too strange
* jQuery is like a high-level language, JavaScript is like assembly
* job adverts ask for jQuery rather than JavaScript

Venn diagram (SVG):
browsers, DOM models, APIs, event model, CSS support, box models
debugging was hard (ie-error.png)

In 2007, smartphones arrived

jQuery in middle

jQuery's only 30Kb so why should we even worry?

Situation in 2014
-----------------

* Top 5 browsers closer than they've ever been
* vendors have adopted standards
* vendors have copied jQuery
* IE6/7 dead (cheer!)
* IE8 usage is around 1 in 20 (unless you're unlucky)
* jQuery 2 has dropped IE6/7/8 support
* write less, do more - perhaps a few years ago, but not necessarily now


JavaScript is cool
Naked JavaScript makes you even cooler
But there are misconceptions...

Are we using jQuery as a crutch or out of habit rather than because it's necessary?


Selectors
---------

var s = $(".myclass");

alternative:
document.querySelectorAll(".myclass");

can use it in IE8+ -- but not CSS2.1 selectors. jQuery uses it. Adds some extra selectors, but you'll rarely venture outside of them.

document.querySelector(".myclass"); - first
document.getElementById(".myclass");

document.getElementsByClassName(".myclass");
document.getElementsByTagName(".myclass");
live collection - can also be applied to other nodes (not just document)


DOM manipulation
----------------
innerHTML
textContent

Style manipulation
------------------
classList
changing classes


Animation
---------
Forget jQuery. Forget native JavaScript. CSS3 wins

There are exceptions, but they're just that - exceptions. The standard bouncing, fading, scrolling effects will almost certainly be quicker in CSS3.


Chaining inefficiency
---------------------
multiple loops
each


Events
------

Ajax
----





Reasons to retain jQuery
------------------------
* legacy applications - no point ripping it out unless it's causing performance issues
* complex projects using a significant proportion of jQuery functionality
* projects with large teams with varying client-side skills. jQuery can help them be more productive - easy to understand and well documented.
* projects requiring IE6/7 support (jQuery 1)
* stupidly short deadlines - client wants something quick and cheap rather than good (don't work for those clients!)



Alternative minimalistic API equivalents
----------------------------------------

http://tutorialzine.com/2012/04/5-lightweight-jquery-alternatives/

Modular build of jQuery
Zepto.js - 8Kb
$dom - 2Kb
minified.js
https://github.com/remy/min.js - 600 bytes, selector and events
