---
title: hard-coded-locale
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – hard-coded-locale
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427406"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Warnung

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein. Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt. Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.

Diese Überprüfung soll für die folgenden Websites durchgeführt werden:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>Lösung

Entfernen Sie lokale Codes aus Links zu Microsoft-Websites. Dies ist ein Beispiel:

Vorher:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Nachher:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]