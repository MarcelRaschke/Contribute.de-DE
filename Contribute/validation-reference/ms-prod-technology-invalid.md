---
title: ms-prod-and-technology-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236344"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Warnung

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Verwenden Sie `ms.prod` zur Angabe lokaler Produkte. Um detailliertere Informationen zu `ms.prod` anzugeben, können Sie optional `ms.technology` angeben. Die Werte für `ms.prod` und `ms.technology` müssen ein gültiges Paar sein. Entweder ist Ihr `ms.prod`-Wert ungültig, oder Ihr `ms.technology`-Wert bildet mit Ihrem `ms.prod` kein gültiges Paar.

## <a name="resolution"></a>Lösung

Bestätigen Sie, dass Ihr `ms.prod`-Wert für Ihren Artikel richtig ist. Wählen Sie dann einen gültigen `ms.technology`-Wert aus.

Gültige Werte finden Sie auf dieser [Microsoft-internen Website](https://docsmetadatatool.azurewebsites.net/allowlists). [Gehen Sie folgendermaßen vor](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master), um neue Werte anzufordern.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
