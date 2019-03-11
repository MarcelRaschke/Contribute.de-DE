---
title: snippet-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – snippet-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459094"
---
# <a name="snippet-not-found"></a>snippet-not-found

## <a name="warning"></a>Warnung

`Code snippet '{snippet path}' not found.`

Die Verweise auf Codeausschnitte sind im angegebenen Pfad nicht vorhanden, oder auf den Pfad kann von der aktuellen Datei aus nicht zugegriffen werden.

## <a name="resolution"></a>Lösung

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Stellen Sie sicher, dass der Pfad zu Ihrem Codeausschnitt korrekt ist. Wenn der Codeausschnitt außerhalb des aktuellen Repositorys gespeichert ist, müssen Sie sicherstellen, dass dieses als abhängiges Repository konfiguriert wurde. Weitere Informationen finden Sie im internen Microsoft-Artikel zu [Codeausschnitten](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
