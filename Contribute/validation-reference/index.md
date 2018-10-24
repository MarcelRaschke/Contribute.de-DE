---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084528"
---
# <a name="docs-pr-validation-service"></a>Docs PR-Überprüfungsdienst

Der Docs PR-Überprüfungsdienst ist eine GitHub-App, die Gültigkeitsprüfungsregeln für die Dateien in einem PR (Pull Request) ausführt.

Wenn der Überprüfungsdienst für ein Repository aktiviert ist, werden Sie das folgende Verhalten beobachten:

1. Sie senden einen PR.
1. Im GitHub-Kommentar, der den Status Ihres PRs anzeigt, wird der Status der für das Repository aktivierten „Überprüfungen“ angezeigt. Beachten Sie, dass in diesem Beispiel zwei Überprüfungen aktiviert sind, „Commit Validation“ und „OpenPublishing.Build“:

   ![Fehler bei einigen Überprüfungen](media/validation-failed.png)

   Die „Build“-Überprüfung kann erfolgreich sein, selbst wenn die „Commit Validation“-Überprüfung fehlschlägt.

1. Klicken Sie auf **Details**, um weitere Informationen zu erhalten.
1. Auf der Details-Seite werden alle fehlgeschlagenen Gültigkeitsüberprüfungen mit Information zur Problembehandlung angezeigt:

   ![Validierungsmeldung](media/validation-details.png)

Die Liste der derzeit im Dienst verfügbaren Gültigkeiten finden Sie links im Inhaltsverzeichnis dieses Artikels.