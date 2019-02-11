---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713175"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte, `ms.service` für Clouddienste. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie `ms.subservice` angeben. Sie können nicht `ms.prod` mit `ms.subservice` oder `ms.service` mit `ms.technology` verwenden.

## <a name="resolution"></a>Lösung

Überprüfen Sie zuerst, ob Sie das richtige übergeordnete Attribut (`ms.prod` oder `ms.service`) für Ihren Artikel ausgewählt haben. Fügen Sie dann das entsprechende untergeordnete Feld mit einem gültigen gepaarten Wert hinzu. Entfernen Sie ggf. zusätzliche Felder.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
