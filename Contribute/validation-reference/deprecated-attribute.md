---
title: deprecated-attribute
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987788"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Geben Sie mit `ms.service` Clouddienste an. Um detailliertere Informationen zu `ms.service` anzugeben, können Sie optional `ms.subservice` angeben. Verwenden Sie `ms.component` nicht; es ist für diesen Inhalt veraltet.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.service`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.subservice`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
