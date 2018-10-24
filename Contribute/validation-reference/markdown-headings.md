---
title: Markdown-Überschriften
description: Beschreibt Anforderungen für Markdown-Überschriften
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084488"
---
# <a name="markdown-headings"></a>Markdown-Überschriften

Die folgenden Validierungsanforderungen gelten für Überschriften in OPS-Markdown-Dateien.

## <a name="h1"></a>H1

`H1` bezieht sich auf die erste Überschrift in einer Markdown-Datei. Wenn die H1 auf docs.microsoft.com veröffentlicht wurde, wird sie oben auf der Seite in einer großen Schrift angezeigt.

Eine H1 wird erstellt, indem eine Zeile mit einem Rautezeichen (`#`) begonnen wird, gefolgt von einem Leerzeichen und dem Text der Überschrift. Die H1 dieses Artikels sieht beispielsweise wie folgt aus:

```md
# Markdown headings
```

Für H1-Überschriften gelten folgende Regeln:

- Eine H1 muss in der Datei vorhanden sein.
- Eine H1 darf nur einmal vorkommen.
- Die H1 muss Inhalt aufweisen.

  ```markdown
  # 
  This is not allowed.
  ```
- Zwischen dem `#` und dem Inhalt der H1 muss ein Leerzeichen stehen. Eine H1 ohne Leerzeichen rendert auf der veröffentlichten Seite nicht als Überschrift.

  ```markdown
  #This looks bad on the site.
  ```
- Die H1 muss nach dem YML-Metadatenheader der erste Inhalt in der Datei sein. Zwischen dem Ende des YML-Headers und der H1 sind keine Inhalte wie Text oder Bilder zulässig.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- Das HTML-Element für Überschriften der obersten Ebene, `<h1>`, sollte nicht verwendet werden. Verwenden Sie die Markdown-Syntax (`# `).
- Die H1 darf nicht mehr als 100 Zeichen enthalten. Dies ist eine Stilrichtlinie.

## <a name="h2---h6"></a>H2 – H6

H2 (`## `) durch H6 (`###### `) sind in OPS zulässig. Verwenden Sie zum Erstellen von Überschriften die Markdown-Header, nicht die HTML-Header (`<h2>` - `<h6>`).
