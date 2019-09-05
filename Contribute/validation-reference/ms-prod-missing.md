---
title: ms-prod-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236322"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

## <a name="warning"></a>Warnung

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben, aber wenn Sie `ms.technology` angeben, müssen Sie auch `ms.prod` angeben. Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass der `ms.technology`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist. Fügen Sie dann den entsprechenden `ms.prod`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.technology` ist.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists). [Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
