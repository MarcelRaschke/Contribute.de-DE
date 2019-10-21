---
title: Spezifischer Leitfaden zum Schreiben der Cmdlet-Referenz
description: Dieser Artikel enthält spezifische Regeln zum Formatieren von PowerShell-Codebeispielen. Dies gilt für konzeptionelle Artikel mit Beispielen sowie für die Cmdlet-Referenz.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290286"
---
# <a name="updating-reference-articles"></a>Aktualisieren von Referenzartikeln

Cmdlet-Referenzartikel weisen eine bestimmte Struktur auf. Diese Struktur wird von [PlatyPS][] definiert.
PlatyPS ist das Tool, das zum Generieren von Cmdlet-Hilfe für PowerShell-Module verwendet wird. PlatyPS erstellt die grundlegende Markdowndatei für ein Cmdlet. Nachdem die Markdowndateien bearbeitet wurden, wird PlatyPS zum Erstellen der MAML-Hilfsdateien für das Cmdlet `Get-Help` verwendet.

PlatyPS verfügt über ein hartcodiertes Schema für Cmdlet-Referenzen, das im Code enthalten ist. Im Dokument [platyPS.schema.md][] wird diese Struktur beschrieben. Verstöße gegen das Schema führen zu Buildfehlern, die behoben werden müssen, bevor Ihr Beitrag akzeptiert werden kann.

## <a name="general-guidelines"></a>Allgemeine Richtlinien

- Entfernen Sie keine der Überschriftstrukturen. PlatyPS erwartet spezifische Überschriften.
- Die Header **Input type** (Eingabetyp) und **Output type** (Ausgabetyp) müssen einen Typ aufweisen. Wenn das Cmdlet keine Eingaben akzeptiert oder keinen Wert zurückgibt, verwenden Sie den Wert „None“ (Keiner).
- Umgrenzte Codeblöcke sind nur im Abschnitt [Beispiele](#format-for-examples) zulässig.
- Inlinecodespannen können in allen Absätzen verwendet werden.

## <a name="formatting-about_-files"></a>Formatieren von „About_“-Dateien

`About_*`-Dateien werden nun von [Pandoc][] anstelle von PlatyPS verarbeitet. `About_*`-Dateien werden für die bestmögliche Kompatibilität mit allen Versionen von PowerShell und den Veröffentlichungstools formatiert.
Nehmen Sie keine Änderungen an der Formatierung von `about_*`-Dateien vor, ohne dies mit einem Entwickler des Repositorys zu klären.

Grundlegende Formatierungsrichtlinien:

- Beschränken Sie die Zeilen auf 80 Zeichen.
- Codeblöcke, Blockzitate und Tabellen werden auf 76 Zeichen beschränkt, da Pandoc bei der Konvertierung Einzüge mit vier Leerzeichen für diese einfügt.
- Tabellen müssen in 76 Zeichen passen.
  - Umschließen Sie Inhalte von Zellen in mehreren Zeilen manuell.
  - Verwenden Sie öffnende und schließende `|`-Zeichen in jeder Zeile.
  - Ein funktionierendes Beispiel finden Sie unter [about_Comparison_Operators][about-example].
- Bei der Verwendung der Sonderzeichen `\`, `$`, `` ` `` und `<` von Pandoc:
  - In einer Überschrift: müssen diese Zeichen mit einem voranstehenden `\`-Escapezeichen versehen werden.
  - In einem Absatz: müssen diese Zeichen in Codespannen eingefügt werden. Beispiel:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Formatierung von Beispielen

Im PlatyPS-Schema ist die Überschrift **EXAMPLES** eine H2-Überschrift, und alle Beispiele sind H3-Überschriften.

Das Schema lässt nicht zu, dass Codeblöcke in einem Beispiel durch Absätze getrennt werden. Das folgende Schema ist gültig:

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Geben Sie für alle Beispiele eine Zahl und einen kurzen Titel an.

Beispiel:

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org