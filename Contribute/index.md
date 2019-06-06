---
title: 'Leitfaden für Mitwirkende an der Microsoft-Dokumentation: Übersicht'
description: In diesem Leitfaden erfahren Sie, wie Sie an der Dokumentationswebsite von Microsoft unter docs.microsoft.com mitwirken können.
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.openlocfilehash: 9b091f864f5191c9f7a00900ec11a4a1cffdb698
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653503"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Leitfaden für Mitwirkende an der Microsoft-Dokumentation: Übersicht

Willkommen beim Leitfaden für Mitwirkende an unserer Dokumentation auf [docs.microsoft.com](https://docs.microsoft.com).

Einige der Dokumentationssammlungen von Microsoft sind Open-Source und werden auf GitHub gehostet. Nicht alle Dokumentationssammlungen sind vollständig frei verfügbar. Für viele gibt es aber öffentliche Repositorys, in denen Sie über Pull Requests vorgeschlagene Änderungen vornehmen können. Dieser Open Source-Ansatz optimiert und verbessert die Kommunikation zwischen Produkttechnikern, Inhaltsteams und Kunden. Außerdem bietet er weitere Vorteile:

- Durch die _öffentliche Planung_ in Open-Source-Repositorys erhalten wir Feedback zu benötigten Dokumentationen.
- Durch die _öffentliche Prüfung_ in Open-Source-Repositorys können wir mit dem ersten Release den bestmöglichen Inhalt veröffentlichen.
- Durch _öffentliche Updates_ in Open-Source-Repositorys können wir Inhalt kontinuierlich verbessern.

Die Benutzeroberfläche auf [docs.microsoft.com](https://docs.microsoft.com) bezieht [GitHub](https://github.com)-Workflows direkt ein, um den Prozess noch einfacher zu gestalten. Beginnen Sie mit dem [Bearbeiten des angezeigten Dokuments](#quick-edits-to-existing-documents). Alternativ können Sie [neue Artikel prüfen](#review-open-prs) oder [nützliche Tickets erstellen](#create-quality-issues).

> [!IMPORTANT]
> Für alle Repositorys, die Veröffentlichungen auf „docs.microsoft.com“ durchführen, gilt der Verhaltenskodex von [Microsoft Open-Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache). Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Für kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys gelten die [Nutzungsbestimmungen zu docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind. Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request prüfen oder annehmen können.

## <a name="quick-edits-to-existing-documents"></a>Schnelle Änderungen an vorhandenen Dokumenten

Schnelle Änderungen optimieren das Melden und Beheben von geringfügigen Fehlern und Auslassungen in Dokumenten. Trotz aller Bemühungen kommt es zu _geringfügigen_ Grammatik- und Rechtschreibfehlern in unseren Dokumenten. Sie können Tickets erstellen, um Fehler zu melden – es ist jedoch schneller und einfacher, einen Pull Request (PR) zum Beheben des Fehlers zu erstellen, wenn diese Option verfügbar ist.

1. Einige Seiten der Dokumentation ermöglichen es Ihnen, Inhalte direkt im Browser zu bearbeiten. Wenn dies der Fall ist, wird eine Schaltfläche **Bearbeiten** angezeigt, wie unten gezeigt. Wenn Sie auf **Bearbeiten** klicken, werden Sie zur Quelldatei auf GitHub weitergeleitet. Wenn die Schaltfläche **Bearbeiten** (Stiftsymbol ohne Text) fehlt, bedeutet dies, dass die Dokumentationsseite nicht bearbeitet werden kann.

   ![Ort des Links „Bearbeiten“](./media/index/edit-article.png)

2. Klicken Sie anschließend auf das Stiftsymbol, um den Artikel wie gezeigt zu bearbeiten. Wenn das Stiftsymbol abgeblendet ist, müssen Sie sich mit Ihrem GitHub-Konto anmelden oder ein neues Konto erstellen. 

   ![Ort des Bleistiftsymbols](./media/index/edit-icon.png)


3. Nehmen Sie im Web-Editor die Änderungen vor. Klicken Sie auf die Registerkarte **Preview changes** (Vorschau der Änderungen), um sich das Format Ihrer Änderungen anzusehen.

4. Wenn Sie alle gewünschten Änderungen vorgenommen haben, scrollen Sie auf der Seite ganz nach unten. Geben Sie einen Titel und eine Beschreibung für Ihre Änderungen ein, und klicken Sie wie unten dargestellt auf **Propose file change** (Dateiänderung vorschlagen):

   ![Propose file change](./media/index/submit-pull-request.png)

5. Jetzt haben Sie Ihre Änderungen vorgeschlagen und müssen die Besitzer des Repositorys bitten, Ihre Änderungen in ihr Repository zu „pullen“. Dies erfolgt mit einem sogenannten „Pull Request“. Wenn Sie in der oberen Abbildung auf **Propose file change** geklickt haben, müssten Sie zu einer neuen Seite gelangt sein, die folgender Abbildung entspricht:

   ![Pull Request erstellen](media/index/create-pull-request.png)

   Klicken Sie auf **Pull Request erstellen**, geben Sie einen Titel (und optional eine Beschreibung) für den Pull Request ein, und klicken Sie erneut auf **Pull Request erstellen**. (Wenn Sie neu bei GitHub sind, finden Sie unter [About Pull Requests (Über Pull Requests)](https://help.github.com/en/articles/about-pull-requests) wichtige Informationen zum Einstieg.)

6. Das ist alles! Das Inhaltsteam sieht sich Ihren PR an und mergt ihn bei Bedarf. Wenn Sie größere Änderungen vorgeschlagen haben, erhalten Sie möglicherweise eine Anfrage zum Vornehmen von Änderungen.

Die GitHub-Benutzeroberfläche zum Bearbeiten spiegelt Ihre Berechtigungen für das Repository wider. Die oben aufgeführten Abbildungen gelten für Mitwirkende, die keine Schreibberechtigungen für das Zielrepository haben. GitHub erstellt automatisch einen Fork des Zielrepositorys in Ihrem Konto. Wenn Sie Schreibberechtigungen für das Zielrepository haben, erstellt GitHub einen neuen Branch im Zielrepository. Der Branchname folgt dem Format **\<GitHubID\>-patch-n** mit Ihrer GitHub-ID und einem numerischen Bezeichner für den Patchbranch.

Wir verwenden Pull Requests für alle Änderungen, auch für Mitwirkende mit Schreibberechtigungen. In den meisten Repositorys ist der `master`-Branch geschützt, damit Änderungen als Pull Requests vorgeschlagen werden.

Das Bearbeiten im Browser eignet sich am besten für geringfügige oder seltene Änderungen. Wenn Sie umfangreichere Änderungen vornehmen oder erweiterte Git-Features verwenden (z.B die Branchverwaltung oder erweiterte Auflösung von Mergekonflikten), müssen Sie [einen Fork für das Repository erstellen und lokal arbeiten](how-to-write-workflows-major.md).

> [!NOTE]
> Falls aktiviert, können Sie einen Artikel in einer **beliebigen Sprache** bearbeiten und, je nach Typ der Bearbeitung, geschieht Folgendes:
> 1. Jede sprachliche Änderung, die genehmigt wird, dient auch der Verbesserung unserer Maschinenübersetzungs-Engine.
> 2. Jede Bearbeitung, die den Inhalt des Artikels signifikant ändert, wird intern verarbeitet, um eine Änderung desselben Artikels in Englisch zu übermitteln, sodass sie bei Genehmigung in allen Sprachen lokalisiert wird.
> Die von Ihnen vorgeschlagenen Verbesserungen haben also nicht nur positive Auswirkungen auf Artikel in Ihrer eigenen, sondern in allen verfügbaren Sprachen.

## <a name="review-open-prs"></a>Prüfen offener PRs

Sie können neue Artikel vor der Veröffentlichung lesen, indem Sie sich die aktuell offenen PRs ansehen. Diese Prüfung folgt dem [GitHub-Flow](https://guides.github.com/introduction/flow/). Sie können sich vorgeschlagene Änderungen oder neue Artikel in öffentlichen Repositorys ansehen. Prüfen Sie diese, und fügen Sie eigene Kommentare hinzu. Sie können beliebige Dokumentationsrepositorys aufrufen und sich offene Pull Requests für Themenbereiche ansehen, die Sie interessieren. Vom Feedback der Community zu vorgeschlagenen Änderungen profitiert die gesamte Community.

## <a name="create-quality-issues"></a>Erstellen nützlicher Tickets

Unsere Dokumentationen können fortlaufend geändert und verbessert werden. Mit nützlichen Tickets können wir uns immer auf das konzentrieren, was für die Community am wichtigsten ist. Je ausführlicher die Informationen im Tickets, desto nützlicher ist dieses für uns. Sagen Sie uns, welche Informationen Sie gesucht haben. Nennen Sie uns die Suchbegriffe, die Sie verwendet haben. Wenn Ihnen der Einstieg schwerfällt, dann sagen Sie uns einfach, wie Sie sich am liebsten mit neuen Technologien vertraut machen würden.

Viele der Dokumentationsseiten von Microsoft weisen unten auf der Seite einen Abschnitt **Feedback** auf, in dem Sie auf **Produktfeedback** oder **Inhaltsfeedback** klicken können, um Probleme nachzuverfolgen, die spezifisch für diesen Artikel sind.

Durch Tickets erfahren wir, wo Verbesserungsbedarf besteht. Das Inhaltsteam reagiert dann auf diese Tickets mit Veränderungsvorschlägen und holt Ihre Meinung dazu ein. Nachdem wir einen Entwurf veröffentlicht haben, können Sie [den PR prüfen](#review-open-prs).

## <a name="get-more-involved"></a>Beteiligen Sie sich

In anderen Artikeln erhalten Sie Informationen zum produktiven Mitwirken an der Microsoft-Dokumentation. Dort erfahren Sie, wie Sie mit GitHub-Repositorys, Markdown-Tools und Erweiterungen der Plattform für Microsoft-Dokumentationen arbeiten können.
