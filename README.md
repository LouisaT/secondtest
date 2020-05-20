Eine Lösung für das Problem, das ich bei Nerinas Webseite hatte.
Es geht darum, dass eine unterschiedliche Zahl von Karten in jeweils gleichem Abstand auf der Seite zentriert in einem Block dargestellt werden sollen. Der Block soll sich responsive verhalten, das heißt auf breiten Bildschirmen sollen vier Karten in einer Reihe sichbar sein, auf Mobiles hingegen nur eine. Da die Zahl der Karten unterschiedlich ist, bleibt immer ein Rest in der unteren Reihe.
Die letzte Reihe sollte aber nicht zentriert sein, sondern linksbündig. Sobald man Justify-content: center; verwendet bleiben sie aber zentriert.

Dafür habe ich eine Lösung gesucht, und musste daher das Flex-Box Modell genauer untersuchen, vor allem ob es eine Lösung mittels "align.self:" oder "flex:" eine Lösung gibt.

Ergebnis: so geht es nicht.

Lösung: Man belässt "display: flex" in der Basiseinstelung, muss den Karten einen margin geben, ihrem Container ein padding, muss alles zusammenrechnen, und dann dem Container diesen Breite zuteilen. Mit Mediaqueries setzt man dann Umbruchpunkte in der exakt ausgerechneten Breite die sich ergibt wenn nur mehr drei Karten in einer Reihe sind (samt deren margins und den paddings des Containers) ... dann 2, dann eine.

So sind die Karten bei jeder Viewport-Breite in der Mitte, und die letzte Reihe bleibt linksbündig.
