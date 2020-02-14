---
title:  References
layout: page
---


As part of the hackathon, you'll learn how to cite texts, pages of the manuscript and images using URN notation.

We'll use the following URNs in our collaborative editions:


-   Collection of images: `urn:cite2:ecod:bern88imgs.v1:`
-   Pages of the manuscript: `urn:cite2:mid:bern88pages.v1:`
-   The text of the *Aratea*:  `urn:cts:latinLit:phi0881.phi003.bern88:`
-   The text of scholia:  `urn:cts:hcmidlatin:scholia.aratea.bern88:`


## Punctuation characters

We will allow periods, commas, high stops (raised dots), and question marks

-  .
-  ,
- ·
- ?



## A lexicon

[A nice electronic Lewis-Short lexicon](http://folio2.furman.edu/lewis-short/index.html), one of the main scholarly lexica of Latin (from Furman University).



## Using the `bash` shell in your terminal

Commands you'll need:

-  `cd`  ("**C**hange **D**irectory"): change your shell to a new folder
-   `pwd`   ("**P**rint **W**orking **D**irectorty"): show what folder your terminal is currently in


## Running test scripts

Make sure your terminal is in the right folder (use `pwd`)

Start the testing environment:  `sbt console`


## XML element names


Our editions allow the following TEI elements:


**Basic organizational structure**

`div`:  organize your sections in *div*isions.  Use the `@n` attribute to name it.

`p`:  within your `div`, organize your text in paragraphs

**Identifying what's legible**

`unclear`: if you're uncertain what the text says

`gap`:  if something is missing


**Identifying content that needs to be treated specially**


`num`:  numbers written numerically

`persName`:  proper names of persons

`placeName`:  proper names of places

If you have an abbreviation, you should identify it and how it should be expanded:

`abbr`:  abbreviation

`expan`:  full version (supplied by you)

Group these two together by wrapping them in a `choice` element.
