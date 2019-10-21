---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246307"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Warnung

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Lösung

Ändern Sie den `ms.author`-Wert in den gültigen Microsoft-Alias des aktuellen Autors. Es wird empfohlen, dass der festgelegte Autor ein Vollzeitmitarbeiter oder Mitglied einer Teamverteilerliste (DL) und kein vorübergehender Anbieter ist. Wenn der Alias eine Verteilerliste (Distribution List, DL) ist, muss dieser sich ebenfalls auf der `ms.author`-Zulassungsliste befinden.

Gültige Werte für `ms.author`-Verteilerlisten finden Sie auf [dieser internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
