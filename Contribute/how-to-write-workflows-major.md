---
title: GitHub-Beitragsworkflow für größere oder langfristige Änderungen
description: In diesem Artikel erfahren Sie, wie Sie den Beitragsworkflow für größere Änderungen bei der Mitwirkung an docs.microsoft.com-Artikeln verwenden.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: e26b62923eed22d5b2005b1d84dc4ae240d262b1
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469553"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>GitHub-Beitragsworkflow für größere oder langfristige Änderungen

> [!IMPORTANT]
> Für alle Repositorys, die in „docs.microsoft.com“ veröffentlichen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache). Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys werden durch die [docs.microsoft.com - Nutzungsbestimmungen](https://docs.microsoft.com/legal/termsofuse) abgedeckt. Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind. Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request zusammenführen können.

## <a name="overview"></a>Übersicht

Dieser Workflow eignet sich für Mitwirkende, die eine größere Änderung vornehmen müssen oder häufig an einem Repository mitwirken werden. Häufig Mitwirkende befassen sich in der Regel mit laufenden (langfristigen) Änderungen, die vor der Genehmigung des Pull Requests und Zusammenführung der Änderungen mehrere Build-/Validierungs-/Stagingzyklen durchlaufen oder sich über mehrere Tage erstrecken.

Zu den Beispielen für diese Arten von Beiträgen zählen:

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Bevor Sie beginnen, betrachten wir einige der in diesem Workflow verwendeten Git-/GitHub-Begriffe und Moniker. Es macht nichts, wenn Sie sie jetzt noch nicht verstehen. Sie werden sie kennenlernen. Und sollten Sie einmal eine Definition überprüfen wollen, können Sie auf diesen Abschnitt zurückgreifen.

| Name | Beschreibung |
|-----------|-------------|
|Fork|Wird beim Verweis auf eine Kopie des GitHub-Repositorys normalerweise als Substantiv verwendet. Praktisch ist ein Fork einfach ein anderes Repository. Aber das Besondere daran ist, dass GitHub eine Verbindung zurück zum Haupt-/übergeordneten Repository aufrechterhält. Der Begriff wird manchmal als Verb verwendet, wie in „Sie müssen zuerst das Repositorys forken“.|
|Remote|Eine benannte Verbindung mit einem Remoterepository, wie ein „Origin“- oder „Uppstreamremote“. Git bezeichnet diese als „Remotes“, weil sie zum Verweis auf ein Repository verwendet werden, das auf einem anderen Computer gehostet wird. In diesem Workflow ist ein Remote immer ein GitHub-Repository.|
|Origin|Der Name der Verbindung zwischen Ihrem lokalen Repository und dem Repository, von dem es geklont wurde. In diesem Workflow stellt Origin die Verbindung mit Ihrem Fork dar. Er wird manchmal als Moniker für das Ursprungsrepository selbst verwendet, wie in „Denken Sie daran, Ihre Änderungen an Origin zu pushen“.|
|Upstream|Wie Originremote ist Upstream eine benannte Verbindung mit einem anderen Repository. In diesem Workflow stellt Upstream die Verbindung zwischen Ihrem lokalen Repository und dem Hauptrepository dar, aus dem Ihr Fork erstellt wurde. Der Begriff wird manchmal als Moniker für das Upstreamrepository selbst verwendet, wie in „Denken Sie daran, Ihre Änderungen vom Upstream zu pullen.“|

## <a name="workflow"></a>Workflow

>[!IMPORTANT]
> Falls nicht bereits geschehen, müssen Sie die im Bereich [Setup](get-started-setup-github.md) beschriebenen Schritte ausführen. Dieser Abschnitt führt Sie durch die Einrichtung Ihres GitHub-Kontos, wobei Git Bash und ein Markdown-Editor installiert, ein Fork erstellt und Ihr lokales Repository eingerichtet wird. Wenn Sie mit Git- und GitHub-Konzepten wie Repository oder Branch nicht vertraut sind, lesen Sie bitte zuerst [Git and GitHub essentials (Git- und GitHub-Grundlagen)](git-github-fundamentals.md).

In diesem Workflow fließen Änderungen in einen Wiederholungszyklus ein. Vom lokalen Repository Ihres Geräts fließen sie zurück zu Ihrem GitHub-Fork, in das GitHub-Hauptrepository und wieder zum lokalen Repository zurück, während Sie Änderungen anderer Mitwirkender einbeziehen.

### <a name="use-github-flow"></a>Verwenden des GitHub-Flows

In [Git and GitHub essentials (Git- und GitHub-Grundlagen)](git-github-fundamentals.md#git) haben Sie gelernt, dass ein Git-Repository einen Masterbranch sowie einige zusätzliche Branches in Bearbeitung enthält, die nicht in den Masterbranch integriert wurden. Immer dann, wenn Sie mehrere logisch verknüpfte Änderungen vornehmen, sollten Sie einen *Arbeitsbranch* erstellen, um Ihre Änderungen über den Workflow zu verwalten. Wir verwenden hier die Bezeichnung Arbeitsbranch, weil es sich um einen Arbeitsbereich zum Durchlaufen bzw. Optimieren von Änderungen handelt, bis diese wieder in den Masterbranch integriert werden können.

Mit der Isolation zugehöriger Änderungen in einem bestimmten Branch können Sie diese Änderungen unabhängig steuern und einführen und zu einem bestimmten Zeitpunkt im Veröffentlichungszyklus freigeben. Sie könnten abhängig vom Typ Ihrer Arbeit mühelos über mehrere Arbeitsbranches in Ihrem Repository verfügen. Es ist nicht ungewöhnlich, mit mehreren Branches gleichzeitig zu arbeiten, wobei jeder Branch für ein Projekt steht.

>[!TIP]
>Änderungen im Masterbranch vorzunehmen, ist *keine* bewährte Methode. Stellen Sie sich vor, Sie wurden den Masterbranch verwenden, um mehrere Änderungen für die Freigabe von Features zu einem bestimmten Zeitpunkt einzuführen. Sie schließen die Änderungen ab und warten auf ihre Freigabe. Dann erhalten Sie in der Zwischenzeit die dringende Anfrage, ein Problem zu beheben, also nehmen Sie die Änderung in einer Datei im Masterbranch vor und veröffentlichen dann die Änderung. In diesem Beispiel veröffentlichen Sie unabsichtlich die Problembehebung *und* die Änderungen, die Sie zur Freigabe zu einem bestimmten Datum zurückgehalten haben.

Nun erstellen wir einen neuen Arbeitsbranch in Ihrem lokalen Repository, um die von Ihnen vorgeschlagenen Änderungen zu erfassen. Jeder Git-Client ist anders, informieren Sie sich also in der Hilfe über die Anforderungen für Ihren bevorzugten Client. Eine Übersicht über den Prozess finden Sie im GitHub-Leitfaden unter [GitHub-Flow](https://guides.github.com/introduction/flow/) (in englischer Sprache).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Nächste Schritte

Das ist alles! Sie haben einen Beitrag zum Inhalt von docs.microsoft.com geleistet!

- Fahren Sie mit dem Abschnitt zu Schreibgrundlagen fort, um u.a. mehr über Themen wie Markdown und Markdownerweiterungssyntax zu erfahren.
