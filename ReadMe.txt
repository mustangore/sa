== Encoding: ISO8859-1 ==

Lieber Anwender, liebe Anwenderin,

dies ist die IKS-Vorlage f�r Diplom-/Studien-/Bachelor- und 
Master-Arbeiten. Als Grundlage diente die hervorragende Vorlage
von Roland Bless. Der Text der originalen README-Datei ist
unten angef�gt.

Viel Erfolg bei der Verwendung w�nscht

Das IKS-Vorlagenteam

====================================================================
Hallo LaTeX-User!

Dies ist ein kleines Paket, welches ein Layout f�r wissenschaftliche
Arbeiten, z.B. Diplom-, Studienarbeiten oder Dissertationen, zur
Verf�gung stellt.  Das Paket ist f�r LaTeX2e gedacht (mehr zu LaTeX2e
siehe unten).  Die TeX-Sourcen enthalten derzeit Umlaute in 
UTF-8-Codierung, der Unterordner iso-8859-15 enth�lt noch die Version
f�r ISO 8859-15 (Latin1).
Der TeX-Source ist mit echten Umlauten besser lesbar, daher empfehle
ich Euch dringend, Umlaute zu verwenden (PC-Umlaute gibt's nat�rlich
auch --> schaut mal im "inputenc" Paket nach).  Ohne das InputEncoding
geht's vermutlich auch mit �lteren LaTeX2e-Versionen. Die
gew�hlten Einstellungen sollten bei Verwendung von pdflatex eine
vern�nftige PDF-Datei erzeugen.

Hauptbestandteil ist die Datei "wissdoc.cls", welche die notwendigen
Anpassungen vornimmt. "ausarbeitung.tex" ist die Hauptdatei, welche die
anderen Teile der Arbeit einbindet und durch "pdflatex ausarbeitung"
bzw. "latex ausarbeitung" �bersetzt werden muss (siehe Makefile). Die
Hauptdatei solltet Ihr Euren Bed�rfnissen entsprechend anpassen. Die
Titelseite ist nur ein Vorschlag und bindet zwei Logos ein.

Nochmals ein kurzer �berblick:

wissdoc.cls - Klassendefinition f�r Diplom-/Studienarbeiten
svnver.sty  - Package um subversion Versionsinformation einzublenden
ausarbeitung.tex - Hauptdatei, die weitere Teile einbindet
macros.tex  - einige mehr oder weniger n�tzliche Macros
              (mit \ignore{...} l�sst sich zum Beispiel etwas
               auskommentieren, mit \anm{...} kann man Anmerkungen
               einf�gen). Nicht unbedingt notwendig.
titelseite.tex    - Beispiel f�r eine Titelseite
erklaerung.tex    - Notwendige Erkl�rung f�r eine Diplomarbeit
einleitung.tex    - (Nahezu) leere Schablone
analyse.tex       - (Nahezu) leere Schablone
entwurf.tex       - (Nahezu) leere Schablone
implemen.tex      - (Nahezu) leere Schablone
eval.tex          - (Nahezu) leere Schablone
zusammenf.tex     - (Nahezu) leere Schablone
ausarbeitung.bib  - Beispiel f�r eine BiBTeX-Datei (Literaturdatenbank)
ausarbeitung.ist  - F�r Makeindex notwendig, siehe Makefile
Makefile          - Beispiel-Makefile, welches Aufrufe zeigt.
                    Funktioniert aber bei weitem nicht perfekt, wenn �berhaupt...
itmalpha.bst      - BibTeX Style File f�r Literaturangaben mit 4 Buchstaben
                    (muss noch auf neueren geralpha.bst angepasst werden...)
itmabbrv.bst      - BibTeX Style File f�r Literaturangaben mit 4 Buchstaben
                    (gek�rzte Vornamen im Literaturverzeichnis)
logos/            - Verzeichnis, das Logos enth�lt
images/           - leeres Verzeichnis, in das die Bilder kommen
                    (f�r die PDF-Datei m�ssen aus den .eps- .pdf-Dateien
                     erzeugt werden [funktioniert mit gs6.50 ganz gut, 
                     s. scripts/generatePDFfromEPS], zum
                     Einbinden der Bilder kann die Endung .pdf
                     weggelassen werden)
scripts/          - Mehr oder weniger n�tzliche Skripte, vor allem ps2eps,
                    um Postscript-Dateien als Grafiken in TeX einzubinden.


Bitte beachten:
===============
Zur Erzeugung einer PDF-Datei mit pdflatex m�ssen u.U. vorher die
.aux-Dateien vollst�ndig gel�scht werden (s. Makefile), ansonsten kann
es zu Fehlermeldungen kommen (die sollten aber nach vorherigem "make
clean" verschwinden). Die verwendeten Fonts m�ssen als
Postscript-Type-1-Font zur Verf�gung stehen, ansonsten sieht die
Ausgabe auf dem Bildschirm sehr schlecht aus (das kommt durch
Verwendung von Postscript-Type-3-Fonts, Drucken ist aber trotzdem ok).
Daher wird als Zeichensatz "ae" (almost european) verwendet, der auf
den cm-Fonts aufbaut, die als Type-1 vorliegen. N�heres dazu in der
TeX-FAQ auf http://www.dante.de/.  Die Bilder m�ssen f�r pdflatex als
PDF (empfohlen), PNG oder JPG vorliegen.  Zur Wandlung kann das
beigelegte Script generatePDFfromEPS bzw. "epstopdf" verwendet werden,
welches ghostscript (gs) dazu einsetzt. Erst ab gs 6.50 funktioniert
die Fontbehandlung ausreichend gut, so dass auch in den Bildern keine
Type-3-Fonts mehr kodiert werden (falls nicht unbedingt notwendig) und
damit die Bilder auch am Bildschirm in hoher Qualit�t wiedergegeben
werden.

F�r die Perfektionisten sei noch auf die Tools "thumbpdf" und
"rmligs" verwiesen.

Gru�,
 Roland

P.S.:
 Literatur zu LaTeX2e:
 1. Leslie Lamport: "Das LaTeX-Handbuch", Addison-Wesley
 2. Goosens, Mittelbach, Samarin: "Der LaTeX-Begleiter"
 Referenz und Grundbefehle sind in 1. zu finden, 2. erkl�rt
 Zusatz-Pakete, die einem Dokument ein individuelleres Aussehen verleihen
 koennen.

P.P.S.:
Die Vorlage darf gerne weiterverwendet und abgewandelt werden, 
d.h. ihr k�nnt einfach Titelseite Logos etc. nach Belieben anpassen.

