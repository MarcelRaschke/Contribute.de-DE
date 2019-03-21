---
title: ms-prod-service-mismatch
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987613"
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

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
