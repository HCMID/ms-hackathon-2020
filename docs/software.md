---
layout: page
title: Software for editing manuscripts
---

## Summary

1.  the bash shell (a terminal) to run commands
2.  [atom](https://atom.io) (text editor)
4.  docker, to ru software packages (docker containers) on different host operating systems


## Details: terminal

Windows users can run a windows terminal console.

Mac OS X users can use the `Terminal` app (in `Applications/Utilities`).


## Details:  Atom for text editing

In today's workshop, we will edit tables of data in delimited text files, and diplomatic editions of texts marked up in XML.  The plugin architecture of the [Atom editor](https://atom.io/) provides excellent support for all of these.

Download and install atom from <https://atom.io/>. If you are using Mac OS X, open atom and choose from the Atom menu, "Install Shell Commands".  (This step should not be necessary on Windows or Linux operating systems.)


### Configuring Atom for scholarly work on manuscripts


Installing atom should have installed the command-line atom package manager `apm`.   Copy and paste the the following commands into a terminal to install all of these packages:

    apm install intentions
    apm install busy-signal
    apm install linter
    apm install linter-ui-default
    apm install linter-autocomplete-jing
    apm install atom-xsltransform
    apm install xml-formatter
    apm install https://github.com/mfripp/atom-tablr.git
    apm install rainbow-csv



Download the file [atom-tablr-conf.cson](http://hcmid.github.io/tech/atom-tablr-conf.cson), and copy it to atom's default location for config files. You can do that with the `cp` command in your terminal.

    cp atom-tablr-conf.cson $HOME/.atom/config.cson


(Gotcha: if your browser renames your file for you  when you download -- e.g., if it calls it `atom-tablr-conf.txt` -- it, you'll have to use the name it chose instead of `atom-tablr-conf.cson`.)


Finally,

1. add the [linter-autocomplete-jing](https://github.com/aerhard/linter-autocomplete-jing) plugin
2. install [this package](https://github.com/neelsmith/atomic-tei) for automatic validation of documents following the Text Encoding Initiative (TEI) schema



## Details:  Running scripts

To test and validate our editions, we use scripts written in Scala, a language that runs on the Java Virtual Machine.  `sbt` is a build system that will find the appropriate version of Scala and any other code libraries your scripts need, and automatically download them, so if you install Java and sbt, everything you need to run MID scripts is taken care of for you.

-  from [this confusing page](http://www.oracle.com/technetwork/java/javase/downloads/index.html), find the link to the most recent **JDK** (the Java Development Kit), download it, and install it
- download and install the "simple build tool," `sbt`:  <https://www.scala-sbt.org/>
