---
title: Senden eines Pull Requests
description: In diesem Artikel werden der Pull Request-Prozess und bewährte Methoden beschrieben, um sicherzustellen, dass Ihre Beiträge zusammengeführt werden können.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188226"
---
# <a name="best-practices-for-pull-requests"></a>Bewährte Methoden für Pull Requests (PRs)

Um Inhaltsänderungen zu veröffentlichen, übermitteln Sie einen Pull Request aus Ihrem Fork. Jeder Pull Request muss vor dem Zusammenführen geprüft werden.

## <a name="target-the-correct-branch"></a>Korrekter Branch als Ziel

Alle Änderungen sollten am Branch `staging` erfolgen. Änderungen sollten niemals auf den Branch `live` ausgerichtet sein. Änderungen, die im Branch `staging` vorgenommen wurden, werden in `live` zusammengeführt, sodass alle Änderungen an `live` überschrieben werden.

Wenn Sie eine Änderung an der Dokumentation einreichen, die nur für eine nicht veröffentlichte Version von PowerShell gilt, überprüfen Sie, ob es einen Releasebranch für diese Version gibt. Alle Änderungen, die für eine bestimmte, zukünftige Version gelten, sollten auf den Releasebranch ausgerichtet sein. Releasebranches haben das folgende Namensmuster: `release-<version>`.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>Bessere Bearbeitung der Pull Request-Warteschlange im Interesse aller Beteiligten

Für die PR-Warteschlange gelten zwei grundlegende Wahrheiten:

- Pull Requests mit kleinem Umfang und verwandten Änderungen können schneller geprüft werden.
- Bei Pull Requests mit großem Umfang oder nicht verwandten Änderungen dauert die Prüfung länger.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>Vermeiden von Branchs, die eine große Zahl von Dateien aktualisieren

Trennen Sie geringfügige Updates vorhandener Artikel von neuen Artikeln oder wesentlichen Überarbeitungen. Arbeiten Sie in separaten Arbeitsbranchs an diesen Änderungen.

Umfangreiche Änderungen haben PRs mit einer großen Anzahl von geänderten Dateien zur Folge. Beschränken Sie Ihre PRs auf maximal 50 geänderte Dateien. Große PRs sind schwer zu überprüfen und sind anfälliger für Fehler.

### <a name="renaming-or-deleting-files"></a>Umbenennen oder Löschen von Dateien

Wenn Sie Dateien umbenennen oder löschen, sollten Sie diese Änderungen nicht mit Inhaltsergänzungen oder Updates kombinieren.
Behandeln Sie die Änderungen in einem separaten PR, der nach dem PR für verwandte Updates gemergt wird. Aktualisieren Sie z.B. die Datei der Umleitung, und überprüfen Sie vor dem Löschen eines Artikels, ob die Umleitung ausgeführt wird.

Sie müssen alle Dateien aktualisieren, die mit der umbenannten Datei verknüpft sind. Dies schließt alle Dateien des Inhaltsverzeichnisses ein. Des Weiteren müssen Sie die Umleitungseinträge in der Masterumleitungsdatei (`.openpublishing.redirection.json`) im Stammverzeichnis des Repository hinzufügen.

## <a name="docs-pr-validation-service"></a>Docs PR-Überprüfungsdienst

Der Docs PR-Überprüfungsdienst ist eine GitHub-App, die Gültigkeitsprüfungsregeln für die Dateien in einem PR (Pull Request) ausführt.

Daraufhin wird folgendes Verhalten dargestellt:

1. Sie senden einen PR.
1. Im GitHub-Kommentar, der den Status Ihres PRs anzeigt, wird der Status der für das Repository aktivierten „Überprüfungen“ angezeigt. Beachten Sie, dass in diesem Beispiel zwei Überprüfungen aktiviert sind, „Commit Validation“ und „OpenPublishing.Build“:

   ![Fehler bei einigen Überprüfungen](media/powershell-pull-requests/validation-failed.png)

   Die „Build“-Überprüfung kann erfolgreich sein, selbst wenn die „Commit Validation“-Überprüfung fehlschlägt.

1. Klicken Sie auf **Details**, um weitere Informationen zu erhalten.
1. Auf der Seite „Details“ werden alle fehlgeschlagenen Gültigkeitsüberprüfungen mit Information zur Problembehandlung angezeigt.
1. Wenn die Überprüfung erfolgreich ist, wird dem PR der folgende Kommentar hinzugefügt:

   ![Buildüberprüfung](media/powershell-pull-requests/build-validation.png)

Wenn Sie ein externer (nicht von Microsoft) Mitwirkender sind, haben Sie keinen Zugriff auf die ausführlichen Buildberichte oder Vorschaulinks.

### <a name="build-warnings"></a>Buildwarnungen

Normalerweise sollten Sie alle Buildfehler, Warnungen und Vorschläge beheben. Es gibt jedoch einige Warnungen, die ignoriert werden können.

Die folgenden Warnungen können ignoriert werden:

- > Der Dienstname für `<version>/<modulepath>/About/About.md` kann nicht gefunden werden!

- > Metadaten mit folgenden Namen dürfen nicht im YAML-Header oder als Metadaten auf Dateiebene in „docfx.JSON“ oder als globale Metadaten in „docfx.JSON“ festgelegt werden: `locale`. Diese werden von der Microsoft Dokumentation-Plattform generiert, sodass die Werte, die an diesen drei Stellen festgelegt werden, ignoriert werden. Entfernen Sie diese bitte von allen drei Stellen, um die Warnung zu beheben.
