---
title: ms-prod-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987696"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben, aber wenn Sie `ms.technology` angeben, müssen Sie auch `ms.prod` angeben. Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass der `ms.technology`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist. Fügen Sie dann den entsprechenden `ms.prod`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.technology` ist.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
