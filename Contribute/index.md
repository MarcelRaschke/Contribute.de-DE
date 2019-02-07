---
title: 'Leitfaden für Mitwirkende an der Microsoft-Dokumentation: Übersicht'
description: In diesem Leitfaden erfahren Sie, wie Sie an der Dokumentationswebsite von Microsoft unter docs.microsoft.com mitwirken können.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 04/17/2018
ms.openlocfilehash: 4a9a7573a62cfc7d5187b90de7e1fe147825273e
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712853"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Leitfaden für Mitwirkende an der Microsoft-Dokumentation: Übersicht

Willkommen beim Leitfaden für Mitwirkende an unserer Dokumentation auf [docs.microsoft.com](https://docs.microsoft.com).

Einige unserer Dokumentationen sind Open Source und werden auf GitHub gehostet. Immer mehr Teams bei Microsoft steigen auf dieses Modell um. Auch Dokumentationen, die nicht vollständig Open Source sind, verfügen über öffentliche Repositorys, in denen Sie gerne Pull Requests erstellen können. Dadurch wird die Kommunikation zwischen Produktingenieuren, den Inhaltsteams und unseren Kunden effizienter gestaltet und allgemein verbessert. Durch diese Art, gemeinsam zu arbeiten, ergeben sich mehrere Vorteile:

- Durch die öffentliche Planung von Open-Source-Repositorys erhalten wir Feedback zu benötigten Dokumentationen.
- Durch die öffentliche Prüfung in Open-Source-Repositorys können wir mit dem ersten Release den bestmöglichen Inhalt veröffentlichen.
- Durch das öffentliche Aktualisieren von Open-Source-Repositorys können wir Inhalt kontinuierlich verbessern.

Die Benutzeroberfläche auf [docs.microsoft.com](https://docs.microsoft.com) bezieht [GitHub](https://github.com)-Workflows direkt ein, um den Prozess noch einfacher zu gestalten. Beginnen Sie mit dem [Bearbeiten des angezeigten Dokuments](#quick-edits-to-existing-documents). Alternativ können Sie [neue Artikel prüfen](#review-open-prs) oder [nützliche Tickets erstellen](#create-quality-issues).

> [!IMPORTANT]
> Für alle Repositorys, die Veröffentlichungen auf „docs.microsoft.com“ durchführen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache). Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys werden durch die [docs.microsoft.com - Nutzungsbestimmungen](https://docs.microsoft.com/legal/termsofuse) abgedeckt. Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind. Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request prüfen oder annehmen können.

## <a name="quick-edits-to-existing-documents"></a>Schnelle Änderungen an vorhandenen Dokumentationen

Schnelle Änderungen optimieren das Melden und Beheben von geringfügigen Fehlern und Auslassungen in Dokumentationen. Trotz aller Bemühungen finden sich immer wieder geringfügige grammatische und orthografische Fehler in unseren Dokumentationen. Sie können Tickets erstellen, um Fehler zu melden – es ist jedoch schneller und einfacher, einen Pull Request (PR) zum Beheben des Fehlers zu erstellen. Fast jeder Artikel verfügt wie in der folgenden Grafik dargestellt über die Schaltfläche „Bearbeiten“. Wenn Sie auf **Bearbeiten** (oder die lokalisierte Entsprechung) klicken, werden Sie zur Quelldatei auf GitHub weitergeleitet.

![Ort des Links „Bearbeiten“](./media/index/edit-article.png)

Klicken Sie dann wie unten dargestellt auf das Stiftsymbol.

![Ort des Bleistiftsymbols](./media/index/edit-icon.png)

> [!NOTE]
> Wenn das Stiftsymbol ausgegraut ist, müssen Sie sich mit Ihrem GitHub-Konto anmelden oder ein neues Konto erstellen.

Nehmen Sie im Web-Editor die Änderungen vor. Sie können auf die Registerkarte **Preview changes** (Vorschau der Änderungen) klicken, um sich das Format Ihrer Änderungen anzusehen.

Wenn Sie alle gewünschten Änderungen vorgenommen haben, scrollen Sie auf der Seite ganz nach unten. Geben Sie einen Titel und eine Beschreibung für Ihren PR ein, und klicken Sie wie unten dargestellt auf **Propose file change** (Dateiänderung vorschlagen):

![Änderungen vorschlagen](./media/index/submit-pull-request.png)

Jetzt haben Sie Ihre Änderungen vorgeschlagen und müssen die Besitzer des Repositorys bitten, Ihre Änderungen in ihr Repository zu „pullen“. Dies erfolgt mit einem sogenannten „Pull Request“. Wenn Sie in der oberen Abbildung auf **Dateiänderung vorschlagen** geklickt haben, müssten Sie zu einer neuen Seite gelangt sein, die folgender Abbildung entspricht:

![Pull Request erstellen](media/index/create-pull-request.png)

Klicken Sie auf **Pull Request erstellen**, geben Sie einen Titel (und optional eine Beschreibung) für den Pull Request ein, und klicken Sie erneut auf **Pull Request erstellen**.

Das ist alles! Das Inhaltsteams sieht sich Ihren PR an und führt ihn ggf. zusammen. Wenn Sie größere Änderungen vorgeschlagen haben, erhalten Sie möglicherweise eine Anfrage zum Vornehmen von Änderungen.

Die GitHub-Benutzeroberfläche zum Bearbeiten spiegelt Ihre Berechtigungen für das Repository wider. Die oben aufgeführten Abbildungen gelten für Mitwirkende, die keine Schreibberechtigungen für das Zielrepository haben. GitHub erstellt automatisch einen Fork des Zielrepositorys in Ihrem Konto. Wenn Sie Schreibberechtigungen für das Zielrepository haben, erstellt GitHub einen neuen Branch im Zielrepository. Der Branchname folgt dem Format **\<GitHubID\>-patch-n** mit Ihrer GitHub-ID und einem numerischen Bezeichner für den Patchbranch.

Wir verwenden PRs für alle Änderungen, auch für Mitwirkende mit Schreibberechtigungen. In den meisten Repositorys ist der `master`-Branch geschützt, damit Änderungen als PRs vorgeschlagen werden.

Das Bearbeiten im Browser eignet sich am besten für geringfügige oder seltene Änderungen. Wenn Sie umfangreichere Änderungen vornehmen oder erweiterte Git-Features verwenden (z.B die Branchverwaltung oder erweiterte Auflösung von Mergekonflikten), müssen Sie [einen Fork für das Repository erstellen und lokal arbeiten](how-to-write-workflows-major.md).

> [!NOTE]
> Falls aktiviert, können Sie einen Artikel in einer **beliebigen Sprache** bearbeiten und, je nach Typ der Bearbeitung, geschieht Folgendes:
> 1. jede genehmigte linguistische Änderung verbessert auch unser Machine Translation-Modul
> 2. jede Bearbeitung, die den Inhalt des Artikels signifikant ändert, wird intern behandelt, um eine Änderung desselben Artikels in Englisch zu übermitteln, sodass sie bei Genehmigung in allen Sprachen lokalisiert wird.
> Die von Ihnen vorgeschlagenen Verbesserungen haben also nicht nur positive Auswirkungen auf Artikel in Ihrer eigenen, sondern in allen verfügbaren Sprachen.

## <a name="review-open-prs"></a>Prüfen offener PRs

Sie können neue Artikel vor der Veröffentlichung lesen, indem Sie sich die aktuell offenen PRs ansehen. Diese Prüfung folgt dem [GitHub-Flow](https://guides.github.com/introduction/flow/). Sie können sich vorgeschlagene Änderungen oder neue Artikel in öffentlichen Repositorys ansehen. Prüfen Sie diese, und fügen Sie eigene Kommentare hinzu. Sehen Sie sich eins unserer Dokumentationsreporitorys an, und überprüfen Sie die offenen Pull Requests (PRs) in für Sie interessanten Bereichen. Vom Feedback der Community zu vorgeschlagenen Änderungen profitiert die gesamte Community.

## <a name="create-quality-issues"></a>Erstellen nützlicher Tickets

Unsere Dokumentationen können fortlaufend geändert und verbessert werden. Mit nützlichen Tickets können wir uns immer auf das konzentrieren, was für die Community am wichtigsten ist. Je ausführlicher die Informationen im Tickets, desto nützlicher ist dieses für uns. Sagen Sie uns, welche Informationen Sie gesucht haben. Nennen Sie uns die Suchbegriffe, die Sie verwendet haben. Wenn Sie nicht beginnen können, sagen Sie uns, wie Sie sich mit neuen Technologien vertraut machen möchten.

Durch Tickets erfahren wir, wo Verbesserungsbedarf besteht. Das Inhaltsteam reagiert dann auf diese Tickets mit Veränderungsvorschlägen und holt Ihre Meinung dazu ein. Nachdem wir einen Entwurf veröffentlicht haben, können Sie [den PR prüfen](#review-open-prs).

## <a name="get-more-involved"></a>Beteiligen Sie sich

In anderen Artikeln erhalten Sie Informationen zum produktiven Mitwirken an der Microsoft-Dokumentation. Dort erfahren Sie, wie Sie mit GitHub-Repositorys, Markdown-Tools und Erweiterungen der Plattform für Microsoft-Dokumentationen arbeiten können.
