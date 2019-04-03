---
title: deprecated-attribute
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636883"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben. Verwenden Sie `ms.component` nicht; es ist für diesen Inhalt veraltet.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
