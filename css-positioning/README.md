# Positionierung

Die Positionseigenschaft ist nützlich, wenn Sie ein HTML-Element manuell platzieren möchten. Es gibt 5 verschiedene Werte zur Definition der Position:

| Typ                  | Beschreibung                                                                                                                                 |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `position: static`   | Die Position des Elements wird durch den Dokumentenfluss bestimmt (Standardeinstellung).                                                     |
| `position: relative` | Positionieren Sie das Element relativ zu der Stelle, an der es normalerweise platziert würde.                                                |
| `position: absolute` | Positioniere das Element absolut innerhalb des **nächstgelegenen nicht-statischen Vorgängerelements.**                                       |
| `position: fixed`    | Positionieren Sie das Element an einer festen Position auf dem Bildschirm.                                                                   |
| `position: sticky`   | Das Element wird normal im Dokumentenfluss platziert, behält aber einen Versatz relativ zu seinem nächstgelegenen scrollbaren Vorfahren bei. |

Die Position wird dann durch die vier Positionseigenschaften `top`, `bottom`, `right`, festgelegt `left`. Diese funktionieren je nach Positionierungsmethode unterschiedlich.

---

# **`position: static`**

Die Elemente werden gemäß dem normalen Dokumentenfluss positioniert. Die Eigenschaften `top`, `bottom`, haben keine Auswirkung. Dies ist `right`der `left`Standardwert.

---

# **`position: relative`**

Elemente werden gemäß dem normalen Dokumentenfluss positioniert und anschließend mithilfe der Eigenschaften `top``<position>` `bottom`, `<position> `right``, ` <position>` verschoben `left`. Diese Methode dient auch dazu, den Bezugsrahmen für ein absolut positioniertes Kindelement festzulegen. Dadurch wird das Kindelement absolut innerhalb dieses Elements platziert.

# **`position: absolute`**

Elemente werden aus dem normalen Dokumentenfluss entfernt und es wird kein Platz für sie geschaffen – sie hinterlassen also keine Lücke auf der Seite. Mit `position absolute` platzieren Sie ein Element (mit den Eigenschaften `<body> `top``, `bottom``<body> `right``, ` `left`<body>`) relativ zu einem Bezugsrahmen. Der Bezugsrahmen ist der Viewbox des nächstgelegenen übergeordneten Elements, das keine `position absolute`-Eigenschaft besitzt `position: static`(Standardwert).

Im ersten Fall existiert kein nicht-statisches Vorgängerelement, daher wird der Referenzrahmen auf die Seite zurückgegriffen.

Im zweiten Beispiel befindet sich das Element innerhalb eines anderen Elements mit `position: relative`. Daher ist das Element absolut auf dieses Element und nicht auf die gesamte Seite ausgerichtet.

---

# **`position: fixed`**

Elemente werden aus dem normalen Dokumentenfluss entfernt und es wird kein Platz für sie geschaffen – sie hinterlassen also keine Lücke auf der Seite. Ein Element mit der Einstellung „position: fixed“ wird vom Scrollen nicht beeinflusst und bleibt daher an der festgelegten Position. Dies wird häufig für Navigationsleisten oder „Zurück nach oben“-Schaltflächen verwendet.

---

# **`position: sticky`**

Dies ist eine ungewöhnliche, aber sehr raffinierte Positionierungsmethode. Das Element wird erst dann positioniert, wenn es sich dem Rand seines Scrollcontainers (normalerweise der Seite selbst) nähert. Scrollt der Benutzer weiter, wird ein festgelegter Versatz angewendet. Das Element bleibt an diesem Versatz und erscheint wie ein fixiertes Element.

---

# **`z-index`**

Der z-Index bestimmt die Stapelreihenfolge von HTML-Elementen. Elemente mit einem höheren z-Index liegen oben, wenn sie andere Elemente überlappen. Der z-Index kann eine ganze Zahl sein (auch negative Zahlen sind möglich) oder den Standardwert haben, `auto`der die Stapelreihenfolge an die der Elternelemente anpasst. Der z-Index wirkt sich nur auf positionierte Elemente aus – also auf Elemente mit einer nicht-statischen Position.

---

# Links

MDN web docs: position

MDN web docs: Using positioning

MDN web docs: z-index

MDN web docs: Using z-index

MDN web docs: Stacking context

`z-index` and stacking context by Josh W. Comeau
