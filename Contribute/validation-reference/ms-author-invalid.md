---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236541"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Warnung

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Lösung

Überprüfen Sie, ob es sich bei dem Wert `ms.author` um den gültigen Microsoft-Alias des aktuellen Autors handelt. Wenn der Alias eine Verteilerliste ist, muss dieser sich ebenfalls auf der Zulassungsliste befinden.

Gültige Werte für Verteilerlisten finden Sie auf dieser [internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
