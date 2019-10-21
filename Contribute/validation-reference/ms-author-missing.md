---
title: ms-author-missing
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246256"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>Warnung

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>Lösung

Fügen Sie den Microsoft-Alias des aktuellen Autors für `ms.author` hinzu. Falls sich der Besitzer geändert hat, muss dies der *aktuelle* Besitzer des Artikels sein und nicht der ursprüngliche Autor. Es wird empfohlen, dass der festgelegte Autor ein Vollzeitmitarbeiter oder Mitglied einer Teamverteilerliste (DL) und kein vorübergehender Anbieter ist. 

Wenn der Alias eine Verteilerliste (Distribution List, DL) ist, muss dieser sich ebenfalls auf der `ms.author`-Zulassungsliste befinden.

Gültige Werte für `ms.author`-Verteilerlisten finden Sie auf [dieser internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
