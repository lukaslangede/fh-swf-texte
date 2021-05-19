---
export_on_save:
  #html: true
  #pandoc: true
  #pdf_document: true

#args "--standalone, -V lang=de-DE -V papersize=a4paper, -V geometry:margin=3cm, -V lang=de-DE, -V fontsize=12pt, -V breakurl, -V hyphens=URL, -V colorlinks, "
output:
  pdf_document:
    latex_engine: lualatex


title: Intune als Ablösung zu GPOs
author:
  - Lukas Lange
  - Im Leuchensang 64
  - 54634 Bitburg

mail: lukas@lukaslange.de
date: \today

Pandoc:
  Filter:
    - pandoc-crossref
    - pandoc-citeproc
  pandoc_args: [ -V hyphens=URL,]

link-citations: true
color-links: true
breakurl: true


fontsize: 12pt
geometry:
  - top=25mm
  - bottom=20mm
  - left=30mm
  - right=20mm
linestretch: 1.5
lang: de-DE
numbersections: true
papersize: A4

#bibliography: Projektarbeit1.bib
csl: fachhochschule-suedwestfalen.csl

toc-title: Inhaltsverzeichnis
lofTitle : Abbildungsverzeichnis
lotTitle: Tabellenverzeichnis
figureTitle: Abbildung
tableTitle: Tabelle
---

\pagenumbering{gobble}
\pagebreak
\pagenumbering{Roman}
\tableofcontents
\pagebreak

\addcontentsline{toc}{section}{\listfigurename}
\listoffigures

\addcontentsline{toc}{section}{\listtablename}
\listoftables


# Abkürzungsverzeichnis {.unnumbered}

AD
: Active Directory

VPN
: Virtual Private Network

\pagebreak
\pagenumbering{arabic}

<!--

Editor: Atom.io
Packages für Atom:
- language-markdown
- markdown-preview-enhanced
- markdown-writer
- tool-bar-markdown-writer
- atom-latex

Converter: pandoc.org
Einstellungen in markdown-preview-enhanced:
- use pandoc parser
- pandoc arguments: --css="C:\Users\lukas.lange\.atom\packages\markdown-preview-enhanced\node_modules\@shd101wyy\mume\styles\preview_theme\github-light.css", --standalone

http://www.weinelt.de/latex/
https://pandoc.org/MANUAL.html#citations

## Beispiele
### Tabellen
Table labels

a   b   c
--- --- ---
1   2   3
4   5   6

: Tabelle des ABCs {#tbl:TabelleABC}

### Bilder
![Bildbeispiel[^eigene-darstellung]](Bilder\001_mac.png)

![Bild von einem Himmel](DATEI.xxx){#fig:Himmel}

Verweis auf eine Abbildung (s. [@fig:Himmel])

### Fußnoten
[^meine]

[^deine]

### Linksammlung
 Linksammlung
[wikipedia-galaxie]: https://en.wikipedia.org/wiki/Galaxy#/media/File:NGC_4414_(NASA-med).jpg

Verweis auf Link

<!-- Fußnoten
[^eigene-darstellung]: Eigene Darstellung
[^wikipedia-galaxie]: [Wikipedia.org][wikipedia-galaxie]
[^meine]: Fußnote 1
[^deine]: Fußnote 2
-->

____


# Überschrift 1

## Unterüberschrift 1

# Überschrift 2

Hier zitiere ich mit Fußnote [Vgl. @dausch2013, S. 17f.].

Hier erstelle ich eine manuelle Fußnote [^Fußnotenname]

[^Fußnotenname]: Diese Fußnote kann überall im Text definiert werden


![Bild der FH-SWF](https://www.fh-swf.de/media/_tech__fhswf/layout__fhswf/images__fhswf/Logo.png){#fig:logo_fh-swf}


Spalte1 | Spalte2
--------|--------
Zeile1  | Zeile 1
Zeile2  | Zeile 2

: Tabellenname {#tbl:tabellenlabel}

**Quelle**: Eigene Darstellung


\pagebreak

# Eidesstattliche Erklärung {.unnumbered}
Hiermit versichere ich an Eides statt, dass ich die vorliegende Hausarbeit

"Intune als Alternative zu GPOs"

selbstständig und ohne Inanspruchnahme fremder Hilfe angefertigt habe. Alle von anderen Autoren wörtlich übernommenen Stellen wie auch die sich an die Gedankengänge anderer Autoren
eng anlehnenden Ausführungen meiner Arbeit habe ich besonders gekennzeichnet und die
Quellen zitiert.
Die Arbeit habe ich in dieser oder ähnlicher Form oder auszugsweise im Rahmen einer anderen
Prüfung noch keiner anderen Prüfungsbehörde vorgelegt.
Mir ist bekannt, dass diese Arbeit auch auf elektronischem Wege auf Einhaltung wissenschaftlicher Standards überprüft wird und im Falle eines Plagiats als Täuschungsversuch qualifiziert
werden kann.

**Ort**, den \today


# Literaturverzeichnis {.unnumbered}

\footnotesize
