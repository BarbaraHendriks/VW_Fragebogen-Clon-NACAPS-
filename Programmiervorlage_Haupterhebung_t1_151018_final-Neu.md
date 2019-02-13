\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________index_________________________________________\_
-------------------------------------------------------------------------------------------

tc: (alle)

vn: aict01

qt: Mehrfachauswahl

hl:

in:

q:

!!Herzlich Willkommen zur ersten Onlinebefragung der Begleitforschung "Wissenschaft und berufliche Praxis in der Graduiertenausbildung"!!!

In Abhängigkeit von Ihrer persönlichen Lebenssituation wird die Befragung etwa 25 bis 35 Minuten dauern. Sie können die Befragung auch am Smartphone ausfüllen, allerdings ist die Beantwortung an einem größeren Bildschirm bequemer und schneller. Sie haben jederzeit die Möglichkeit, die Befragung zu unterbrechen und zu einem späteren Zeitpunkt fortzuführen.

Für Ihre Teilnahme danken wir Ihnen bereits an dieser Stelle ganz herzlich!

Barbara Hendriks und Prof. Dr. Stefan Hornbostel

!!Hinweise zum Datenschutz!!

Ihre Teilnahme ist selbstverständlich freiwillig. Ihre Angaben werden für Forschungs- und Evaluationszwecke genutzt. Sämtliche Nacaps-Daten werden nur in anonymisierter Form publiziert und anderen Wissenschaftler(inne)n nur anonymisiert zur Verfügung gestellt. Ihre Kontaktdaten werden stets getrennt von den Befragungsdaten verarbeitet und gespeichert. Keinesfalls werden Ihre Kontaktdaten an Dritte weitergegeben.

ao: 1 : : Ich habe die in der Einladungsemail als PDF angehängten Datenschutzbestimmungen gelesen und bin damit einverstanden.

!!Kontakt!!

Bei !!Fragen zum Datenschutz!! wenden Sie sich bitte an den Datenschutzbeauftragten des DZHW, Herrn Martin Fuchs: Tel.: +49 511 450 670 491; E-Mail: \#\#URL:datenschutz\@dzhw.eu\#\#. Weitere Informationen zum Datenschutz am DZHW finden Sie \#\#URL:[hier](https://www.dzhw.eu/gmbh/datenschutz)\#\#.

Auch bei allen !!anderen Fragen und Anmerkungen!! stehen wir Ihnen gerne zur Verfügung:

Frau Barbara Hendriks erreichen Sie per Email unter (mailto:hendriks@dzhw.eu). 

mv:

ka:

vc: SHOW fv IF aict01 = FALSE

av:

kh:

fv: (flag_index): Bitte beachten Sie, dass ohne Zustimmung zu den
Datenschutzbestimmungen eine Teilnahme an der Onlinebefragung leider nicht möglich ist.

hv:

fo:

tr:

GOTO index2 IF aict01 = TRUE AND (preload01 = 10 OR preload01 = 11 OR preload01 = 13 OR preload01 = 15 OR preload01 = 24)

GOTO A01 IF aict01 = TRUE

GOTO cancel1 IF aict01 = FALSE AND flag_index = TRUE

hi: Hinweistext (fv) bitte in rot

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________A01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adbi01

qt: Einfachauswahl mit vertikalen ao

hl: Die Befragung ist in sechs thematische Blöcke gegliedert, die durch die Buchstaben A bis F gekennzeichnet werden.

q: Anfang Dezember 2018 waren Sie an Ihrer Hochschule offiziell als Doktorand(in) registriert. In der Zwischenzeit
kann sich daran etwas geändert haben.

Bitte geben Sie an, was aktuell auf Sie zutrifft.

is: Ihr Promotionsverfahren gilt als abgeschlossen, wenn Sie die letzte Prüfung
(in der Regel: Disputation) erfolgreich abgelegt haben.

it:

ao1: 1 : : Ich promoviere.

ao2: 2 : : Ich habe das Promotionsverfahren abgeschlossen.

ao3: 3 : : Ich habe mein Promotionsvorhaben unterbrochen.

ao4: 4 : : Ich habe mein Promotionsvorhaben abgebrochen.

mv:

ka:

vc:

av:

kh:

fv: (flag_A01): Für den weiteren Verlauf der Befragung ist diese Frage wichtig.
Ohne eine Angabe würden Sie Fragen erhalten, die nicht auf Ihre Situation
zutreffen. Beantworten Sie deshalb bitte diese Frage, um fortfahren zu können.
(IF adbi01 = SYSMISS)

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A02 IF adbi01 = 3

GOTO A03 IF adbi01 = 4

GOTO A05 IF adbi01 = 1

GOTO A06 IF adbi01 = 2

GOTO cancel2 IF adbi01 = SYSMISS AND flag_A01 = TRUE

hi: Bitte hier Icon 1 für Modul A einfügen (oben rechts) und durchgängig
einblenden bis das Modul B beginnt.

Hinweistext (fv) bitte in rot

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 3

(wenn A01 „Promotionsstatus“= 3 „unterbrochen“)

vn: adid01

qt: offene Frage (string)

hl:

in:

q: Aus welchen Gründen haben Sie das Promotionsvorhaben unterbrochen?

is:

it:

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO A04

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 4

(wenn A01 „Promotionsstatus“= 4 „abgebrochen“)

vn: adid02

qt: offene Frage (string)

hl:

in:

q: Aus welchen Gründen haben Sie das Promotionsvorhaben abgebrochen?

is:

it:

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO A06

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 3

(wenn A01 „Promotionsstatus“ = 3 „unterbrochen“)

vn: adid03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Handelt es sich um eine offiziell der Hochschule gemeldete Unterbrechung?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A05

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 „Promotionsstatus“ = 1 „promoviere“)

vn:
adtc01(adtc01a/adtc01b/adtc01c/adtc01d/adtc01e/adtc01f/adtc01g/adtc01h/adtc01i), q01a/q01b

qt: Matrix mit horizontaler Einfachauswahl 

hl:

in:

q: Warum haben Sie die Promotion begonnen?

is:

it1: (adtc01a): Weil mich die Fragestellung interessiert

it2: (adtc01b): Weil ich zum wissenschaftlichen Fortschritt beitragen möchte

it3: (adtc01c): Weil es in meinem Fach üblich ist

it4: (adtc01d): Weil mein persönliches Umfeld es erwartet

it5: (adtc01e): Weil sich nichts Anderes ergeben hat

it6: (adtc01f): Weil ich dauerhaft wissenschaftlich arbeiten möchte

it7: (adtc01g): Weil ich zur Lösung dringender gesellschaftlicher Probleme
beitragen möchte

it8: (adtc01h): Weil ich mein Ansehen steigern möchte

it9: (adtc01i): Weil ich meine Berufschancen auf dem außerakademischen
Arbeitsmarkt verbessern möchte

it10: (q01a): Sonstiges, und zwar: (q01b): [string] 6 cm

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 :

ao3: 3 : 3 :

ao4: 4 : 4 :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc: SHOW it10 IF preload01 = 1

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO A06

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adbi02a/adbi02b

qt: Einfachauswahlmatrix mit drop-down Menü

hl:

in:

q: Wann haben Sie mit der inhaltlichen Arbeit an Ihrer Promotion begonnen?

is: Beziehen Sie hierbei bitte auch die Vorbereitungs- und Orientierungsphase
mit ein (z. B. Erstellung des Exposés, Literaturrecherche, Laborversuche usw.).

it1: (adbi02a): Monat:

it2: (adbi02b): Jahr:

ao1: (adbi02a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi02b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010,
2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000, vor 2000

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO A07 IF adbi02a = SYSMISS AND adbi02b \<\> SYSMISS

GOTO A08 IF adbi02a \<\> SYSMISS OR adbi02b = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi02a = SYSMISS AND adbi02b \<\> SYSMISS

(wenn bei A06 („wann mit Promotion begonnen“) ein Jahr, aber kein Monat
angegeben wurde)

vn: adbi03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Können Sie sich noch erinnern, in welchem Quartal Sie mit den Arbeiten
begonnen haben?

q2: Können Sie sich noch erinnern, in welchem Quartal Sie mit den Arbeiten
begonnen hatten?

is:

it:

ao1: 1 : : 1. Quartal

ao2: 2 : : 2. Quartal

ao3: 3 : : 3. Quartal

ao4: 4 : : 4. Quartal

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2 OR adbi01 = 4

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A08

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adbi04a/adbi04b/adbi04c

qt: Einfachauswahlmatrix mit drop-down Menü und Mehrfachauswahl

hl:

in:

q: Wann wurden Sie von der Hochschule zur Promotion zugelassen?

is: D. h.: Seit wann haben Sie eine schriftliche Bestätigung über die Annahme
Ihres Promotionsvorhabens von Ihrer Hochschule?

it1: (adbi04a): Monat:

it2: (adbi04b): Jahr:

ao1: (adbi04a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi04b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010,
2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000, vor 2000

it3: (adbi04c): Ich wurde noch nicht zugelassen./Ich habe noch keinen
Zulassungsantrag gestellt.

mv:

ka:

vc:

SHOW it3 IF adbi01 = 1 OR adbi01 = 3 or adbi01 = 4

av:

kh:

fv:

hv:

fo: item 3 absetzen

tr:

GOTO A09 IF adbi04a = SYSMISS AND adbi04b \<\> SYSMISS

GOTO A10 IF ((adbi04a \<\> SYSMISS OR adbi04b = SYSMISS) AND (adbi01 = 2))

GOTO A11 IF ((adbi04a \<\> SYSMISS OR adbi04b = SYSMISS) AND (adbi01 = 4))

GOTO A14 IF ((adbi04a \<\> SYSMISS OR adbi04b = SYSMISS) AND (adbi01 = 1 OR
adbi01 = 3))

GOTO A10 IF adbi01 == 2

GOTO A11 IF adbi01 == 4

GOTO A14 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi04a = SYSMISS AND adbi04b \<\> SYSMISS

(wenn bei A08 („wann zur Promotion zugelassen“) ein Jahr, aber kein Monat
angegeben wurde)

vn: adbi05

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Können Sie sich noch erinnern, in welchem Quartal Sie zugelassen wurden?

is:

it:

ao1: 1 : : 1. Quartal

ao2: 2 : : 2. Quartal

ao3: 3 : : 3. Quartal

ao4: 4 : : 4. Quartal

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A10 IF adbi01 = 2

GOTO A11 IF adbi01 = 4

GOTO A14 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 2

(wenn bei A01 („Promotionsstatus“) = 2 („abgeschlossen“))

vn: adbi06a/adbi06b

qt: Einfachauswahlmatrix mit horizontalem drop-down Menü

hl:

in:

q: Wann haben Sie die Promotion abgeschlossen?

is:

it1: (adbi06a): Monat:

it2: (adbi06b): Jahr:

ao1: (adbi06a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi06b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010,
2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000, vor 2000

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO A14

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 4

(wenn A01 („Promotionsstatus“) = 4 („abgebrochen))

vn: adbi07

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist Ihre Hochschule darüber informiert, dass Sie Ihre Promotion abgebrochen
haben?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A12

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 4

(wenn A01 („Promotionsstatus“) = 4 („abgebrochen) und A11 („Hochschule
informiert“) = 1 („ja“))

vn: adbi08a/adbi08b

qt: Einfachauswahlmatrix mit drop-down Menü

hl:

in:

q: Wann haben Sie die Promotion abgebrochen?

is:

it1: (adbi08a): Monat:

it2: (adbi08b): Jahr:

ao1: (adbi08a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi08b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010,
2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000, vor 2000

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO A13 IF adbi08a = SYSMISS AND adbi08b \<\> SYSMISS

GOTO A14 IF adbi08a \<\> SYSMISS OR adbi08b = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi08a = SYSMISS AND adbi09b \<\> SYSMISS

(wenn bei A12 („Promotionsabbruch: Zeitpunkt“) ein Jahr, aber kein Monat
angegeben wurde)

vn: adbi09

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Können Sie sich noch erinnern, in welchem Quartal Sie Ihre Promotion
abgebrochen haben?

is:

ao1: 1 : : 1. Quartal

ao2: 2 : : 2. Quartal

ao3: 3 : : 3. Quartal

ao4: 4 : : 4. Quartal

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A14

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adbi10a/adbi10b

qt: offene Frage (string)

hl:

in:

q1: An welcher Hochschule promovieren Sie?

q2: An welcher Hochschule haben Sie promoviert?

q3: An welcher Hochschule wollten Sie promovieren?

is:

ao1: (adbi09a): 10 cm, Präfix [ao]: Name der Hochschule (z. B. Universität
Erlangen-Nürnberg): [string]

ao2: (adbi09b): 10 cm, Präfix [ao]: Standort der Hochschule (z. B. Nürnberg):
[string]

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

SHOW q3 IF adbi01 = 4

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A15 IF ((adbi01 = 1 OR adbi01 = 3) AND (adbi10a \<\> SYSMISS))

GOTO A16 IF ((adbi01 = 1 OR adbi01 = 3) AND (adbi10a = SYSMISS))

GOTO A20 IF adbi01 = 2 OR adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adbi10a \<\> SYSMISS

(wenn A01 („Promotionsstatus“)= 1 („promoviere“) oder 3 („unterbrochen“) und A14
(„Hochschule Promotion“) ausgefüllt)

vn: adtc02(adtc02a/adtc02b/adtc02c/adtc02d/adtc02e/adtc02f/adtc02g/adtc02h)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Warum haben Sie sich für eine Promotion an dieser Hochschule entschieden?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adtc02a): Weil ich gerne an diesem Standort sein wollte

ao2: (adtc02b): Wegen der guten Forschungsbedingungen in meinem Fach

ao3: (adtc02c): Wegen des Betreuers/der Betreuerin

ao4: (adtc02d): Wegen des guten Rufs der Hochschule

ao5: (adtc02e): Weil es dort attraktive Serviceangebote für Promovierende gibt

ao6: (adtc02f): Es hat sich einfach so ergeben. [EK]

ao7: (adtc02g): Sonstiges, und zwar: (adtc02h): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A16

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adbi11

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist an Ihrem Promotionsverfahren eine Hochschule im Ausland beteiligt?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A17 IF adbi11 = 1

GOTO A18 IF adbi11 = 2 OR adbi11 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A17_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adbi11 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
A16 („Hochschule im Ausland beteiligt“) = 1 („Ja“))

vn: adbi12

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Handelt es sich dabei um einen gemeinsamen Abschluss der Hochschulen aus dem
In- und Ausland (cotutelle de thèse)?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A18

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A18_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adbi13

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist an ihrem Promotionsverfahren eine Fachhochschule bzw. Hochschule für
angewandte Wissenschaften beteiligt?

q1: Ist an ihrem Promotionsverfahren eine Fachhochschule, eine Hochschule für angewandte Wissenschaften bzw. eine Verwaltungshochschule beteiligt? 

is:

it:

ao1: (adbi13): 1 : : Ja

ao2: (adbi13): 2 : : Ja, eine Fachhochschule/Hochschule für angewandte Wissenschaften.

ao3: (adbi13): 3 : : Ja, eine Verwaltungshochschule.

ao4: (adbi13): 4 : : Nein


mv:

ka:

vc: 

SHOW q and ao1 AND ao4 IF preload01 \<\> 1

SHOW q1 and ao2 AND ao3 AND ao4 IF preload01 = 1



av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO A19 IF adbi13 = 1 OR adbi13 = 2

GOTO A20 IF adbi13 = 4 OR adbi13 = 3 OR adbi13 = SYSMISS 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A19_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adbi13 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
A18 („Fachhochschule beteiligt“) = 1 („Ja“))

vn: adbi14(adbi14a/adbi14b/adbi14c/adbi14d/adbi14e/adbi14f/adbi14g/adbi14h)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche Aussagen treffen auf Ihr Promotionsverfahren zu?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adbi14a): Ich habe/hatte einen Arbeitsvertrag an der
Fachhochschule/Hochschule für angewandte Wissenschaften.

ao2: (adbi14b): Wesentliche Teile der Arbeit finden an der
Fachhochschule/Hochschule für angewandte Wissenschaften statt.

ao3: (adbi14c): Der/Die FH-Professor(in) ist Prüfer(in).

ao4: (adbi14d): Der/Die FH-Professor(in) ist Gutachter(in).

ao5: (adbi14e): Der/Die FH-Professor(in) ist Betreuer(in).

ao6: (adbi14f): Es gibt einen Kooperationsvertrag zwischen der Universität und
der FH.

ao7: (adbi14g): Ich habe eine Betreuungsvereinbarung, die sowohl der/die
Universitäts- als auch der/die FH-Professor(in) unterschrieben hat.

ao8: (adbi14h): Keine der genannten Aussagen trifft auf mein Promotionsverfahren zu. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao8 von den übrigen Antwortoptionen absetzen

tr:

GOTO A20

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________A20_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adbi15

qt: offene Frage (string)

hl:

in:

q1: In welchem Fach promovieren Sie?

q2: In welchem Fach haben Sie promoviert?

q3: In welchem Fach waren Sie eingeschrieben?

is: Bitte geben Sie eine möglichst genaue Fachbezeichnung an.

it:

ao1: [string] 8 cm, 1 Zeile

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

SHOW q3 IF adbi01 = 4

av:

kh:

fv:

hv:

fo:

tr:

GOTO K01 IF preload01 = 2 

GOTO S01 IF preload01 = 4

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 
(wenn preload01 = 2 ("Kiel")) 

vn: k01(k01a/k01b/k01c/k01d/k01e/k01f/k01g/k01h/k01i/k01j)

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q1: Bitte bewerten Sie die folgenden Aussagen in Bezug auf Ihre bisherige Promotionszeit. Inwieweit treffen folgende Aussagen auf Sie zu?


is: 

it1a: (k01a): Ich empfinde die Dauer meiner bisherigen Promotion als viel zu lang. 

it2a: (k01b): Ich kann die formalen Vorgaben (z. B. Antrag auf Annahme als Doktorand(in) an der für mich zuständigen Fakultät, Antrag auf Zulassung zum Promotionsprüfungsverfahren) für meine Promotion sehr leicht erfüllen. 

it3a: (k01c): Ich empfinde das Verfahren zum Wechsel zwischen zwei Fakultäten als sehr transparent.

it4a: (k01d): Ich empfinde das Verfahren zum Wechsel zwischen zwei Fakultäten als sehr einfach. 

it5a: (k01e): Mein Promotionsprojekt ist sehr eng und kooperativ als Zusammenarbeit mit außerakademischen Stakeholdern (Person oder Gruppe, die ein berechtigtes Interesse am Verlauf oder Ergebnis des Projektes hat) angelegt.

it6a: (k01f): Ich habe meine Forschungsfrage sehr mit Hilfe von außerakademischen Stakeholdern konkretisiert.

it7: (k01g): Meine Annahme als Doktorand(in) an der Fakultät verlief sehr unproblematisch

it8: (k01h): Das Thema meiner Promotion entwickelt sich thematisch sehr in eine Richtung, die voraussichtlich einer anderen Fakultät zugehörig sein wird.



q2: Bitte bewerten Sie die folgenden Aussagen in Bezug auf Ihre gesamte Promotionszeit.
Inwieweit treffen folgende Aussagen auf Sie zu?


it1b: (k01a): Ich habe die Dauer meiner gesamten Promotion als viel zu lang empfunden.

it2b: (k01b): Ich konnte die formalen Vorgaben (z. B. Antrag auf Annahme als Doktorand(in) an der für mich zuständigen Fakultät, Antrag auf Zulassung zum Promotionsprüfungsverfahren) für meine Promotion sehr leicht erfüllen.

it3b: (k01c): Ich habe das Verfahren zum Wechsel zwischen zwei Fakultäten als sehr transparent empfunden. 

it4b: (k01d): Ich habe das Verfahren zum Wechsel zwischen zwei Fakultäten als sehr einfach empfunden. 

it5b: (k01e): Mein Promotionsprojekt war sehr eng und kooperativ als Zusammenarbeit mit außerakademischen Stakeholdern (Person oder Gruppe, die ein berechtigtes Interesse am Verlauf oder Ergebnis des Projektes hat) angelegt. 

it6b: (k01f): Ich habe meine Forschungsfrage sehr mit Hilfe von außerakademischen Stakeholdern konkretisiert. 

it9: (k01i): Ich habe die Abschlussphase meiner Promotion formal als sehr transparent empfunden. 

it10: (k01j): Ich habe die Abschlussphase meiner Promotion als sehr klar strukturiert empfunden. 


ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : : 

ao5: 5 : 5 : trifft völlig zu

ao6: 6 : : Kann ich nicht beurteilen.



mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW it1a - it6a AND it7 AND it8 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2 OR adbi01 = 4

SHOW it1b - it6b IF adbi01 = 2 OR adbi01 = 4

SHOW it9 AND it10 IF adbi01 = 2


av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao6 bitte von den anderen ao abgrenzen

tr:

GOTO K02

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________K02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 
(wenn preload01 = 2 ("Kiel")) 

vn: k02(k02a/k02b/k02c/k02d/k02e)

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q1: Bitte bewerten Sie die folgenden Aussagen in Bezug auf Ihre bisherige Promotionszeit.
Inwieweit treffen folgende Aussagen auf Ihre Situation zu?

is: 

it1a: (k02a): Ich habe während meiner Promotion die Möglichkeit, zwischen zwei Fakultäten zu wechseln.

it2a: (k02b): Ich bin in Kiel an einer Fakultät als Doktorand(in) angenommen worden, deren Fächerauswahl nicht meinen promotionsqualifizierenden Abschluss beinhaltet.

it3a: (k02c): In meinem Promotionsvorhaben sind außerakademische Stakeholder involviert, die aber nicht aktiv am Projekt mitarbeiten (z. B. Geldgebende, Beratende, Stiftungen).



q2: Bitte bewerten Sie die folgenden Aussagen in Bezug auf Ihre abgebrochene Promotion.
Inwieweit treffen folgende Aussagen auf Ihre Situation während der abgebrochenen Promotion zu?


q3: Bitte bewerten Sie die folgenden Aussagen in Bezug auf Ihre abgeschlossene Promotion.
Inwieweit treffen folgende Aussagen auf Ihre Situation während der abgeschlossenen Promotion zu?



it1b: (k02a): Ich hatte während meiner Promotion die Möglichkeit, zwischen zwei Fakultäten zu wechseln.

it2b: (k02b): Ich bin in Kiel an einer Fakultät als Doktorand(in) angenommen worden, deren Fächerauswahl nicht meinen promotionsqualifizierenden Abschluss beinhaltet.

it3b: (k02c): In meinem Promotionsvorhaben waren außerakademische Stakeholder involviert, die aber nicht aktiv am Projekt mitgearbeitet haben (z. B. Geldgebende, Beratende, Stiftungen).

it4: (k02d): Das Thema meiner Promotion hat sich thematisch in eine Richtung entwickelt, die einer anderen Fakultät zugehörig war.

it5: (k02e): Meine Promotion war eine Voraussetzung für meinen derzeitigen Beruf.


ao1: 1 :  : Ja

ao2: 2 :  : Nein


mv:

ka:

vc:

SHOW q1 AND it1a AND it2a AND it3a IF adbi01 = 1 OR adbi01 = 3

SHOW q2 AND it1b - it3b AND it4 IF adbi01 = 4

SHOW q3 AND it1b - it3b AND it4 AND it5 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi: it1a-it3a und it1b-it3b unterscheiden sich hinsichtlich der Zeitform. 

\-------------------------------------------------------------------------------------------------------------------------------------------------



\__________________________________________S01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s01

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Waren Sie in den letzten Jahren an der Universität des Saarlandes (UdS) als wissenschaftliche(r) Beschäftigte(r) tätig?  

is: 

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S02 IF s01 = 1

GOTO S05 IF s01 = 2 OR s01 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s02a/s02b

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q: Wie beurteilen Sie die allgemeine Arbeitssituation…  

is: 

it1: (s02a): zum !!Zeitpunkt Ihrer ersten Anstellung an der UdS!! für wissenschaftliche Mitarbeiter(innen) an der UdS?

it2: (s02b): zum !!jetzigen Zeitpunkt!! für wissenschaftliche Mitarbeiter(innen) an der UdS?


ao1: 0 : 0 : sehr schlecht

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr gut


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO S03 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s03a/s03b

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q: Wie denken Sie wird die allgemeine Arbeitssituation im Jahr 2020 an der UdS aussehen für…

is: 

it1: (s03a): wissenschaftliche Mitarbeiter(innen) in Ihrem !!Fach!!? 

it2: (s03b): wissenschaftliche Mitarbeiter(innen) !!insgesamt!!? 


ao1: 0 : 0 : sehr schlecht

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr gut

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO S04 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s04

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie attraktiv bewerten Sie die Universität des Saarlandes als Arbeitgeberin?

is: 

it: 

ao1: 0 : 0 : sehr unattraktiv

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr attraktiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO S05 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s05a/s05b

qt: Matrix mit horizontaler Einfachauswahl 

hl:

in:

q: Wie wird die Zukunft…

is: 

it1: (s05a): Ihres !!Fachs!! an der Universität des Saarlandes aussehen?

it2: (s05b): der Universität des Saarlandes !!insgesamt!! aussehen?


ao1: 0 : 0 : sehr negativ

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr positiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO S06

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4
(wenn preload01 = 4 ("Saarbrücken"))

vn: s06

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wurden aus Ihrer Sicht an der Universität des Saarlandes in den letzten Jahren Einsparungen vorgenommen, die zu Veränderungen führten?

is: 

it: 

ao1: 1 : : Ja

ao2: 2 : : Nein

ao3: 3 : : Kann ich nicht beurteilen. 



mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S07 IF s06 = 1

GOTO S08 IF s01 = 1

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________S07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s06 = 1
(wenn preload01 = 4 ("Saarbrücken") und S06 ("Veränderungen durch Einsparungen") = 1 ("Ja"))

vn: s07

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie bewerten Sie diese Veränderungen?

is: 

it: 

ao1: 0 : 0 : sehr negativ

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr positiv


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO S08 IF s01 = 1

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________S08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s01 = 1
(wenn preload01 = 4 ("Saarbrücken") und S01 ("wissenschaftlicher Beschäftigter an UdS") = 1 ("Ja"))

vn: s08

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wurden aus Ihrer Sicht an der Universität des Saarlandes in den letzten Jahren Strukturentscheidungen getroffen, die zu Veränderungen führten?

is: 

it: 

ao1: 1 : : Ja

ao2: 2 : : Nein

ao3: 3 : : Kann ich nicht beurteilen. 

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S09 IF s08 = 1

GOTO S10 IF s08 = 2 OR s08 = 3 OR s08 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s01 = 1 AND s08 = 1
(wenn preload01 = 4 ("Saarbrücken") und S01 ("wissenschaftlicher Beschäftigter an UdS") = 1 ("Ja") und S08 ("Strukturentscheidungen") = 1 ("Ja"))

vn: s09

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie bewerten Sie diese Strukturentscheidungen?

is: 

it: 

ao1: 0 : 0 : sehr negativ

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr positiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO S10 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________S10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s01 = 1
(wenn preload01 = 4 ("Saarbrücken") und S01 ("wissenschaftlicher Beschäftigter an UdS") = 1 ("Ja"))

vn: s10

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Führten in !!Ihrem Bereich/in Ihrem Fach!! Strukturentscheidungen zu Veränderungen?

is: 

it: 

ao1: 1 : : Ja

ao2: 2 : : Nein

ao3: 3 : : Kann ich nicht beurteilen. 

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S11 IF s10 = 1

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s01 = 1 AND s10 = 1
(wenn preload01 = 4 ("Saarbrücken") und S01 ("wissenschaftlicher Beschäftigter an UdS") = 1 ("Ja") und S10 ("Strukturentscheidungen im Bereich/Fach") = 1 ("Ja"))

vn: s11

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie bewerten Sie diese Veränderungen?

is: 

it: 

ao1: 0 : 0 : sehr negativ

ao2: 1 : 1 : 

ao3: 2 : 2 : 

ao4: 3 : 3 : 

ao5: 4 : 4 : 

ao6: 5 : 5 : 

ao7: 6 : 6 : 

ao8: 7 : 7 : 

ao9: 8 : 8 : 

ao10: 9 : 9 : 

ao11: 10 : 10 : sehr positiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO B01 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO B03 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________B01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: adcd01

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Ist Ihre Promotion Teil eines Forschungsprojekts, an dem auch noch andere
Personen arbeiten?

q2: War Ihre Promotion Teil eines Forschungsprojekts, an dem auch noch andere
Personen arbeite(te)n?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B02 IF adcd01 = 1

GOTO B03 IF (adbi01 = 1 OR adbi01 = 3) AND (adcd01 = 2 OR adcd01 = SYSMISS)

GOTO B04 IF (adbi01 = 2 AND (adcd01 = 2 OR adcd01 = SYSMISS))

GOTO B04 IF adbi01 = 2

GOTO B03 IF ELSE

hi: Bitte hier Icon 2 für Modul B einfügen (oben rechts) und durchgängig
einblenden bis das nächste Modul C beginnt.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 2 OR adbi01 = 3) AND adcd01 = 1

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

Und B01 {„Teil eines Forschungsprojekts“) = 1 („Ja“)})

vn: adcd02

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Gibt es in dem Forschungsprojekt – außer Ihnen selbst – noch andere
Promovierende?

q2: Gab es in dem Forschungsprojekt – außer Ihnen selbst – noch andere
Promovierende?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B03 IF adbi01 = 1 OR adbi01 = 3

GOTO B04 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3 OR adbi01 = 4

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 3 („unterbrochen“) oder 4
(„abgebrochen“))

vn: adtc03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Haben Sie schon ein konkretes Promotionsthema?

q2: Hatten Sie schon ein konkretes Promotionsthema?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 4

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B04 IF ((adbi01 = 1 OR adbi01 = 3) AND (adtc03 = 1))

GOTO B05 IF ((adbi01 = 1 OR adbi01 = 3) AND (adtc03 = 2 OR adtc03 = SYSMISS))

GOTO K03 IF adbi01 = 4 AND preload01 = 2

GOTO B38 IF adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND adtc03 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“)) und („konkretes Promotionsthema“) = („Ja“)})

vn:
adtc04(adtc04a/adtc04b/adtc04c/adtc04d/adtc04e/adtc04f/adtc04g/adtc04h/adtc04i/adtc04j)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q1: Wie sind Sie zu Ihrem Promotionsthema gekommen?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1a: (adtc04a): Das Thema baut auf Arbeiten meines vorangegangenen Studiums
auf.

ao2a: (adtc04b): Das Thema wurde mir von einer/einem Betreuer(in) vorgeschlagen.

ao3a: (adtc04c): Das Thema schließt an Berufserfahrungen an, die ich außerhalb
der Wissenschaft gemacht habe.

ao4a: (adtc04d): Das Thema wurde in enger Kooperation mit Partnern außerhalb der
Wissenschaft abgestimmt.

ao5a: (adtc04e): Ich habe das Thema selbst entwickelt.

ao6a: (adtc04f): Das Thema war vorgegeben (z. B. im Rahmen eines
Forschungsprojekts).

ao7a: (adtc04g): Der thematische Rahmen war vorgegeben.

ao8a: (adtc04h): Das Thema wurde ausgeschrieben.

ao9a: (adtc04i): Sonstiges, und zwar: (adtc04j): [string] 6 cm

q2: Wie waren Sie zu Ihrem Promotionsthema gekommen?

ao1b: (adtc04a): Das Thema baute auf Arbeiten meines vorangegangenen Studiums
auf.

ao2b: (adtc04b): Das Thema wurde mir von einer/einem Betreuer(in) vorgeschlagen.

ao3b: (adtc04c): Das Thema schloss an Berufserfahrungen an, die ich außerhalb
der Wissenschaft gemacht habe.

ao4b: (adtc04d): Das Thema wurde in enger Kooperation mit Partnern außerhalb der
Wissenschaft abgestimmt.

ao5b: (adtc04e): Ich habe das Thema selbst entwickelt.

ao6b: (adtc04f): Das Thema war vorgegeben (z. B. im Rahmen eines
Forschungsprojekts).

ao7b: (adtc04g): Der thematische Rahmen war vorgegeben.

ao8b: (adtc04h): Das Thema wurde ausgeschrieben.

ao9b: (adtc04i): Sonstiges, und zwar: (adtc04j): [string] 6 cm

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW ao1a – ao9a IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

SHOW ao1b – ao9b IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B05 IF adbi01 = 1 OR adbi01 = 3

GOTO Q01 IF (adbi01 = 2) AND (preload01=1)

GOTO B06 IF adbi01 = 2

hi: Gleiche Variablen werden bei den Antwortoptionen erhoben, nur der Text ist
in verschiedenen Zeitformen

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adcd03

qt: offene Frage (number)

hl:

in:

q: Wie weit sind Sie mit Ihrer Promotion?

is: 

Bitte geben Sie nur Zahlen ein und verzichten Sie auf Nachkommastellen.

(Beispiel: 25 und nicht 25,00)

it:

ao1: 3 cm, Präfix [ao] Suffix: Ich habe ca. [number] % bewältigt.

mv:

ka:

vc:

av: number : \<= 3 stellig : 0 TO 100

kh: Bitte geben Sie einen Wert zwischen 0 und 100 an.

fv:

hv:

fo:

tr:

GOTO Q01 IF preload01 = 1

GOTO B06

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________Q01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3 OR adbi01 = 2) AND preload01 = 1

((wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) oder 2 ("abgeschlossen")) und preload01 ("Düsseldorf") = 1)

vn: q02

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Sind Sie derzeit Mitglied einer Graduiertenakademie der HHU Düsseldorf?

q2: Waren Sie Mitglied einer Graduiertenakademie der HHU Düsseldorf?

is: 

it:

ao1: 1 : : Ja, Mitglied der iGRAD.

ao2: 2 : : Ja, Mitglied der philGRAD.

ao3: 3 : : Ja, Mitglied der medRSD.

ao4: 4 : : Nein.

mv:

ka:

vc: 

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av: 

kh: 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO Q02 IF q02 = 1 OR q02 = 2

GOTO B06 IF q02 = 4 OR q02 = SYSMISS

GOTO B08 IF q02 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________Q02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3 OR adbi01 = 2) AND preload01 = 1 AND (q02 = 1 OR q02 = 2)

(((wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) oder 2 ("abgeschlossen"))) und (preload01 = 1 ("Düsseldorf")) und (Q01  = 1 ("iGRAD") oder 2 ("philGRAD"))

vn: q03a/q03b/q03c/q03d

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q1: Was trifft für Ihre Mitgliedschaft in der Graduiertenakademie iGRAD zu?

q1b: Was traf für Ihre Mitgliedschaft in der Graduiertenakademie iGRAD zu?

q2: Was trifft für Ihre Mitgliedschaft in der Graduiertenakademie philGRAD zu?

q2b: Was traf für Ihre Mitgliedschaft in der Graduiertenakademie philGRAD zu?


is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q03a): Ich muss an einem verbindlichen Kurs- und Lehrveranstaltungsprogramm teilnehmen.

ao2: (q03b): Ich werde von mehreren Hochschullehrer(inne)n betreut.

ao3: (q03c): Ich habe ein wettbewerbliches Auswahlverfahren mit Ausschreibung durchlaufen.

ao4: (q03d): Keine der drei Aussagen trifft zu. [EK]




ao1b: (q03a): Ich musste an einem verbindlichen Kurs- und Lehrveranstaltungsprogramm teilnehmen.

ao2b: (q03b): Ich wurde von mehreren Hochschullehrer(inne)n betreut.

ao3b: (q03c): Ich habe ein wettbewerbliches Auswahlverfahren mit Ausschreibung durchlaufen.

ao4b: (q03d): Keine der drei Aussagen traf zu. [EK]




mv:

ka:

vc: 

SHOW q1 IF q02 = 1 AND (adbi01 = 1 OR adbi01 = 3)

SHOW q2 IF q02 = 2 (adbi01 = 1 OR adbi01 = 3)

SHOW ao1 - ao4 IF adbi01 = 1 OR adbi01 = 3


SHOW q1b IF q02 = 1 AND adbi01 = 2

SHOW q2b IF q02 = 2 AND adbi01 = 2

SHOW ao1b AND ao2b AND AND ao3b AND ao4b IF adbi01 = 2

av: 

kh: 

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao4 von den übrigen Antwortoptionen absetzen

tr:

GOTO Q03 IF q02 = 2

GOTO B06 IF q02 = 1


hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________Q03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3 OR adbi01 = 2) AND preload01 = 1 AND (q02 = 2)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) oder 2 ("abgeschlossen")) und (preload01 = 1 ("Düsseldorf")) und (Q01  = 2 ("philGRAD"))

vn: q04a/q04b/q04c

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Bekamen Sie im Rahmen der Graduiertenakademie philGRAD ein Stipendium oder eine Stelle?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q04a): Ja, ein Stipendium.

ao2: (q04b): Ja, eine Stelle.

ao3: (q04c): Nein. [EK]

mv:

ka:

vc: 

av: 

kh: 

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao3 von den übrigen Antwortoptionen absetzen

tr:

GOTO B06 


hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________B06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: adcd04

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Sind Sie derzeit Mitglied in einem strukturierten Promotionsprogramm (z. B.
Promotionsstudiengang, Promotionsprogramm, Graduiertenschule,
Graduiertenkolleg)?

q2: Waren Sie Mitglied in einem strukturierten Promotionsprogramm (z. B.
Promotionsstudiengang, Promotionsprogramm, Graduiertenschule,
Graduiertenkolleg)?

is:

it:

ao1: 1 : : Ja, als ordentliches Mitglied.

ao2: 2 : : Ja, als assoziiertes Mitglied.

ao3: 3 : : Nein.

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B07 IF adcd04 = 1 OR adcd04 = 2

GOTO B10 IF ((adbi01 = 1 OR adbi01 = 3) AND (adcd04 = 3 OR adcd04 = SYSMISS))

GOTO B18 IF ((adbi01 = 2) AND (adcd04 = 3 OR adcd04 = SYSMISS))

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND (adcd04 = 1 OR adcd04 = 2)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“)) und

B06 („Mitglied Promotionsprogramm“) = 1 („ordentliches Mitglied“) oder 2
(„assoziiertes Mitglied“))

vn:
adcd05(adcd05a/adcd05b/adcd05c/adcd05d/adcd05e/adcd05f/adcd05g/adcd05h/adcd05i/adcd05j/adcd05k)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q1: In welcher Art von Promotionsprogramm(en) sind Sie Mitglied?

q2: In welcher Art von Promotionsprogramm(en) waren Sie Mitglied?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adcd05a): Graduiertenkolleg (DFG)

ao2: (adcd05b): Integriertes Graduiertenkolleg (innerhalb eines SFB)

ao3: (adcd05c): Graduiertenschule der Exzellenzinitiative (DFG)

ao4: (adcd05d): Promotionsprogramm der Universität ohne Förderung durch die DFG

ao5: (adcd05e): Promotionsprogramm der Universität mit Förderung durch die DFG

ao6: (adcd05f): International Max Planck Research School (IMPRS)

ao7: (adcd05g): Programm der Helmholtz Gemeinschaft

ao8: (adcd05h): Leibniz Graduate School

ao9: (adcd05i): Promotionsstudiengang

ao10: (adcd05j): Sonstiges Programm, und zwar: (adcd05k): [string] 6 cm

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr: GOTO B08

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND ((adcd04 = 1 OR adcd04 = 2) OR (q03 = 1 OR q03 = 2 OR q03))

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“)) und B06 („Mitglied Promotionsprogramm“) = 1 („ordentliches
Mitglied“) oder 2 („assoziiertes Mitglied“))

vn: adcd06(adcd06a/adcd06b/adcd06c/adcd06d)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q1: Was trifft für Ihre Mitgliedschaft in dem/den Promotionsprogramm(en) zu?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1a: (adcd06a): Ich muss an einem verbindlichen Kurs- und Lehrveranstaltungsprogramm teilnehmen.

ao2a: (adcd06b): Ich werde von mehreren Hochschullehrer(inne)n betreut.

ao3a: (adcd06c): Ich habe ein wettbewerbliches Auswahlverfahren mit Ausschreibung durchlaufen.

a04a: (adcd06d): Keine der Aussagen trifft auf meine Mitgliedschaft in dem/den Promotionsprogramm(en) zu. [EK]

q2: Was traf für Ihre Mitgliedschaft in dem/den Promotionsprogramm(en) zu?

ao1b: (adcd06a): Ich musste an einem verbindlichen Kurs- und Lehrveranstaltungsprogramm teilnehmen.

ao2b: (adcd06b): Ich wurde von mehreren Hochschullehrer(inne)n betreut.

ao3b: (adcd06c): Ich habe ein wettbewerbliches Auswahlverfahren mit Ausschreibung durchlaufen.

a04b: (adcd06d): Keine der Aussagen trifft auf meine ehemalige Mitgliedschaft in dem/den Promotionsprogramm(en) zu. [EK]


mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

SHOW ao1a - ao4a IF adbi01 = 1 OR adbi01 = 3

SHOW ao1b - ao4b IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao4 von den übrigen Antwortoptionen absetzen

tr:

GOTO B09

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND (adcd04 = 1 OR adcd04 = 2)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“)) und B06 („Mitglied Promotionsprogramm“) = 1 („ordentliches
Mitglied“) oder 2 („assoziiertes Mitglied“))

vn: adcd07(adcd07a/adcd07b/adcd07c)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Bekamen Sie im Rahmen des Programms/der Programme ein Stipendium oder eine
Stelle?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (acdc07a): Ja, ein Stipendium.

ao2: (adcd07b): Ja, eine Stelle.

ao3: (adcd07c): Nein. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao3 von den übrigen Antwortoptionen absetzen

tr:

GOTO P01 IF preload01 = 3

GOTO B10 IF adbi01 = 1 OR adbi01 = 3

GOTO B18 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3 AND adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn preload01 = 3 ("Potsdam") und (A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: p01(p01a/p01b/p01c/p01d/p01e/p01f/p01g/p01h/p01i)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche Angebote der Potsdam Graduate School (PoGS) haben Sie seit Beginn Ihrer Promotion in Anspruch genommen?

q2: Welche Angebote der Potsdam Graduate School (PoGS) haben Sie während Ihrer Promotion in Anspruch genommen?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (p01a): Finanzielle Förderung (z. B. Reisekosten, Publikationskosten etc.)

ao2: (p01b): Transferable Skills Workshops (z. B. Präsentations-, Kommunikations- oder Führungskompetenzen etc.)

ao3: (p01c): Basic Module

ao4: (p01d): Teaching Professionals (Junior / International)

ao5: (p01e): Science meets Market (EPE)

ao6: (p01f): Mentoring Plus

ao7: (p01g): Promotionscoaching


ao8: (p01h): Ich habe keines der genannten Angebote genutzt./Die PoGS ist mir nicht bekannt. [EK]


mv:

ka:

vc:

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao8 bitte von den anderen ao absetzen

tr:

GOTO P02 IF p01a = TRUE OR p01b = TRUE OR p01c = TRUE OR p01d = TRUE OR p01e = TRUE OR p01f = TRUE OR p01g = TRUE 

GOTO P03 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3 AND adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn preload01 = 3 ("Potsdam") und (A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: p02(p02a/p02b/p02c/p02d/p02e/p02f/p02g)

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q: Die Teilnahme an den Angeboten hat sich folgendermaßen auf meine Karriereentwicklung ausgewirkt:

is: 

it1: (p02a): Finanzielle Förderung

it2: (p02b): Transferable Skills Workshops

it3: (p02c): Basic Module

it4: (p02d): Teaching Professionals

it5: (p02e): Science meets Market (EPE)

it6: (p02f): Mentoring Plus

it7: (p02g): Promotionscoaching


ao1: 1 : 1 : überhaupt nicht hilfreich

ao2: 2 : 2 : eher nicht hilfreich

ao3: 3 : 3 : teils/teils

ao4: 4 : 4 : eher hilfreich

ao5: 5 : 5 : sehr hilfreich

ao6: 6 :  : Kann ich nicht beurteilen.


mv:

ka:

vc:

SHOW it1 IF p01a = TRUE

SHOW it2 IF p01b = TRUE

SHOW it3 IF p01c = TRUE

SHOW it4 IF p01d = TRUE

SHOW it5 IF p01e = TRUE

SHOW it6 IF p01f = TRUE

SHOW it7 IF p01g = TRUE

av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao6 bitte von den anderen ao absetzen

tr:

GOTO P05 IF adbi01 = 2

GOTO P03 IF ELSE


hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3 AND adbi01 = 1 OR adbi01 = 3

(wenn preload01 = 3 ("Potsdam") und (A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: p03

qt: offene Frage (string)

hl:

in:

q: Welche Angebote wünschen Sie sich zusätzlich von der PoGS?

is: 

it:

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO P04 

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: tc: IF preload01 = 3 AND (adbi01 = 1 OR adbi01 = 3)

(wenn preload01 = 3 ("Potsdam") und (A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: p04

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie reagiert Ihr(e) (Haupt-)Betreuer(in) auf Ihren Wunsch der Teilnahme an einem überfachlichen Weiterbildungsangebot, z. B. der PoGS?

is: 

it:

ao1: 1 :  : wird verweigert

ao2: 2 :  : wird toleriert

ao3: 3 :  : wird unterstützt

ao4: 4 :  : trifft nicht zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: bitte ao4 von den andere ao absetzen

tr:

GOTO P05

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3 AND (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3)

(wenn preload01 = 3 ("Potsdam") und (A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: p05a/p05b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Haben Sie bereits an Vernetzungsveranstaltungen der PoGS (z. B. PhDay, Career Talk etc.) teilgenommen?

q2: Haben Sie während Ihrer Promotion an Vernetzungsveranstaltungen der PoGS (z. B. PhDay, Career Talk etc.) teilgenommen?

is: 

it:

ao1: (p05a): 1 :  : Ja, und zwar an: (p05b): [string] 8 cm; 2 Zeilen

ao2: (p05a): 2 :  : Nein

mv:

ka:

vc:

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO P06 IF p05a = 2 OR p05a = SYSMISS

GOTO B10 IF adbi01 = 1 OR adbi01 = 3

GOTO B18 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3

(wenn preload01 = 3 ("Potsdam"))

vn: p06(p06a/p06b/p06c/p06d/p06e/p06f/p06g/p06h)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Warum haben Sie an keiner Netzwerkveranstaltung teilgenommen? 

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1a: (p06a): Ich habe eigentlich Interesse, aber keine Zeit.

ao2a: (p06b): Ich habe eigentlich Interesse, aber mein(e) (Haupt-)Betreuer(in) lässt mich nicht.

ao3: (p06c): Kein Interesse

ao4: (p06d): Uninteressante Formate

ao5: (p06e): Zu viele andere Veranstaltungen

ao6: (p06f): Sonstiges, und zwar: (p06g): [string] 8 cm

ao7a: (p06h): Ich kenne keines dieser Angebote. [EK]


ao1b: (p06a): Ich hatte eigentlich Interesse, aber keine Zeit.

ao2b: (p06b): Ich hatte eigentlich Interesse, aber mein(e) (Haupt-)Betreuer(in) ließ mich nicht.

ao7b: (p06h): Ich kannte keines dieser Angebote. [EK]


mv:

ka:

vc:

SHOW ao1a AND ao2a AND ao7a IF adbi01 <> 2

SHOW ao1b AND ao2b AND ao7b IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao7 bitte von den anderen ao absetzen

tr:

GOTO B10 IF adbi01 = 1 OR adbi01 = 3

GOTO B18 IF adbi01 = 2

hi: Bei den ao1b, ao2b, ao7b wird ein anderes Wording gewählt (Zeitform), wenn adbi01 = 2

\-------------------------------------------------------------------------------------------------------------------------------------------------



\__________________________________________B10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:adcd08(adcd08a/adcd08b/adcd08c/adcd08d/adcd08e/adcd08f/adcd08g/adcd08h/adcd08i/adcd08j/adcd08k/adcd08l/adcd08m/adcd08n/adcd08o); q05(q05a/q05b/q05c/q05d/q05e/q05f/q05g/q05h/q05i/q05j/q05k/q05l)

qt: Mehrfachauswahl mit vertikalen ao mit offener ao (string)

hl:

in:

q: Welche der folgenden Kurse und Lehrveranstaltungen speziell für Promovierende
sind Ihnen an Ihrer Hochschule bekannt?

is: Bitte wählen Sie alles Zutreffende aus.

ka: !!Kurse oder Lehrveranstaltungen…!!

ao1: (adcd08a): zur Konferenz- und Tagungsorganisation 

ao2: (adcd08b): im Bereich Personal- und Mitarbeiterführung 

ao3: (adcd08c): zu speziellen Themen meines Promotionsfachs 

ao4: (adcd08d): zur Karriereplanung 

ao5: (adcd08e): zum Verfassen englischer Texte (z. B. Scientific Writing Skills
in English) 

ao6: (adcd08f): zu den Regeln guter wissenschaftlicher Praxis

ao7: (adcd08g): im Bereich Wissenschaftskommunikation

ao8: (adcd08h): zum Management von Forschungs-/Drittmittelprojekten

ao9: (adcd08i): zu Moderationstechniken und Gremienleitung

ao10: (adcd08j): zur Präsentation von Forschungsergebnissen

ao11: (adcd08k): zu spezifischen Forschungsmethoden für mein Promotionsfach

ao12: (adcd08l): zum wissenschaftlichen Schreiben (Schreibwerkstätten etc.)

ao13: (adcd08m): zur Entwicklung und Beantragung eines
Forschungs-/Drittmittelprojekts

ao16q: (q05a): im Bereich Zeit-/Selbstmanagement

ao17q: (q05b): im Bereich Projektmanagement

ao18q: (q05c): zum Arbeiten in Teams

ao19q: (q05d): zu Lehr-/Lernkompetenzen (Hochschuldidaktik)

ao20q: (q05e): im Bereich weiterer mündlicher Kommunikationskompetenzen (z. B. Rhetorik, Verhandeln, Argumentation, Small Talk) 

ao21q: (q05f): zu Informations-/Wissenskompetenzen bzw. Recherche

ao22q: (q05g): zu Statistik

ao23q: (q05h): zum (Forschungs-)Datenmanagement

ao24q: (q05i): zum Umgang mit Konflikten

ao25q: (q05j): zu gewerblichem Rechtsschutz (z. B. Patent-/Urheberrecht)

ao26q: (q05k): zu Networking bzw. Selbstmarketing

ao27q: (q05l): Selma-Meyer-Mentoring Programme für Promovierende

ao14: (adcd08n): Sonstiges, und zwar: (adcd08o): [string] 6 cm

ao15: (adcd08p): Keine der genannten Kurse oder Lehrveranstaltungen sind mir bekannt. [EK]

mv:

ka:

vc:

SHOW ao16q - ao27q IF preload01 = 1

av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao15 bitte von den übrigen Antwortoptionen absetzen

tr:

GOTO B11 IF (adcd08a = TRUE OR adcd08b = TRUE OR adcd08c = TRUE OR adcd08d =
TRUE OR adcd08e = TRUE OR adcd08f = TRUE OR adcd08g = TRUE OR adcd08h = TRUE OR
adcd08i = TRUE OR adcd08j = TRUE OR adcd08k = TRUE OR adcd08l = TRUE OR adcd08m
= TRUE OR adcd08n = TRUE) AND (preload01 <> 1) 

GOTO B11 IF (adcd08a = TRUE OR adcd08b = TRUE OR adcd08c = TRUE OR adcd08d =
TRUE OR adcd08e = TRUE OR adcd08f = TRUE OR adcd08g = TRUE OR adcd08h = TRUE OR
adcd08i = TRUE OR adcd08j = TRUE OR adcd08k = TRUE OR adcd08l = TRUE OR adcd08m
= TRUE OR adcd08n = TRUE OR q05a = TRUE or q05b = TRUE OR q05c = TRUE OR q05d = TRUE OR q05e = TRUE OR q05f = TRUE q05g = TRUE OR q05h = TRUE OR q05i = TRUE OR q05j = TRUE OR q05k = TRUE OR q05l = TRUE) AND preload01 = 1

GOTO B14 IF ELSE

hi: ao14 bitte als vorletzte Antwortoption und ao15 ganz zum Schluss (abgesetzt) einblenden (relevant wenn zusätzliche Antwortoptionen der Hochschule eingeblendet werden)

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
adcd09(adcd09a/adcd09b/adcd09c/adcd09d/adcd09e/adcd09f/adcd09g/adcd09h/adcd09i/adcd09j/adcd09k/
adcd09l/adcd09m/adcd09n/adcd09o);q06(q06a/q06b/q06c/q06d/q06e/q06f/q06g/q06h/q06i/q06j/q06k/q06l) 

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: An welchen Kursen oder Lehrveranstaltungen speziell für Promovierende an
Ihrer Hochschule haben Sie teilgenommen?

is: Bitte wählen Sie alles Zutreffende aus.

it: !!Kurse oder Lehrveranstaltungen…!!

ao1: (adcd09a): zur Konferenz- und Tagungsorganisation 

ao2: (adcd09b): im Bereich Personal- und Mitarbeiterführung 

ao3: (adcd09c): zu speziellen Themen meines Promotionsfachs

ao4: (adcd09d): zur Karriereplanung 

ao5: (adcd09e): zum Verfassen englischer Texte (z. B. Scientific Writing Skills
in English) 

ao6: (adcd09f): zu den Regeln guter wissenschaftlicher Praxis

ao7: (adcd09g): im Bereich Wissenschaftskommunikation

ao8: (adcd09h): zum Management von Forschungs-/Drittmittelprojekten

ao9: (adcd09i): zu Moderationstechniken und Gremienleitung

ao10: (adcd09j): zur Präsentation von Forschungsergebnissen

ao11: (adcd09k): zu spezifischen Forschungsmethoden für mein Promotionsfach

ao12: (adcd09l): zum wissenschaftlichen Schreiben (Schreibwerkstätten etc.)

ao13: (adcd09m): zur Entwicklung und Beantragung eines
Forschungs-/Drittmittelprojekts

ao16q: (q06a): im Bereich Zeit-/Selbstmanagement

ao17q: (q06b): im Bereich Projektmanagement

ao18q: (q06c): zum Arbeiten in Teams

ao19q: (q06d): zu Lehr-/Lernkompetenzen (Hochschuldidaktik)

ao20q: (q06e): im Bereich weiterer mündlicher Kommunikationskompetenzen (z. B. Rhetorik, Verhandeln, Argumentation, Small Talk) 

ao21q: (q06f): zu Informations-/Wissenskompetenzen bzw. Recherche

ao22q: (q06g): zu Statistik

ao23q: (q06h): zum (Forschungs-)Datenmanagement

ao24q: (q06i): zum Umgang mit Konflikten

ao25q: (q06j): zu gewerblichem Rechtsschutz (z. B. Patent-/Urheberrecht)

ao26q: (q06k): zu Networking bzw. Selbstmarketing

ao27q: (q06l): Selma-Meyer-Mentoring Programme für Promovierende

ao14: (adcd09n): Sonstiges

ao15: (adcd09o): [adcd08o]

mv:

ka:

vc:

SHOW ao1 IF adcd08a = TRUE

SHOW ao2 IF adcd08b = TRUE

SHOW ao3 IF adcd08c = TRUE

SHOW ao4 IF adcd08d = TRUE

SHOW ao5 IF adcd08e = TRUE

SHOW ao6 IF adcd08f = TRUE

SHOW ao7 IF adcd08g = TRUE

SHOW ao8 IF adcd08h = TRUE

SHOW ao9 IF adcd08i = TRUE

SHOW ao10 IF adcd08j = TRUE

SHOW ao11 IF adcd08k = TRUE

SHOW ao12 IF adcd08l = TRUE

SHOW ao13 IF adcd08m = TRUE

SHOW ao16q IF q05a = TRUE

SHOW ao17q IF q05b = TRUE

SHOW ao18q IF q05c = TRUE

SHOW ao19q IF q05d = TRUE

SHOW ao20q IF q05e = TRUE

SHOW ao21q IF q05f = TRUE

SHOW ao22q IF q05g = TRUE

SHOW ao23q IF q05h = TRUE

SHOW ao24q IF q05i = TRUE

SHOW ao25q IF q05j = TRUE

SHOW ao26q IF q05k = TRUE

SHOW ao27q IF q05l = TRUE


SHOW ao14 IF adcd08n = TRUE AND adcd08o = FALSE

SHOW ao15 IF adcd08n = TRUE AND adcd08o = TRUE

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B12

hi: Wenn der Freitext bei der B10 nicht angegeben wurde aber die Sonstiges, und zwar - Kategorie (adcd08n = TRUE AND adcd08o = FALSE) angeklickt wurde, nur den Text "Sonstiges" aneinblenden (hier: ao14); wenn der Freitext (adcd08o= TRUE) mit angegeben wurde bitte nur diesen losgelöst von "Sonstiges, und zwar:" anzeigen. 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adcd10

qt: offene Frage (number)

hl:

in:

q: An wie vielen Kursen und Lehrveranstaltungen speziell für Promovierende haben
Sie in den vergangenen zwölf Monaten teilgenommen?

is:

it:

ao: 2 cm, [ao] Suffix: [number] Kurs(e)/Lehrveranstaltung(en)

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 99

kh:

fv:

hv:

fo:

tr:

GOTO B13 IF adcd10 \> 0

GOTO B14 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adcd10 \>= 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B12 („Anzahl Kurse“) \>= 1))

vn: adcd11

qt: offene Frage (number)

hl:

in:

q: Wie viele dieser Kurse und Lehrveranstaltungen waren verpflichtend?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Kurs(e)/Lehrveranstaltung(en)

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 99

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe.

fv:

hv:

fo:

tr:

GOTO B14

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adcd12

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Alles in allem, wie zufrieden sind Sie mit dem Kurs- und
Lehrveranstaltungsangebot für Promovierende an Ihrer Hochschule?

is:

it:

ao1: 0 : 0 : : überhaupt nicht zufrieden

ao2: 1 : 1 : :

ao3: 2 : 2 : :

ao4: 3 : 3 : :

ao5: 4 : 4 : :

ao6: 5 : 5 : :

ao7: 6 : 6 : :

ao8: 7 : 7 : :

ao9: 8 : 8 : :

ao10: 9 : 9 : :

ao11: 10 : 10 : völlig zufrieden

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO Q04 IF preload01 = 1

GOTO B15 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________Q04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (IF adbi01 = 1 OR adbi01 = 3) AND preload = 1

((wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und preload01 ("Düsseldorf") = 1)

vn: q07(q07a/q07b/q07c/q07d/q07e/q07f/q07g/q07h/q07i/q07j/q07k/q07l/q07m)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welche der folgenden Beratungsangebote speziell für Promovierende sind Ihnen an Ihrer Hochschule bekannt?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q07a): Beratung/Coaching zu allgemeinen Fragen rund um die Promotion

ao2: (q07b): Beratung/Coaching zu Konflikten im Promotionskontext

ao3: (q07c): Beratung zu Fragen guter wissenschaftlicher Praxis

ao4: (q07d): Beratung/Coaching zur !!akademischen!! Karriereentwicklung

ao5: (q07e): Beratung/Coaching zur !!außerakademischen!! Karriereentwicklung

ao6: (q07f): Schreibberatung/-coaching

ao7: (q07g): Beratung zu Drittmittelanträgen

ao8: (q07h): Beratung für internationale Promovierende

ao9: (q07i): Beratung zur Vereinbarkeit von Beruf und Familie

ao10: (q07j): Beratung/Coaching zur individuellen Karriereentwicklung 

ao11: (q07k): Beratung zu Selbstständigkeit bzw. Firmengründung

ao12: (q07l): Sonstiges, und zwar (q07m): [string] 6 cm


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO Q05 IF q07a = TRUE OR q07b = TRUE OR q07c = TRUE OR q07d = TRUE OR q07e = TRUE OR q07f = TRUE OR q07g = TRUE OR q07h = TRUE OR q07i = TRUE OR q07j = TRUE OR q07k = TRUE OR q07l = TRUE

GOTO B15 IF q07a = FALSE AND q07b = FALSE AND q07c = FALSE AND q07d = FALSE AND q07e = FALSE AND q07f = FALSE AND q07g = FALSE AND q07h = FALSE AND q07i = FALSE AND q07j = FALSE AND q07k = FALSE AND q07l = FALSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________Q05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (IF adbi01 = 1 OR adbi01 = 3) AND preload = 1 AND (q07a = TRUE OR q07b = TRUE OR q07c = TRUE OR q07d = TRUE OR q07e = TRUE OR q07f = TRUE OR q07g = TRUE OR q07h = TRUE OR q07i = TRUE OR q07j = TRUE OR q07k = TRUE OR q07l = TRUE)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und preload01 ("Düsseldorf") = 1 und Q04 ("Beratungsangebote bekannt") eine Antwortoption ausgewählt

vn: q08(q08a/q08b/q08c/q08d/q08e/q08f/q08g/q08h/q08i/q08j/q08k/q08l/q08m)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche Beratungsangebote speziell für Promovierende an ihrer Hochschule haben Sie wahrgenommen? 

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q08a): Beratung/Coaching zu allgemeinen Fragen rund um die Promotion

ao2: (q08b): Beratung/Coaching zu Konflikten im Promotionskontext

ao3: (q08c): Beratung zu Fragen guter wissenschaftlicher Praxis

ao4: (q08d): Beratung/Coaching zur !!akademischen!! Karriereentwicklung

ao5: (q08e): Beratung/Coaching zur !!außerakademischen!! Karriereentwicklung

ao6: (q08f): Schreibberatung/-coaching

ao7: (q08g): Beratung zu Drittmittelanträgen

ao8: (q08h): Beratung für internationale Promovierende

ao9: (q08i): Beratung zur Vereinbarkeit von Beruf und Familie

ao10: (q08j): Beratung/Coaching zur individuellen Karriereentwicklung 

ao11: (q08k): Beratung zu Selbstständigkeit bzw. Firmengründung

ao12: (q08l): Sonstiges 

ao13: (q08m): [q07m]

mv:

ka:

vc:

SHOW ao1 IF q07a = TRUE

SHOW ao2 IF q07b = TRUE

SHOW ao3 IF q07c = TRUE

SHOW ao4 IF q07d = TRUE

SHOW ao5 IF q07e = TRUE

SHOW ao6 IF q07f = TRUE

SHOW ao7 IF q07g = TRUE

SHOW ao8 IF q07h = TRUE

SHOW ao9 IF q07i = TRUE

SHOW ao10 IF q07j = TRUE

SHOW ao11 IF q07k = TRUE

SHOW ao12 IF q07l = TRUE AND q07m = FALSE

SHOW ao13 IF q07l = TRUE AND q07m = TRUE

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B15

hi: Bitte hier die ao12 mit dem Text "Sonstiges" anzeigen, wenn bei der Q04 der Freitext bei der open attached nicht mit angegeben wurde (q07l = TRUE AND q07m = FALSE). Wenn der Freitext angegeben wurde (q07m = TRUE), dann bitte nur diesen bei der ao13 losgelöst von "Sonstiges, und zwar:" anzeigen. 

\-------------------------------------------------------------------------------------------------------------------------------------------------



\__________________________________________B15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adcd13(adcd13a/adcd13b/adcd13c/adcd13d/adcd13e), q09

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Findet Ihre Promotion in Kooperation mit einer oder mehreren externen
Organisationen statt?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adcd13a): Ja, mit einem Unternehmen der Privatwirtschaft.

ao2: (adcd13b): Ja, mit einer außeruniversitären Forschungseinrichtung.

ao2q: (q09): Ja, mit einer Behörde bzw. einer Kulturinstitution.

ao3: (adcd13c): Ja, mit einer sonstigen Organisation, und zwar: (adcd13d):
[string] 6 cm

ao4: (adcd13e): Nein. [EK]

mv:

ka:

vc:

SHOW ao2q IF preload01 = 1

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao4 von den übrigen Antwortoptionen absetzen

tr:

GOTO Q06 IF preload01 = 1 AND adcd13b = TRUE

GOTO Q07 IF (preload01 = 1 AND adcd13b = FALSE AND ((q09 = TRUE) OR (adcd13a = TRUE)))

GOTO B16 IF (adcd13a = TRUE) OR (adcd13b = TRUE) OR (adcd13c = TRUE)

GOTO B18 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________Q06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3 AND preload01 = 1 AND adcd13b = TRUE

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und preload01 ("Düsseldorf") = 1 und B15 = "Ja" ("Ja, mit einer außeruniversitären Forschungseinrichtung")

vn: q10(q10a/q10b/q10c/q10d/q10e/q10f/q10g/q10h/q10i/q10j/q10k)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche Aussagen treffen auf Ihr Promotionsverfahren zu? 

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q10a): Ich habe/hatte einen Arbeitsvertrag an diesem Forschungsinstitut.

ao2: (q10b): Wesentliche Teile der Arbeit finden/fanden an diesem Forschungsinstitut statt.

ao3: (q10c): Die/der Betreuende am freien Forschungsinstitut ist offiziell prüfungsberechtigt an der HHU Düsseldorf (z. B. Professur an der HHU oder dort habilitiert).

ao4: (q10d): Ich habe zudem eine(n) weitere(n) Betreuende(n) bzw. Mentor(in) an der HHU Düsseldorf.

ao5: (q10e): Die/der Betreuende des Forschungsinstitutes wird offiziell Gutachter(in) meiner Dissertation sein.

ao6: (q10f): Die/der Betreuende des Forschungsinstitutes wird Mitglied der Promotionsprüfungskommission sein.

ao7: (q10g): Ich habe eine einzelne Betreuungsvereinbarung mit meinen Betreuenden abgeschlossen, die sowohl von der HHU Düsseldorf als auch dem freien Forschungsinstitut anerkannt wird.

ao8: (q10h): Ich habe eine einzelne Betreuungsvereinbarung mit meinen Betreuenden abgeschlossen, die ausschließlich für die HHU Düsseldorf relevant ist.

ao9: (q10i): Ich habe eine Betreuungsvereinbarung mit meinen Betreuenden abgeschlossen, die ausschließlich für das freie Forschungsinstitut relevant ist.

ao10: (q10j): Ich habe zwei Betreuungsvereinbarungen mit meinen Betreuenden abgeschlossen - eine für die HHU Düsseldorf und eine für das freie Forschungsinstitut. 

ao11: (q10k): Keine der Aussagen trifft auf mein Promotionsverfahren zu. [EK]


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao11 von den übrigen Antwortoptionen absetzen.

tr:

GOTO Q07 IF q09 = TRUE OR adcd13a = TRUE

GOTO B16 IF q09 = FALSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________Q07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND preload01 = 1 AND (q09 = TRUE OR adcd13a = TRUE)

{(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und preload01 ("Düsseldorf") = 1 
und B15 = "Ja" ("Unternehmen der Privatwirtschaft" oder "mit einer Behörde bzw. einer Kulturinstitution")}

vn: q11(q11a/q11b/q11c/q11d/q11e/q11f/q11g/q11h)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche Aussagen treffen auf Ihr Promotionsverfahren zu?  

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (q11a): Ich habe/hatte einen Arbeitsvertrag mit diesem Unternehmen, dieser Behörde bzw. Kulturinstitution etc.

ao2: (q11b): Wesentliche Teile der Arbeit finden/fanden an diesem Unternehmen, dieser Behörde bzw. Kulturinstitution o. Ä.  statt. 

ao3: (q11c): Die/der Betreuende aus diesem Unternehmen, dieser Behörde bzw. Kulturinstitution ist offiziell prüfungsberechtigt an der HHU Düsseldorf (z. B. Professur an der HHU oder dort habilitiert).

ao4: (q11d): Ich habe zudem eine(n) weitere(n) Betreuende(n) bzw. Mentor(in) an der HHU Düsseldorf.

ao5: (q11e): Die/der Betreuende aus dem Unternehmen, der Behörde bzw. Kulturinstitution wird offiziell Gutachter(in) meiner Dissertation sein.

ao6: (q11f): Die/der Betreuende aus dem Unternehmen, der Behörde bzw. Kulturinstitution wird Mitglied der Promotionsprüfungskommission sein. 

ao7: (q11g): Ich habe eine Betreuungsvereinbarung, die sowohl von der Betreuung der HHU Düsseldorf als auch von der Betreuung des Unternehmens, der Behörde bzw. Kulturinstitution unterschrieben ist.

ao8: (q11h): Keine der Aussagen trifft auf mein Promotionsverfahren zu. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao8 von den übrigen Antwortoptionen absetzen.

tr:

GOTO B16

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (adcd13a = TRUE OR adcd13b = TRUE OR
adcd13c = TRUE OR q09 = TRUE)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B15 = „Ja“ („Ja, Unternehmen Privatwirtschaft“ oder „Ja, außeruniversitären
Forschungseinrichtung“ oder „Ja, sonstige Organisation“ oder "Ja, mit einer Behörde bzw. einer Kulturinstitution"))

vn: adcd14

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Entstand der Kontakt zu dem/zu den externen Kooperationspartner(n) bereits
vor dem Beginn Ihrer Promotion?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B17

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B17_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (adcd13a = TRUE OR adcd13b = TRUE OR
adcd13c = TRUE OR q09 = TRUE)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B15 = „Ja“ („Ja, Unternehmen Privatwirtschaft“ oder „Ja, außeruniversitären
Forschungseinrichtung“ oder „Ja, sonstige Organisation“ oder "Ja, mit einer Behörde bzw. einer Kulturinstitution"))

vn: adcd15

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Trägt Ihre Promotion dazu bei, eine für diese Organisation relevante
Fragestellung zu beantworten?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B18

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B18_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder = 2 („abgeschlossen“)
oder 3 („unterbrochen“))

vn: adcd16a/adcd16b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q1: In welcher Form planen Sie Ihre Dissertation zu publizieren?

q2: In welcher Form wird/wurde Ihre Dissertation publiziert?

is:

it:

ao1: (adcd16a): 1 : : In Form einer Monographie

ao2: (adcd16a): 2 : : In Form mehrerer Artikel in Fachjournalen (kumulativ)

ao3: (adcd16a): 3 : : Sonstiges, und zwar: (adcd16b): [string] 6 cm

ao4: (adcd16a): 4 : : Ich bin noch unentschieden./Ich habe mich noch nicht
festgelegt.

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

SHOW ao4 IF adbi01 = 1 OR adbi01 = 3

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B19 IF adbi01 = 1 OR adbi01 = 3

GOTO B21 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B19_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adid04

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Kam/Kommt es vor, dass Sie ernsthaft über einen Abbruch Ihrer Promotion
nachdachten/nachdenken?

is:

it:

ao1: 1 : : niemals

ao2: 2 : : selten

ao3: 3 : : gelegentlich

ao4: 4 : : oft

ao5: 5 : : ständig

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO B20 IF adid04 \> 1

GOTO B21 IF adid04 = 1 OR adid04 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B20_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adid04 \> 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
B19 („Gedanken Abbruch“) = 2 („Selten“), 3 („Gelegentlich“), 4 („Häufig“) oder 5
(„Ständig“))

vn:
adid05(adid05a/adid05b/adid05c/adid05d/adid05e/adid05f/adid05g/adid05h/adid05i/adid05j); q12a/q12b

qt: Matrix mit horizontaler Einfachauswahl und offener ao (string)

hl:

in:

q: Inwieweit spiel(t)en die folgenden Gründe dafür eine Rolle?

is:

it1: (adid05a): Zu hohe Arbeitsbelastung durch berufliche Tätigkeit

it2: (adid05b): Veränderung der Lebenssituation der Partnerin/des Partners (z.
B. neuer Arbeitsplatz)

it3: (adid05c): Vereinbarkeit von Promotion und Familie 

it4: (adid05d): Probleme mit der Betreuung der Promotion

it5: (adid05e): Gesundheitliche Probleme

it6: (adid05f): Aufnahme eines (anderen) Beschäftigungsverhältnisses

it7: (adid05g): Thema hat sich als schwer realisierbar herausgestellt

it8: (adid05h): Zweifel an meiner Eignung für eine Promotion

it9: (adid05i): Mangelndes Interesse am Promotionsthema

it10: (adid05j): Keine ausreichende Finanzierung

it11: (q12a): Sonstiges, und zwar: (q12b) [string] 6 cm

ao1: 1 : 1 : spielt(e) gar keine Rolle

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : spielt(e) eine sehr große Rolle

mv:

ka:

vc:

SHOW it11 IF preload01 = 1

av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao6 von den übrigen absetzen

tr:

GOTO B21

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B21_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01=1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn:
adcd17(adcd17a/adcd17b/adcd17c/adcd17d/adcd17e/adcd17f/adcd17g/adcd17h/adcd17i/adcd17j/adcd17k/adcd17l); q13 

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Ihre Promotionsphase zu?

is:

ka1: !!In meinem wissenschaftlichen Umfeld gibt es immer jemanden, der …!!

it1a: (adcd17a): mir bei inhaltlichen Fragen zu meiner Promotion weiterhilft.

it2a: (adcd17b): mir bei methodischen/technischen Fragen zu meiner Promotion
behilflich ist.

it3a: (adcd17c): mir mit seinem Fachwissen zur Seite steht.

it4a: (adcd17d): mich emotional unterstützt.

it5a: (adcd17e): ein offenes Ohr für meine Sorgen hat.

it6a: (adcd17f): mir in schwierigen Zeiten Mut macht.

it7a: (adcd17g): mir Kontakte zu Forscher(inne)n an anderen Hochschulen und
Forschungseinrichtungen vermittelt.

it8a: (adcd17h): mir Kontakte zu Personen vermittelt, die für mein
Forschungsthema besonders relevant sind.

it9a: (adcd17i): mich bei dem Ausbau meiner wissenschaftlichen Kontakte und
Netzwerke unterstützt.

it10a: (adcd17j): mir bei der Karriereplanung hilft.

it11a: (adcd17k): mir Tipps für meine berufliche Zukunft gibt.

it12a: (adcd17l): mir Kontakte zu Personen verschafft, die meine berufliche
Karriere positiv beeinflussen könnten.

it13a: (q13): mir Zugang zu benötigten Ressourcen vermittelt. 


ka2: !!In meinem wissenschaftlichen Umfeld gab es immer jemanden, der …!!

it1b: (adcd17a): mir bei inhaltlichen Fragen zu meiner Promotion weiterhalf.

it2b: (adcd17b): mir bei methodischen/technischen Fragen zu meiner Promotion
behilflich war.

it3b: (adcd17c): mir mit seinem Fachwissen zur Seite stand.

it4b: (adcd17d): mich emotional unterstützt hat.

it5b: (adcd17e): ein offenes Ohr für meine Sorgen hatte.

it6b: (adcd17f): mir in schwierigen Zeiten Mut machte.

it7b: (adcd17g): mir Kontakte zu Forscherinnen/Forschern an anderen Hochschulen
und Forschungseinrichtungen vermittelte.

it8b: (adcd17h): mir Kontakte zu Personen vermittelte, die für mein
Forschungsthema besonders relevant waren.

it9b: (adcd17i): mich bei dem Ausbau meiner wissenschaftlichen Kontakte und
Netzwerke unterstützte.

it10b: (adcd17j): mir bei der Karriereplanung half.

it11b: (adcd17k): mir Tipps für meine berufliche Zukunft gab.

it12b: (adcd17l): mir Kontakte zu Personen verschaffte, die meine berufliche
Karriere positiv beeinflussen konnten.

it13b: (q13): mir Zugang zu benötigten Ressourcen vermittelte.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

SHOW ka1 AND it1a – it12a IF adbi01 = 1 OR adbi01 = 3

SHOW it13a IF (adbi01 = 1 OR adbi01 = 3) AND preload01 = 1


SHOW ka2 AND it1b - it12b IF adbi01 = 2

SHOW it13b IF adbi01 = 2 AND preload01 = 1

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B22

hi: Gleiche Variablen werden bei den Items erhoben, nur der Text ist in
verschiedenen Zeitformen

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B22_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: adsv01(adsv01a/adsv01b/adsv01c/adsv01d/adsv01e/adsv01f)

qt: Matrix mit horizontaler Einfachauswahl

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Ihre Promotionsphase zu?

is:

it1a: (adsv01a): Die Betreuung meiner Promotion ist voraussichtlich über den gesamten
Promotionszeitraum gewährleistet.

it2a: (adsv01b): Es gibt/gab Phasen während meiner Promotion, in denen ich nicht
ausreichend betreut werde/wurde.

it3a: (adsv01c): Ich muss(te) mich während meiner Promotionsphase nach
alternativen Betreuungsmöglichkeiten umsehen.

it4a: (adsv01d): Mein(e) Betreuer(in) stellt an mich den Anspruch, fortlaufend
über den Stand meiner Promotion informiert zu werden.

it5a: (adsv01e): Es gibt regelmäßige, feste Termine mit der/dem Betreuer(in), um
den Stand der Promotion zu besprechen.

it6a: (adsv01f): Ich muss bei meiner/meinem Betreuer(in) häufig Rechenschaft
über den Stand meiner Promotion ablegen.

it1b: (adsv01a): Die Betreuung meiner Promotion war über den gesamten
Promotionszeitraum gewährleistet.

it2b: (adsv01b): Es gab Phasen während meiner Promotion, in denen ich nicht
ausreichend betreut wurde.

it3b: (adsv01c): Ich musste mich während meiner Promotionsphase nach
alternativen Betreuungsmöglichkeiten umsehen.

it4b: (adsv01d): Mein(e) Betreuer(in) hat an mich den Anspruch gestellt,
fortlaufend über den Stand meiner Promotion informiert zu werden.

it5b: (adsv01e): Es gab regelmäßige, feste Termine mit der/dem Betreuer(in), um
den Stand der Promotion zu besprechen.

it6b: (adsv01f): Ich musste bei meiner/meinem Betreuer(in) häufig Rechenschaft
über den Stand meiner Promotion ablegen.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

SHOW it1a - it6a IF adbi01 = 1 OR adbi01 = 3

SHOW it1b - it6b IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B23 IF adbi01 = 1 OR adbi01 = 3

GOTO B35 IF adbi01 = 2

hi: Gleiche Variablen werden bei den Items erhoben, nur der Text ist in
verschiedenen Zeitformen

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B23_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adsv02

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie eine Promotions- bzw. Betreuungsvereinbarung getroffen?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B24 IF adsv02 = 1

GOTO B25 IF adsv02 = 2 OR adsv02 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B24_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv02 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
B23 („Promotionsvereinbarung“) = 1 („Ja“))

vn:
adsv03(adsv03a/adsv03b/adsv03c/adsv03d/adsv03e/adsv03f/adsv03g/adsv03h/adsv03i/adsv03j/adsv03k/adsv03l/adsv03m/adsv03n); q14

qt: Matrix mit horizontaler Einfachauswahl und offener ao (string)

hl:

in:

q: Welche Inhalte wurden in welcher Form vereinbart?

is:

it1: (adsv03a): Ein Arbeitstitel

it2: (adsv03b): Die Betreuer(innen)

it3: (adsv03c): Ein Zeitplan für die Erstellung der Dissertationsschrift

it4: (adsv03d): Ein Termin für die Abgabe

it5: (adsv03e): Regelmäßige Berichtspflichten zum Stand der Promotion
(Zwischenziele, Meilensteine, Lernziele)

it6: (adsv03f): Zeitliche Ressourcen/Freiräume zum Promovieren

it7: (adsv03g): Die Publikation von Zwischenergebnissen

it8: (adsv03h): Regeln guter wissenschaftlicher Praxis

it9: (adsv03i): Verfahren in Konfliktfällen

it10: (adsv03j): Ressourcen, die zur Verfügung gestellt werden (z. B. Software,
Zugang zum Labor, studentische Hilfskräfte)

it11: (adsv03k): Die Finanzierung von Publikationen

it12: (adsv03l): Die Finanzierung von Konferenzteilnahmen

it12q: (q14): Bedingungen, die aus Perspektive der Betreuung für einen erfolgreichen Abschluss erfüllt werden müssen

it13: (adsv03m): Sonstiges, und zwar: (adsv03n): [string] 6 cm


ao1: 1 : : schriftlich vereinbart

ao2: 2 : : mündlich vereinbart

ao3: 3 : : nicht vereinbart

mv:

ka:

vc:

SHOW it12q IF preload01 = 1

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B25

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B25_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adsv04

qt: offene Frage (number)

hl:

in:

q: Wie viele Personen betreuen aktuell Ihr Promotionsvorhaben?

is: Bitte beziehen Sie alle Personen ein, die Ihre Promotion faktisch
(mit-)betreuen, auch wenn diese keine offiziellen Gutachter(innen) sind.

it:

ao1: 1 cm, [ao] Suffix: [number] Person(en)

mv:

ka:

vc:

av: number : \<= 1 stellig : 0 TO 9

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe.

fv:

hv:

fo:

tr:

GOTO B26 IF adsv04 \> 0

GOTO B35 IF adsv04 = 0 OR adsv04 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B26_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv04 \>= 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B25 (Anzahl der Betreuer \>= 1 (mehr als 1 Betreuer))

vn1: adsv05a (adsv05aa/advs05ab)

vn2: adsv05b (adsv05ba/adsv05bb)

vn3: adsv05c (adsv05ca/adsv05cb)

qt: Comparison mit offener Angabe (string)

hl:

in: Bitte denken Sie an die drei wichtigsten Betreuer(innen) und machen Sie
nachfolgend Angaben zu diesen drei Personen.

q1: An welcher Hochschule/Einrichtung sind Ihre Betreuer(innen) (überwiegend)
tätig?

q2: An welcher Hochschule/Einrichtung ist Ihr(e) Betreuer(in) (überwiegend)
tätig?

is:

it:

mv:

ka1: (adsv05a): !!Betreuer(in) 1!!

ao1: (adsv05aa): 1 : : Hochschule, an der ich promoviere

ao2: (adsv05aa): 2 : : An einer anderen Hochschule oder Forschungseinrichtung,
und zwar: (adsv05ab): [string] 6 cm

ka2: (adsv05b): !!Betreuer(in) 2!!

ao1: (adsv05ba): 1 : : Hochschule, an der ich promoviere

ao2: (adsv05ba): 2 : : An einer anderen Hochschule oder Forschungseinrichtung,
und zwar: (adsv05bb): [string] 6 cm

ka3: (adsv05c): !!Betreuer(in) 3!!

ao1: (adsv05ca): 1 : : Hochschule, an der ich promoviere

ao2: (adsv05ca): 2 : : An einer anderen Hochschule oder Forschungseinrichtung,
und zwar: (adsv05cb): [string] 6 cm

vc:

SHOW in IF adsv04 \> 3

SHOW q1 IF adsv04 \>= 2

SHOW ka1 AND ka2 IF adsv04 = 2

SHOW ka1 AND ka2 AND ka3 IF adsv04 \>= 3

SHOW q2 IF adsv04 = 1

SHOW ka1 IF adsv04 = 1

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B27

hi: Die Variablenendung (das erste) a (nach den ersten 6 Zeichen) bezieht sich
auf den 1. Betreuer, das zweite (a) auf die Antwortoptionen (ao1 oder ao2) und
(das zweite) b auf die offene Angabe; das (erste) b auf den 2. Betreuer etc.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B27_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv04 \>= 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B25 (Anzahl der Betreuer \>= 1 (mehr als 1 Betreuer))

vn1: adsv06a

vn2: adsv06b

vn3: adsv06c

qt: Comparison

hl:

in:

q1: Welches Geschlecht haben Ihre Betreuer(innen)?

q2: Welches Geschlecht hat Ihr(e) Betreuer(in)?

is:

it:

mv:

ka1: (adsv06a): !!Betreuer(in) 1!!

ao1: (adsv06a): 1 : : Weiblich

ao2: (adsv06a): 2 : : Männlich

ka2: (adsv06b): !!Betreuer(in) 2!!

ao1: (adsv06b): 1 : : Weiblich

ao2: (adsv06b): 2 : : Männlich

ka3: (adsv06c): !!Betreuer(in) 3!!

ao1: (adsv06c): 1 : : Weiblich

ao2: (adsv06c): 2 : : Männlich

vc:

SHOW q1 IF adsv04 \>= 2

SHOW ka1 AND ka2 IF adsv04 = 2

SHOW ka1 AND ka2 AND ka3 IF adsv04 \>= 3

SHOW q2 IF adsv04 = 1

SHOW ka1 IF adsv04 = 1

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B28

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B28_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv04 \>= 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B25 (Anzahl der Betreuer \>= 1 (mehr als 1 Betreuer))

vn1: adsv07a

vn2: adsv07b

vn3: adsv07c

qt: Comparison

hl:

in:

q1: Welchen formalen Betreuungsstatus haben Ihre Betreuer(innen)?

q2: Welchen formalen Betreuungsstatus hat Ihr(e) Betreuer(in)?

is:

it:

mv:

ka1: (adsv07a): !!Betreuer(in) 1!!

ao1: (adsv07a): 1 : : Erstbetreuer(in)/Erstgutachter(in)

ao2: (adsv07a): 2 : : Zweitbetreuer(in)/Zweitgutachter(in)

ao3: (adsv07a): 3 : : Sonstige(r) offizielle(r) Betreuer(in)/Gutachter(in)

ao4: (adsv07a): 4 : : Nicht-offizielle(r) Betreuer(in)

ka2: (adsv07b): !!Betreuer(in) 2!!

ao1: (adsv07b): 1 : : Erstbetreuer(in)/Erstgutachter(in)

ao2: (adsv07b): 2 : : Zweitbetreuer(in)/Zweitgutachter(in)

ao3: (adsv07b): 3 : : Sonstige(r) offizielle(r) Betreuer(in)/Gutachter(in)

ao4: (adsv07b): 4 : : Nicht-offizielle(r) Betreuer(in)

ka3: (adsv07c): !!Betreuer(in) 3!!

ao1: (adsv07c): 1 : : Erstbetreuer(in)/Erstgutachter(in)

ao2: (adsv07c): 2 : : Zweitbetreuer(in)/Zweitgutachter(in)

ao3: (adsv07c): 3 : : Sonstige(r) offizielle(r) Betreuer(in)/Gutachter(in)

ao4: (adsv07c): 4 : : Nicht-offizielle(r) Betreuer(in)

vc:

SHOW q1 IF adsv04 \>= 2

SHOW ka1 AND ka2 IF adsv04 = 2

SHOW ka1 AND ka2 AND ka3 IF adsv04 \>= 3

SHOW q2 IF adsv04 = 1

SHOW ka1 IF adsv04 = 1

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B29

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B29_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv04 \>= 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B25 (Anzahl der Betreuer \>= 1 (mindestens 1 Betreuer))

vn1: adsv08a (adsv08aa/adsv08ab)

vn2: adsv08b (adsv08ba/adsv08bb)

vn3: adsv08c (adsv08ca/adsv08cb)

qt: Comparison mit offener ao (string)

hl:

in:

q1: Welche Positionen haben Ihre Betreuer(innen)?

q2: Welche Position hat Ihr(e) Betreuer(in)?

is:

it:

mv:

ka1: (adsv08a): !!Betreuer(in) 1!!

ao1: (adsv08aa): 1 : : Professor(in)

ao2: (adsv08aa): 2 : : Privatdozent(in)

ao3: (adsv08aa): 3 : : Juniorprofessor(in)

ao4: (adsv08aa): 4 : : Nachwuchsgruppenleiter(in)

ao5: (adsv08aa): 5 : : Postdoc

ao6: (adsv08aa): 6 : : Andere(r) Doktorand(in)

ao7: (adsv08aa): 7 : : Sonstige, und zwar: (adsv08ab): [string] 6 cm

ka2: (adsv08b): !!Betreuer(in) 2!!

ao1: (adsv08ba): 1 : : Professor(in)

ao2: (adsv08ba): 2 : : Privatdozent(in)

ao3: (adsv08ba): 3 : : Juniorprofessor(in)

ao4: (adsv08ba): 4 : : Nachwuchsgruppenleiter(in)

ao5: (adsv08ba): 5 : : Postdoc

ao6: (adsv08ba): 6 : : Andere(r) Doktorand(in)

ao7: (adsv08ba): 7 : : Sonstige, und zwar: (adsv08bb): [string] 6 cm

ka3: (adsv08c): !!Betreuer(in) 3!!

ao1: (adsv08ca): 1 : : Professor(in)

ao2: (adsv08ca): 2 : : Privatdozent(in)

ao3: (adsv08ca): 3 : : Juniorprofessor(in)

ao4: (adsv08ca): 4 : : Nachwuchsgruppenleiter(in)

ao5: (adsv08ca): 5 : : Postdoc

ao6: (adsv08ca): 6 : : Andere(r) Doktorand(in)

ao7: (adsv08ca): 7 : : Sonstige, und zwar: (adsv08cb): [string] 6 cm

vc:

SHOW q1 IF adsv04 \>= 2

SHOW ka1 AND ka2 IF adsv04 = 2

SHOW ka1 AND ka2 AND ka3 IF adsv04 \>= 3

SHOW q2 IF adsv04 = 1

SHOW ka1 IF adsv04 = 1

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B30 IF adsv04 \> 1

GOTO B31 IF adsv04 = 1

hi: Die Variablenendung (das erste) a (nach den ersten 6 Zeichen) bezieht sich
auf den 1. Betreuer, das zweite (a) auf die Antwortoptionen (ao1 oder ao2) und
(das zweite) b auf die offene Angabe; das (erste) b auf den 2. Betreuer etc.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B30_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adsv04 \> 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
B25 (Anzahl der Betreuer \>= 1 (mehr als 1 Betreuer))

vn: adsv09

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wer ist Ihr(e) Hauptbetreuer(in)?

is: Gemeint ist die Person, die Ihre Arbeit im Alltag am intensivsten betreut.
Diese Person muss nicht dieselbe sein, die Ihre Promotion offiziell betreut
(Erstbetreuer(in)/Erstgutachter(in)).

it:

ao1: 1 : : Betreuer(in) 1: [adsv08aa OR adsv08ab] und Ihr(e) [adsv07a], [adsv06a], [adsv05aa OR adsv05ab]

ao2: 2 : : Betreuer(in) 2: [adsv08ba OR adsv08bb] und Ihr(e) [adsv07b], [adsv06b], [adsv05ba OR adsv05bb]

ao3: 3 : : Betreuer(in) 3: [adsv08ca OR adsv08cb] und Ihr(e) [adsv07c], [adsv06c], [adsv05ca OR adsv05cb]

ao4: 4 : : Jemand anderes

mv:

ka:

vc:

SHOW ao1 AND ao4 IF adsv04 = 1

SHOW ao1 AND ao2 AND ao4 IF adsv04 = 2

SHOW ao1 – ao4 IF adsv04 =\> 3

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B31

hi: Die Variablen bei den Antwortoptionen (ao1 – ao3) nur einblenden, wenn eine
Angabe vorliegt; bei adsv05ab, adsv05bb und adsv05cb bitte nur den Freitext eingeben und Präfix "An einer anderen Hochschule oder Forschungseinrichtung, und zwar:" abschneiden, wenn kein Freitext vorhanden ist, dann bitte nur das Präfix anzeigen. 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B31_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND ((adsv04 = 1) OR (adsv04 \> 1 AND adsv09
\<\> SYSMISS))

(wenn (A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
(B25 (Anzahl der Betreuer = 1 (genau 1 Betreuer) oder (B25 (Anzahl der Betreuer
\> 1 und B30 \<\> SYSMISS)))

vn: adsv10

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q1: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrer Betreuerin
über Ihre Promotion ausgetauscht?

q2: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrem Betreuer
über Ihre Promotion ausgetauscht?

q3: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrer
Betreuerin bzw. Ihrem Betreuer über Ihre Promotion ausgetauscht?

q4: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrer
Hauptbetreuerin über Ihre Promotion ausgetauscht?

q5: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrem
Hauptbetreuer über Ihre Promotion ausgetauscht?

q6: Wie häufig haben Sie sich in den letzten zwölf Monaten mit Ihrer
Hauptbetreuerin bzw. Ihrem Hauptbetreuer über Ihre Promotion ausgetauscht?

is:

it:

ao1: 1 : : seltener als einmal pro Semester

ao2: 2 : : etwa einmal im Semester

ao3: 3 : : mehrmals im Semester

ao4: 4 : : einmal pro Woche

ao5: 5 : : mehrmals pro Woche

mv:

ka:

vc:

SHOW q1 IF adsv04 = 1 AND adsv06a = 1

SHOW q2 IF adsv04 = 1 AND adsv06a = 2

SHOW q2 IF adsv04 = 1 AND adsv06a = SYSMISS

SHOW q4 IF adsv04 > 1 AND ((adsv09 = 1 AND adsv06a = 1) OR (adsv09 = 2 AND adsv06b = 1) OR
(adsv09 = 3 AND adsv06c = 1))

SHOW q5 IF adsv04 > 1 AND ((adsv09 = 1 AND adsv06a = 2) OR (adsv09 = 2 AND adsv06b = 2) OR
(adsv09 = 3 AND adsv06c = 2))

SHOW q6 IF adsv04 > 1 AND adsv09 = 4

av:

kh:

fv:

hv:

fo:

tr:

GOTO B32

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B32_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adsv11(adsv11a/adsv11b/adsv11c/adsv11d/adsv11e/adsv11f/adsv11g)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q1: Wie nehmen Sie das Verhalten Ihrer Betreuerin Ihnen gegenüber wahr?

Meine Betreuerin …

q2: Wie nehmen Sie das Verhalten Ihres Betreuers Ihnen gegenüber wahr?

Mein Betreuer …

q3: Wie nehmen Sie das Verhalten Ihrer Betreuerin bzw. Ihres Betreuers
Ihnen gegenüber wahr?

Mein(e) Betreuer(in) …

q4: Wie nehmen Sie das Verhalten Ihrer Hauptbetreuerin Ihnen gegenüber wahr?

Meine Hauptbetreuerin …

q5: Wie nehmen Sie das Verhalten Ihres Hauptbetreuers Ihnen gegenüber wahr?

Mein Hauptbetreuer …

q6: Wie nehmen Sie das Verhalten Ihrer Hauptbetreuerin bzw. Ihres Hauptbetreuers
Ihnen gegenüber wahr?

Mein(e) Hauptbetreuer(in) …

is:

it1: (adsv11a): verhält sich engagiert.

it2: (adsv11b): verhält sich fürsorglich.

it3: (adsv11c): gibt mir eine klare Richtung vor.

it4: (adsv11d): lässt mir große Freiräume.

it5: (adsv11e): führt mit mir Gespräche auf Augenhöhe.

it6a: (adsv11f): wartet, bis ich auf sie zukomme.

it6b: (adsv11f): wartet, bis ich auf ihn zukomme.

it6c: (adsv11f): wartet, bis ich auf sie/ihn zukomme.

it7: (adsv11g): inspiriert mich.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

SHOW q1 IF adsv04 = 1 AND adsv06a = 1

SHOW q2 IF adsv04 = 1 AND adsv06a = 2

SHOW q3 IF (adsv09 = 1 AND adsv06a = 1) OR (adsv09 = 2 AND adsv06b = 1) OR
(adsv09 = 3 AND adsv06c = 1)

SHOW q4 IF (adsv09 = 1 AND adsv06a = 2) OR (adsv09 = 2 AND adsv06b = 2) OR
(adsv09 = 3 AND adsv06c = 2)

SHOW q5 IF adsv09 = 4

SHOW it6a IF (adsv04 = 1 AND adsv06a = 1) OR (adsv09 = 1 AND adsv06a = 1) OR
(adsv09 = 2 AND adsv06b = 1) OR (adsv09 = 3 AND adsv06c = 1)

SHOW it6b IF (adsv04 = 1 AND adsv06a = 2) OR (adsv09 = 1 AND adsv06a = 2) OR
(adsv09 = 2 AND adsv06b = 2) OR (adsv09 = 3 AND adsv06c = 2)

SHOW it6c IF adsv09 = 4  ### hier fehlt noch eine Aktualisierung: ODER-Verknüpfung der beiden Visible Conditions für q3 und q6

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B33

hi: Nur Item 6 ändert sich im Wording

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B33_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adsv12(adsv12a/adsv12b/adsv12c)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

is:

q1: Wie zufrieden sind Sie …

it1a_1: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihre Betreuerin?

it1a_2: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihren Betreuer?

it2: (adsv12b): mit den Angeboten für Promovierende an Ihrer Hochschule?

it3: (adsv12c): mit der Betreuung Ihrer Promotion im Allgemeinen?

q2: Wie zufrieden sind Sie …

it1b_1: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihre Hauptbetreuerin?

it1b_2: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihren Hauptbetreuer?

it2: (adsv12b): mit den Angeboten für Promovierende an Ihrer Hochschule?

it3: (adsv12c): mit der Betreuung Ihrer Promotion im Allgemeinen?

q3: Wie zufrieden sind Sie …

it1a: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihre(n)
Hauptbetreuer(in)?

it1b: (adsv12a): mit der Betreuung Ihrer Promotion durch Ihre(n)
Betreuer(in)?

it2: (adsv12b): mit den Angeboten für Promovierende an Ihrer Hochschule?

it3: (adsv12c): mit der Betreuung Ihrer Promotion im Allgemeinen?

ao1: 1 : 1 : gar nicht zufrieden

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr zufrieden

mv:

ka:

vc:  

SHOW q1 IF adsv04 = 1

SHOW it1a_1 IF adsv04 = 1 AND adsv06a = 1

SHOW it1a_2 IF adsv04 = 1 AND adsv06a = 2

SHOW q2 IF adsv04 \>= 2

SHOW it1b_1 IF (adsv09 = 1 AND adsv06a = 1) OR (adsv09 = 2 AND adsv06b = 1) OR
(adsv09 = 3 AND adsv06c = 1)

SHOW it1b_2 IF (adsv09 = 1 AND adsv06a = 2) OR (adsv09 = 2 AND adsv06b = 2) OR
(adsv09 = 3 AND adsv06c = 2)

SHOW q3 AND it1 IF adsv09 = 4

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B34

hi: Nur das Item 1 (it1, it1a, it1b) ändert sich im Wording

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B34_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adsv13

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q1: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihre Betreuerin als Person?

q2: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihr Betreuer als Person?

q3: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihr(e) Betreuer(in) als Person?

q4: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihre Hauptbetreuerin als Person?

q5: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihr Hauptbetreuer als Person?

q6: Abgesehen von Ihrer Zufriedenheit mit der Betreuung: Wie sympathisch ist
Ihnen Ihr(e) Hauptbetreuer(in) als Person?

is:

it:

ao1: 1 : 1 : äußerst unsympathisch

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : :

ao6: 6 : 6 : :

ao7: 7 : 7 : : äußerst sympathisch

mv:

ka:

vc: ### müssen angepasst werden!

SHOW q1 IF adsv04 = 1 AND adsv06a = 1

SHOW q2 IF adsv04 = 1 AND adsv06a = 2

SHOW q4 IF (adsv09 = 1 AND adsv06a = 1) OR (adsv09 = 2 AND adsv06b = 1) OR
(adsv09 = 3 AND adsv06c = 1)

SHOW q5 IF (adsv09 = 1 AND adsv06a = 2) OR (adsv09 = 2 AND adsv06b = 2) OR
(adsv09 = 3 AND adsv06c = 2)

SHOW q6 IF adsv09 = 4

av:

kh:

fv:

hv:

fo:

tr:

GOTO B35

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B35_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3 

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: adcd18

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Sind Sie mit den Regelungen zu guter wissenschaftlicher Praxis vertraut?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B36 IF adcd18 = 1

GOTO K03 IF ((adcd18 = 2 OR adcd18 = SYSMISS) AND preload01 = 2)

GOTO B38 IF adcd18 = 2 OR adcd18 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B36_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3 OR ) AND adcd18 = 1

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 2 ("abgeschlossen") oder 3 („unterbrochen“)} und
{B35 („Regeln guter wissenschaftlicher Praxis“) = 1 („Ja“)})

vn: adcd19

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Erhalten Sie durch Ihre Hochschule Unterstützung bei der Einhaltung der
Regeln guter wissenschaftlicher Praxis?

q1: Erhielten Sie während Ihrer Promotion durch Ihre Hochschule Unterstützung bei der Einhaltung der
Regeln guter wissenschaftlicher Praxis?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

SHOW q IF adbi01 = 1 OR adbi01 = 3

SHOW q1 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B37 IF adcd19 = 1

GOTO K03 IF preload01 = 2 

GOTO B38 IF adcd19 = 2 OR adcd19 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B37_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND (adcd18 = 1 AND adcd19 = 1)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 2 ("abgeschlossen") oder 3 („unterbrochen“)} und
{B35 („Regeln guter wissenschaftlicher Praxis“) = 1 („Ja“)} und {B36
(„Unterstützung Einhaltung gute wissenschaftliche Praxis“) = 1 („Ja“)})

vn: adcd20

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie zufrieden sind Sie mit der Unterstützung, die Regeln guter
wissenschaftlicher Praxis einzuhalten?

q1: Wie zufrieden waren Sie während Ihrer Promotion mit der Unterstützung, die Regeln guter
wissenschaftlicher Praxis einzuhalten?

is:

it:

ao1: 1 : 1 : gar nicht zufrieden

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr zufrieden

mv:

ka:

vc:

SHOW q IF adbi01 = 1 OR adbi01 = 3

SHOW q1 IF adbi01 = 2

av:

kh:

fv:

hv:

fo:

tr:

GOTO K03 IF preload01 = 2

GOTO B38

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________K03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 

(wenn preload01 = 2 ("Kiel")) 

vn: k03

qt: Einfachauswahl mit vertikalen ao

hl:

in1: Für Promovierende der Christian-Albrechts-Universität zu Kiel haben wir noch vier weitere Fragen zu diesem Thema. 
„Gute Wissenschaftliche Praxis“ beschreibt den verantwortlichen Umgang mit der Forschung, das Erkennen und Minimieren von Forschungsrisiken, die Dokumentation dieser Risiken, eine seriöse Veröffentlichungspraxis, sowie die Aufklärung und Schulung von wissenschaftlichem Nachwuchs.

q1: Bitte geben Sie den Zeitpunkt in Bezug auf Ihre Promotion an, an dem Sie zum ersten Mal Informationen zum Thema „Gute Wissenschaftliche Praxis“ erhalten haben.

in2: Für ehemalige Promovierende der Christian-Albrechts-Universität zu Kiel haben wir vier (weitere) Fragen zum Thema "gute wissenschaftliche Praxis". 
„Gute Wissenschaftliche Praxis“ beschreibt den verantwortlichen Umgang mit der Forschung, das Erkennen und Minimieren von Forschungsrisiken, die Dokumentation dieser Risiken, eine seriöse Veröffentlichungspraxis, sowie die Aufklärung und Schulung von wissenschaftlichem Nachwuchs.

q2: Bitte geben Sie den Zeitpunkt in Bezug auf Ihre Promotion an, an dem Sie zum ersten Mal Informationen zum Thema „Gute Wissenschaftliche Praxis“ erhalten haben.

is:

it:

ao1: 1 :  : vorher

ao2: 2 :  : zu Beginn

ao3: 3 :  : währenddessen

ao4a: 4 :  : bisher noch nicht

ao4b: 4 :  : zum Ende




mv:

ka:

vc:

SHOW in1 AND q1 AND ao4a IF adbi01 = 1 OR adbi01 = 3

SHOW in2 AND q2 AND ao4b IF adbi01 = 2 OR adbi01 = 4

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO K04


hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 

(wenn preload01 = 2 ("Kiel")) 

vn: k04a/k04b/k04c/k04d/k04e/k04f

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welche Personen und/oder Einrichtungen der CAU haben Ihnen Informationen zum Thema „Gute Wissenschaftliche Praxis“ zukommen lassen?

is:

it:

ao1: (k04a): Betreuende und/oder Lehrende während des Bachelorstudium 

ao2: (k04b): Betreuende und/oder Lehrende während des Masterstudiums 

ao3: (k04c): Betreuende und/oder Lehrende während der Promotion

ao4: (k04d): Veranstaltungen durch Graduiertenkolleg, Sonderforschungsbereich, Graduiertenschule oder Promotionsprogramm, Graduiertenzentrum

ao5: (k04e): Sonstiges, und zwar: (k04f): [string] 8 cm


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO K05

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 

(wenn preload01 = 2 ("Kiel")) 

vn: k05

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wurden Sie zum Thema „Gute Wissenschaftliche Praxis“ bis zum jetzigen Zeitpunkt ausreichend informiert?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO K06 IF k05 = 2

GOTO B38 IF k05 = 1 OR k05 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2 

(wenn preload01 = 2 ("Kiel")) 

vn: k06

qt: offene Frage (string) 

hl:

in:

q: Warum fühlen Sie sich nicht ausreichend informiert? 

is:

it:

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO B38

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________B38_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn:
afin01(afin01a/afin01b/afin01c/afin01d/afin01e/afin01f/afin01g/afin01h/afin01i/afin01j/afin01k/afin01l/afin01m)

qt: Mehrfachauswahl mit vertikalen ao und 2 offenen ao (string)

hl:

in:

q1: Wie finanzieren Sie Ihren Lebensunterhalt im aktuellen Semester?

q2: Wie haben Sie während Ihrer Promotion Ihren Lebensunterhalt finanziert?

is: Bitte wählen Sie alles Zutreffende aus.

it1: (afin01a): Durch eine Beschäftigung an einer Hochschule oder
Forschungseinrichtung

it2: (afin01b): Durch eine Beschäftigung außerhalb einer Hochschule oder
Forschungseinrichtung

it3: (afin01c): Durch Selbstständigkeit bzw. freiberufliche Tätigkeit !!mit!!
Forschungs- oder Entwicklungsbezug

it4: (afin01d): Durch Selbstständigkeit bzw. freiberufliche Tätigkeit !!ohne!!
Forschungs- oder Entwicklungsbezug

it5: (afin01e): Durch eine sonstige Beschäftigung (z. B. Referendariat,
Volontariat, Traineeship), und zwar: (afin01f): [string] 6 cm

it6: (afin01g): Durch ein Stipendium

it7: (afin01h): Durch Arbeitslosengeld I oder II

it8: (afin01i): Durch Elterngeld, Erziehungsgeld, Mutterschaftsgeld während des
Mutterschutzes

it9: (afin01j): Durch Geldbeträge von der/dem Partner(in), den Eltern oder
Verwandten

it10: (afin01k): Aus sonstigen Quellen (Vermögensanlagen, Ersparnisse,
Versicherungen oder Darlehen)

it11: (afin01l): Durch Sonstiges, und zwar: (afin01m): [string] 6 cm

ao:

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2 OR adbi01 = 4

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B39 IF afin01i = TRUE

GOTO C48 IF adbi01 = 2

GOTO K07 IF preload01 = 2 AND adbi01 = 4

GOTO E01 IF adbi01 = 4

GOTO B40 IF afin01g = TRUE

GOTO B41 IF afin01g = FALSE

GOTO C48 IF ELSE

hi: IF SET COUNT (Zusammenzählen der Antworten): h_multicontext

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B39_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF afin01i = TRUE

(wenn B38 („Finanzierung“) "Elterngeld, Erziehungsgeld, Mutterschaftsgeld“))

vn:
afin02(afin02a/afin02b/afin02c/afin02d/afin02e/afin02f/afin02g/afin02h/afin02i/afin02j/afin02k/afin02l)

qt: Mehrfachauswahl mit vertikalen ao und 2 offenen ao (string)

hl:

in:

q: Wie haben Sie sich unmittelbar vor Beginn Ihrer Elternzeit finanziert?

is: Bitte wählen Sie alles Zutreffende aus.

it1: (afin02a): Durch eine Beschäftigung an einer Hochschule oder
Forschungseinrichtung

it2: (afin02b): Durch eine Beschäftigung außerhalb einer Hochschule oder
Forschungseinrichtung

it3: (afin02c): Durch Selbstständigkeit bzw. freiberufliche Tätigkeit !!mit!!
Forschungs- oder Entwicklungsbezug

it4: (afin02d): Durch Selbstständigkeit bzw. freiberufliche Tätigkeit !!ohne!!
Forschungs- oder Entwicklungsbezug

it5: (afin02e): Durch eine sonstige Beschäftigung (z. B. Referendariat,
Volontariat, Traineeship), und zwar: (afin02f): [string] 6 cm

it6: (afin02g): Durch ein Stipendium

it7: (afin02h): Durch Arbeitslosengeld I oder II

it8: (afin02i): Durch Geldbeträge von der/dem Partner(in), den Eltern oder
Verwandten

it9: (afin02j): Aus sonstigen Quellen (Vermögensanlagen, Ersparnisse,
Versicherungen oder Darlehen)

it10: (afin02k): Durch Sonstiges, und zwar: (afin02l): [string] 6 cm

ao:

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C48 IF adbi01 = 2

GOTO K07 IF adbi01 = 4 AND preload01 = 2

GOTO E01 IF adbi01 = 4

GOTO B40 IF afin01g = TRUE OR afin02g = TRUE

GOTO B41 IF afin01g = FALSE AND afin02g = FALSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B40_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01g = TRUE OR afin02g = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) = “Stipendium“ oder B39 („Finanzierung vor Elternzeit“)
=“Stipendium“}})

vn: afin03a/afin03b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q1: Von welcher Organisation bzw. Institution werden Sie durch ein Stipendium
hauptsächlich gefördert?

q2: Von welcher Organisation bzw. Institution wurden Sie vor Ihrer Elternzeit
durch ein Stipendium hauptsächlich gefördert?
q3: Von welcher Organisation bzw. Institution werden (bzw. wurden Sie vor Ihrer
Elternzeit) durch ein Stipendium hauptsächlich gefördert?

is:

it:

ao1: (afin03a): 1 : : Deutsche Forschungsgemeinschaft (DFG)

ao2: (afin03a): 2 : : Studienstiftung des deutschen Volkes

ao3: (afin03a): 3 : : Friedrich-Ebert-Stiftung

ao4: (afin03a): 4 : : Friedrich-Naumann-Stiftung für die Freiheit

ao5: (afin03a): 5 : : Hanns-Seidel-Stiftung

ao6: (afin03a): 6 : : Hans-Böckler-Stiftung

ao7: (afin03a): 7 : : Heinrich-Böll-Stiftung

ao8: (afin03a): 8 : : Konrad-Adenauer-Stiftung

ao9: (afin03a): 9 : : Rosa-Luxemburg-Stiftung

ao10: (afin03a): 10 : : Stiftung der deutschen Wirtschaft (inkl.
Studienförderwerk Klaus Murmann)

ao11: (afin03a): 11 : : Universität

ao12: (afin03a): 12 : : Fachhochschule

ao13: (afin03a): 13 : : Außeruniversitäre Forschungseinrichtung

ao14: (afin03a): 14 : : Sonstige, und zwar: (afin03b): [string] 6 cm

mv:

ka:

vc:

SHOW q1 IF afin01g = TRUE AND afin02g = FALSE

SHOW q2 IF afin01g = FALSE AND afin02g = TRUE

SHOW q3 IF afin01g = TRUE AND afin02g = TRUE

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B41

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B41_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
adcd21(adcd21a/adcd21b/adcd21c/adcd21d/adcd21e/adcd21f/adcd21g/adcd21h/adcd21i/adcd21j/adcd21k/adcd21l/adcd21m/adcd21n/adcd21o/adcd21p)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Erhalten Sie im aktuellen Semester eine ideelle Promotionsförderung von einer der folgenden Organisationen bzw. Institutionen?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adcd21a): Deutsche Forschungsgemeinschaft (DFG)

ao2: (adcd21b): Studienstiftung des deutschen Volkes

ao3: (adcd21c): Friedrich-Ebert-Stiftung

ao4: (adcd21d): Friedrich-Naumann-Stiftung für die Freiheit

ao5: (adcd21e): Hanns-Seidel-Stiftung

ao6: (adcd21f): Hans-Böckler-Stiftung

ao7: (adcd21g): Heinrich-Böll-Stiftung

ao8: (adcd21h): Konrad-Adenauer-Stiftung

ao9: (adcd21i): Rosa-Luxemburg-Stiftung

ao10: (adcd21j): Stiftung der deutschen Wirtschaft (inkl. Studienförderwerk
Klaus Murmann)

ao11: (adcd21k): Universität

ao12: (adcd21l): Fachhochschule

ao13: (adcd21m): Außeruniversitäre Forschungseinrichtung

ao14: (adcd21n): Sonstige, und zwar: (adcd21o): [string] 6 cm

ao15: (adcd21p): Nein, von keiner der genannten Organisationen/Institutionen. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao15 von den übrigen Antwortoptionen absetzen

tr:

GOTO B42 IF afin03a = 2 OR adcd21b = TRUE

GOTO B43 IF (afin01a = TRUE OR afin01b = TRUE OR afin01c = TRUE OR afin01d =
TRUE OR afin01e = TRUE OR afin01g = TRUE OR afin01h = TRUE OR afin01i = TRUE OR
afin01j = TRUE OR afin01k = TRUE OR afin01l = TRUE)

GOTO C34 IF (afin03a \<\> 2 AND adcd21b = FALSE) AND (afin01a = FALSE AND
afin01b = FALSE AND afin01c = FALSE AND afin01d = FALSE AND afin01e = FALSE AND
afin01g = FALSE AND afin01h = FALSE AND afin01i = FALSE AND afin01j = FALSE AND
afin01k = FALSE AND afin01l = FALSE))

GOTO C34 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B42_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin03a = 2 OR adcd21b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B40 („Stipendiengeber“) = 2= Studienstiftung des deutschen Volkes} oder {B41
(„Ideelle Förderung“) = „Studienstiftung des deutschen Volkes“}})

vn: aict02

qt: Einfachauswahl mit vertikalen ao

hl:

in: Um Doppelbefragungen zu vermeiden, möchten wir - Ihr Einverständnis vorausgesetzt - 
die von Ihnen in der Befragung gemachten Angaben an die Studienstiftung des deutschen 
Volkes übermitteln. Ihre Angaben werden ohne Nennung des Hochschulnamens übermittelt.
Das Promotionsfach wird nicht mit direktem Namen angegeben, sondern zuvor einer
Studienbereichsgruppe zugeordnet. Alle Ortsangaben werden vor Übergabe der Daten
gelöscht. Die so organisierten Daten lassen keinen Rückschluss auf Ihre Person
zu. Auf diese Weise wird gewährleistet, dass Sie nicht nochmals zu einer
ähnlichen Befragung durch die Studienstiftung des deutschen Volkes eingeladen
werden.

q: Meine Daten werden zum Zwecke wissenschaftlicher Auswertungen an die Studienstiftung des deutschen Volkes übermittelt.

is:

it:

ao1: 1 : : Ja, ich bin damit einverstanden.

ao2: 2 : : Nein, ich bin damit nicht einverstanden.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B43 IF (afin01a = TRUE OR afin01b = TRUE OR afin01c = TRUE OR afin01d =
TRUE OR afin01e = TRUE OR afin01g = TRUE OR afin01h = TRUE OR afin01i = TRUE OR
afin01j = TRUE OR afin01k = TRUE OR afin01l = TRUE)

GOTO C34 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B43_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin01b = TRUE OR
afin01c = TRUE OR afin01d = TRUE OR afin01e = TRUE OR afin01g = TRUE OR afin01h
= TRUE OR afin01i = TRUE OR afin01j = TRUE OR afin01k = TRUE OR afin01l = TRUE)

(wenn {A01 = 1 “promoviere” oder = 3} “unterbrochen” und B38 (“Finanzierung)
mindestens 1 Nennung)

vn:
afin04(afin04a/afin04b/afin04c/afin04d/afin04e/afin04f/afin04g/afin04h/afin04i/afin04j/afin04k)

qt: offene Matrix (number)

hl:

in:

q1: Bitte geben Sie an, in welcher monatlichen Höhe Sie im aktuellen Semester
durchschnittlich durch die genannten Quellen Einkünfte erzielen.

q2: Bitte geben Sie an, in welcher monatlichen Höhe Sie im aktuellen Semester
durchschnittlich durch die genannte Quelle Einkünfte erzielen.

is: Geben Sie dazu bitte die Netto-Werte, also nach Abzug von Steuern und Abgaben, an.
Achten Sie bitte auch darauf, nur Zahlen einzugeben und auf Nachkommastellen oder Trennzeichen zu verzichten.
(Beispiel: 12345 und nicht 12.345,00)

it:

ao1: (afin04a): 5 cm, Präfix [ao]: Beschäftigung an einer Hochschule oder
Forschungseinrichtung [number] Euro pro Monat

ao2: (afin04b): 5 cm, Präfix [ao]: Beschäftigung außerhalb einer Hochschule oder
Forschungseinrichtung [number] Euro pro Monat

ao3: (afin04c): 5 cm, Präfix [ao]: Selbstständigkeit bzw. freiberufliche
Tätigkeit !!mit!! Forschungs- oder Entwicklungsbezug [number] Euro pro Monat

ao4: (afin04d): 5 cm, Präfix [ao]: Selbstständigkeit bzw. freiberufliche
Tätigkeit !!ohne!! Forschungs- oder Entwicklungsbezug [number] Euro pro Monat

ao5a: (afin04e): 5 cm, Präfix [ao]: Sonstige Beschäftigung (z. B. Referendariat,
Volontariat, Traineeship) [number] Euro pro Monat

ao5b: (afin04e): 5 cm, Präfix [ao]: [afin01f] [number] Euro pro Monat

ao6: (afin04f): 5 cm, Präfix [ao]: Stipendium [number] Euro pro Monat

ao7: (afin04g): 5 cm, Präfix [ao]: Arbeitslosengeld I oder II [number] Euro pro Monat

ao8: (afin04h): 5 cm, Präfix [ao]: Elterngeld, Erziehungsgeld, Mutterschaftsgeld
während des Mutterschutzes [number] Euro pro Monat

ao9: (afin04i): 5 cm, Präfix [ao]: Geldbeträge von der/dem Partner(in), den
Eltern oder Verwandten [number] Euro pro Monat

ao10: (afin04j): 5 cm, Präfix [ao]: Einkommen aus sonstigen Quellen
(Vermögensanlagen, Ersparnissen, Versicherungen oder Darlehen) [number] Euro pro Monat

ao11a: (afin04k): 5 cm, Präfix [ao]: Sonstiges [number] Euro pro Monat

ao11b: (afin04k): 5 cm, Präfix [ao]: [afin01m] [number] Euro pro Monat

mv:

ka:

vc:

SHOW q1 IF h_multicontext \> 1

SHOW q2 IF h_multicontext = 1

SHOW ao1 IF afin01a = TRUE

SHOW ao2 IF afin01b = TRUE

SHOW ao3 IF afin01c = TRUE

SHOW ao4 IF afin01d = TRUE

SHOW ao5a IF afin01e = TRUE AND afin01f = FALSE

SHOW ao5b IF afin01e = TRUE AND afin01f = TRUE

SHOW ao6 IF afin01g = TRUE

SHOW ao7 IF afin01h = TRUE

SHOW ao8 IF afin01i = TRUE

SHOW ao9 IF afin01j = TRUE

SHOW ao10 IF afin01k = TRUE

SHOW ao11a IF afin01l = TRUE AND afin01m = FALSE

SHOW ao11b IF afin01l = TRUE AND aifn01m = TRUE

av: (afin01a – afin01k): number : \<= 6 stellig : 0 TO 99999

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (afin04a
\> 99999 OR afin04b \> 99999 OR afin04c \> 99999 OR afin04d \> 99999 OR afin04e
\> 99999 OR afin04f \> 99999 OR afin04g \> 99999 OR afin04h \> 99999 OR afin04i
\> 99999 OR afin04j \> 99999OR afin04k \> 99999)

)fv:

hv: h_multicontext

fo: Items (Zebramuster)

tr:

GOTO B44 IF (afin04a \> 0 OR afin04b \> 0 OR afin04c \> 0 OR afin04d \> 0 OR
afin04e \> 0 OR afin04f \> 0 OR afin04g \> 0 OR afin04h \> 0 OR afin04i \> 0 OR
afin04j \> 0 OR afin04k \> 0)

GOTO B45 IF afin01a = TRUE OR afin02a = TRUE

GOTO C01 IF ((afin01b = TRUE OR afin01e = TRUE) OR (afin02b = TRUE OR afin02e = TRUE)) AND (adsv04 = 1 OR adsv09 \<\>
SYSMISS))

GOTO C12 IF afin01b = TRUE OR afin02b = TRUE

GOTO C22 IF afin01e = TRUE OR afin02e = TRUE

GOTO C32 IF afin01c = TRUE OR afin02c = TRUE

GOTO C33 IF afin01d = TRUE OR afin02d = TRUE

GOTO C34 IF ELSE

hi: Bitte hier bei der ao11a nur "Sonstiges" anzeigen, wenn bei der B38 der Freitext fehlt, aber die Checkbox ausgewählt wurde (afin01l= TRUE AND afin01m = FALSE). Wenn der Freitext angegeben wurde, bitte nur diesen hier bei der ao11b übernehmen (afin01m = TRUE) losgelöst von "Sonstiges, und zwar:". 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B44_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin04a \> 0 OR afin04b \> 0 OR afin04c
\> 0 OR afin04d \> 0 OR afin04e \> 0 OR afin04f \> 0 OR afin04g \> 0 OR afin04h
\> 0 OR afin04i \> 0 OR afin04j \> 0 OR afin04k \> 0)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B43 („Geldbeträge“) mindestens ein Wert \> 0}})

vn: afin05a/afin05b

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Ihre finanzielle Situation zu?

is:

it1: (afin05a): Ich kann mit meinem Einkommen meinen Lebensunterhalt gut
bestreiten.

it2: (afin05b): Die Finanzierung meines Lebensunterhalts während meiner
Promotion ist sichergestellt.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO B45 IF afin01a = TRUE OR afin02a = TRUE

GOTO C01 IF ((afin01b = TRUE OR afin01e = TRUE OR afin02b = TRUE OR afin02e =
TRUE) AND (adsv04 = 1 OR adsv09 \<\> SYSMISS))

GOTO C12 IF afin01b = TRUE OR afin02b = TRUE

GOTO C22 IF afin01e = TRUE OR afin02e = TRUE

GOTO C32 IF afin01c = TRUE OR afin02c = TRUE

GOTO C33 IF afin01d = TRUE OR afin02d = TRUE

GOTO C34 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B45_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) „Beschäftigung an
einer Hochschule oder Forschungseinrichtung“}})

vn: aemp01a/aemp01b

qt: Einfachauswahl mit vertikalen ao und offener ao [string]

hl:

in:

q1: Im Folgenden geht es um ihre Beschäftigung an einer Hochschule oder
Forschungseinrichtung. Sind Sie an der Hochschule beschäftigt, an der Sie
promovieren?

q2: Sind Sie an der Hochschule beschäftigt, an der Sie promovieren?

is:

it:

ao1: (aemp01a): 1 : : Ja

ao2: (aemp01a): 2 : : Nein, sondern an dieser Universität/Forschungseinrichtung:
(aemp01b): [string] 6 cm

mv:

ka:

vc:

SHOW q1 IF (afin01b = TRUE OR afin02b = TRUE) OR (afin01e = TRUE OR afin02e =
TRUE)

SHOW q2 IF (afin01b = FALSE AND afin02b = FALSE) AND (afin01e = FALSE AND
afin02e = FALSE)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B46

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B46_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 ((„Finanzierung vor Elternzeit“) „Beschäftigung
an einer Hochschule oder Forschungseinrichtung“}})

vn: aemp02(aemp02a/aemp02b/aemp02c/aemp02d/aemp02e/aemp02f/aemp02g)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Wie haben Sie Ihre Stelle bekommen?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (aemp02a): Ich habe eine schriftliche Bewerbung eingereicht.

ao2: (aemp02b): Durch Kontakte aus meinem vorhergehenden Studium.

ao3: (aemp02c): Ich wurde aufgefordert, mich auf die Stelle zu bewerben.

ao4: (aemp02d): Ich musste ein Auswahlverfahren durchlaufen, in dem mehrere
Personen an der  
Entscheidung zur Besetzung der Stelle beteiligt waren.

ao5: (aemp02e): Ich habe nicht nach einer Stelle an einer Hochschule oder
Forschungseinrichtung gesucht, sondern es hat sich so ergeben.

ao6: (aemp02f): Sonstiges, und zwar: (aemp02g): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO B47

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________B47_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) Beschäftigung an
einer Hochschule oder Forschungseinrichtung}})

vn: aemp03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wissen Sie, ob Ihre Stelle aus Haushalts- oder aus Drittmitteln bezahlt wird?

is:

it:

ao1: 1 : : Ja, sie wird aus Haushaltsmitteln bezahlt.

ao2: 2 : : Ja, sie wird aus Drittmitteln bezahlt.

ao3: 3 : : Ja, sie wird sowohl aus Haushalts- als auch aus Drittmitteln bezahlt.

ao4: 4 : : Nein, das weiß ich nicht.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C01 IF adsv04 = 1 OR adsv09 \<\> SYSMISS

GOTO C02 IF adsv04 \<\> 1 AND adsv09 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND ((afin01a = TRUE OR afin01b = TRUE OR
afin01e = TRUE) OR (afin02a = TRUE OR afin02b = TRUE OR afin01e = TRUE) AND
(adsv04 = 1 OR adsv09 \<\> SYSMISS)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierungsquellen“) eine „Beschäftigung an einer Hochschule oder
Forschungseinrichtung“ oder eine „Beschäftigung außerhalb einer Hochschule oder
Forschungseinrichtung“ oder eine „sonstige Beschäftigung“ angegeben wurde oder
bei B39 („Finanzierungsquellen vor der Elternzeit“) eine „Beschäftigung an einer
Hochschule oder Forschungseinrichtung“ oder eine „Beschäftigung außerhalb einer
Hochschule oder Forschungseinrichtung“ oder eine „sonstige Beschäftigung“
angegeben wurde und {B25 („Anzahl Betreuer(innen)“ = 1 oder bei B30
(„Hauptbetreuer(in)“) ein(e) Erstbetreuer(in) angegeben wurde}})

vn: adsv14

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Betreut Ihr(e) Vorgesetzte(r) gleichzeitig Ihre Promotion?

is: z. B. Beschäftigung als wissenschaftliche(r) Mitarbeiter(in) am Lehrstuhl
der Erstbetreuerin/des Erstbetreuers

it:

ao1: 1 : : Ja, als offizielle(r) Betreuer(in).

ao2: 2 : : Nein, wir tauschen uns aber über meine Promotion aus.

ao3: 3 : : Nein, und wir tauschen uns auch nicht über meine Promotion aus.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C02 IF afin01a = TRUE OR afin02a = TRUE

GOTO C12 IF afin01b = TRUE OR afin02b = TRUE

GOTO C22 IF afin01e = TRUE OR afin02e = TRUE

hi: Bitte hier Icon 3 für Modul C einfügen (oben rechts) und durchgängig
einblenden bis das Modul D beginnt.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{(B38 („Finanzierung“) „Beschäftigung innerhalb Hochschule“ oder bei B39
(„Finanzierungsquellen vor der Elternzeit“) eine „Beschäftigung an einer
Hochschule oder Forschungseinrichtung“ genannt wurde)}})

vn: aemp04

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist Ihre Stelle …

is:

it:

ao1: 1 : : befristet?

ao2: 2 : : unbefristet?

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C03 IF aemp04 = 1

GOTO C05 IF aemp04 = 2 OR aemp04 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE) AND
aemp04 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{(B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde} und {C02 („Befristung Stelle
Hochschule“) = 1 (ja“)}})

vn: aemp05a/aemp05b

qt: Einfachauswahlmatrix mit drop-down Menü

hl:

in:

q: Wann hat Ihr gegenwärtiger Vertrag begonnen?

is:

it1: (adbi02a): Monat:

it2: (adbi02b): Jahr:

ao1: (adbi02a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi02b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, vor 2013

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C04

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE) AND
aemp04 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde} und {C02 („Befristung Stelle
Hochschule“) = 1 (ja“)}})

vn: aemp06/aemp07/aemp08

qt: Question Open (aemp06) und MC (aemp07) + Attached Open (aemp08)

hl:

in:

q: Welche Gesamtlaufzeit (in Monaten) hat Ihr gegenwärtiger Vertrag?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp06): 2 cm, [ao] Suffix: [number] Monate

ao2: (aemp07): 1 : : Ich habe bereits einen Folgevertrag mit einer Laufzeit von
((aemp08): [number] 2 cm) Monaten unterschrieben.

mv:

ka:

vc:

av: (aemp06; aempt07): number : \<= 2 stellig : 0 TO 72

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C05

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde})

vn: aemp09/aemp10/aemp11

qt: Einfachauswahl mit vertikalen ao und 2 offenen ao (number)

hl:

in:

q: Ist Ihre Stelle …

is: Bitte geben Sie nur Zahlen ein und verzichten Sie auf Nachkommastellen.

it:

ao1: (aemp09): 1 : : Vollzeit?

ao2: (aemp09): 2 : : Teilzeit, mit ((aemp10): [number] 2 cm) % der Arbeitszeit
bzw. ((aemp11): [number] 2 cm) Stunden pro Woche?

mv:

ka:

vc:

av: (aemp10): number : \<= 2 stellig : 1 TO 99; (aemp11): number : \<= 2 stellig : 1 TO 42

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C06 IF aemp04 = 1

GOTO C08 IF aemp04 = 2 OR aemp04 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE) AND
aemp04 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde} und {C02 („Befristung Stelle
Hochschule“) = 1 (ja“)}})

vn: aemp12

qt: offene Frage (number)

hl:

in:

q: Wie viele Verträge hatten Sie bereits mit diesem Arbeitgeber in derselben
beruflichen Stellung?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Vertrag/Verträge

mv:

ka:

vc:

av: number : 1 stellig : 1 TO 9

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 
fv:

hv:

fo:

tr:

GOTO C07 IF aemp12 \> 1

GOTO C08 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE) AND
aemp04 = 1 AND aemp12 \> 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C02 („Befristung Stelle Hochschule“) = 1 (ja“)} und {C06 („Anzahl Verträge
Hochschule“) \> 1}})

vn: aemp13

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Schließt diese Folge von Verträgen auch Phasen der Arbeitslosigkeit mit ein?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C08

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde}})

vn: aemp14

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist in Ihrem Arbeitsvertrag oder in Nebenabsprachen ein Qualifizierungsziel
festgelegt worden?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C09 IF aemp14 = 1

GOTO C10 IF aemp14 = 2 OR aemp14 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE) AND
aemp14 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
bei B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde) und bei C08
(„Qualifizierungsziel liegt vor“) 1 („ja“) angegeben wurde)

vn: aemp15/aemp16

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welches Qualifizierungsziel ist in Ihrem Arbeitsvertrag oder in
Nebenabsprachen festgelegt worden?

is:

it:

ao1: (aemp15): 1 : : Promotion

ao2: (aemp15): 2 : : Ein anderes Qualifizierungsziel, und zwar: (aemp16):
[string] 6cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C10

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde}})

vn: aemp17/aemp18

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Steht Ihnen ein arbeitsvertraglich festgelegter Anteil Ihrer Arbeitszeit für
die Arbeit an Ihrer Promotion zur Verfügung?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp17): 1 : : Ja, und zwar ((aemp18): [number] 2 cm) % meiner Arbeitszeit.

ao2: (aemp17): 2 : : Nein, kein vertraglich festgelegter Anteil.

mv:

ka:

vc:

av: number : \<= 3 stellig : 0 TO 100

kh: Bitte geben Sie einen Wert zwischen 0 und 100 an.

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C11

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01a = TRUE OR afin02a = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung innerhalb Hochschule“ genannt wurde}})

vn: aemp19

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie schätzen Sie den thematischen Bezug Ihrer Beschäftigung zu Ihrem
Promotionsprojekt ein?

is:

it:

ao1: 1 : 1 : kein Bezug

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : : sehr starker Bezug

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C12 IF afin01b = TRUE OR afin02b = TRUE

GOTO C22 IF afin01e = TRUE OR afin02e = TRUE

GOTO C32 IF afin01c = TRUE

GOTO C33 IF afin01d = TRUE

GOTO C34 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) „Beschäftigung
außerhalb Hochschule“ genannt wurde}})

vn: aemp20

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Im Folgenden geht es um ihre Beschäftigung außerhalb einer Hochschule oder
Forschungseinrichtung.

Ist Ihre Stelle …

q2: Ist Ihre Stelle …

is:

it:

ao1: 1 : : befristet?

ao2: 2 : : unbefristet?

mv:

ka:

vc:

SHOW q1 IF (afin01a = TRUE OR afin02a = TRUE) OR (afin01e = TRUE OR afin02e =
TRUE)

SHOW q2 IF ((afin01b = TRUE OR afin02b = TRUE) AND ((afin01a = FALSE AND afin02a
= FALSE) AND (afin01e = FALSE AND afin02e = FALSE))

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C13 IF aemp20 = 1

GOTO C15 IF aemp20 = 2 OR aemp20 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE) AND
aemp20 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) „Beschäftigung
außerhalb Hochschule“ genannt wurde} und {C12 „außerhalb HS/FE: Befristung Stelle“ = 1 „befristet“})

vn: aemp21a/aemp21b

qt: Einfachauswahlmatrix mit drop-down Menü

hl:

in:

q: Wann hat Ihr gegenwärtiger Vertrag begonnen?

is:

it1: (adbi02a): Monat:

it2: (adbi02b): Jahr:

ao1: (adbi02a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi02b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, vor 2013

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C14

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE) AND
aemp20 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) „Beschäftigung
außerhalb Hochschule“ genannt wurde}} und {C12 „außerhalb HS/FE: Befristung Stelle“ = 1 „befristet“})

vn: aemp22/aemp23/aemp24

qt: Question Open (aemp22) und MC (aemp23) + Attached Open (aemp24)

hl:

in:

q: Welche Gesamtlaufzeit (in Monaten) hat Ihr gegenwärtiger Vertrag?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp22): 2 cm, [ao] Suffix: [number] Monate

ao2: (aemp23): 1 : : Ich habe bereits einen Folgevertrag mit einer Laufzeit von
((aemp24): [number] 2cm) Monaten unterschrieben.

mv:

ka:

vc:

av: (aemp22; aemp23): number : \<= 2 stellig : 1 TO 72

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C15

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“) „Beschäftigung
außerhalb Hochschule“ genannt wurde}

vn: aemp25/aemp26/aemp27

qt: Einfachauswahl mit vertikalen ao und 2 offenen ao (number)

hl:

in:

q: Ist Ihre Stelle …

is: Bitte geben Sie nur Zahlen ein und verzichten Sie auf Nachkommastellen.

it:

ao1: (aemp25): 1 : : Vollzeit?

ao2: (aemp25): 2 : : Teilzeit, mit ((aemp26): [number] 2 cm) % der Arbeitszeit
bzw. ((aemp27): [number] 2 cm) Stunden?

mv:

ka:

vc:

av: (aemp26): number : /<= 2 stellig: 1 TO 99; (aemp27): number : \<= 2 stellig : 1 TO 42

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C16 IF aemp20 = 1

GOTO C18 IF aemp20 = 2 OR aemp20 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aemp20 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C12 („Befristung Stelle außerhalb“) = 1 („befristet“)}})

vn: aemp28

qt: offene Frage (number)

hl:

in:

q: Wie viele Verträge hatten Sie bereits mit diesem Arbeitgeber in derselben
beruflichen Stellung?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Vertrag/Verträge

mv:

ka:

vc:

av: number : 1 stellig : 1 TO 9

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo:

tr:

GOTO C17 IF aemp28 \> 1

GOTO C18 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C17_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aemp20 = 1 AND aemp28 \> 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C12 („Befristung Stelle außerhalb“) = 1 („befristet“)} und {C16 („Anzahl
Verträge außerhalb“) \> 1}})

vn: aemp29

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Schließt diese Folge von Verträgen auch Phasen der Arbeitslosigkeit mit ein?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C18

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C18_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung außerhalb Hochschule“ genannt wurde}})

vn: aemp30

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist in Ihrem Arbeitsvertrag oder in Nebenabsprachen ein Qualifizierungsziel
festgelegt worden?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C19 IF aemp30 = 1

GOTO C20 IF aemp30 = 2 OR aemp30 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C19_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE) AND
aemp30 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung außerhalb Hochschule“ genannt wurde} und {C18
(„Qualifizierungsziel liegt vor“) 1 („ja“) angegeben wurde}})

vn: aemp31/aemp32

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welches Qualifizierungsziel ist in Ihrem Arbeitsvertrag oder in
Nebenabsprachen festgelegt worden?

is:

it1:

ao1: (aemp31): 1 : : Promotion

ao2: (aemp31): 2 : : Ein anderes Qualifizierungsziel, und zwar: (aemp32):
[string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C20

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C20_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung außerhalb Hochschule“ genannt wurde}}

vn: aemp33/aemp34

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Steht Ihnen ein arbeitsvertraglich festgelegter Anteil Ihrer Arbeitszeit für
die Arbeit an Ihrer Promotion zur Verfügung?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp33): 1 : : Ja, und zwar ((aemp34): [number] 3 cm) % meiner Arbeitszeit.

ao2: (aemp33): 2 : : Nein, kein vertraglich festgelegter Anteil.

mv:

ka:

vc:

av: number : \<= 3 stellig : 0 TO 100

kh: Bitte geben Sie einen Wert zwischen 0 und 100 an.

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C21

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C21_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01b = TRUE OR afin02b = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„Beschäftigung außerhalb Hochschule“ genannt wurde}})

vn: aemp35

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie schätzen Sie den thematischen Bezug Ihrer Beschäftigung zu Ihrem
Promotionsprojekt ein?

is:

it:

ao1: 1 : 1 : kein Bezug

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : : sehr starker Bezug

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C22 IF afin01e = TRUE OR afin02e = TRUE

GOTO C32 IF afin01c = TRUE OR afin02c = TRUE

GOTO C33 IF afin01d = TRUE OR afin02d = TRUE

GOTO C34 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C22_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde}})

vn: aemp36

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Im Folgenden geht es um Ihre sonstige Beschäftigung (z. B. Referendariat,
Volontariat, Traineeship).

Ist Ihre Stelle …

q2: Ist Ihre Stelle …

is:

it1:

ao1: 1 : : befristet?

ao2: 2 : : unbefristet?

mv:

ka:

vc:

SHOW q1 IF (afin01a = TRUE OR afin01b = TRUE) OR (afin02a = TRUE OR afin02b =
TRUE)

SHOW q2 IF (afin01a = FALSE AND afin01b = FALSE) AND (afin02a = FALSE AND
afin02b = FALSE)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C23 IF aemp36 = 1

GOTO C25 IF aemp36 = 2 OR aemp36 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C23_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE) AND
aemp36 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde}} und {C22 „sonstige
Beschäftigung: Befristung Stelle“ = 1 „befristet“})

vn: aemp37a/aemp37b

qt: Einfachauswahlmatrix mit drop-down Menü

hl:

in:

q: Wann hat Ihr gegenwärtiger Vertrag begonnen?

is:

it1: (adbi04a): Monat:

it2: (adbi04b): Jahr:

ao1: (adbi04a): Januar, Februar, März, April, Mai, Juni, Juli, August,
September, Oktober, November, Dezember

ao2: (adbi04b): 2019, 2018, 2017, 2016, 2015, 2014, 2013, vor 2013

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C24

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C24_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE) AND
aemp36 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde}} und {C22 „sonstige
Beschäftigung: Befristung Stelle“ = 1 „befristet“})

vn: aemp38/aemp39/aemp40

qt: Question Open (aemp38) und MC (aemp39) + Attached Open (aemp40)

hl:

in:

q: Welche Gesamtlaufzeit (in Monaten) hat Ihr gegenwärtiger Vertrag?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp38): 2 cm, [ao] Suffix: [number] Monate

ao2: (aemp39): 1 : : Ich habe bereits einen Folgevertrag mit einer Laufzeit von
((aemp40): [number] 2 cm) Monaten unterschrieben.

mv:

ka:

vc:

av: (aemp38; aemp40): number : \<= 2 stellig : 1 TO 82

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C25

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C25_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde}})

vn: aemp41/aemp42/aemp43

qt: Einfachauswahl mit vertikalen ao und offenen ao (number)

hl:

in:

q: Ist Ihre Stelle …

is: Bitte geben Sie nur Zahlen ein und verzichten Sie auf Nachkommastellen.

it:

ao1: (aemp41): 1 : : Vollzeit?

ao2: (aemp41): 2 : : Teilzeit, mit ((aemp42): [number] 2 cm) % der Arbeitszeit
bzw. ((aemp43): [number] 2 cm) Stunden?

mv:

ka:

vc:

av: (aemp42): number : /<= 2 stellig : 1 TO 99; (aemp43): number : \<= 2 stellig : 1 TO 42

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C26 IF aemp36 = 1

GOTO C28 IF aemp36 = 2 OR aemp36 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C26_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aemp36 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C22 „Stelle sonstige Beschäftigung“ = 1 „befristet“}})

vn: aemp44

qt: offene Frage (number)

hl:

in:

q: Wie viele Verträge hatten Sie bereits mit diesem Arbeitgeber in derselben
beruflichen Stellung?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Vertrag/Verträge

mv:

ka:

vc:

av: number : 1 stellig : 1 TO 9

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo:

tr:

GOTO C27 IF aemp44 \> 1

GOTO C28 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C27_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aemp44 \> 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C26 („Anzahl Verträge sonstige“) \> 1}})

vn: aemp45

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Schließt diese Folge von Verträgen auch Phasen der Arbeitslosigkeit mit ein?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C28

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C28_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde}})

vn: aemp46

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist mit Ihrem Arbeitsvertrag oder in Nebenabsprachen ein Qualifizierungsziel
festgelegt worden?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C29 IF aemp46 = 1

GOTO C30 IF aemp46 = 2 OR aemp46 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C29_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE) AND
aemp46 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde} und {C28 („Qualifizierungsziel liegt
vor“) 1 („ja“) angegeben wurde}})

vn: aemp47/aemp48

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welches Qualifizierungsziel ist in Ihrem Arbeitsvertrag oder in
Nebenabsprachen festgelegt worden?

is:

it:

ao1: (aemp47): 1 : : Promotion

ao2: (aemp47): 2 : : Ein anderes Qualifizierungsziel, und zwar: (aemp48):
[string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C30

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C30_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde})

vn: aemp49/aemp50

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Steht Ihnen ein arbeitsvertraglich festgelegter Anteil Ihrer Arbeitszeit für
die Arbeit an Ihrer Promotion zur Verfügung?

is: Bitte geben Sie nur Zahlen ein.

it:

ao1: (aemp49): 1 : : Ja, und zwar ((aemp50): [number] 3 cm) % meiner Arbeitszeit.

ao2: (aemp49): 2 : : Nein, kein vertraglich festgelegter Anteil.

mv:

ka:

vc:

av: number : \<= 3 stellig : 0 TO 100

kh: Bitte geben Sie einen Wert zwischen 0 und 100 an.

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C31

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C31_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01e = TRUE OR afin02e = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierungsquellen vor der Elternzeit“)
„sonstige Beschäftigung“ genannt wurde})

vn: aemp51

qt: Einfachauswahl mit horizontaler ao

hl:

in:

q: Wie schätzen Sie den thematischen Bezug Ihrer Beschäftigung zu Ihrem
Promotionsprojekt ein?

is:

it:

ao1: 1 : 1 : kein Bezug

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : : sehr starker Bezug

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C32 IF afin01c = TRUE OR afin02c = TRUE

GOTO C33 IF afin01d = TRUE OR afin02d = TRUE

GOTO C34 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C32_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01c = TRUE OR afin02c = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“)
„Selbstständigkeit mit Forschung/Entwicklung“ genannt wurde}})

vn: aemp52

qt: Einfachauswahl mit horizontaler ao

hl:

in:

q1: Im Folgenden geht es um ihre Selbstständigkeit bzw. freiberufliche Tätigkeit
!!mit!! Forschungs- oder Entwicklungsbezug.

Wie schätzen Sie den thematischen Bezug Ihrer Erwerbstätigkeit zu Ihrem
Promotionsprojekt ein?

q2: Wie schätzen Sie den thematischen Bezug Ihrer Erwerbstätigkeit zu Ihrem
Promotionsprojekt ein?

is:

it:

ao1: 1 : 1 : kein Bezug

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : : sehr starker Bezug

mv:

ka:

vc:

SHOW q1 IF (afin01a = TRUE OR afin02a = TRUE) OR (afin01b = TRUE OR afin02b =
TRUE) OR (afin01e = TRUE OR afin02e = TRUE) OR (afin01d = TRUE OR afin02d =
TRUE)

SHOW q2 IF (afin01a = FALSE AND afin02a = FALSE) AND (afin01b = FALSE AND
afin02b = FALSE) AND (afin01e = FALSE AND afin02e = FALSE) AND (afin01d = FALSE
AND afin02d = FALSE)

av:

kh:

fv:

hv:

fo:

tr:

GOTO C33 IF afin01d = TRUE OR afin02d = TRUE

GOTO C34 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C33_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (afin01d = TRUE OR afin02d = TRUE)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{B38 („Finanzierung“) oder B39 („Finanzierung vor Elternzeit“)
„Selbstständigkeit ohne Forschung/Entwicklung“ genannt wurde}})

vn: aemp53

qt: Einfachauswahl mit horizontaler ao

hl:

in:

q1: Im Folgenden geht es um ihre Selbstständigkeit bzw. freiberufliche Tätigkeit
!!ohne!! Forschungs- oder Entwicklungsbezug.

Wie schätzen Sie den thematischen Bezug Ihrer Erwerbstätigkeit zu Ihrem
Promotionsprojekt ein?

q2: Wie schätzen Sie den thematischen Bezug Ihrer Erwerbstätigkeit zu Ihrem
Promotionsprojekt ein?

is:

it:

ao1: 1 : 1 : kein Bezug

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : : sehr starker Bezug

mv:

ka:

vc:

SHOW q1 IF (afin01a = TRUE OR afin02a = TRUE) OR (afin01b = TRUE OR afin02b =
TRUE) OR (afin01e = TRUE OR afin02e = TRUE) OR (afin01c = TRUE OR afin02c =
TRUE)

SHOW q2 IF (afin01a = FALSE AND afin02a = FALSE) AND (afin01b = FALSE AND
afin02b = FALSE) AND (afin01e = FALSE AND afin02e = FALSE) AND (afin01c = FALSE
AND afin02c = FALSE)

av:

kh:

fv:

hv:

fo:

tr:

GOTO C34

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C34_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adcd22

qt: offene Frage (number)

hl:

in:

q1: Wie viele Stunden in der Woche können Sie im Durchschnitt an Ihrer Promotion
arbeiten?

q2: Wie viele Stunden in der Woche konnten Sie im Durchschnitt vor Ihrer
Unterbrechung an Ihrer Promotion arbeiten?

is: 
Bitte geben Sie nur Zahlen ein und verzichten Sie auf Nachkommastellen.

(Beispiel: 12 und nicht 12,00)

it:

ao1: 2 cm, [ao] Suffix: [number] Stunden

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1

SHOW q2 IF adbi01 = 3

av: number : \<= 2 stellig : 0 TO 60

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo:

tr:

GOTO C35

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C35_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
adwr01(adwr01a/adwr01b/adwr01c/adwr01d/adwr01e/adwr01f/adwr01g/adwr01h/adwr01i/adwr01j/adwr01k/adwr01l/adwr01m/adwr01n/adwr01o/adwr01p/adwr01q)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welche der folgenden Tätigkeiten haben Sie in den letzten zwölf Monaten im
Rahmen Ihrer Promotion oder Ihrem sonstigen wissenschaftlichen Arbeitsalltag
ausgeübt?

is: Bitte wählen Sie alles Zutreffende aus.

it1: (adwr01a): Mitwirken beim Aufbau einer Forschungsinfrastruktur (z. B.
Aufbereiten, Bereitstellen oder Pflegen von Datenbeständen zur Nutzung durch die
Fachöffentlichkeit)

it2: (adwr01b): Schreiben an der Dissertation

it3: (adwr01c): Konzeption von Forschungs-/Erhebungsdesigns

it4: (adwr01d): Begutachten von eingereichten Manuskripten (Reviewertätigkeit
für Fachzeitschriften und Verlage)

it5: (adwr01e): Durchführen von Experimenten

it6: (adwr01f): Betreuung von Examensarbeiten

it7: (adwr01g): Präsentieren eigener Forschung auf Fachtagungen oder
Konferenzen

it8: (adwr01h): Erheben von Forschungsdaten (Experimentieren, Messen,
Beobachten, Befragen)

it9: (adwr01i): Anleiten anderer Forscherinnen und Forscher

it10: (adwr01j): Durchführen von Lehrveranstaltungen

it11: (adwr01k): Schreiben sonstiger Fachtexte (z. B. Artikel, Bücher, Beiträge
in Sammelbänden)

it12: (adwr01l): Analysieren von Daten

it13: (adwr01m): Organisation von Tagungen und Workshops

it14: (adwr01n): Verfassen von Berichten (z. B. Projektberichte, graue
Literatur)

it15: (adwr01o): Ausüben von Verwaltungstätigkeiten (z. B. Vorbereiten von
Gremiensitzungen, Verfassen von Protokollen oder Anträgen)

it16: (adwr01p): Sonstige Tätigkeit, und zwar: (adwr01q): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (im Zebramuster)

tr:

GOTO C36 IF adwr01a = TRUE OR adwr01b = TRUE OR adwr01c = TRUE OR adwr01d = TRUE
OR adwr01e = TRUE OR adwr01f = TRUE OR adwr01g = TRUE OR adwr01h = TRUE OR
adwr01i = TRUE OR adwr01j = TRUE OR adwr01k = TRUE OR adwr01l = TRUE OR adwr01m
= TRUE OR adwr01n = TRUE OR adwr01o = TRUE OR adwr01p = TRUE

GOTO C37 IF adbi01 = 1

GOTO C38 IF adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C36_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (adwr01a = TRUE OR adwr01b = TRUE OR
adwr01c = TRUE OR adwr01d = TRUE OR adwr01e = TRUE OR adwr01f = TRUE OR adwr01g
= TRUE OR adwr01h = TRUE OR adwr01i = TRUE OR adwr01j = TRUE OR adwr01k = TRUE
OR adwr01l = TRUE OR adwr01m = TRUE OR adwr01n = TRUE OR adwr01o = TRUE OR
adwr01p)

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
entsprechendes Item bei C35 („Tätigkeiten im Arbeitsalltag“) = 1 („gemacht“))

vn:adwr02(adwr02a/adwr02b/adwr02c/adwr02d/adwr02e/adwr02f/adwr02g/adwr02h/adwr02i/adwr02j/adwr02k/adwr02l/adwr02m/adwr02n/adwr02o/adwr02p/adwr02q)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Wie viel Ihrer wissenschaftlichen Arbeitszeit haben Sie insgesamt betrachtet
für die einzelnen Tätigkeiten verwendet?

is:

it1: (adwr02a): Mitwirken beim Aufbau einer Forschungsinfrastruktur (z. B.
Aufbereiten, Bereitstellen oder Pflegen von Datenbeständen zur Nutzung durch die
Fachöffentlichkeit)

it2: (adwr02b): Schreiben an der Dissertation

it3: (adwr02c): Konzeption von Forschungs-/Erhebungsdesigns

it4: (adwr02d): Begutachten von eingereichten Manuskripten (Reviewertätigkeit
für Fachzeitschriften und Verlage)

it5: (adwr02e): Durchführen von Experimenten

it6: (adwr02f): Betreuung von Examensarbeiten

it7: (adwr02g): Präsentieren eigener Forschung auf Fachtagungen oder
Konferenzen

it8: (adwr02h): Erheben von Forschungsdaten (Experimentieren, Messen,
Beobachten, Befragen)

it9: (adwr02i): Anleiten anderer Forscherinnen und Forscher

it10: (adwr02j): Durchführen von Lehrveranstaltungen

it11: (adwr02k): Schreiben sonstiger Fachtexte (z. B. Artikel, Bücher, Beiträge
in Sammelbänden)

it12: (adwr02l): Analysieren von Daten

it13: (adwr02m): Organisation von Tagungen und Workshops

it14: (adwr02n): Verfassen von Berichten (z. B. Projektberichte, graue
Literatur)

it15: (adwr02o): Ausüben von Verwaltungstätigkeiten (z. B. Vorbereiten von
Gremiensitzungen, Verfassen von Protokollen oder Anträgen)

it16a: (adwr02p): Sonstiges

it16b: (adwr02q): [adwr01q]

ao1: 1 : 1 : einen sehr geringen Teil meiner Zeit

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : einen sehr großen Teil meiner Zeit

mv:

ka:

vc:

SHOW it1 IF adwr01a = TRUE

SHOW it2 IF adwr01b = TRUE

SHOW it3 IF adwr01c = TRUE

SHOW it4 IF adwr01d = TRUE

SHOW it5 IF adwr01e = TRUE

SHOW it6 IF adwr01f = TRUE

SHOW it7 IF adwr01g = TRUE

SHOW it8 IF adwr01h = TRUE

SHOW it9 IF adwr01i = TRUE

SHOW it10 IF adwr01j = TRUE

SHOW it11 IF adwr01k = TRUE

SHOW it12 IF adwr01l = TRUE

SHOW it13 IF adwr01m = TRUE

SHOW it14 IF adwr01n = TRUE

SHOW it15 IF adwr01o = TRUE

SHOW it16a IF adwr01p = TRUE AND adwr01q = FALSE

SHOW it16b IF adwr01p = TRUE AND adwr01q = TRUE

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C37 IF adbi01 = 1

GOTO C38 IF adbi01 = 3

hi: Bitte bei dem Item it16a nur "Sonstiges" einblenden, wenn bei der C35 kein Freitext beim open attached angegeben, aber die Sonstige Kategorie angeklickt wurde (adwr01p = TRUE AND adwr01q = FALSE). Wenn der Freitext mit angegeben wurde (adwr01q= TRUE), bitte nur den Freitext einblenden losgelöst von "Sonstiges, und zwar:". 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C37_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1

(Wenn A01 („Promotionsstatus“) = 1 („promoviere“))

vn:
adtc05(adtc05a/adtc05b/adtc05c/adtc05d/adtc05e/adtc05f/adtc05g/adtc05h/adtc05i/adtc05j/adtc05k)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Was treibt Sie zur Arbeit an Ihrer Promotion an?

is:

it: !!Ich bin motiviert, an meiner Promotion zu arbeiten, weil …!!

it1: (adtc05a): es mir persönlich viel bedeutet zu promovieren.

it2: (adtc05b): mir die Promotion Anerkennung von Anderen verschafft.

it3: (adtc05c): die Promotion für meine geplante Karriere notwendig ist.

it4: (adtc05d): ich mir beweisen muss, dass ich das schaffe.

it5: (adtc05e): es meinem Selbstbild entspricht.

it6: (adtc05f): es mir Spaß macht zu forschen.

it7: (adtc05g): ich ein schlechtes Gewissen hätte, wenn ich es nicht täte.

it8: (adtc05h): es mir später bessere Berufschancen eröffnet.

it9: (adtc05i): ich damit gegenwärtig meinen Lebensunterhalt verdiene.

it10: (adtc05j): ich die Inhalte meiner Promotion spannend finde.

it11: (adtc05k): Eigentlich bin ich nicht motiviert, die Promotion fortzuführen. 

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C38

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C38_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adwr03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie in den letzten zwölf Monaten in einem Forschungs- oder
Publikationsprojekt mit anderen Wissenschaftler(inne)n zusammengearbeitet?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (im Zebramuster)

tr:

GOTO C39 IF adwr03 = 1

GOTO C40 IF adwr03 = 2 OR adwr03 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C39_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adwr03 = 1

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C38 („Kooperation andere Wissenschaftler(innen)“) = 1 ("Ja")}})

vn: adwr04(adwr04a/adwr04b/adwr04c/adwr04d/adwr04e/adwr04f/adwr04g/adwr04h)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Wie groß war Ihr Beitrag bei Ihrem jüngsten kooperativen Projekt, verglichen
mit den anderen Forscher(inne)n im Team?

is:

it1: (adwr04a): Entwickeln von Forschungsideen

it2: (adwr04b): Konzipieren von Forschungs- und Erhebungsdesigns

it3: (adwr04c): Erheben von Daten

it4: (adwr04d): Analysieren von Daten

it5: (adwr04e): Entwickeln neuer Analysetools oder Auswertungsstrategien

it6: (adwr04f): Interpretieren von Daten/ Ergebnissen

it7: (adwr04g): Verfassen von Publikationen, Verschriftlichen von Ergebnissen

it8: (adwr04h): Anleiten von anderen Wissenschaftler(inne)n, Koautor(inn)en

ao1: 1 : : kein Beitrag von mir

ao2: 2 : : kleinerer Beitrag von mir

ao3: 3 : : in etwa gleicher Beitrag wie andere

ao4: 4 : : größerer Beitrag von mir

ao5: 5 : : kompletter Beitrag von mir (ich alleine)

ao6: 6 : : kam in dem Projekt nicht vor

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C40

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C40_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: adwr05(adwr05a/adwr05b/adwr05c/adwr05d/adwr05e/adwr05f/adwr05g/adwr05h)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Kooperieren Sie in einem der folgenden Bereiche mit Partnern außerhalb der
Wissenschaft?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (adwr05a): Forschung

ao2: (adwr05b): Entwicklung und Testung von Prototypen

ao3: (adwr05c): Beantragung von Forschungsprojekten oder sonstigen Drittmitteln

ao4: (adwr05d): Erbringung von Dienstleistungsaufträgen (z. B. Gutachten
verfassen, Beraten, Evaluieren)

ao5: (adwr05e): Nutzung von Infrastruktur (z. B. Messstand oder Rechenkapazität)

ao6: (adwr05f): Sonstiges, und zwar: (adwr05g): [string] 6 cm

ao7: (adwr05h): In keinem der Bereiche [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); a07 von den übrigen Antwortoptionen absetzen

tr:

GOTO C41 IF adwr01j = TRUE

GOTO C42 IF afin01a = TRUE OR afin02a = TRUE

GOTO C43 IF adwr01j = FALSE AND afin01a = FALSE AND afin02a = FALSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C41_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND adwr01i = TRUE

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C35 („Tätigkeiten“): „Durchführen von Lehrveranstaltungen“ genannt}})

vn: adwr06

qt: offene Frage (number)

hl:

in:

q: Wie viele Semesterwochenstunden haben Sie in den vergangenen zwölf Monaten an
einer Hochschule gelehrt?

is: Waren es z. B. im Sommersemester 2018 zwei Semesterwochenstunden und im
Wintersemester 2018/19 vier Semesterwochenstunden, so geben Sie bitte den Wert
„6“ als Summe dieser beiden Werte an.

it:

ao1: 2 cm, [ao] Suffix: [number] !!unterrichtete!! Semesterwochenstunden

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 50

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo:

tr:

GOTO C42 IF adwr06 \> 0 OR (afin01a = TRUE OR afin02a = TRUE)

GOTO C43 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C42_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND (adwr06 \> 0 OR (afin01a = TRUE OR afin02a
= TRUE))

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C41 („Semesterwochenstunden“) \> 0} oder {B38 („Finanzierung“) oder B39
(„Finanzierungsquellen vor der Elternzeit“) „Beschäftigung an Hochschule“
genannt}})

vn: adwr07/adwr08

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Sind Sie vertraglich zur Lehre verpflichtet?

is:

it:

ao1: (adwr07): 1 : : Ja, und zwar mit ((adwr08): [number] 2cm) !!vertraglich
vereinbarten!! Semesterwochenstunden.

ao2: (adwr07): 2 : : Nein

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 50

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (im Zebramuster)

tr:

GOTO C43

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C43_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: aabr01

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Waren Sie seit Beginn Ihrer Promotion schon einmal promotionsbedingt oder zu
anderen wissenschaftlichen Zwecken im Ausland?

is: Nicht gemeint sind Kurzzeitaufenthalte wie Konferenzbesuche, Arbeitstreffen
internationaler Forschungsgruppen, Summer Schools o. Ä.

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (im Zebramuster)

tr:

GOTO C44 IF aabr01 = 1

GOTO C46 IF aabr01 = 2 OR aabr01 = SYSMISS

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C44_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aabr01 = 1

(Wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C43 („Auslandsaufenthalt“) = 1 („Ja“)}})

vn: aabr02(aabr02a/aabr02b/aabr02c/aabr02d/aabr02e)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Zu welchem Zweck waren Sie im Ausland?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (aabr02a): Forschungsaufenthalt

ao2: (aabr02b): Lehraufenthalt

ao3: (aabr02c): Weiterbildung

ao4: (aabr02d): Sonstiges, und zwar: (aabr02e): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO C45

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C45_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aabr01 = 1

(Wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{C43 („Auslandsaufenthalt“) „ja“}})

vn: aabr03

qt: offene Frage (string)

hl:

in:

q: In welchem Land/in welchen Ländern waren Sie?

is:

it:

ao1: [string] 8 cm; 2 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO C46

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C46_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
aabr04(aabr04a/aabr04b/aabr04c/aabr04d/aabr04e/aabr04f/aabr04g/aabr04h/aabr04i)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Inwieweit erachten Sie Auslandsaufenthalte als nützlich im Hinblick auf die
folgenden Aspekte?

is: Bitte geben Sie auch dann eine Einschätzung, wenn Sie während Ihrer
Promotion bislang nicht außerhalb Deutschlands waren oder solche Aufenthalte
derzeit nicht planen.

it1: (aabr04a): Um meine Fremdsprachenkenntnisse zu verbessern 

it2: (aabr04b): Um Kooperationen mit Wissenschaftler(inne)n außerhalb
Deutschlands einzugehen 

it3: (aabr04c): Um Zugang zu attraktiven Stellen !!in!! der Wissenschaft zu
erhalten 

it4: (aabr04d): Um Zugang zu attraktiven Stellen !!außerhalb!! der Wissenschaft zu erhalten

it5: (aabr04e): Um meine Einkommenschancen zu verbessern/zu erhalten

it6: (aabr04f): Um meine Forschungskompetenzen zu verbessern

it7: (aabr04g): Um Zugang zu (internationalen oder ausländischen) Fördermitteln
zu erhalten

it8: (aabr04h): Um meine berufliche Karriere voranzubringen

it9: (aabr04i): Um die in meinem Fach üblichen Anforderungen zu erfüllen

ao1: 1 : 1 : gar nicht nützlich

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr nützlich

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C47

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C47_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(Wenn {{A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
aabr05(aabr05a/aabr05b/aabr05c/aabr05d/aabr05e/aabr05f/aabr05g/aabr05h/aabr05i/aabr05j)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Wie hinderlich sind für Sie die folgenden Aspekte bei der Durchführung eines
(weiteren) Auslandsaufenthalts während Ihrer Promotion?

is:

it1: (aabr05a): Mangelnde Fremdsprachenkenntnisse

it2: (aabr05b): Kulturelle Schwierigkeiten

it3: (aabr05c): Mangelnde Motivation  

it4: (aabr05d): Fehlende Beratungs- und Unterstützungsangebote

it5: (aabr05e): Kontaktverlust zum wissenschaftlichen Netzwerk in Deutschland

it6: (aabr05f): Schwierigkeiten, eine passende Position außerhalb Deutschlands zu finden

it7: (aabr05g): Gesundheitliche Probleme

it8: (aabr05h): Trennung von Partner(in), Kind(ern), Freund(inn)en

it9: (aabr05i): Schwierigkeiten, Finanzierung für Mobilität oder Forschung zu
erhalten

it10: (aabr05j): Geringer persönlicher Nutzen

ao1: 1 : 1 : gar nicht hinderlich

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr hinderlich

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO C48

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________C48_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: aabr06(aabr06a/aabr06b/aabr06c/aabr06d/aabr06e/aabr06f/aabr06g)

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie vor, nach der Promotion ins Ausland zu gehen?

is: Bitte beantworten Sie die Frage auch, wenn Sie (derzeit) außerhalb
Deutschlands leben.

Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (aabr06a): Ja, für eine dauerhafte Erwerbstätigkeit !!ohne!!
Forschungsbezug.

ao2: (aabr06b): Ja, für eine dauerhafte Erwerbstätigkeit !!mit!!
Forschungsbezug.

ao3: (aabr06c): Ja, für eine zeitweilige Erwerbstätigkeit !!ohne!!
Forschungsbezug.

ao4: (aabr06d): Ja, für einen zeitweiligen Forschungs- !!und/oder!!
Lehraufenthalt.

ao5: (aabr06e): Ja, für einen Weiterbildungsaufenthalt.

ao6: (aabr06f): Ja, für einen anderen/privaten Aufenthalt.

ao7: (aabr06g): Nein. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (im Zebramuster); a07 von den übrigen Antwortoptionen absetzen

tr:

GOTO D01 IF adbi01 = 1 OR adbi01 = 3

GOTO D27 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: apsy01

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie zufrieden sind Sie gegenwärtig, alles in allem, mit Ihrem Leben?

is:

it:

ao1: 0 : 0 : überhaupt nicht zufrieden

ao2: 1 : 1 : :

ao3: 2 : 2 : :

ao4: 3 : 3 : :

ao5: 4 : 4 : :

ao6: 5 : 5 : :

ao7: 6 : 6 : :

ao8: 7 : 7 : :

ao9: 8 : 8 : :

ao10: 9 : 9 : :

ao11: 10 : 10 : völlig zufrieden

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO D02

hi: Bitte hier Icon 4 für Modul D einfügen (oben rechts) und durchgängig
einblenden bis das nächste Modul E beginnt.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: alcd01

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie derzeit eine(n) feste(n) Partner(in)?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D03 IF alcd01 = 1

GOTO D07 IF alcd01 = 2 OR alcd01 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd01 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
D02 („feste(r) Partner(in)“) = 1 („Ja“))

vn: alcd02

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Leben Sie mit Ihrer/Ihrem Partner(in) zusammen?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D04

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd01 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
D02 („feste(r) Partner(in)“) = 1 („Ja“))

vn: alcd03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Welche berufliche Qualifikation hat Ihr(e) Partner(in)?

is:

it:

ao1: 1 : : Keine abgeschlossene Berufsausbildung

ao2: 2 : : Abgeschlossene Berufsausbildung

ao3: 3 : : Hochschulabschluss

ao4: 4 : : Hochschulabschluss und Promotion

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (im Zebramuster)

tr:

GOTO D05

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd01 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
D02 („feste(r) Partner(in)“) = 1 („Ja“))

vn: alcd04a/alcd04b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Ist Ihr(e) Partner(in) derzeit …

is:

it:

ao1: (alcd04a): 1 : : in Vollzeit erwerbstätig?

ao2: (alcd04a): 2 : : in Teilzeit erwerbstätig?

ao3: (alcd04a): 3 : : in Ausbildung, Umschulung o. Ä.?

ao4: (alcd04a): 4 : : in Elternzeit, Mutterschutz, beurlaubt?

ao5: (alcd04a): 5 : : nicht erwerbstätig (einschließlich Stipendiat(inn)en und
Studierende ohne Erwerbseinkommen)?

ao6: (alcd04a): 6 : : in sonstiger Weise tätig? Und zwar: (alcd04b): [string] 6
cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D06 IF alcd04a = 1 OR alcd04a = 2 OR alcd04a = 3 OR alcd04a = 4 OR alcd04a
= 6

GOTO D07 alcd04a = 5 OR alcd04a = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D06_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd01 = 1 AND (alcd04a = 1 OR alcd04a = 2
OR alcd04a = 3 OR alcd04a = 4 OR alcd04a = 6)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
D02 („feste(r) Partner(in)“) = 1 („Ja“)) und D05 („Erwerbstätigkeit
Partner(in)“) = 1 („Vollzeit“), 2 („Teilzeit“), 3 („Ausbildung“), 4
(„Elternzeit/ Mutterschutz/ beurlaubt“) oder 6 („Sonstiges“))

vn: alcd05

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Ist Ihr(e) Partner(in) als Wissenschaftler(in) tätig?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D07

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: alcd06/alcd07

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Haben Sie Kinder?

is:

it:

ao1: (alcd06): 1 : : Ja, und zwar: ((alcd07): [number] 2 cm) Kind(er)

ao2: (alcd06): 2 : : Nein

mv:

ka:

vc:

av: number : \<= 2 stellig : 1 TO 10

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. 

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D08 IF alcd06 = 1 AND alcd07 > 0

GOTO D10 IF alcd06 = 1

GOTO D09 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd06 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
D07 („Kinder“) = 1 („Ja“))

vn:
alcd08(alcd08a/alcd08b/alcd08c/alcd08d/alcd08e/alcd08f/alcd08g/alcd08h/alcd08i/alcd08j)

qt: offene Frage (number)

hl:

in:

q1: In welchem Jahr wurde Ihr Kind geboren?

q2: Wann wurden Ihre Kinder geboren?

is1: Bitte geben Sie das Geburtsjahr vierstellig an, z. B. 2012.

is2: Bitte geben Sie die Geburtsjahre an, und zwar vierstellig, z. B. 2012.

it:

ao1: (alcd08a): 4 cm, Präfix [ao]: 1. Kind [number]

ao2: (alcd08b): 4 cm, Präfix [ao]: 2. Kind [number]

ao3: (alcd08c): 4 cm, Präfix [ao]: 3. Kind [number]

ao4: (alcd08d): 4 cm, Präfix [ao]: 4. Kind [number]

ao5: (alcd08e): 4 cm, Präfix [ao]: 5. Kind [number]

ao6: (alcd08f): 4 cm, Präfix [ao]: 6. Kind [number]

ao7: (alcd08g): 4 cm, Präfix [ao]: 7. Kind [number]

ao8: (alcd08h): 4 cm, Präfix [ao]: 8. Kind [number]

ao9: (alcd08i): 4 cm, Präfix [ao]: 9. Kind [number]

ao10: (alcd08j): 4 cm, Präfix [ao]: 10. Kind [number]

mv:

ka:

vc:

SHOW q1 IF alcd07 = 1

SHOW q2 IF alcd07 \> 1

SHOW is1 IF alcd07 = 1

SHOW is2 IF alcd07 > 1

SHOW ao1 IF alcd07 = 1

SHOW ao1 - ao2 IF alcd07 = 2

SHOW ao1 - ao3 IF alcd07 = 3

SHOW ao1 - ao4 IF alcd07 = 4

SHOW ao1 – ao5 IF alcd07 = 5

SHOW ao1 – ao6 IF alcd07 = 6

SHOW ao1 – ao7 IF alcd07 = 7

SHOW ao1 – ao8 IF alcd07 = 8

SHOW ao1 – ao9 IF alcd07 = 9

SHOW ao1 – ao10 IF alcd07 = 10

av: (alcd08a – alcd08j): number : 4 stellig : 1940 TO 2019

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
alcd08a \< 1940 OR alcd08b \< 1940 OR alcd08c \< 1940 OR alcd08d \< 1940 OR
alcd08e \< 1940 OR alcd08f \< 1940 OR alcd08g \< 1940 OR alcd08h \< 1940 OR
alcd08i \< 1940 OR alcd08j\< 1940)

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D10

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd06 = 2

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
D07 („Kinder“) = 2 („Nein“)

vn: alcd09

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Möchten Sie in der Zukunft Kinder haben?

is:

it:

ao1: 1 : : Ja, in der nächsten Zeit.

ao2: 2 : : Ja, später einmal.

ao3: 3 : : Nein, sicher nicht.

ao4: 4 : : Das kann ich zurzeit nicht sagen.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D11

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND alcd06 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und

D07 („Kinder“) = 1 („Ja“))

vn: alcd10

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Wünschen Sie sich weitere Kinder?

is:

it:

ao1: 1 : : Ja, in der nächsten Zeit.

ao2: 2 : : Ja, später einmal.

ao3: 3 : : Nein, sicher nicht.

ao4: 4 : : Das kann ich zurzeit nicht sagen.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (im Zebramuster)

tr:

GOTO D11

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: alcd11(alcd11a/alcd11b/alcd11c/alcd11d/alcd11e/alcd11f/alcd11g/alcd11h)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welche Schwierigkeiten sehen Sie bei der Familienplanung und der Realisierung
eines möglichen Kinderwunsches?

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (alcd11a): Unsicherheit der eigenen beruflichen Perspektive und Karriere

ao2: (alcd11b): Mangelnde Vereinbarkeit von Berufs- und Privatleben

ao3: (alcd11c): Geringe finanzielle Sicherheit

ao4: (alcd11d): Probleme, die in der Partnerschaft liegen

ao5: (alcd11e): Einschränkungen der persönlichen Entwicklung und Entfaltung

ao6: (alcd11f): Sonstiges, und zwar: (alcd11g): [string] 6 cm

ao7: (alcd11h): Keine Schwierigkeiten [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); a07 von den übrigen Antwortoptionen absetzen

tr:

GOTO D12

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: alcd12

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie zufrieden sind Sie mit Ihrer derzeitigen Vereinbarkeit von Arbeits- und
Privatleben?

is:

it:

ao1: 0 : 0 : überhaupt nicht zufrieden

ao2: 1 : 1 : :

ao3: 2 : 2 : :

ao4: 3 : 3 : :

ao5: 4 : 4 : :

ao6: 5 : 5 : :

ao7: 6 : 6 : :

ao8: 7 : 7 : :

ao9: 8 : 8 : :

ao10: 9 : 9 : :

ao11: 10 : 10 : völlig zufrieden

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO S12 IF preload01 = 4

GOTO D13

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4

(wenn preload01 = 4 ("Saarbrücken"))

vn: s12

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie schon einmal einen Kinderwunsch aus beruflichen Gründen zurückgestellt?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S13 IF s12 = 1

GOTO S14 IF alcd06 = 1

GOTO S15 IF alcd06 = 2 OR alcd06 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________S13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND s12 = 1 

(wenn preload01 = 4 ("Saarbrücken") und S12 ("Kinderwunsch aus beruflichen Gründen zurückgestellt") = 1 ("Ja"))

vn: s13(s13a/s13b/s13c/s13d/s13e/s13f/s13g/s13h/s13i)

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Unter welchen Umständen hätten Sie Ihren Kinderwunsch nicht zurückgestellt? 

is: Bitte wählen Sie alles Zutreffende aus.

it:

ao1: (s13a): Meine Ausbildung/Promotion hätte abgeschlossen sein müssen.

ao2: (s13b): Die Ausbildung/Promotion meines Partners/meiner Partnerin hätte abgeschlossen sein müssen.

ao3: (s13c): Ich hätte unbefristet beschäftigt sein müssen.

ao4: (s13d): Mein(e) Partner(in) hätte unbefristet beschäftigt sein müssen.

ao5: (s13e): Ich hätte in Vollzeit beschäftigt sein müssen.

ao6: (s13f): Mein(e) Partner(in) hätte in Vollzeit beschäftigt sein müssen.

ao7: (s13g): Private Gründe

ao8: (s13h): Sonstiges, und zwar: (s13i): [string] 8 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S14 IF alcd06 = 1

GOTO S15 IF alcd06 = 2 OR alcd06 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND alcd06 = 1

(wenn preload01 = 4 ("Saarbrücken") und D07 ("Kinder vorhanden") = 1 ("Ja"))

vn: s14(s14a/s14b/s14c/s14d/s14e/s14f)

qt: offene Matrix (number)

hl:

in:

q: Wenn Sie einmal an eine normale Woche denken:
Von wem wird das (jüngste) Kind in welchem Umfang (%) betreut?

is: Bitte achten Sie darauf, dass die Summe der Angaben 100 (%) ergibt und dass Sie auf Nachkommastellen verzichten.
(Beispiel: 25 und nicht 25,00)

it:

ao1: (s14a): 4 cm, Präfix [ao] Suffix: Von mir: [number] %

ao2: (s14b): 4 cm, Präfix [ao] Suffix: Von meinem/meiner (Ehe-)Partner(in): [number] %

ao3: (s14c): 4 cm, Präfix [ao] Suffix: Von dem Vater/der Mutter des Kindes (falls nicht im Haushalt): [number] %

ao4: (s14d): 4 cm, Präfix [ao] Suffix: Von anderen Familienmitgliedern: [number] %

ao5: (s14e): 4 cm, Präfix [ao] Suffix: Außeruniversitär institutionell (Tagesmutter/-vater, Kindergarten, Krippe, Babysitter, Ganztagsbetreuung in der Schule): [number] %
 
ao6: (s14f): 4 cm, Präfix [ao] Suffix: Universitär institutionell (Kindertagesstätte für Bedienstete, FlexiMedKids –Kurzzeitbetreuung, Online-Babysittingbörse der UdS): [number] %

mv:

ka:

vc:

av: number : \<= 3 stellig : 0 TO 100

kh: Bitte geben Sie einen Wert zwischen 0 und 100 an. (IF s14a-s14f \> 100)

fo: Antwortoptionen (Zebramuster)

tr:

GOTO S15

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 

(wenn preload01 = 4 ("Saarbrücken"))

vn: s15(s15a/s15b/s15c/s15d/s15e/s15f/s15g/s15h/s15i)

qt: Matrix mit horizontaler Einfachauswahl

hl:

in: Über die Aufgaben von Müttern und Vätern gibt es verschiedene Meinungen.

q: Inwieweit stimmen Sie den folgenden Aussagen zu?

is: 

it1: (s15a): Eine Vollzeit erwerbstätige Mutter kann zu ihrem Kleinkind normalerweise ein genauso inniges Verhältnis haben wie eine Mutter, die nicht berufstätig ist.

it2: (s15b): Die beste Arbeitsteilung in einer Familie ist die, dass beide Partner in Vollzeit arbeiten und sich gleichermaßen um den Haushalt und die Kinder kümmern.

it3: (s15c): Ein Kleinkind wird sicherlich darunter leiden, wenn seine Mutter berufstätig ist.

it4: (s15d): Es ist für alle Beteiligten viel besser, wenn der Mann voll im Berufsleben steht und die Frau zu Hause bleibt und sich um den Haushalt und die Kinder kümmert.

it5: (s15e): Es ist für ein Kind sogar gut, wenn seine Mutter berufstätig ist und sich nicht nur auf den Haushalt konzentriert.

it6: (s15f): Ein Vollzeit erwerbstätiger Vater kann sich nicht ausreichend um seine Kinder kümmern.

it7: (s15g): Auch wenn beide Eltern erwerbstätig sind, ist es besser, wenn die Verantwortung für den Haushalt und die Kinder hauptsächlich bei der Frau liegt.

it8: (s15h): Ein Vollzeit erwerbstätiger Vater kann zu seinem Kleinkind normalerweise ein genauso inniges Verhältnis haben wie ein Vater, der nicht berufstätig ist.

it9: (s15i): In einer Familie kann auch der Mann für den Haushalt und die Kinder verantwortlich sein, während die Frau Vollzeit erwerbstätig ist.


ao1: 1 : : stimme überhaupt nicht zu

ao2: 2 : : stimme eher nicht zu

ao3: 3 : : stimme eher zu

ao4: 4 : : stimme voll und ganz zu

mv:

ka:

vc:

av: 

kh: 

fo: Items (Zebramuster)

tr:

GOTO D13

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: ahea01

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie würden Sie Ihren Gesundheitszustand im Allgemeinen beschreiben?

is:

it:

ao1: 1 : : sehr gut

ao2: 2 : : gut

ao3: 3 : : mittelmäßig

ao4: 4 : : schlecht

ao5: 5 : : sehr schlecht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO D14

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: aict03

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q:  Wir möchten Ihnen gerne Fragen zur Gesundheit und möglichen Beeinträchtigungen stellen. Diese Informationen liefern 
wichtige Anhaltspunkte zur Verbreitung gesundheitlicher Beeinträchtigungen bei Promovierenden und tragen dazu bei, die 
Promotionsbedingungen für Personen mit gesundheitlichen Beeinträchtigungen zu verbessern.

is:  Sofern Sie generell bereit sind, die Fragen zu den Themen Gesundheit und Beeinträchtigung zu beantworten, steht es Ihnen 
dennoch selbstverständlich frei, einzelne Fragen nicht zu beantworten. 

it:

ao1: 1 : : Ja, ich möchte die Fragen zu den Themen Gesundheit und Beeinträchtigung beantworten.

ao2: 2 : : Nein, ich möchte die Fragen zu den Themen Gesundheit und Beeinträchtigung nicht beantworten.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D15 IF aict03 = 1

GOTO D24 IF aict03 = 2 OR aict03 = SYSMISS

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)})

vn: ahea02

qt: offene Frage (number)

hl:

in:

q: Bitte denken Sie an Ihre körperliche Gesundheit – dazu zählen körperliche
Krankheiten und Verletzungen. An wie vielen Tagen der letzten vier Wochen ging
es Ihnen körperlich nicht gut?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Tag(e)

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 28

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
ahea02 \> 28)

fv:

hv:

fo:

tr:

GOTO D16

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)})

vn: ahea03

qt: offene Frage (number)

hl:

in:

q: Bitte denken Sie an Ihr seelisches Befinden – dazu zählen auch Stress,
Depressionen oder Ihre Stimmung ganz allgemein. An wie vielen Tagen der letzten
vier Wochen ging es Ihnen seelisch nicht gut?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Tag(e)

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 28

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
ahea03 \> 28)

fv:

hv:

fo:

tr:

GOTO D17

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D17_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)})

vn: ahea04

qt: offene Frage (number)

hl:

in:

q: An wie vielen Tagen der letzten vier Wochen waren Sie durch Ihre körperliche
Gesundheit oder Ihr seelisches Befinden in der Ausübung alltäglicher Aktivitäten
– wie Promotion, Versorgung, Erholung oder Pflege sozialer Kontakte –
beeinträchtigt?

is:

it:

ao1: 2 cm, [ao] Suffix: [number] Tag(e)

mv:

ka:

vc:

av: number : \<= 2 stellig : 0 TO 28

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
ahea04 \> 28)

fv:

hv:

fo:

tr:

GOTO D18

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D18_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)})

vn: ahea05

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie eine amtlich anerkannte Behinderung?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D19 IF ahea05 = 1

GOTO D24 IF ahea05 = 2 OR ahea05 = SYSMISS

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D19_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1 AND ahea05 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)} und D18(„Behinderung“) = 1
(„ja“)})

vn: ahea06

qt: offene Frage (string)

hl:

in:

q: Um welche Art von Behinderung handelt es sich?

is:

it:

ao1: [string] 8 cm; 3 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO D20

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D20_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1 AND ahea05 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)} und D18(„Behinderung“) = 1
(„ja“)})

vn: ahea07

qt: offene Frage (number)

hl:

in:

q: In welchem Jahr wurde die Behinderung anerkannt?

is:

it:

ao1: 4 cm, Präfix: [ao]: Jahr: [number]

mv:

ka:

vc:

av: number : 4 stellig : 1920 TO 2019

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
ahea07 \< 1920 OR ahea07 \> 2019)

fv:

hv:

fo:

tr:

GOTO D21

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D21_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1 AND ahea05 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)} und D18(„Behinderung“) = 1
(„ja“)})

vn: ahea08

qt: offene Frage (number)

hl:

in:

q: Welcher Grad der Behinderung liegt heute vor?

is:

it:

ao1: 3 cm, [ao] Suffix: [number] %

mv:

ka:

vc:

av: number : \<= 3 stellig : 1 TO 100

kh: Bitte geben Sie einen Wert zwischen 1 und 100 an.

fv:

hv:

fo:

tr:

GOTO D22

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D22_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1 AND ahea05 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“)} und D18(„Behinderung“) = 1
(„ja“)})

vn: ahea09

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Kennen Sie Programme für Menschen mit Behinderung an Ihrer Hochschule?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D23 IF ahea09 = 1

GOTO D24 IF ahea09 = 2 OR ahea09 = SYSMISS

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D23_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3) AND aict03 = 1 AND ahea05 = 1 AND ahea09 = 1

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“) und
{D14 („Einverständnis Gesundheit“) = 1 („Ja“) und D18(„Behinderung“) = 1 („ja“)
und D22 („Behindertenprogramme bekannt“) = 1 („ja“)})

vn: ahea10

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie an solchen Programmen teilgenommen?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D24

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D24_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:apsy02(apsy02a/apsy02b/apsy02c/apsy02d/apsy02e/apsy02f/apsy02g/apsy02h/apsy02i/apsy02j/apsy02k/apsy02l/apsy02m/apsy02n/apsy02o)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: In welchem Ausmaß treffen die folgenden Eigenschaften auf Sie zu?

is:

it: !!Ich bin jemand, der …!!

it1: (apsy02a): gründlich arbeitet.

it2: (apsy02b): kommunikativ, gesprächig ist.

it3: (apsy02c): manchmal etwas grob zu anderen ist.

it4: (apsy02d): originell ist, neue Ideen einbringt.

it5: (apsy02e): sich oft Sorgen macht.

it6: (apsy02f): zurückhaltend ist.

it7: (apsy02g): verzeihen kann.

it8: (apsy02h): eher faul ist.

it9: (apsy02i): aus sich herausgehen kann, gesellig ist.

it10: (apsy02j): künstlerische, ästhetische Erfahrungen schätzt.

it11: (apsy02k): leicht nervös wird.

it12: (apsy02l): Aufgaben wirksam und effizient erledigt.

it13: (apsy02m): rücksichtsvoll und freundlich mit anderen umgeht.

it14: (apsy02n): eine lebhafte Phantasie, Vorstellungen hat.

it15: (apsy02o): entspannt ist, gut mit Stress umgehen kann.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : :

ao6: 6 : 6 : :

ao7: 7 : 7 : trifft völlig zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D25

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D25_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: apsy03

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie schätzen Sie sich persönlich ein: Wie risikobereit sind Sie im
Allgemeinen?

is:

it:

ao1: 1 : 1 : gar nicht risikobereit

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : :

ao6: 6 : 6 : :

ao7: 7 : 7 : sehr risikobereit

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO D26

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D26_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn: apsy04(apsy04a/apsy04b/apsy04c/apsy04d)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Sie zu?

is:

it1: (apsy04a): Ich habe mein Leben selbst in der Hand.

it2: (apsy04b): Wenn ich mich anstrenge, werde ich auch Erfolg haben.

it3: (apsy04c): Egal ob privat oder Beruf: Mein Leben wird zum großen Teil
von anderen bestimmt.

it4: (apsy04d): Meine Pläne werden oft vom Schicksal durchkreuzt.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D26a

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------
\__________________________________________D26A_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: apsy05(apsy05a/apsy05b/apsy05c)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Sie zu?

is:

it1: (apsy05a): In schwierigen Situationen kann ich mich auf meine Fähigkeiten
verlassen.

it2: (apsy05b): Die meisten Probleme kann ich aus eigener Kraft gut meistern.

it3: (apsy05c): Auch anstrengende und komplizierte Aufgaben kann ich in der
Regel gut lösen.

ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : trifft völlig zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D27

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D27_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 3)

(wenn {(A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“))

vn:
acrg01(acrg01a/acrg01b/acrg01c/acrg01d/acrg01e/acrg01f/acrg01g/acrg01h/acrg01i/acrg01j/acrg01k/acrg01l/acrg01m)

qt: Einfachauswahlmatrix mit horizontalen ao und offener ao (string)

hl:

in:

q1: Wie wichtig sind Ihnen die folgenden Eigenschaften von Stellen für Ihre
berufliche Tätigkeit nach der Promotion?

q2: Nun zur Erwerbssituation nach der Promotion. Wie wichtig sind Ihnen die
folgenden Eigenschaften bei einer beruflichen Tätigkeit?

is:

it1: (acrg01a): Führungsverantwortung

it2: (acrg01b): Vereinbarkeit von Beruf und Familie

it3: (acrg01c): Verfügbarkeit von Ressourcen (z. B. technische und finanzielle
Ausstattung)

it4: (acrg01d): Gute Aufstiegsmöglichkeiten

it5: (acrg01e): Gesellschaftliche Anerkennung

it6: (acrg01f): Arbeitsplatzsicherheit

it7: (acrg01g): Gesellschaftlicher Nutzen der Arbeit

it8: (acrg01h): Die Höhe des Gehalts

it9: (acrg01i): Entscheidungsautonomie

it10: (acrg01j): Arbeiten im Team

it11: (acrg01k): Intellektuelle Herausforderung

it12: (acrg01l): Sonstiges, und zwar: (acrg01m): [string] 6 cm

ao1: 1 : 1 : gar nicht wichtig

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr wichtig

mv:

ka:

vc:

SHOW q1 IF adbi01 = 1 OR adbi01 = 3

SHOW q2 IF adbi01 = 2

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D28

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D28_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: acrg02(acrg02a/acrg02b/acrg02c/acrg02d)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Unabhängig von der Realisierungsmöglichkeit: Wie attraktiv finden Sie die
folgenden Beschäftigungsmöglichkeiten?

is:

it1: (acrg02a): Tätigkeit als Wissenschaftler(in) an einer Hochschule bzw.
Forschungseinrichtung

it2: (acrg02b): Tätigkeit als Professor(in) an einer Hochschule bzw.
Forschungseinrichtung

it3: (acrg02c): Tätigkeit außerhalb der Wissenschaft !!mit!! Bezug zu Forschung
und Entwicklung

it4: (acrg02d): Tätigkeit außerhalb der Wissenschaft !!ohne!! Bezug zu Forschung
und Entwicklung

ao1: 1 : 1 : sehr unattraktiv

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr attraktiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D29

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D29_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: acrg03(acrg03a/acrg03b/acrg03c/acrg03d)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Und wie attraktiv sind für Sie – unabhängig von der Realisierungsmöglichkeit – die folgenden Formen der Erwerbstätigkeit?

is:

it1: (acrg03a): Tätigkeit in einem etablierten Betrieb/Unternehmen

it2: (acrg03b): Tätigkeit in einem Startup-Unternehmen

it3: (acrg03c): Selbstständigkeit als Freiberufler(in)

it4: (acrg03d): Gründung eines eigenen Unternehmens

ao1: 1 : 1 : sehr unattraktiv

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr attraktiv

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D30 IF adbi01 = 1 OR adbi01 = 3

GOTO D31 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D30_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adbi01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), oder 3 („unterbrochen“))

vn: acrg04

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Möchten Sie nach der Promotion im Wissenschaftsbereich bleiben?

is:

it:

ao1: 1 : : Ja, ich möchte (zunächst) in der Wissenschaft bleiben.

ao2: 2 : : Nein, ich möchte (zunächst) den Wissenschaftsbereich verlassen.

ao3: 3 : : Ich bin noch unentschlossen.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D32 IF acrg04 = 2

GOTO D34 IF acrg04 = 1 OR acrg04 = 3 OR acrg04 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D31_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 2

(wenn A01 („Promotionsstatus“) = 2 („abgeschlossen“))

vn: acrg05

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Sind Sie derzeit erwerbstätig?

is: 

it

ao1: 1 : : Ja

ao2: 2 : : Nein


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D33 IF acrg05 = 1

GOTO D34 IF ELSE


hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D32_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF ((adbi01 = 1, 3) AND acrg04 = 2) OR ((adbi01 = 2) AND (acrg05 = 1) AND (aemp54a = 3, 4, 5, 6))

vn: acrg06

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Können Sie sich vorstellen, später noch einmal in die Wissenschaft
zurückzukehren?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

ao3: 3 : : Ich möchte mir das offen halten.

ao4: 4 : : Weiß ich noch nicht.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D34 IF adbi01 = 1 OR adbi01 = 3

GOTO D35 IF adbi01 = 2 AND acrg06 = 1

GOTO D38 IF adbi01 = 2 AND (acrg06 \<\> 1 OR acrg06 = SYSMISS)

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D33_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF ((adbi01 = 2) AND (acrg05 = 1))

vn: aemp54a/aemp54b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: In welchem Sektor sind Sie (vorrangig) tätig?

is:

it:

ao1: (aemp54a): 1 : : Hochschulen 

ao2: (aemp54a): 2 : : öffentlich geförderte außeruniversitäre Forschungseinrichtungen

ao3: (aemp54a): 3 : : Sonstiger öffentlicher Dienst

ao4: (aemp54a): 4 : : Privatwirtschaft/Industrie

ao5: (aemp54a): 5 : : Privater Non-Profit-Sektor

ao6: (aemp54a): 6 : : Sonstiges, und zwar: (aemp54b): [string] 6cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D32 IF aemp54a = 3 OR aemp54a = 4 OR aemp54a = 5 OR aemp54a = 6

GOTO D35 IF aemp54a = 1 OR aemp54a = 2 OR aemp54a = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D34_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF ((adbi01 = 1, 3) AND (acrg04 = 1,3,SYSMISS)) OR (adbi01 = 2 AND acrg05 <> 1)

vn: acrg07a/acrg07b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: In welchem Sektor beabsichtigen Sie zukünftig vorrangig tätig zu sein?

is:

it:

ao1: (acrg07a): 1 : : Hochschulen

ao2: (acrg07a): 2 : : Öffentlich geförderte außeruniversitäre Forschungseinrichtungen

ao3: (acrg07a): 3 : : Sonstiger öffentlicher Dienst

ao4: (acrg07a): 4 : : Privatwirtschaft/Industrie

ao5: (acrg07a): 5 : : Privater Non-Profit-Sektor

ao6: (acrg07a): 6 : : Sonstiges, und zwar: (acrg07b): [string] 6 cm

ao7: (acrg07a): 7 : : Ich bin noch unentschlossen.

ao8: (acrg07a): 8 : : Ich habe nicht vor, eine Erwerbstätigkeit aufzunehmen.


mv:

ka:

vc: SHOW ao8 IF (adbi01 = 2 AND (acrg05 = 2 OR acrg05 = SYSMISS))

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E01 IF acrg07a = 8

GOTO D35 IF acrg04 = 1 OR acrg06 = 1

GOTO D38 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D35_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (acrg06 = 1) OR (aemp54a = 1,2,SYSMISS) OR ((acrg07a <> 8) AND (acrg04 = 1))

vn: acrg08

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Streben Sie eine Professur an?

is:

it:

ao1: 1 : 1 : Ja

ao2: 2 : 2 : Nein

ao3: 3 : 3 : Weiß ich noch nicht.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D36 IF acrg08 = 1

GOTO D37 IF adbi01 = 2 AND (acrg08 = 2 OR acrg08 = 3 OR acrg08 = SYSMISS)

GOTO D38 IF adbi01 = 1 OR adbi01 = 3

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D36_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3) AND acrg08 = 1

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 2 („abgeschlossen“ ) oder
3 („unterbrochen“)) und D35 („Professur angestrebt“) = 1 („Ja“))

vn: acrg09

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Welche Professur bevorzugen Sie?

is:

it:

ao1: 1 : : Universitätsprofessur

ao2: 2 : : Fachhochschulprofessur

ao3: 3 : : Da bin ich mir noch unsicher.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO D38

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D37_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 2 AND acrg08 = 2

(wenn A01 („Promotionsstatus“) = 2 („abgeschlossen“) und D35 („Professur
angestrebt“) = 2 („Nein“))

vn: acrg10

qt: Einfachauswahl mit horizontalen ao

hl:

in:

q: Wie sehr wünschen Sie sich dennoch, dauerhaft in der Wissenschaft tätig zu
sein?

is:

it:

ao1: 1 : 1 : gar nicht

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : sehr stark

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO D38

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D38_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR (adbi01 = 2 AND (acrg05 = 1 OR acrg07a <> 8)) OR adbi01 = 3

vn: acrg11(acrg11a/acrg11b)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Wie leicht ist es für Promotionsabsolvent(inn)en in Ihrem Fach, nach dem
Abschluss folgende Stellen zu finden?

is:

it1: (acrg11a): Eine Postdocstelle in der Wissenschaft

it2: (acrg11b): Eine qualifikationsadäquate Stelle außerhalb der Wissenschaft

ao1: 0 : 0 : sehr leicht

ao2: 1 : 1 : :

ao3: 2 : 2 : :

ao4: 3 : 3 : :

ao5: 4 : 4 : :

ao6: 5 : 5 : :

ao7: 6 : 6 : :

ao8: 7 : 7 : :

ao9: 8 : 8 : :

ao10: 9 : 9 : :

ao11: 10 : 10 : sehr schwer

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D39

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D39_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR (adbi01 = 2 AND (acrg05 = 1 OR acrg07a <> 8)) OR adbi01 = 3

vn: acrg12(acrg12a/acrg12b)

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Wie leicht wäre es für Sie persönlich, folgende Stellen zu bekommen?

is:

it1: (acrg12a): Eine Postdocstelle in der Wissenschaft

it2: (acrg12b): Eine qualifikationsadäquate Stelle außerhalb der Wissenschaft

ao1: 0 : 0 : sehr leicht

ao2: 1 : 1 : :

ao3: 2 : 2 : :

ao4: 3 : 3 : :

ao5: 4 : 4 : :

ao6: 5 : 5 : :

ao7: 6 : 6 : :

ao8: 7 : 7 : :

ao9: 8 : 8 : :

ao10: 9 : 9 : :

ao11: 10 : 10 : sehr schwer

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO D41

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________D41_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR (adbi01 = 2 AND (acrg05 = 1 OR acrg07a <> 8)) OR adbi01 = 3

vn: apsy06a/apsy06b

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Und wie sicher sind Sie, dass Sie die erforderlichen Fähigkeiten für die im
Folgenden genannten Tätigkeiten haben?

is:

it1: (apsy06a): Ich habe die erforderlichen Fähigkeiten für eine Tätigkeit
!!innerhalb!! der Wissenschaft.

it2: (apsy06b): Ich habe die erforderlichen Fähigkeiten für eine Tätigkeit
!!außerhalb!! der Wissenschaft.

ao1: 1 : 1 : gar nicht sicher

ao2: 2 : 2 : :

ao3: 3 : 3 : :

ao4: 4 : 4 : :

ao5: 5 : 5 : ganz sicher

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO K07 if preload01 = 2

GOTO E01

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (preload01 = 2 AND (adbi01 = 1 OR adbi01 = 3 OR adbi01 = 4 OR (adbi01 = 2 AND (acrg05 = 1 OR acrg07a <> 8))))

(wenn preload01 = 2 ("Kiel"))

vn: k07a/k07b/k07c

qt: Einfachauswahlmatrix mit horizontalem drop-down Menü

hl:

in:

q: Bitte beziehen Sie folgende Aussage auf den Entscheidungsprozess zwischen einer wissenschaftlichen und nicht-wissenschaftlichen Karriere und vervollständigen Sie.

is:

it1a: (k07a): Ich habe [ao1a] 

it2a: (k07b): angefangen, mich für den Entscheidungsprozess zu interessieren und mich [ao1a] 



it1b: (k07a): Ich habe [ao1b] 

it2b: (k07b): angefangen, mich für den Entscheidungsprozess zu interessieren und mich [ao1b] 

it3: (k07c): für [ao2] 


ao1a: vor meiner Promotion, zu Beginn meiner Promotion, während meiner Promotion, bisher noch nicht

ao1b: vor meiner Promotion, zu Beginn meiner Promotion, während meiner Promotion, zum Ende meiner Promotion

ao2: keinen konkreten Berufsweg entschieden., einen wissenschaftlichen Berufsweg entschieden., einen nicht-wissenschaftlichen Berufsweg entschieden.


mv:

ka:

vc:

SHOW it1a AND it2a IF adbi01 = 1 OR adbi01 = 3

SHOW it1b AND it2b IF adbi01 = 2 OR adbi01 = 4

av:

kh:

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO K08

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (preload01 = 2 AND (adbi01 = 1 OR adbi01 = 3 OR adbi01 = 4 OR (adbi01 = 2 AND (acrg05 = 1 OR acrg07a <> 8))))

(wenn preload01 = 2 ("Kiel"))

vn: k08a/k08b/k08c/k08d/k08e/k08f/k08g/k08h/k08i

qt: Einfachauswahlmatrix 

hl:

in:

q: Wenn Sie über Ihren Entscheidungsprozess zwischen einer wissenschaftlichen und nicht-wissenschaftlichen Karriere bis zum jetzigen Zeitpunkt insgesamt nachdenken. Inwieweit treffen folgende Aussagen auf Sie zu?

is:

it1: (k08a): Meine persönlichen Erfahrungen innerhalb der CAU (z. B. Professorenschaft, Studierende, Verwaltungspersonal, institutionelles Umfeld) haben positiv zur finalen Entscheidungsfindung beigetragen.

it2: (k08b): Meine persönlichen Erfahrungen außerhalb der CAU (z. B. Familie, Freundeskreis, Kooperationspartner(innen), Berufsumfeld) haben positiv zur finalen Entscheidungsfindung beigetragen.

it3: (k08c): Mein wissenschaftliches Umfeld vor meiner Promotion hat positiv zur finalen Entscheidungsfindung beigetragen.

it4: (k08d): Mein wissenschaftliches Umfeld während der Promotion hat positiv zur finalen Entscheidungsfindung beigetragen.

it5: (k08e): Ich habe sehr häufig Messen (z. B. Karriere-, Job-, Berufsmessen) als Beratungs- und/oder Informationsquelle für meinen Entscheidungsprozess genutzt.

it6: (k08f): Ich habe sehr häufig persönliche Kontakte (z. B. berufstätige Bekannte, ehemalige Kolleg(inn)en) als Beratungs- und/oder Informationsquelle für meinen Entscheidungsprozess genutzt. 

it7: (k08g): Ich habe sehr häufig Alumni der CAU als Beratungs- und/oder Informationsquelle für meinen Entscheidungsprozess genutzt.

it8: (k08h): Ich habe sehr häufig Medien (z. B. Stellenportale im Internet, Stellenabonnements und Jobinformationen von Zeitschriften, Karriereratgeber) als Beratungs- und/oder Informationsquelle für meinen Entscheidungsprozess genutzt.

it9: (k08i): Ich habe sehr häufig meine Betreuer(innen) für meine Promotion als Beratungs- und/oder Informationsquelle für meinen Entscheidungsprozess genutzt.


ao1: 1 : 1 : trifft gar nicht zu

ao2: 2 : 2 : : 

ao3: 3 : 3 : : 

ao4: 4 : 4 : : 

ao5: 5 : 5 : trifft völlig zu

ao6: 6 : 6 : Kann ich nicht beurteilen.

mv:

ka:

vc:



av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao6 bitte von anderen ao absetzen

tr:

GOTO E01

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________E01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adem01

qt: Einfachauswahl mit vertikalen ao

hl: Wir haben noch ein paar Fragen zu Ihrer Person.

in: 

q: Welches Geschlecht haben Sie?

is:

it:

ao1: 1 : : Weiblich

ao2: 2 : : Männlich

ao3: 3 : : Divers

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E02

hi: Bitte hier Icon 5 für Modul D einbauen (oben rechts) und durchgängig
einblenden bis das nächste Modul E beginnt.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E02_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adem02

qt: offene Frage (number)

hl:

in:

q: Wann wurden Sie geboren?

is:

it:

ao1: 4cm, Präfix [ao]: Jahr: [number]

mv:

ka:

vc:

av: number : 4 stellig : 1920 TO 2000

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
adem02 \< 1920)

fv:

hv:

fo:

tr:

GOTO E03

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: adem03/adem04

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Wo wurden Sie geboren?

is:

it:

ao1: (adem03): In Deutschland

ao2: (adem03): In einem anderen Land, und zwar: (adem04): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E04 IF adem02 \< 1991 AND adem03 = 1

GOTO E05 IF adem03 = 2

GOTO E06a IF adem02 \> 1990 OR adem02 = SYSMISS OR adem03 = SYSMISS

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E04_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adem02 \< 1991 AND adem03 = 1

(wenn E02 („Geburtsjahr“) \< 1991 und E03 („Geburtsland“) = 1 („Deutschland“))

vn: adem05a/adem05b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in: Am 3. Oktober 1990 erfolgte die deutsche Wiedervereinigung. Am 1. Juli 1990
erfolgte die Währungs-, Wirtschafts- und Sozialunion zwischen der Bundesrepublik
Deutschland (BRD) und der Deutschen Demokratischen Republik (DDR).

q: Wo lebten Sie am 30. Juni 1990?

is:

it:

ao1: (adem05a): 1 : : In der BRD

ao2: (adem05a): 2 : : In der DDR

ao3: (adem05a): 3 : : In einem anderen Land, und zwar: (adem05b): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E06a

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E05_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adem03 = 2

(alle Statusgruppen und E03 („Geburtsland“) = 2 („anderes Land“)

vn: adem06

qt: offene Frage (number)

hl:

in:

q: Seit wann leben Sie in Deutschland?

is:

it:

ao1: 4 cm, Präfix [ao]: Jahr: [number]

mv:

ka:

vc:

av: number : 4 stellig : 1920 TO 2019

kh: Das Jahr der Zuwanderung darf nicht vor dem Geburtsjahr liegen. Bitte korrigieren Sie Ihre Eingabe. (IF
adem06 < adem02)

fv:

hv:

fo:

tr:

GOTO E06a

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E06a_________________________________________\_
------------------------------------------------------------------------------------------

tc: (alle)

vn: adem07a/adem07b/adem10

qt: Mehrfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Welche Staatsangehörigkeit(en) haben Sie?

is: Wenn Sie mehr als eine Staatsangehörigkeit haben, geben Sie bitte alle an.

it:

ao1: (adem07a): 1 : : Deutsche Staatsangehörigkeit

ao2: (adem07b): 1 : : Andere Staatsangehörigkeit(en), und zwar: (adem10): [string] 6
cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E06b IF adem07a = 1

GOTO E07 IF ELSE

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E06b_________________________________________\_
------------------------------------------------------------------------------------------

tc: IF adem07a = 1

((alle) und wenn E06a Staatsangehörigkeit (adem07a) = 1 „Deutsche
Staatsangehörigkeit“)

vn: adem08/adem09

qt: Einfachauswahl mit vertikalen ao und offener ao (number)

hl:

in:

q: Seit wann besitzen Sie die deutsche Staatsangehörigkeit?

is:

it:

ao1: (adem08): 1 : : seit Geburt

ao2: (adem08): 2 : : seit dem Jahr: (adem09): [number] 4 cm

mv:

ka:

vc:

av: number : 4 stellig : 1920 TO 2019

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
adem09 \< adem02)

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E07

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn1: apar01a/apar02a

vn2: apar01b/apar02b

qt: Comparison mit vertikalen ao und offener ao (string)

hl:

in: Nun zu Ihren Eltern

q: Wo wurden Ihre Eltern geboren?

is: Bitte beziehen Sie sich im Folgenden auf die Person(en), mit denen Sie bis
zum 15. Lebensjahr den größten Teil Ihrer Kindheit verbracht haben, also ggf.
auch Stiefvater, Stiefmutter oder Adoptiveltern.

it:

mv:

ka1: !!Vater!!

ao1: (apar01a): 1 : : In Deutschland

ao2: (apar01a): 2 : : In einem anderen Land, und zwar: (apar02a): [string] 6 cm

ao3: (apar01a): 3 : : Weiß ich nicht/Vater unbekannt

ka2: !!Mutter!!

ao1: (apar01b): 1 : In Deutschland

ao2: (apar01b): 2 : In einem anderen Land, und zwar: (apar02b): [string] 6 cm

ao3: (apar01b): 3 : Weiß ich nicht/Vater unbekannt

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E08 IF apar01a = 2 OR apar01b = 2

GOTO E09 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) OR (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

GOTO E18 IF (apar01a = 3 OR apar01a = SYSMISS) AND (apar01b = 3 OR apar01b =
SYSMISS)

hi: Endung a bei (vn) bezieht sich auf den Vater und b auf die Mutter

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E08_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF apar01a = 2 OR apar01b = 2

(wenn E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) = 2 („in einem
anderen Land“))

vn: apar03a/apar03b

qt: Comparison mit vertikalen ao

hl:

in:

q1: Sind Ihre Eltern nach Deutschland zugewandert?

q2: Ist Ihr Vater nach Deutschland zugewandert?

q3: Ist Ihre Mutter nach Deutschland zugewandert?

is:

it:

ka1: (apar03a): !!Vater!!

ao1: (apar03a): 1 : : Ja

ao2: (apar03a): 2 : : Nein

ka2: (apar03b): !!Mutter!!

ao1: (apar03b): 1 : : Ja

ao2: (apar03b): 2 : : Nein

mv:

ka:

vc:

SHOW q1 IF apar01a = 2 AND apar01b = 2

SHOW ka1 AND ka2 IF apar01a = 2 AND apar01b = 2

SHOW q2 IF apar01a = 2 AND (apar01b \<\> 2 OR apar01b = SYSMISS)

SHOW ka1 IF apar01a = 2 AND (apar01b \<\> 2 OR apar01b = SYSMISS)

SHOW q3 IF (apar01a \<\> 2 OR apar01a = SYSMISS) AND apar01b = 2

SHOW ka2 IF (apar01a \<\> 2 OR apar01a = SYSMISS) AND apar01b = 2

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E09

hi: Endung a (bei vn) bezieht sich auf den Vater und b auf die Mutter

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND (apar01a \<\> 3 AND apar01a \<\> SYSMISS)
OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn1: apar04aa/apar04ab/apar05a

vn2: apar04ba/apar04bb/apar05b

qt: Comparison mit vertikaler Mehrfachauswahl und offener ao (string)

hl:

in:

q1: Welche Staatsangehörigkeit(en) haben Ihre Eltern?

is1: Wenn Ihre Eltern mehr als eine Staatsangehörigkeit haben, geben Sie bitte
alle an.

q2: Welche Staatsangehörigkeit(en) hat Ihr Vater?

is2: Wenn Ihr Vater mehr als eine Staatsangehörigkeit hat, geben Sie bitte alle
an.

q3: Welche Staatsangehörigkeit(en) hat Ihre Mutter?

is3: Wenn Ihre Mutter mehr als eine Staatsangehörigkeit hat, geben Sie bitte
alle an.

it:

ka1: !!Vater!!

ao1: (apar04aa): 1 : : Deutsche Staatsangehörigkeit

ao2: (apar04ab): 1 : : Andere Staatsangehörigkeit, und zwar: (apar05a): [string]
6 cm

ka2: !!Mutter!!

ao1: (apar04ba): 1 : : Deutsche Staatsangehörigkeit

ao2: (apar05bb): 1 : : Andere Staatsangehörigkeit, und zwar: (apar05b): [string]
6 cm

mv:

ka:

vc:

SHOW q1 AND is1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3
AND apar01b \<\> SYSMISS)

SHOW ka1 – ka2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3
AND apar01b \<\> SYSMISS)

SHOW q2 AND is2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW ka1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW q3 AND is3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

SHOW ka2 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E10 IF apar04aa = TRUE OR apar04ba = TRUE

GOTO E11 IF apar04aa = FALSE AND apar04ba = FALSE

hi: Die erste Endung a (bei vn) bezieht sich auf den Vater und b auf die Mutter;
der zweite Buchstabe (a oder b) auf ao1 (a) oder ao2 (b)

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (apar04aa = TRUE AND (apar01a \<\> 3 AND apar01 \<\> SYSMISS) OR
(apar04ba = TRUE AND apar01b = \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {{E09 („Staatsangehörigkeit Vater“) = 1 („deutsch“) und E07 („Geburtsland
Vater“) \<\> 3 („weiß nicht/Vater unbekannt“)} oder {E09 („Staatsangehörigkeit
Mutter“) = 1 („deutsch“) und E07 („Geburtsland Mutter“) \<\> 3 („weiß
nicht/Mutter unbekannt“)}})

vn1: apar06a/apar07a

vn2: apar06b/apar07b

qt: Comparison mit vertikalen ao und offener ao (string)

hl:

in:

q1: Wo lebten Ihre Eltern am 30. Juni 1990?

q2: Wo lebte Ihr Vater am 30. Juni 1990?

q3: Wo lebte Ihre Mutter am 30. Juni 1990?

is:

it:

ka1: !!Vater!!

ao1: (apar06a): 1 : : In der BRD

ao2: (apar06a): 2 : : In der DDR

ao3: (apar06a): 3 : : In einem anderen Land, und zwar: (apar07a): [string] 6 cm

ka2: !!Mutter!!

ao1: (apar06b): 1 : : In der BRD

ao2: (apar06b): 2 : : In der DDR

ao3: (apar06b): 3 : : In einem anderen Land, und zwar: (apar07b): [string] 6 cm

mv:

ka:

vc:

SHOW q1 IF apar04aa = TRUE AND apar04ba = TRUE

SHOW ka1 AND ka2 IF apar04aa = TRUE AND apar04ba = TRUE

SHOW q2 IF apar04aa = TRUE AND apar04ba = FALSE

SHOW ka1 IF apar04aa = TRUE AND apar04ba = FALSE

SHOW q3 IF apar04aa = FALSE AND apar04ba = TRUE

SHOW ka2 IF apar04aa = FALSE AND apar04ba = TRUE

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E11

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND (apar01a \<\> 3 AND apar01a \<\> SYSMISS)
OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn1: apar08a/apar09a

vn2: apar08b/apar09b

qt: Comparison mit vertikalen ao und offener ao (string)

hl:

in:

q1: Welchen höchsten Schulabschluss haben Ihre Eltern?

q2: Welchen höchsten Schulabschluss hat Ihr Vater?

q3: Welchen höchsten Schulabschluss hat Ihre Mutter?

is: Bei im Ausland erworbenen allgemein bildenden Schulabschlüssen geben Sie bitte an, welchem Abschluss in Deutschland dieser Schulabschluss ungefähr entspricht.

it:

ka1: !!Vater!!

ao1: (apar08a): 1 : : Allgemeine Hochschulreife/Abitur

ao2: (apar08a): 2 : : Fachgebundene Hochschulreife

ao3: (apar08a): 3 : : Fachhochschulreife

ao4: (apar08a): 4 : : Realschulabschluss (Mittlere Reife), Polytechnische
Oberschule der DDR mit Abschluss der 10. Klasse

ao5: (apar08a): 5 : : Hauptschulabschluss, Polytechnische Oberschule der DDR mit
Abschluss der 8. oder 9. Klasse

ao6: (apar08a): 6 : : Kein Abschluss/unter 8. Klasse

ao7: (apar08a): 7 : : Schulabschluss unbekannt

ao8: (apar08a): 8 : : Einen anderen Schulabschluss, und zwar: (apar09a):
[string] 6 cm

ka2: !!Mutter!!

ao1: (apar08b): 1 : : Allgemeine Hochschulreife/Abitur

ao2: (apar08b): 2 : : Fachgebundene Hochschulreife

ao3: (apar08b): 3 : : Fachhochschulreife

ao4: (apar08b): 4 : : Realschulabschluss (Mittlere Reife), Polytechnische
Oberschule der DDR mit Abschluss der 10. Klasse

ao5: (apar08b): 5 : : Hauptschulabschluss, Polytechnische Oberschule der DDR mit
Abschluss der 8. oder 9. Klasse

ao6: (apar08b): 6 : : Kein Abschluss/unter 8. Klasse

ao7: (apar08b): 7 : : Schulabschluss unbekannt

ao8: (apar08b): 8 : : Einen anderen Schulabschluss, und zwar: (apar09b):
[string] 6 cm

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW ka1 AND ka2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\>
3 AND apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW ka1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

SHOW ka2 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E12

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND (apar01a \<\> 3 AND apar01a \<\> SYSMISS)
OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn1: apar10a

vn2: apar10b

qt: Comparison mit vertikalen ao

hl:

in:

q1: Welchen höchsten Ausbildungsabschluss haben Ihre Eltern?

q2: Welchen höchsten Ausbildungsabschluss hat Ihr Vater?

q3: Welchen höchsten Ausbildungsabschluss hat Ihre Mutter?

is: Bei im Ausland erworbenen beruflichen Ausbildungsabschlüssen geben Sie bitte an, welchem Abschluss in Deutschland dieser berufliche Ausbildungsabschluss ungefähr entspricht.

it:

ka1: (apar10a): !!Vater!!

ao1: (apar10a): 1 : : Promotion (Doktortitel)

ao2: (apar10a): 2 : : Universitätsabschluss

ao3: (apar10a): 3 : : Fachhochschulabschluss

ao4: (apar10a): 4 : : Abschluss an einer Fachschule (nur DDR)

ao5: (apar10a): 5 : : Abschluss an einer Meister-/ Techniker-/Fachschule,
Berufs- oder Fachakademie

ao6: (apar10a): 6 : : Beruflich-betriebliche Berufsausbildung (Lehre)

ao7: (apar10a): 7 : : Beruflich-schulische Ausbildung (Berufsfachschule,
Handelsschule)

ao8: (apar10a): 8 : : Sonstigen beruflichen Abschluss

ao9: (apar10a): 9 : : Keinen beruflichen Abschluss

ao10: (apar10a): 10 : : Beruflicher Abschluss unbekannt

ka2: (apar10b): !!Mutter!!

ao1: (apar10b): 1 : : Promotion (Doktortitel)

ao2: (apar10b): 2 : : Universitätsabschluss

ao3: (apar10b): 3 : : Fachhochschulabschluss

ao4: (apar10b): 4 : : Abschluss an einer Fachschule (nur DDR)

ao5: (apar10b): 5 : : Abschluss an einer Meister-/ Techniker-/Fachschule,
Berufs- oder Fachakademie

ao6: (apar10b): 6 : : Beruflich-betriebliche Berufsausbildung (Lehre)

ao7: (apar10b): 7 : : Beruflich-schulische Ausbildung (Berufsfachschule,
Handelsschule)

ao8: (apar10b): 8 : : Sonstigen beruflichen Abschluss

ao9: (apar10b): 9 : : Keinen beruflichen Abschluss

ao10: (apar10b): 10 : : Beruflicher Abschluss unbekannt

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW ka1 AND ka2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\>
3 AND apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW ka1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

SHOW ka2 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E13

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E13_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND IF (apar01a \<\> 3 AND apar01a \<\>
SYSMISS) OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn1: apar11a

vn2: apar11b

qt: Comparison mit vertikalen ao

hl:

in:

q1: Welche berufliche Stellung nehmen Ihre Eltern ein?

q2: Welche berufliche Stellung nimmt Ihr Vater ein?

q3: Welche berufliche Stellung nimmt Ihre Mutter ein?

is: Wenn Ihre Eltern nicht mehr berufstätig oder bereits verstorben sind, geben Sie bitte die letzte berufliche Stellung an.

it:

ka1: (apar11a): !!Vater!!

ao1: (apar11a): 1 : : Selbstständiger mit Angestellten

ao2: (apar11a): 2 : : Selbstständiger ohne Angestellte

ao3: (apar11a): 3 : : Angestellter

ao4: (apar11a): 4 : : Beamter

ao5: (apar11a): 5 : : Arbeiter

ao6: (apar11a): 6 : : Nie erwerbstätig gewesen

ao7: (apar11a): 7 : : Berufliche Stellung unbekannt

ao8: (apar11a): 8 : : Kann ich nicht einordnen.

ka2: (apar11b): !!Mutter!!

ao1: (apar11b): 1 : : Selbstständige mit Angestellten

ao2: (apar11b): 2 : : Selbstständige ohne Angestellten

ao3: (apar11b): 3 : : Angestellte

ao4: (apar11b): 4 : : Beamtin

ao5: (apar11b): 5 : : Arbeiterin

ao6: (apar11b): 6 : : Nie erwerbstätig gewesen

ao7: (apar11b): 7 : : Berufliche Stellung unbekannt

ao8: (apar11b): 8 : : Kann ich nicht einordnen.

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW ka1 AND ka2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\>
3 AND apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW ka1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

SHOW ka2 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E15 IF apar11a = 6 AND apar11b = 6

GOTO E14

hi: Die Antwortoptionen unterscheiden sich jeweils nach Vater und Mutter

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E14_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) OR (apar01b \<\> 3 AND apar01b
\<\> SYSMISS) 

(wenn {E07 („Geburtsland Vater“) \<\> 3 („weiß nicht/Vater unbekannt“)} oder
{E07 („Geburtsland Mutter“) \<\> 3 („weiß nicht/Mutter unbekannt“)}})

vn1: apar12a/apar13a

vn2: apar12b/apar13b

qt: Comparison mit offenen ao (string)

hl:

in:

q1: Welchen Beruf üben/übten Ihre Eltern aktuell bzw. zuletzt hauptberuflich
aus?

q2: Welchen Beruf übt(e) Ihr Vater aktuell bzw. zuletzt hauptberuflich aus?

q3: Welchen Beruf übt(e) Ihre Mutter aktuell bzw. zuletzt hauptberuflich aus?

is1: Bitte beschreiben Sie hierbei den ausgeübten Beruf der Eltern !!möglichst
genau!!, z. B. Speditionskauffrau/-mann, Blumenverkäufer(in),
Maschinenschlosser(in), Realschullehrer(in); tragen Sie !!bitte nicht!!
Arbeiter(in), Angestellte(r), Beamter/Beamtin ein.

is2: Bitte beschreiben Sie hierbei den ausgeübten Beruf Ihres Vaters !!möglichst
genau!!, z. B. Speditionskaufmann, Blumenverkäufer, Maschinenschlosser,
Realschullehrer; tragen Sie !!bitte nicht!! Arbeiter, Angestellter, Beamter ein.

is3: Bitte beschreiben Sie hierbei den ausgeübten Beruf Ihrer Mutter !!möglichst
genau!!, z. B. Speditionskauffrau, Blumenverkäuferin, Maschinenschlosserin,
Realschullehrerin; tragen Sie !!bitte nicht!! Arbeiterin, Angestellte, Beamtin
ein.

it:

ka1: !!Vater!!

ao1: (apar12a): 6 cm, Präfix [ao]: Beruf [string]

ao2: (apar13a): 6 cm, Präfix [ao]: ggf. Erläuterungen [string]

ka2: !!Mutter!!

ao1: (apar12b): 6 cm, Präfix [ao]: Beruf [string]

ao2: (apar13b): 6 cm, Präfix [ao]: ggf. Erläuterungen [string]

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS) AND (apar11a \<\> 6 AND apar11b \<\> 6)

SHOW ka1 AND ka2 IF (apar01a \<\> 3 OR apar01a \<\> SYSMISS) AND (apar01b \<\> 3
OR apar01b \<\> SYSMISS) AND (apar11a \<\> 6 AND apar11b \<\> 6)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS) OR ((apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS) AND (apar11a \<\> 6 AND apar11b = 6))

SHOW ka1 IF ((apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)) OR ((apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS) AND (apar11a \<\> 6 AND apar11b = 6))

SHOW q3 IF ((apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)) OR ((apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS) AND (apar11b \<\> 6 AND apar11a = 6))

SHOW ka2 IF ((apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)) OR ((apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS) AND (apar11b \<\> 6 AND apar11a = 6))

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E15 IF adbi01 = 1 OR adbi01 = 3

GOTO E18 IF adbi01 = 2 OR adbi01 = 4

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E15_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND IF (apar01a \<\> 3 AND apar01a \<\>
SYSMISS) OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn: apar14

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q1: Unterhalten Sie sich mit Ihren Eltern über Inhalte Ihrer Promotion?

q2: Unterhalten Sie sich mit Ihrem Vater über Inhalte Ihrer Promotion?

q3: Unterhalten Sie sich mit Ihrer Mutter über Inhalte Ihrer Promotion?

is:

it:

ao1: 1 : : Ja, aber eher oberflächlich.

ao2: 2 : : Ja, über einzelne Aspekte.

ao3: 3 : : Ja, auch sehr detailliert.

ao4: 4 : : Nein, gar nicht.

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E16

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND (apar01a \<\> 3 AND apar01a \<\> SYSMISS)
OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn: apar15a /apar15b

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q1: Wie gut verstehen Sie sich mit Ihren Eltern …

q2: Wie gut verstehen Sie sich mit Ihrem Vater …

q3: Wie gut verstehen Sie sich mit Ihrer Mutter …

is:

it1: (apar15a): bei gesellschaftspolitischen Themen?

it2: (apar15b): bei Themen des Alltags, der Freizeit und Lebensführung?

ao1: 1 : : überhaupt nicht gut

ao2: 2 : : weniger gut

ao3: 3 : : gut

ao4: 4 : : sehr gut

ao5: 5 : : Wir unterhalten uns gar nicht über solche Themen.

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster) und ao6 absetzen

tr:

GOTO E17

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E17_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF (adbi01 = 1 OR adib01 = 3) AND (apar01a \<\> 3 AND apar01a \<\> SYSMISS)
OR (apar01b \<\> 3 AND apar01b \<\> SYSMISS)

(wenn {A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)} und
{E07 („Geburtsland Vater“) oder E07 („Geburtsland Mutter“) ≠ 3 („weiß nicht /
unbekannt“)}])

vn: apar16a/apar16b

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q1: Wie wichtig ist es Ihren Eltern, dass …

q2: Wie wichtig ist es Ihrem Vater, dass …

q3: Wie wichtig ist es Ihrer Mutter, dass …

is:

it1: (apar16a): Sie promovieren?

it2: (apar16b): Sie beruflich erfolgreich sind?

ao1: 1 : : gar nicht wichtig

ao2: 2 : : eher unwichtig

ao3: 3 : : teils/teils

ao4: 4 : : wichtig

ao5: 5 : : sehr wichtig


ao6a: 6 : : Meine Eltern haben keine Meinung dazu.

ao6b: 6 : : Mein Vater hat keine Meinung dazu.

ao6c: 6 : : Meine Mutter hat keine Meinung dazu.

mv:

ka:

vc:

SHOW q1 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW ao6a IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b \<\> 3 AND
apar01b \<\> SYSMISS)

SHOW q2 IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR apar01b
= SYSMISS)

SHOW ao6b IF (apar01a \<\> 3 AND apar01a \<\> SYSMISS) AND (apar01b = 3 OR
apar01b = SYSMISS)

SHOW q3 IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR apar01a
= SYSMISS)

SHOW ao6c IF (apar01b \<\> 3 AND apar01b \<\> SYSMISS) AND (apar01a = 3 OR
apar01a = SYSMISS)

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster); ao6 absetzen

tr:

GOTO E18

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E18_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: aedb01a/aedb01b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Wo haben Sie Ihre Studienberechtigung erworben?

is:

it:

ao1: (aedb01a): 1 : : In Deutschland

ao2: (aedb01a): 2 : : In einem anderen Land, und zwar: (aedb01b): [string] 6 cm

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E19

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E19_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: aedb02/aedb03

qt: 2 offene Fragen (Matrix)

hl:

in:

q: In welchem Jahr und mit welcher Abschlussnote haben Sie Ihre
Studienberechtigung (z. B. Abitur) erworben?

is: Geben Sie bitte an, welcher Note des deutschen Systems (beste Note: 1,0; schlechteste Note: 4,0) Ihre ausländische
Abschlussnote entspricht.

it:

ao1: (aedb02): 3 cm, Präfix [ao]: Abschlussjahr: [number]

ao2: (aedb03): 2 cm, Präfix [ao]: Abschlussnote (1,0 bis 4,0): [number]

mv:

ka:

vc:

SHOW is IF aedb01a = 2

av: (aedb02): number : 4 stellig : 1930 TO 2019

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
(aedb02 - 12 \< adem02) OR (aedb02 \> 2019) OR (aedb03 \< 1,0 OR aedb03 \> 4,0)

fv:

hv:

fo:

tr:

GOTO S16 IF preload01 = 4 AND aedb01a = 1

GOTO E20

hi: (aedb03): als Notenfeld deklarieren

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________S16_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 4 AND aedb01a = 1
(wenn preload01 = 4 ("Saarbrücken") und E19 ("wo HZB erworben") = 1 ("in Deutschland"))

vn: s16

qt: Einfachauswahl mit drop-down Menü

hl:

in:

q: In welchem Bundesland haben Sie Ihre Hochschulzugangsberechtigung erworben?

is: 

it:

ao1: (s16): Baden-Württemberg, Bayern, Berlin, Brandenburg, Bremen, Hamburg, Hessen, Mecklenburg-Vorpommern, Niedersachsen, Nordrhein-Westfalen, Rheinland-Pfalz, Saarland, Sachsen, Sachsen-Anhalt, Schleswig-Holstein, Thüringen

mv:

ka:

vc:

av: 

kh: 

fv:

hv:

fo:

tr:

GOTO E20

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E20_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: aedb04(aedb04a/aedb04b/aedb04c/aedb04d/aedb04e/aedb04f/aedb04ga/aedb04gb/aedb04h)

qt: offene Fragen (string); Einfachauswahl mit vertikalen ao und offener ao
(string); offene Fragen (number)

hl:

in:

q: Wir bitten Sie noch um Angaben zu dem Studienabschluss, der Sie zur Aufnahme
Ihrer Promotion berechtigte.

is:  Sofern Sie noch keinen Abschluss haben (z. B. als Promovierende(r) der Medizin), lassen Sie die Seite bitte unausgefüllt. 
Bei ausländischen Studienabschlüssen geben Sie bitte an, welcher Note des
deutschen Systems (1,0 (sehr gut) bis 4,0 (ausreichend)) Ihre Abschlussnote entspricht.

it1: (aedb04a): 6 cm, Präfix [ao]: Studienfach: [string]

it2: (aedb04b): 6 cm, Präfix [ao]: Name der Hochschule (z. B. Universität
Erlangen-Nürnberg): [string]

it3: (aedb04c): 6 cm, Präfix [ao]: Standort der Hochschule (z. B. Nürnberg):
[string]

it4: (aedb04d): 6 cm, Präfix [ao]: Land (z. B. Deutschland): [string]

it5: (aedb04e): Art des Abschlusses:

ao1: (aedb04e): 1 : : Bachelor

ao2: (aedb04e): 2 : : Master

ao3: (aedb04e): 3 : : Staatsexamen

ao4: (aedb04e): 4 : : Diplom

ao5: (aedb04e): 5 : : Magister

ao6: (aedb04e): 6 : : Sonstiges, und zwar: (aedb04f): [string] 6 cm

it6: Gesamtnote (1,0 bis 4,0): (aedb04ga): [number] bzw. Punktzahl (4,00 bis 18,00): (aedb04gb): [number]

it7: (aedb04h): 3 cm, Präfix [ao]: Abschlussjahr: [number]

mv:

ka:

vc:

av:

(aedb04ga): number : 2 stellig : 1, 0 TO 4,0;

(aedb04gb): number : \<=4 stellig : 4,00 TO 18,00;

(aedb04h): number : 4 stellig : 1940 TO 2019

kh: Bitte überprüfen und korrigieren Sie Ihre Eingabe. (IF
(aedb04ga \< 1,0 OR aedb04ga\> 4,0) OR (aedb04gb \< 4,00 OR aedb04gb \> 18,00) OR
(aedb04h - 16 \< adem02))

fv:

hv:

fo: Items (Zebramuster)

tr:

GOTO K09 IF preload01 = 2

GOTO E21 if adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO F01 if adbi01 = 4

hi: (aedb04ga): als Notenfeld deklarieren; (aedb04gb): Komma zulassen (ähnlich
wie Notenfeld)

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K09_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2
(wenn preload01 = 2 ("Kiel"))

vn: k09a/k09b/k09c/k09d/k09e/k09f/k09g/k09h/k09i/k09j

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche der folgenden Inhalte und Kompetenzen haben Sie in Ihrem Studium vor Ihrer Promotion erworben?

is: 

it: 

ao1: (k09a): Verfassen umfangreicher wissenschaftlicher Texte

ao2: (k09b): Forschungsdatenmanagement

ao3: (k09c): Labormethoden

ao4: (k09d): Statistik

ao5: (k09e): Programmieren

ao6: (k09f): Sprachen

a07: (k09g): Bearbeitung einer Fragestellung, die zwei oder mehrere Fachdisziplinen einbezieht 

ao8: (k09h): Zusammenarbeit mit Partnerinnen und/oder Partnern aus mindestens einer anderen Fachdisziplin 

ao9: (k09i): Verwendung mindestens einer anderen Fachdisziplin

ao10: (k09j): Keine der genannten Inhalte und Kompetenzen habe ich in meinem Studium vor meiner Promotion erworben. [EK]

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao10 von den übrigen Antwortoptionen absetzen

tr:

GOTO K10

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K10_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2
(wenn preload01 = 2 ("Kiel"))

vn: k10a/k10b/k10c/k10d/k10e/k10f/k10g/k10h/k10i/k10j

qt: Mehrfachauswahl mit vertikalen ao

hl:

in:

q: Welche der folgenden Inhalte und Kompetenzen haben Sie während Ihrer Promotion angewendet und/oder neu erworben?

is: 

it: 

ao1: (k10a): Verfassen umfangreicher wissenschaftlicher Texte

ao2: (k10b): Forschungsdatenmanagement

ao3: (k10c): Labormethoden

ao4: (k10d): Statistik

ao5: (k10e): Programmieren

ao6: (k10f): Sprachen

a07: (k10g): Bearbeitung einer Fragestellung, die zwei oder mehrere Fachdisziplinen einbezieht 

ao8: (k10h): Zusammenarbeit mit Partnerinnen und/oder Partnern aus mindestens einer anderen Fachdisziplin 

ao9: (k10i): Verwendung mindestens einer anderen Fachdisziplin

ao10: (k10j): Keine der genannten Inhalte und Kompetenzen habe ich während meiner Promotion angewendet und/oder neu erworben [EK]


mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Items (Zebramuster); ao10 von den übrigen Antwortoptionen absetzen

tr:

GOTO K11

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________K11_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2
(wenn preload01 = 2 ("Kiel"))

vn: k11

qt: offene Frage (string)

hl:

in:

q: Welche Qualifikationen, die Sie im Studium an der Christian-Albrechts-Universität zu Kiel erworben haben, haben Ihnen während Ihrer Promotion besonders geholfen?

is: 

it: 

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO K12

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________K12_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 2
(wenn preload01 = 2 ("Kiel"))

vn: k12

qt: offene Frage (string)

hl:

in:

q: Welche Form und Struktur der Unterstützung würden Sie sich während Ihrer Promotion wünschen (u. a. in Hinblick auf die Zusammenarbeit mit außerakademischen Stakeholdern, Beratungs- und Informationsangebote zu wissenschaftlichen und/oder nicht-wissenschaftlichen Karrierewegen, weitere Qualifikationsangeboten für konkrete Inhalte und Kompetenzen)?

is: 

it: 

ao: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO E21 IF adbi01 = 1 OR adbi01 = 2 OR adbi01 = 3

GOTO F01 IF adbi01 = 4

hi: bitte als Kommentarfeld programmieren 

\-------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________E21_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adib01 = 2 OR adib01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“), 2 („abgeschlossen“) oder 3
(„unterbrochen“))

vn: adcd23

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Fühlen Sie sich ausreichend über das deutsche Wissenschaftssystem informiert?

is:

it:

ao1: 1 : : Ja

ao2: 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO P07 IF preload01 = 3

GOTO E22 IF adbi01 = 1 OR adbi01 = 3

GOTO F01 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________P07_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF preload01 = 3

(wenn preload01 = 3 ("Potsdam"))

vn: p07a/p07b

qt: Einfachauswahl mit vertikalen ao und offener ao (string)

hl:

in:

q: Hätten Sie sich im Vorfeld Ihrer Promotion mehr Informationen zum Thema Promovieren, wie beispielsweise eine Informationsveranstaltung, gewünscht?

is:

it:

ao1: (p07a): 1 : : Ja, und zwar: (p07b): [string] 8 cm; 2 Zeilen

ao2: (p07a): 2 : : Nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr:

GOTO E22 IF adbi01 = 1 OR adbi01 = 3

GOTO F01 IF adbi01 = 2

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________E22_________________________________________\_
-----------------------------------------------------------------------------------------

tc: IF adbi01 = 1 OR adib01 = 3

(wenn A01 („Promotionsstatus“) = 1 („promoviere“) oder 3 („unterbrochen“)

vn: acrg13

qt: offene Frage (string)

hl:

in:

q: Welche Wünsche haben Sie mit Blick auf den weiteren Fortgang der Promotion?

is:

it:

ao1: [string] 8 cm, 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO F01

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________F01_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

vn: ainf01

qt: Mehrfachauswahl

it:

q1: In etwa einem Jahr möchten wir Sie gerne zu einer weiteren Nacaps-Befragung einladen. Wenn Sie an dieser weiteren 
Befragung oder an der Verlosung teilnehmen möchten, klicken Sie bitte auf den [Link](Link zum add-on). 
In beiden Fällen benötigen wir Ihre Kontaktdaten. 

is: Wir sichern Ihnen zu, dass Ihre Kontaktdaten streng getrennt von Ihren Angaben in der Befragung verarbeitet 
und gespeichert werden.

ao1: (ainf01): Nein, ich möchte nicht an der Folgebefragung teilnehmen und verzichte auch auf die Teilnahme an der Verlosung.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: 

tr:

GOTO F02

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________F02_________________________________________\_
-----------------------------------------------------------------------------------------

tc:

vn: ainf02

qt: Mehrfachauswahl

hl:  Für den Erfolg von Nacaps ist es von besonderer Wichtigkeit, dass wir Sie erneut befragen dürfen. Nacaps ist als 
Längsschnittstudie konzipiert, um Promotions- und Karriereverläufe über einen längeren Zeitraum untersuchen zu können. 
Deshalb möchten wir Sie noch einmal darum bitten, dass wir Sie in etwa einem Jahr erneut kontaktieren dürfen. 

in:

q: Wenn Sie an der weiteren Befragung oder an der Verlosung teilnehmen möchten, klicken Sie bitte auf den [Link](Link zum add-on).

is: Wir sichern Ihnen zu, dass Ihre Kontaktdaten streng getrennt von Ihren Angaben in der Befragung verarbeitet und 
gespeichert werden. 

it:

ao1: (ainf02): Nein, ich möchte nicht an der Folgebefragung teilnehmen und verzichte auch auf die Teilnahme an der Verlosung.

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr: 

GOTO F03

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________F03_________________________________________\_
-----------------------------------------------------------------------------------------

tc: 

vn: acmt01

qt: offene Frage (string)

hl:

in:

q: Wir sind bestrebt, unsere Befragungen stets weiter zu verbessern. Gibt es
Ihrer Meinung nach Themen, die unmittelbar mit Ihrer Promotion zusammenhängen,
aber nicht thematisiert wurden? Was haben Sie vermisst? Was möchten Sie 
noch anmerken?

Bitte beachten Sie, dass wir Ihnen aus Datenschutzgründen zu Ihren
Anmerkungen nicht persönlich antworten können. Bitte geben Sie in dieses Feld aus
diesem Grund auch keine Telefonnummer oder andere Kontaktdaten ein. Wenn
Sie Fragen haben, können Sie unsere Projektmitarbeiterinnen gerne unter den Telefonnummern +49 30 206 417 746 (Madeleine Siegel) oder +49 511 450 670 106 (Susanne Redeke) oder per E-Mail an [nacaps@dzhw.eu](mailto:nacaps\@dzhw.eu)
kontaktieren.

is: Zum Speichern Ihrer Angaben klicken Sie bitte auf "weiter".

it:

ao1: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO end

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________end_________________________________________\_
-----------------------------------------------------------------------------------------

tc: (alle)

ka1: !!Sie sind nun am Ende der Befragung angelangt und können das Fenster nun
schließen. Herzlichen Dank für Ihre Teilnahme!!!

ka2: !!Sie können das Fenster nun schließen.!!

is:  Auf der Website \#\#URL:www.nacaps.de\#\# und auf Twitter unter \#\#URL:@Nacaps_Panel\#\# finden Sie übrigens auch stets aktuelle Informationen zur Studie.

vc:

SHOW ka1 IF adbi01 \<\> SYSMISS AND flag_A01 = FALSE

SHOW ka2 IF (adbi01 = SYSMISS AND flag_A01 = TRUE) OR (aict01 = FALSE AND
flag_index = TRUE)

tr:

hi:

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________cancel1_________________________________________\_
---------------------------------------------------------------------------------------------

tc: IF aict01 = FALSE AND flag_index = TRUE

(wenn trotz Warntext (flag_index = TRUE) erneut keine Zustimmung (aict01 =
FALSE) zu den Datenschutzbestimmungen)

vn: acmt02

qt: offene Frage (string)

hl:

in:

q:

!!Liebe Teilnehmerin, lieber Teilnehmer,

bitte beachten Sie, dass eine Teilnahme an der Nacaps-Befragung nur möglich ist,
wenn Sie unseren Datenschutzbestimmungen zugestimmt haben.

Wenn Sie an der Nacaps-Befragung teilnehmen möchten, klicken Sie bitte
unten auf den Button „Zurück“ und stimmen Sie nachfolgend den
Datenschutzbestimmungen zu.

Ansonsten können Sie uns unten Kommentare und Anregungen zur Studie zukommen
lassen.!!

ao1: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO end

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________cancel2_________________________________________\_
---------------------------------------------------------------------------------------------

tc: IF adbi01 = SYSMISS AND flag_A01 = TRUE

(wenn trotz Warntext erneut keine Angabe zum Status der Promotion (adbi01))

vn: acmt03

qt: offene Frage (string)

hl:

in:

q:

!!Liebe Teilnehmerin, lieber Teilnehmer,

bitte beachten Sie, dass Sie die Nacaps-Befragung nur fortführen können, wenn
Sie eine Angabe zu der Frage gemacht haben, welchen Status Ihre Promotion hat.

Sofern Sie Interesse an der Teilnahme an der Studie haben, klicken Sie bitte
unten auf den Button „Zurück“ und beantworten Sie nachfolgend die Frage zum
Status Ihrer Promotion.

Ansonsten können Sie uns unten Kommentare und Anregungen zur Studie zukommen
lassen.!!

is:

it:

ao1: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO end

hi: großes Textfeld

\-------------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------------


\__________________________________________add-on1_________________________________________\_
--------------------------------------------------------------------------------------------

tc: 

vn: aict04, aict05, aict06

qt: Mehrfachauswahl

hl:

in:


q1: Bitte geben Sie an, für welche Zwecke wir Sie erneut kontaktieren dürfen und ob Sie an der Verlosung teilnehmen möchten.

it1: (aict04): Ja, ich bin damit einverstanden, dass Sie mich für weitere Nacaps-Befragungen erneut kontaktieren.

it2: (aict05): Ja, ich möchte über Nacaps-Ergebnisse informiert werden.

it3: (aict06): Ja, ich möchte an der Verlosung teilnehmen (Hauptpreis: 1 x Apple iPad Pro 11'' mit 256 GB im Wert von 1049 Euro)



mv:

ka:

vc:

av: 

kh:

fv:

hv:

fo: 

tr: GOTO add-on2 if aict04 = TRUE OR aict05 = TRUE OR aict05 = TRUE

GOTO add-on3 if ELSE

hi: 

\-------------------------------------------------------------------------------------------------------------------------------------------------



\__________________________________________add-on2_________________________________________\_
--------------------------------------------------------------------------------------------

tc:

vn: acnt01a,acnt01b,acnt02a, acnt02b, acnt03a, acnt03b, acnt03c, acnt03d, acnt03e, acnt03f, acnt03g, acnt03h

qt: offene Fragen (string) und (number); drop-down-Menü bei Anrede und Titel

hl:

in:


q1: Bitte geben Sie eine möglichst stabile E-Mail-Adresse an, über die wir Sie erreichen können. Gerne können Sie uns auch eine zusätzliche, ggf. private, E-Mail-Adresse geben.

ao1: (acnt01a): 8cm, Präfix [ao]: E-Mail-Adresse (über die Sie am besten zu erreichen sind): [string]

ao2: (acnt01b): 8cm, Präfix [ao]: Ggf. weitere E-Mail-Adresse: [string]


q2: Bitte geben Sie nun Ihre aktuelle Anschrift an. Zum Speichern Ihrer Angaben klicken Sie bitte auf "weiter".

is: 

it1: (acnt02a): Anrede:

it2: (acnt02b): Titel:

ao1: (acnt02a): Herr, Frau, --

ao2: (acnt02b): --, Dr., Prof., Prof. Dr.


it3:

ao1: (acnt03a): 8 cm, Präfix [ao]: Vorname: [string]

ao2: (acnt03b): 8 cm, Präfix [ao]: Nachname: [string]

ao3: (acnt03c): 8 cm, Präfix [ao]: Adresszeile 1 (Straße und Hausnummer, Postfach, Firma, c/o etc.): [string]

ao4: (acnt03d): 8 cm, Präfix [ao]: Adresszeile 2 (Adresszusatz, z. B.: Zi., Apt., Hinterhaus): [string]

ao5: (acnt03e): 5 cm, Präfix [ao]: Postleitzahl oder ZIP Code: [string]

a06: (acnt03f): 8 cm, Präfix [ao]: Ort: [string]

ao7: (acnt03g): 8 cm, Präfix [ao]: Ggf. Bundesstaat, Provinz, Region: [string]

ao8: (acnt03h): 8 cm, Präfix [ao]: Land: [string]


q3: Ihre Kontaktdaten werden stets getrennt von den Befragungsdaten verarbeitet und gespeichert.
Die Zustimmung zur Speicherung Ihrer Kontaktdaten können Sie jederzeit schriftlich 
(per E-Mail an \#\#URL:nacaps\@dzhw.eu\#\#) ohne Angabe von Gründen widerrufen. 
Wir werden Ihre Kontaktdaten dann unverzüglich löschen.

mv:

ka:

vc:

av: (aict03e): number : 5 stellig

kh:

fv:

hv:

fo: Antwortoptionen (Zebramuster)

tr: GOTO add-on3

hi: Add-on Seite für die Eingabe der Kontaktdaten durch die Teilnehmer. "q3" soll einfach als Text unterhalb der Textfelder angezeigt werden.

\-------------------------------------------------------------------------------------------------------------------------------------------------

\__________________________________________add-on3_________________________________________\_
-----------------------------------------------------------------------------------------

tc: 

vn: acmt04

qt: offene Frage (string)

hl:

in:

q: Wir sind bestrebt, unsere Befragungen stets weiter zu verbessern. Gibt es Ihrer Meinung nach Themen, die unmittelbar mit Ihrer Promotion zusammenhängen, aber nicht thematisiert wurden? Was haben Sie vermisst? Was möchten Sie noch anmerken?

Bitte beachten Sie, dass wir Ihnen aus Datenschutzgründen zu Ihren Anmerkungen nicht persönlich antworten können. 
Bitte geben Sie in dieses Feld aus diesem Grund auch keine Telefonnummer oder andere Kontaktdaten ein.
Wenn Sie Fragen haben, können Sie unsere Projektmitarbeiterinnen gerne unter den Telefonnummern +49 30 206 417 746 
(Madeleine Siegel) oder +49 511 450 670 106 (Susanne Redeke) oder per E-Mail an nacaps@dzhw.eu kontaktieren.

is: Zum Speichern Ihrer Angaben klicken Sie bitte auf "weiter".

it:

ao1: [string] 8 cm; 4 Zeilen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO end

hi: großes Textfeld
