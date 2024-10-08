# Variablen

Die meiste Zeit muss eine JavaScript-Anwendung mit Informationen arbeiten. Hier sind zwei Beispiele:
1. Ein Onlineshop - die Informationen können verkaufte Waren und einen Warenkorb enthalten.
2. Eine Chat-Anwendung - die Informationen können Benutzer, Nachrichten und vieles mehr beinhalten.

Diese Informationen werden in Variablen gespeichert.

## Eine Variable

Eine [Variable](https://de.wikipedia.org/wiki/Variable_(Programmierung)) ist ein "benannter Speicher" für Daten. Wir können Variablen verwenden, um Leckereien, Besucher und andere Daten zu speichern.

Um eine Variable in JavaScript zu erstellen, verwende das `let` Schlüsselwort.

Die folgende Anweisung erzeugt (mit anderen Worten: *deklariert*) eine Variable mit dem Namen "message":

```js
let message;
```

Nun können wir sie mit Daten befüllen, indem wir den Zuweisungsoperator `=` verwenden: 

```js
let message;

*!*
<<<<<<< HEAD
message = 'Hello'; // speichere diese Zeichenkette
=======
message = 'Hello'; // store the string 'Hello' in the variable named message
>>>>>>> a82915575863d33db6b892087975f84dea6cb425
*/!*
```

Diese Zeichenkette wird nun in den mit der Variable verbundenen Speicherbereich gespeichert. Wir können über den Variablennamen darauf zugreifen:

```js run
let message;
message = 'Hello!';

*!*
alert(message); // zeigt den Inhalt der Variable an
*/!*
```

Um es kurz zu machen, können wir die Variablendeklaration und -zuweisung in einer einzigen Zeile zusammenfassen:

```js run
let message = 'Hello!'; // definiere die Variable und weise ihr einen Wert zu

alert(message); // Hello!
```

Wir können auch mehrere Variablen in einer Zeile deklarieren:

```js no-beautify
let user = 'John', age = 25, message = 'Hello';
```

Das mag kürzer erscheinen, aber wir empfehlen es nicht. Aus Gründen der besseren Lesbarkeit verwende bitte eine einzige Zeile pro Variable.

Die mehrzeilige Variante ist etwas länger, aber leichter lesbar:

```js
let user = 'John';
let age = 25;
let message = 'Hello';
```

<<<<<<< HEAD
Einige Leute definieren auch mehrere Variablen in diesem mehrzeiligen Stil:
=======
Some people also define multiple variables in this multiline style:
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10

```js no-beautify
let user = 'John',
  age = 25,
  message = 'Hello';
```

...oder sogar im "Komma-zuerst"-Stil:

```js no-beautify
let user = 'John'
  , age = 25
  , message = 'Hello';
```

<<<<<<< HEAD
Technisch gesehen machen alle diese Varianten dasselbe. Es ist also eine Frage des persönlichen Geschmacks und der Ästhetik.

````smart header="`var` anstatt `let`"
In älteren Scripts findest du womöglich noch ein anderes Schlüsselwort: `var` anstatt `let`:
=======
Technically, all these variants do the same thing. So, it's a matter of personal taste and aesthetics.

````smart header="`var` instead of `let`"
In older scripts, you may also find another keyword: `var` instead of `let`:
>>>>>>> d35baee32dcce127a69325c274799bb81db1afd8

```js
*!*var*/!* message = 'Hello';
```

<<<<<<< HEAD
Das `var` Schlüsselwort ist *fast* dasselbe wie `let`. Es deklariert auch eine Variable, aber auf eine etwas andere, "altbackene" Weise.

Es gibt subtile Unterschiede zwischen `let` und `var`, aber sie sind für uns noch nicht wichtig. Wir werden sie im Kapitel <info:var> ausführlich behandeln.
=======
The `var` keyword is *almost* the same as `let`. It also declares a variable but in a slightly different, "old-school" way.

There are subtle differences between `let` and `var`, but they do not matter to us yet. We'll cover them in detail in the chapter <info:var>.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d
````

## Eine Analogie aus dem wirklichen Leben

Wir können das Konzept einer "Variablen" leicht verstehen, wenn wir sie uns als eine "Kiste" für Daten vorstellen, mit einem eindeutig benannten Aufkleber darauf.

<<<<<<< HEAD
Zum Beispiel kann man sich die Variable `message` als eine Kiste vorstellen mit der Bezeichnung `"message"` und dem Wert `"Hello!"` darin:
=======
For instance, the variable `message` can be imagined as a box labelled `"message"` with the value `"Hello!"` in it:
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

![](variable.svg)

Wir können jeden Wert in die Kiste legen.

<<<<<<< HEAD
Wir können den Wert auch so oft ändern, wie wir wollen:
=======
We can also change it as many times as we want:

>>>>>>> d694e895efe89922a109702085b6ca1efeffea10
```js run
let message;

message = 'Hello!';

message = 'World!'; // Wert verändert

alert(message);
```

Wenn der Wert geändert wird, werden die alten Daten aus der Variable entfernt:

![](variable-change.svg)

Wir können auch zwei Variablen deklarieren und Daten von der einen in die andere kopieren.

```js run
let hello = 'Hello world!';

let message;

*!*
// kopiere 'Hello world' von hello nach message
message = hello;
*/!*

// jetzt beinhalten zwei Variablen die gleichen Daten
alert(hello); // Hello world!
alert(message); // Hello world!
```

<<<<<<< HEAD
```smart header="Funktionale Sprachen"
Interessant ist, dass es [funktionale](https://de.wikipedia.org/wiki/Funktionale_Programmierung) Programmiersprachen wie [Scala](http://www.scala-lang.org/) oder [Erlang](http://www.erlang.org/) gibt, die das Ändern von Variablenwerten verbieten.
=======
````warn header="Declaring twice triggers an error"
A variable should be declared only once.

A repeated declaration of the same variable is an error:

```js run
let message = "This";

// repeated 'let' leads to an error
let message = "That"; // SyntaxError: 'message' has already been declared
```
So, we should declare a variable once and then refer to it without `let`.
````

```smart header="Functional languages"
<<<<<<< HEAD
It's interesting to note that there exist [functional](https://en.wikipedia.org/wiki/Functional_programming) programming languages, like [Scala](http://www.scala-lang.org/) or [Erlang](http://www.erlang.org/) that forbid changing variable values.
>>>>>>> d35baee32dcce127a69325c274799bb81db1afd8
=======
It's interesting to note that there exist so-called [pure functional](https://en.wikipedia.org/wiki/Purely_functional_programming) programming languages, such as [Haskell](https://en.wikipedia.org/wiki/Haskell), that forbid changing variable values.
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10

In solchen Sprachen ist der Wert, sobald er "in der Kiste" gespeichert ist, für immer da. Wenn wir etwas anderes speichern wollen, zwingt uns die Sprache dazu, eine neue Kiste zu erstellen (eine neue Variable zu deklarieren). Wir können die alte nicht wiederverwenden.

<<<<<<< HEAD
Auch wenn es auf den ersten Blick etwas seltsam erscheint, sind diese Sprachen durchaus für seriöse Softwareentwicklung geeignet. Mehr noch, es gibt Bereiche wie Parallelberechnungen, in denen diese Einschränkung gewisse Vorteile bringt. Das Studium einer solchen Sprache (auch wenn man nicht vorhat, sie bald zu benutzen) wird empfohlen, um den Geist zu erweitern.
=======
Though it may seem a little odd at first sight, these languages are quite capable of serious development. More than that, there are areas like parallel computations where this limitation confers certain benefits.
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10
```

## Benennen der Variablen [#variable-naming]

Es gibt zwei Einschränkungen für Variablennamen in JavaScript:

1. Der Name darf nur Buchstaben, Ziffern oder die Symbole `$` und `_` enthalten.
2. Das erste Zeichen darf keine Ziffer sein.

Beispiele für gültige Namen:

```js
let userName;
let test123;
```

Wenn der Name mehrere Wörter enthält, wird üblicherweise [camelCase](https://en.wikipedia.org/wiki/CamelCase) verwendet. Das heißt: Wörter kommen eins nach dem anderen, jedes Wort, außer dem ersten, mit einem großen Anfangsbuchstaben: `myVeryLongName`.

Was interessant ist - das Dollarzeichen `'$'` und der Unterstrich `'_'` können auch in Namen verwendet werden. Sie sind normale Symbole, genau wie Buchstaben, ohne besondere Bedeutung.

Diese Namen sind gültig:

```js run untrusted
let $ = 1; // deklariert eine Variable mit dem Namen "$"
let _ = 2; // und nun eine Variable mit dem Namen "_"

alert($ + _); // 3
```

Beispiele für falsche Variablennamen:

```js no-beautify
let 1a; // kann nicht mit einer Ziffer beginnen

let my-name; // Bindestriche '-' sind im Namen nicht erlaubt
```

<<<<<<< HEAD
```smart header="Groß- und Kleinschreibung"
Variablen mit den Namen `apple` und `AppLE` sind zwei unterschiedliche Variablen.
```

````smart header="nicht-lateinische Buchstaben sind erlaubt, aber nicht empfohlen"
Es ist möglich, jede Sprache, einschließlich kyrillischer Buchstaben oder sogar chinesische Schriftzeichen, wie diese zu verwenden:
=======
```smart header="Case matters"
Variables named `apple` and `APPLE` are two different variables.
```

````smart header="Non-Latin letters are allowed, but not recommended"
<<<<<<< HEAD
It is possible to use any language, including cyrillic letters, Chinese logograms and so on, like this:
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10
=======
It is possible to use any language, including Cyrillic letters, Chinese logograms and so on, like this:
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

```js
let имя = '...';
let 我 = '...';
```

<<<<<<< HEAD
<<<<<<< HEAD
Technisch gesehen gibt es hier keinen Fehler, solche Namen sind erlaubt, aber es gibt eine internationale Tradition, Englisch in Variablennamen zu verwenden. Selbst wenn wir ein kleines Script schreiben, kann es ein langes Leben vor sich haben. Menschen aus anderen Ländern müssen es vielleicht irgendwann einmal lesen.
=======
Technically, there is no error here. Such names are allowed, but there is an international convention to use English in variable names. Even if we're writing a small script, it may have a long life ahead. People from other countries may need to read it some time.
>>>>>>> d35baee32dcce127a69325c274799bb81db1afd8
=======
Technically, there is no error here. Such names are allowed, but there is an international convention to use English in variable names. Even if we're writing a small script, it may have a long life ahead. People from other countries may need to read it sometime.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d
````

````warn header="Reservierte Namen"
Es gibt eine [Liste mit reservierten Wörtern](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords), die nicht als Variablennamen verwendet werden können, da sie von der Sprache selbst verwendet werden.

Zum Beispiel: `let`, `class`, `return`, und `function` sind reserviert.

Der folgende Code ergibt einen Syntaxfehler:

```js run no-beautify
let let = 5; // kann Variable nicht "let" benennen, Fehler!
let return = 5; // kann sie auch nicht "return" benennen, Fehler!
```
````

````warn header="Eine Zuweisung ohne `use strict`"

Normalerweise müssen wir eine Variable definieren, bevor wir sie verwenden können. Aber in den alten Zeiten war es technisch möglich, eine Variable durch eine einfache Zuweisung des Wertes zu erstellen, ohne `let` zu benutzen. Um die Kompatibilität mit alten Scripts beizubehalten, funktioniert das auch jetzt noch, wenn wir in unseren Scripts nicht `use strict` verwenden.

```js run no-strict
// beachte: kein "use strict" in diesem Beispiel

num = 5; // die Variable "num" wird erstellt, wenn sie nicht existiert

alert(num); // 5
```

Dies ist eine schlechte Vorgehensweise und würde im "strict-mode" einen Fehler verursachen:

```js
"use strict";

*!*
num = 5; // Fehler: "num" ist nicht definiert
*/!*
```
````

## Konstanten

Um eine konstante (unveränderliche) Variable zu deklarieren, verwende `const` anstatt `let`:

```js
const myBirthday = '18.04.1982';
```

Variablen, die mit `const` deklariert werden, nennen wir "Konstante". Sie können nicht neu zugewiesen werden. Ein Versuch, dies zu tun, würde einen Fehler verursachen:

```js run
const myBirthday = '18.04.1982';

myBirthday = '01.01.2001'; // Fehler, Konstante kann nicht neu zugewiesen werden!
```

<<<<<<< HEAD
Wenn ein Programmierer sicher ist, dass eine Variable sich nie ändern wird, kann er sie mit `const` deklarieren, um diese Tatsache zu garantieren und jedem klar zu kommunizieren.

<<<<<<< HEAD
=======
When a programmer is sure that a variable will never change, they can declare it with `const` to guarantee and communicate that fact to everyone.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

### Konstanten in Großbuchstaben
=======
### Uppercase constants
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10

<<<<<<< HEAD
Es ist eine weit verbreitete Vorgehensweise, Konstanten als Alias für schwer zu merkende Werte zu verwenden, die bereits vor der Ausführung bekannt sind.
=======
There is a widespread practice to use constants as aliases for difficult-to-remember values that are known before execution.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

Solche Konstanten werden mit Großbuchstaben und Unterstrichen benannt.

Lass uns zum Beispiel Konstanten für Farben im sogenannten "Web-Format" (hexadezimal) erstellen:

```js run
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...wenn wir uns für eine Farbe entscheiden müssen
let color = COLOR_ORANGE;
alert(color); // #FF7F00
```

Vorteile:

- `COLOR_ORANGE` ist viel leichter zu merken als `"#FF7F00"`.
- Es ist viel leichter, sich bei `"#FF7F00"` zu vertippen als bei `COLOR_ORANGE`.
- Beim Lesen des Codes ist `COLOR_ORANGE` viel aussagekräftiger als `#FF7F00`.

Wann sollten wir Großbuchstaben für eine Konstante verwenden und wann sollten wir sie normal benennen? Lass uns das klarstellen.

<<<<<<< HEAD
Eine "Konstante" zu sein bedeutet nur, dass sich der Wert einer Variablen nie ändert. Aber es gibt Konstanten, die vor der Ausführung bekannt sind (wie ein hexadezimaler Wert für die Farbe rot) und es gibt Konstanten, die zur Laufzeit, also während der Ausführung, *berechnet* werden, sich aber nach ihrer anfänglichen Zuweisung nicht mehr ändern.
=======
Being a "constant" just means that a variable's value never changes. But some constants are known before execution (like a hexadecimal value for red) and some constants are *calculated* in run-time, during the execution, but do not change after their initial assignment.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

<<<<<<< HEAD
Zum Beispiel:
=======
For instance:

>>>>>>> d694e895efe89922a109702085b6ca1efeffea10
```js
const pageLoadTime = /* Zeit, die eine Website braucht, um geladen zu werden */;
```

<<<<<<< HEAD
Der Wert von `pageLoadTime` ist vor dem Laden der Seite nicht bekannt, daher wird er normal benannt. Aber es ist immer noch eine Konstante, weil er sich nach der Zuweisung nicht mehr ändert.
=======
The value of `pageLoadTime` is not known before the page load, so it's named normally. But it's still a constant because it doesn't change after the assignment.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

<<<<<<< HEAD
Mit anderen Worten, großgeschriebene Konstanten werden nur als Aliase für "hart kodierte" Werte verwendet.  
=======
In other words, capital-named constants are only used as aliases for "hard-coded" values.
>>>>>>> d694e895efe89922a109702085b6ca1efeffea10

## Dinge richtig benennen

Apropos Variablen, es gibt noch eine extrem wichtige Sache.

Ein Variablenname sollte eine saubere, offensichtliche Bedeutung haben, die die Daten beschreibt, die er speichert.

<<<<<<< HEAD
Die Benennung von Variablen ist eine der wichtigsten und komplexesten Fähigkeiten in der Programmierung. Ein schneller Blick auf Variablennamen kann zeigen, welcher Code von einem Anfänger im Gegensatz zu einem erfahrenen Entwickler geschrieben wurde.

In einem echten Projekt wird die meiste Zeit damit verbracht, eine bestehende Codebasis zu modifizieren und zu erweitern, anstatt etwas völlig Neues zu schreiben. Wenn wir zu irgendeinem Code zurückkehren, nachdem wir eine Weile etwas anderes gemacht haben, ist es viel einfacher Informationen zu finden, die gut beschriftet sind. Oder, mit anderen Worten, wenn die Variablen gute Namen haben.
=======
Variable naming is one of the most important and complex skills in programming. A glance at variable names can reveal which code was written by a beginner versus an experienced developer.

In a real project, most of the time is spent modifying and extending an existing code base rather than writing something completely separate from scratch. When we return to some code after doing something else for a while, it's much easier to find information that is well-labelled. Or, in other words, when the variables have good names.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

Bitte denk über den richtigen Namen für eine Variable nach, bevor du sie deklarierst. Das wird sich ordentlich auszahlen.

Einige Regeln, die gut zu befolgen sind:

<<<<<<< HEAD
- Verwende menschenlesbare Namen, wie `userName` oder `shoppingCart`.
- Halte dich fern von Abkürzungen oder Kürzel wie `a`, `b`, `c`, es sei denn, du weißt wirklich, was du tust.
- Mach Namen maximal beschreibend und prägnant. Beispiele für schlechte Namen sind `data` und `value`. Solche Namen sagen nichts aus. Es ist nur in Ordnung, sie zu benutzen, wenn der Kontext des Codes es außergewöhnlich offensichtlich macht, auf welche Daten oder Werte die Variable verweist.
- Mach dir mit dir selbst und deinem Team Bedingungen aus. Wenn ein Website Besucher "user" genannt wird, dann sollten verwandte Variablen `currentUser` oder `newUser` heißen, anstatt `currentVisitor` oder `newManInTown`.
=======
- Use human-readable names like `userName` or `shoppingCart`.
- Stay away from abbreviations or short names like `a`, `b`, and `c`, unless you know what you're doing.
- Make names maximally descriptive and concise. Examples of bad names are `data` and `value`. Such names say nothing. It's only okay to use them if the context of the code makes it exceptionally obvious which data or value the variable is referencing.
- Agree on terms within your team and in your mind. If a site visitor is called a "user" then we should name related variables `currentUser` or `newUser` instead of `currentVisitor` or `newManInTown`.
>>>>>>> b258d7d5b635c88228f7556e14fbe5e5ca7f736d

Klingt einfach? Ist es auch, aber die Erstellung von beschreibenden und prägnanten Variablennamen ist es in der Praxis nicht. Nur zu.

```smart header="Wiederverwenden oder Erstellen?"
Und die letzte Anmerkung. Es gibt einige faule Programmierer, die, anstatt neue Variablen zu deklarieren, dazu neigen, bestehende wiederzuverwenden.

Als Ergebnis sind ihre Variablen wie Kisten, in die die Menschen verschiedene Dinge werfen, ohne ihre Aufkleber zu verändern. Was ist jetzt in der Box? Wer weiß das schon? Wir müssen näher kommen und nachsehen.

Solche Programmierer sparen ein wenig an der Variablen-Deklaration, verlieren aber zehnmal mehr beim Debuggen.

Eine zusätzliche Variable ist gut, nicht böse.

Moderne JavaScript-Minifier und Browser optimieren den Code gut genug, so dass es keine Performance-Probleme gibt. Die Verwendung verschiedener Variablen für verschiedene Werte kann sogar der Engine helfen, deinen Code zu optimieren.
```

## Zusammenfassung

Wir können Variablen deklarieren, um Daten zu speichern, indem wir die Schlüsselwörter `var`, `let` oder `const` verwenden.

- `let` -- ist eine moderne Variablendeklaration.
- `var` -- ist eine altbackene Variablendeklaration. Normalerweise benutzen wir es überhaupt nicht, aber wir werden die subtilen Unterschiede von `let` im Kapitel <info:var> behandeln, nur für den Fall, dass du sie brauchst.
- `const` -- ist wie `let`, aber der Wert der Variable kann nicht mehr verändert werden.

Variablen sollten so benannt werden, dass wir leicht verstehen können, was in ihnen enthalten ist.
