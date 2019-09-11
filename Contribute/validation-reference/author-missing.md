---
title: author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848580"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Warnung

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
