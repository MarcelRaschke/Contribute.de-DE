---
title: h1-not-first
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895460"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Markdown content is not allowed before H1.`

Nur der YAML-Metadatenheader darf vor der H1-Überschrift in einer Markdowndatei stehen. Wenn Sie einen Hinweis oder ein Bild zum Anfang des Artikels hinzufügen möchten, muss dieses nach der H1-Überschrift stehen. Folgendes ist nicht zulässig:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Gehen Sie stattdessen folgendermaßen vor:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Das Problem wird außerdem häufig durch [Bytereihenfolge-Marken (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) vor dem YAML-Header verursacht. Diese werden manchmal durch Codierungsprobleme ausgelöst, wenn Inhalte an Repositorys committet werden. Dadurch entsteht ein fehlerhaftes Rendering auf GitHub, deshalb sollten diese entfernt werden.

## <a name="resolution"></a>Lösung

Entfernen Sie sämtliche Inhalte außer dem YAML-Metadatenheader vor der H1-Überschrift.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
