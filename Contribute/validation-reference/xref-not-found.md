---
title: xref-not-found
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – xref-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427518"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>Warnung

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

Die verknüpfte UID ist nicht vorhanden oder nicht für Ihr Repository verfügbar.

## <a name="resolution"></a>Lösung

Überprüfen Sie, ob die UID korrekt ist und ob der XRef-Dienst in Ihrem Repository richtig konfiguriert wurde. Weitere Informationen finden Sie in der internen Microsoft-Dokumentation zum [XRef-Dienst](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
