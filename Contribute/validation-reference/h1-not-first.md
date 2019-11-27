---
title: h1-not-first
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528906"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>Warnung

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
