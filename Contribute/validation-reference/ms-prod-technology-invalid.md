---
title: ms-prod-and-technology-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987581"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Bald verfügbar!**

## <a name="warning"></a>Warnung

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben. Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein. Entweder ist Ihr `ms.prod`-Wert ungültig, oder Ihr `ms.technology`-Wert bildet mit Ihrem `ms.prod` kein gültiges Paar.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.prod`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.technology`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
