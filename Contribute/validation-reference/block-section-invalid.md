---
title: block-section-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – block-section-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 500527c7371dd9d4966460b3eafe0a44874fc4eb
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848526"
---
# <a name="block-section-invalid"></a>block-section-invalid

## <a name="warning"></a>Warnung

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

Mehrere Markdownerweiterungen für die Dokumentation beginnen mit der Zeichenfolge `> [!`. Zwischen `>` und `[` muss ein Leerzeichen stehen, und ein schließendes `]`-Zeichen muss vorhanden sein. Wenn die Syntax falsch ist, wird der Text als Blockzitat gerendert.

## <a name="resolution"></a>Lösung

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Stellen Sie sicher, dass die Syntax für die verwendete Erweiterung korrekt ist:

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
