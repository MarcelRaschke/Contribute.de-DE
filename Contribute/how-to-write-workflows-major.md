---
title: GitHub-Beitragsworkflow für größere oder langfristige Änderungen
description: In diesem Artikel erfahren Sie, wie Sie den Beitragsworkflow für größere Änderungen bei der Mitwirkung an docs.microsoft.com-Artikeln verwenden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 997f313e94e4858f37501736c1ec0be2fa8fd552
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188247"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>GitHub-Beitragsworkflow für größere oder langfristige Änderungen

> [!IMPORTANT]
> Für alle Repositorys, die in „docs.microsoft.com“ veröffentlichen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache). Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Für kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys gelten die [Nutzungsbestimmungen zu docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind. Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request zusammenführen können.

## <a name="overview"></a>Übersicht

Dieser Workflow eignet sich für Mitwirkende, die eine größere Änderung vornehmen müssen oder häufig an einem Repository mitwirken werden. Häufig Mitwirkende befassen sich in der Regel mit laufenden (langfristigen) Änderungen, die vor der Genehmigung des Pull Requests und Zusammenführung der Änderungen mehrere Build-/Validierungs-/Stagingzyklen durchlaufen oder sich über mehrere Tage erstrecken.

Zu den Beispielen für diese Arten von Beiträgen zählen:

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Bevor Sie beginnen, betrachten wir einige der in diesem Workflow verwendeten Git-/GitHub-Begriffe und Moniker. Es macht nichts, wenn Sie sie jetzt noch nicht verstehen. Sie werden sie kennenlernen. Und sollten Sie einmal eine Definition überprüfen wollen, können Sie auf diesen Abschnitt zurückgreifen.

| Name | Beschreibung |
|-----------|-------------|
|Fork|Wird beim Verweis auf eine Kopie des GitHub-Repositorys normalerweise als Substantiv verwendet. Praktisch ist ein Fork einfach ein anderes Repository. Aber das Besondere daran ist, dass GitHub eine Verbindung zurück zum Haupt-/übergeordneten Repository aufrechterhält. Der Begriff wird manchmal als Verb verwendet, wie in „Sie müssen zuerst das Repositorys forken“.|
|Remote|Eine benannte Verbindung mit einem Remoterepository, wie ein „Origin“- oder „Uppstreamremote“. Git bezeichnet diese als „Remotes“, weil sie zum Verweis auf ein Repository verwendet wird, das auf einem anderen Computer gehostet wird. In diesem Workflow ist ein Remote immer ein GitHub-Repository.|
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

Nun erstellen wir einen neuen Arbeitsbranch in Ihrem lokalen Repository, um die von Ihnen vorgeschlagenen Änderungen zu erfassen. Wenn Sie Git Bash eingerichtet haben (Informationen finden Sie unter [Installieren von Tools für die Inhaltsentwicklung](get-started-setup-tools.md)), können Sie einen neuen Branch erstellen und diesen mit nur einem Befehl innerhalb Ihres geklonten Repositorys „auschecken“:

````
git checkout -b "branchname"
````

Jeder Git-Client ist anders, informieren Sie sich also in der Hilfe über die Anforderungen für Ihren bevorzugten Client. Eine Übersicht über den Prozess finden Sie im GitHub-Leitfaden unter [GitHub-Flow](https://guides.github.com/introduction/flow/) (in englischer Sprache).

## <a name="making-your-changes"></a>Durchführen von Änderungen

Da Sie nun eine Kopie („Klon“) des Microsoft-Repositorys besitzen und Sie einen Branch erstellt haben, können Sie in einem Text- oder Markdown-Editor beliebige Änderungen durchführen, von denen Sie denken, dass sie für die Community vorteilhaft sein könnten. Weitere Informationen hierzu finden Sie auf der Seite [Installieren von Tools für die Inhaltsentwicklung](get-started-setup-tools.md).  Sie können Ihre Änderungen lokal speichern und müssen sie nicht an Microsoft übermitteln, wenn Sie noch nicht fertig sind.

## <a name="saving-changes-to-your-repository"></a>Speichern von Änderungen in Ihrem Repository

Bevor Sie Ihre Änderungen an den Autor übermitteln, müssen Sie sie zunächst in Ihrem GitHub-Repository speichern.  Da sich alle Tools voneinander unterscheiden, sind nur ein paar einfache Schritte nötig, wenn Sie die Git Bash-Befehlszeile verwenden.

Sie müssen zunächst innerhalb des Repositorys alle Ihre Änderungen _stagen_, sodass diese committet werden.  Dies kann folgendermaßen geschehen:

````
git add --all
````

Als Nächstes müssen Sie Ihre gespeicherten Änderungen in Ihr lokales Repository übernehmen.  Dies kann in Git Bash durchgeführt werden, indem Folgendes ausgeführt wird:

````
git commit -m "Short Description of Changes Made"
````

Nachdem Sie diesen Branch auf Ihrem lokalen Computer erstellt haben, müssen Sie schließlich den Fork in Ihrem GitHub.com-Konto darüber informieren.  Wenn Sie Git Bash verwenden, kann dies folgendermaßen durchgeführt werden:

````
git push --set-upstream origin <branchname>
````

Sie haben es geschafft.  Ihr Code ist jetzt in Ihrem GitHub-Repository verfügbar, und Sie können damit einen Pull Request erstellen.  

>[!TIP]
> Obwohl Ihre Änderungen in Ihrem persönlichen GitHub-Konto sichtbar werden, wenn Sie sie pushen, besagt keine Regel, dass Sie sofort einen Pull Request übermitteln müssen.  Wenn Sie zu einem späteren Zeitpunkt zurückkehren möchten, um zusätzliche Anpassungen vorzunehmen, ist das ebenfalls in Ordnung.

Müssen Sie etwas beheben, das Sie übermittelt haben?  Kein Problem.  Führen Sie Ihre Änderungen einfach im selben Branch durch, und führen Sie noch mal einen Commit und einen Pushvorgang durch (der Upstreamserver muss für nachfolgende Pushvorgänge vom selben Branch nicht festgelegt werden).

Müssen Sie darüber hinaus weitere Änderungen durchführen?  Wechseln Sie zurück zum Masterbranch, und führen Sie einen Checkout auf einen anderen neuen Branch durch. Mit Git Bash ist alles ganz einfach:

````
git checkout master
git checkout -b "branchname"
````

Sie befinden sich nun in einem neuen Branch und sind auf dem besten Weg, ein wichtiger Mitwirkender zu werden.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Nächste Schritte

Das ist alles! Sie haben einen Beitrag zum Inhalt von docs.microsoft.com geleistet!

- Navigieren Sie zum Artikel [Schreibgrundlagen](how-to-write-use-markdown.md), um mehr über Themen wie Markdown und Markdownerweiterungen zu erfahren.
