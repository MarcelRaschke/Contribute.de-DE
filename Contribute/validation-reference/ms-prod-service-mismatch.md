---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636791"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte, `ms.service` für Clouddienste. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie `ms.subservice` angeben. Sie können nicht `ms.prod` mit `ms.subservice` oder `ms.service` mit `ms.technology` verwenden.

## <a name="resolution"></a>Lösung

Überprüfen Sie zuerst, ob Sie das richtige übergeordnete Attribut (`ms.prod` oder `ms.service`) für Ihren Artikel ausgewählt haben. Fügen Sie dann das entsprechende untergeordnete Feld mit einem gültigen gepaarten Wert hinzu. Entfernen Sie ggf. zusätzliche Felder.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
