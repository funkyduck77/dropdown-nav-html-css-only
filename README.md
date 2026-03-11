# dropdown-nav-html-css-only
Dropdown nav only with HTML &amp; CSS 

Ein modernes, responsives und barrierefreies Dropdown-Navigationsmenü, das ohne JavaScript auskommt. 
Genutzt werden die HTML5-Elemente `<details>` und `<summary>` für um die Aufklapp-Logik.

Hier ist ein Dropdown-Navigationsmenü, das komplett ohne JavaScript auskommt. Die Mechanik läuft rein über die nativen html-Tags `<details>` und `<summary>`.

## Was das Menü macht

* Kein JS: Die Aufklapp-Logik übernimmt der Browser selbst.
* Responsive: Auf dem Desktop horizontal, auf dem Handy brechen die Links untereinander um.
* Accessibility: Lässt sich sauber mit der Tab-Taste bedienen. Nutzt `:focus-visible`, damit der Fokus-Rahmen nur bei Tastaturbedienung sichtbar ist und Maus-Nutzer nicht stört.
* Sauberes Layout: Die oft fehlerhafte vertikale Ausrichtung vom summary-Tag ist gefixt (über den Browser-Reset und eine feste line-height von 1.6).

## Wie die Mechanik funktioniert

Anstatt mit JavaScript CSS-Klassen hin und her zu tauschen, nutzen wir das `<details>` Tag. 
Wenn man auf das `<summary>` (den sichtbaren Schalter) klickt, gibt der Browser dem Container nativ das `open`-Attribut. 

Im CSS greifen wir diesen Status einfach über `details[open]` ab, um das visuelle Feedback zu steuern (z.B. um den Pfeil zu drehen).

Das Dropdown-Untermenü liegt auf dem Desktop mit `position: absolute` über dem restlichen Inhalt. Auf mobilen Bildschirmen stellen wir das über eine Media Query auf `position: static` um, damit es wie ein Akkordeon funktioniert und die anderen Links einfach nach unten wegschiebt.

## Einbauen

1. Das html-Gerüst in die eigene Seite kopieren.
2. Wichtig: Im eigenen Browser-Reset im CSS zwingend die Tags `details` und `summary` hinzufügen, sonst setzen die Browser eigene, unsichtbare Abstände (oder meinen Browser-Reset übernehmen).
3. Die Farben und Abstände im CSS an das eigene Layout anpassen.

---
** Gebaut mit ❤️, ☕, Harbio, ![VS Code](https://img.shields.io/badge/-Visual%20Studio%20Code-0078D7?logo=visual-studio-code&logoColor=white), HTML und CSS. **
