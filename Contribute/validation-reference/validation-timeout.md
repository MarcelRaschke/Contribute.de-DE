---
title: validation-timeout
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817417"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Warnung

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

Gelegentlich verhindern vorübergehende Probleme beim Validierungsdienst (z.B. ein fehlerhafter Serverzustand), dass der Dienst bei der Erstellung von Dokumentationsartikeln erfolgreich aufgerufen wird. Nach mehreren Versuchen erfolgt ein Timeout für den Aufruf, und die Validierung wird abgebrochen, um Verzögerungen bei der Erstellung und eine Blockierung der Buildpipeline zu vermeiden.

## <a name="resolution"></a>Lösung

Schließen Sie den PR, und öffnen Sie ihn noch mal, oder führen Sie einen manuellen Buildvorgang über das Docs-Portal durch (nur für Repositoryadministratoren). Häufig erledigen sich Dienstprobleme nach dem ersten Wiederholungsversuch von selbst. Wenn Sie die Hilfe eines Administrators benötigen oder die Meldung weiterhin erhalten, erstellen Sie ein Issue über [https://SiteHelp](https://SiteHelp), wenn Sie Microsoft-Mitarbeiter sind, oder erwähnen Sie in Ihrem PR den Autor eines Artikels mithilfe des @-Zeichens, um Unterstützung zu erhalten, wenn Sie ein externer Mitwirkender sind.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
