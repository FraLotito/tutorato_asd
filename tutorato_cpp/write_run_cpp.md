# Scrivere e compilare file C++

Le lezioni di laboratorio comprendono lo svolgimento di alcuni esercizi di programmazione in C++.

## Compiler
In generale, il consiglio è di compilare ed eseguire il vostro codice in un terminale, pertanto se già non lo avete a disposizione, dovete installare il compilatore g++. 

**[Tutti gli OS]**

Installare un compilatore: [installing a compiler](https://www.cs.odu.edu/~zeil/cs250PreTest/latest/Public/installingACompiler/)

**[(GNU/)Linux]**

Tutte le distribuzioni linux hanno dei pacchetti che forniscono il compilatore GNU (gcc per il C, g++ per il C++), ecco due riferimenti:

[APT-based] (Ubuntu, Debian): [guida](https://www.cyberciti.biz/faq/howto-installing-gnu-c-compiler-development-environment-on-ubuntu/)
[YUM-based] (Fedora, Centos, RHEL): [guida](https://www.cyberciti.biz/faq/centos-rhel-7-redhat-linux-install-gcc-compiler-development-tools/)

**[Windows]**

Guida generale all’installazione di un compilatore e di un editor: [guida](http://stephencoakley.com/2015/01/21/guide-setting-up-a-simple-c-development-environment-on-windows)

**[Mac]**

Installare g++: [guida](http://www.edparrish.net/common/macgpp.php#installg++)


## Editor

Per scrivere il codice sorgente potete scegliere tra decine di editor, salvando il file con estensione *.cpp*:
* [VSCode](https://code.visualstudio.com/)
* [Sublime](https://www.sublimetext.com/)
* [Atom](https://atom.io/)
* Old school: Vim, Emacs, Blocco note

![Editor war](https://imgs.xkcd.com/comics/real_programmers.png)

## IDE
Se preferite avere un ambiente integrato di sviluppo in cui potete scrivere e compilare codice, senza andare a compilare da linea di comando, consigliamo [CodeBlock](http://www.codeblocks.org/). Per creare un nuovo file selezionate dal menù "File" la voce "New" e quindi "Empty file". Quando lo salvate ricordate di scrivere "nomefile.cpp", perchè stiamo programmando in C++. Da lì poi potrete facilmente lanciare il programma con la freccetta verde di "Run". CodeBlocks vi mette anche a disposizione una serie di strumenti per il debug e per il version control.

