---
title: ms-service-and-subservice-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713129"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Bald verfügbar!**

## <a name="warning"></a>Warnung

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben. Die Werte für `ms.service` und `ms.subservice` müssen ein gültiges Paar sein. Entweder ist Ihr `ms.service`-Wert ungültig, oder Ihr `ms.subservice`-Wert bildet mit Ihrem `ms.service` kein gültiges Paar.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
