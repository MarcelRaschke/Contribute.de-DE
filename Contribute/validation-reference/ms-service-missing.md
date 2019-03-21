---
title: ms-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987719"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben, aber wenn Sie `ms.subservice` angeben, müssen Sie auch `ms.service` angeben. Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass der `ms.subservice`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist. Fügen Sie dann den entsprechenden `ms.service`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.subservice` ist.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
