---
title: validation-timeout
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592545"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Warnung

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

Gelegentlich verhindern vorübergehende Probleme beim Validierungsdienst (z.B. ein fehlerhafter Serverzustand), dass der Dienst bei der Erstellung von Dokumentationsartikeln erfolgreich aufgerufen wird. Nach mehreren Versuchen erfolgt ein Timeout für den Aufruf, und die Validierung wird abgebrochen, um Verzögerungen bei der Erstellung und eine Blockierung der Buildpipeline zu vermeiden.

## <a name="resolution"></a>Lösung

Versuchen Sie, Ihren Pull Request zu schließen und nochmals zu öffnen, oder erzwingen Sie einen vollständigen Build über das [Docs-Portal](https://ops.microsoft.com/#/). Häufig erledigen sich Dienstprobleme nach dem ersten Wiederholungsversuch von selbst.

Beachten Sie, dass Sie ein Repositoryadministrator sein müssen, um einen Build über das Docs-Portal zu erzwingen. Wenn Sie nicht wissen, wer Ihr Repositoryadministrator ist oder Sie die Meldung nach einem erzwungenen Build weiterhin erhalten, erstellen Sie ein Issue über [https://SiteHelp](https://SiteHelp), wenn Sie Microsoft-Mitarbeiter sind, oder erwähnen Sie in Ihrem PR den Autor eines Artikels mithilfe des @-Zeichens, um Unterstützung zu erhalten, wenn Sie ein externer Mitwirkender sind.

Wenn Sie ein Repositoryadministrator sind, können Sie wie folgt einen vollständigen Build erzwingen:

1. Navigieren Sie zum [Docs-Portal](https://ops.microsoft.com/#/), und melden Sie sich an.
1. Sie finden Ihr Repository, indem Sie es in linken oberen Ecke suchen und dann auswählen.

   :::image type="content" source="media/find-repo.png" alt-text="Repositorysuche über das Suchfeld im Docs-Portal":::
1. Klicken Sie auf der Registerkarte **Buildverlauf** auf **+ Manual Publish** (Manuelle Veröffentlichung).
1. Wählen Sie den Branch aus, der die Warnung erhält, z. B. „Master“.
1. Behalten Sie für das Ziel die Standardeinstellung **Docs-Website** bei.
1. Aktivieren Sie das Kontrollkästchen **Veröffentlichung erzwingen**.
1. Klicken Sie auf **Veröffentlichen**.

   :::image type="content" source="media/force-build.png" alt-text="Schritte zum Erzwingen eines vollständigen Builds":::

So wird ein vollständiger Build auf dem Branch erzwungen.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
