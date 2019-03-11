---
title: circular-reference
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459209"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Fehler

`Files '{file name 1}' and '{file name 2}' reference each other.`

Dabei könnte es sich beispielsweise um eine eingeschlossene Datei handeln, die auf die aktuelle Datei oder einen Link zu einer Datei verweist, die auf die aktuelle Datei umgeleitet wird.

## <a name="resolution"></a>Lösung

Überprüfen Sie die Links in den Dateien, und nehmen Sie entsprechende Änderungen vor, damit keine Datei mit sich selbst verknüpft ist oder sich selbst einschließt.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
