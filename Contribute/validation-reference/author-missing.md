---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791504"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Missing attribute: author. Add the current author's GitHub ID.`

Das `author`-Attribut identifiziert den Autor des Artikels durch die GitHub-ID. 

## <a name="resolution"></a>Lösung

Fügen Sie die GitHub-ID des aktuellen Autors dem YML-Header hinzu:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Falls sich der Besitzer geändert hat, muss dies der *aktuelle* Besitzer des Artikels sein und nicht der ursprüngliche Autor.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
