# Selectoren-Kombinatoren

## Was sind CSS Selektoren?

Die einfachsten CSS-Selektoren sind Typ- oder Element-Selektoren. Tag-Namen wie p, div oder body suchen nach allen Elementen eines Typs und bringen CSS-Stile in HTML-Elemente.

Ein CSS-Selektor identifiziert HTML-Elemente durch Suchmuster, die miteinander kombiniert werden können, um aus einfachen Selektoren komplexe Filter zu erzeugen.

### Einfacher CSS-Selektor

Alle HTML-Elemente, die innerhalb des body-Elements sitzen, eignen sich als CSS-Selektoren.

Einfacher Element-Selector
a { text-decoration: none; }
p { color: rgb(80,80,10); }
^
|
+---- Element-Selektor

Damit Stylesheet-Regeln nicht immer auf alle Elemente – z.B. alle p-Elemente – angewendet werden, differenzieren Selektoren die Anwendung eines CSS-Stils. Die einfachsten Selektoren nutzen HTML-Attribute wie class und id, um besondere Elemente herauszufiltern.

Klassen- und ID-Selektoren
+-- ID-Selektor
|
v
#extlink { color: green; }
.meta { font-size: smaller }
^
|
+---- Klassen-Selektor

### Komplexe Selektoren

Darüber hinaus filtern Attribut - Selektoren Elemente mit bestimmten Attributen wie einem title- oder lang-Attribut und lassen sich anhand ihrer Position innerhalb des HTML-Dokuments (dem Kontext) identifizieren. Pseudoklassen und Pseudoelemente maskieren Elemente, die es im HTML-Quellcode nicht gibt – z.B. ein Link, über dem die Maus gerade hovert.
Diese grundlegenden Selektoren lassen sich miteinander kombinieren, so dass komplexe Suchmuster entstehen.

- Universal CSS selector | Universal-Selektor
  Alle Elemente der HTML-Seite
- {color: red }

<p>
type selector | Typ-Selektor
Alle p-Elemente der HTML-Seite
p { font-family: fantasy }

<p class="extra">
class selector | Klassen-Selektor
Alle p-Elemente mit dem Attribut class="extra"
.extra { font-size: 2em; } oder
p.extra { font-size: 2em }

<e id="foo">
ID-Selektor
Das HTML-Element mit dem Attribut id="foo"
#foo { float: right } oder
div#foo { float: right }

## CSS Kombinatoren

Ein Kombinator ist etwas, das die Beziehung zwischen den Selektoren erklärt.

Ein CSS-Selektor kann mehr als einen einfachen Selektor enthalten. Zwischen den einfachen Selektoren können wir eine combinator umfassen.
Es gibt vier verschiedene Kombinatoren in CSS3:
• Nachkomme Selektor (space)
• Kindselektor (>)
• benachbarte Geschwister - Selektor (+)
• allgemeine Geschwister - Selektor (~)

### Nachkomme Selector

Der Nachkomme Selektor passt auf alle Elemente, die Nachkommen eines bestimmten Elements sind.
Das folgende Beispiel wählt alle <p> Elemente innerhalb <div> Elemente:
Beispiel
div p {
    background-color: yellow;
}

### Kindselektor

Das Kind Selektor wählt alle Elemente, die die unmittelbaren Kinder eines bestimmten Elements sind.
Das folgende Beispiel wählt alle <p> Elemente, die unmittelbare Kinder eines <div> Element:
Beispiel
div > p {
    background-color: yellow;
}

### Benachbarte Geschwister Selector

Die benachbarten Geschwister-Selektor wählt alle Elemente, die die benachbarten Geschwister eines bestimmten Elements sind.
Geschwister Elemente müssen die gleiche Elternelement haben, und "benachbart" bedeutet "unmittelbar nach".
Das folgende Beispiel wählt alle <p> Elemente , die unmittelbar nach platziert werden <div> Elemente:
Beispiel
div + p {
    background-color: yellow;
}

### Allgemein Geschwister Selector

Die allgemeine Geschwister-Selektor wählt alle Elemente, die Geschwister eines bestimmten Elements sind.
Das folgende Beispiel wählt alle <p> Elemente , die Geschwister sind <div> Elemente:
Beispiel
div ~ p {
    background-color: yellow;
}
