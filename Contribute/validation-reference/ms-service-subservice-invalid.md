---
title: ms-service-and-subservice-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236511"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

## <a name="warning"></a>Warnung

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben. Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein. Entweder ist Ihr `ms.service`-Wert ungültig, oder Ihr `ms.subservice`-Wert bildet mit Ihrem `ms.service` kein gültiges Paar.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists). [Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
