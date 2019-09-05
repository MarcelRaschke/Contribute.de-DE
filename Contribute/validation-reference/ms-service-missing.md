---
title: ms-service-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236501"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>Warnung

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben, aber wenn Sie `ms.subservice` angeben, müssen Sie auch `ms.service` angeben. Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass der `ms.subservice`-Wert, den Sie angegeben haben, für Ihren Artikel richtig ist. Fügen Sie dann den entsprechenden `ms.service`-Wert hinzu, der ein gültiges übergeordnetes Element für `ms.subservice` ist.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists). [Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
