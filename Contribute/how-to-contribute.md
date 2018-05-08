---
title: Möglichkeiten zur Mitwirkung an docs.microsoft.com
description: In diesem Artikel erhalten Sie eine Übersicht der verschiedenen Möglichkeiten, wie Sie an docs.microsoft.com mitwirken können.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a>Möglichkeiten zur Mitwirkung an docs.microsoft.com

Es gibt verschiedene Möglichkeiten, sich an der Verbesserung von Inhalten zu beteiligen, aus denen [docs.microsoft.com](https://docs.microsoft.com) besteht:

- Sie können [Probleme erstellen](#create-issues), um neue Artikel zu empfehlen oder vorhandene Artikel zu verbessern.
- Sie können Artikel [schnell bearbeiten](#quick-edits), indem Sie kleine Änderungen im GitHub-Online-Editor vornehmen.
- Sie können [Entwürfe neuer Artikel überprüfen](#review-new-articles), um die Qualität und die technische Korrektheit sicherstellen zu helfen.
- Sie können zu Themen [neue Artikel erstellen](#create-new-articles), wenn Sie die Verbreitung der Inhalte fördern möchten.
- Sie können Beispiele [aktualisieren](#update-samples) oder [erstellen](#create-samples), um die Codebeispiele zu verbessern, die zur unterstützenden Darstellung wichtiger Konzepte dienen.

In diesem Artikel lernen Sie die verschiedenen Möglichkeiten zur Mitwirkung kennen, erfahren, wie die einzelnen Aufgaben ausgeführt werden und finden Verweise zu weiteren Informationen zu diesen Aufgaben.

Unsere öffentlichen Repositorys sind auf [GitHub](https://wwww.GitHub.com) gehostet.  Um sich an unseren Dokumentationsrepositorys zu beteiligen, müssen Sie ein Konto auf GitHub erstellen.

Ferner benötigen Sie einen Texteditor zum Aktualisieren der Dokumente. Wir empfehlen [Visual Studio Code](https://www.visualstudio.com/code). Sie sollten die Grundlagen der [Markdown](https://daringfireball.net/projects/markdown/syntax)-Syntax kennen.

Wenn Sie Beispiele hinzufügen oder ändern möchten, benötigen Sie eine Entwicklungsumgebung. Wir empfehlen [Visual Studio](https://www.visualstudio.com) für PC und Mac bzw. [Visual Studio Code](https://www.visualstudio.com/code) für alle Plattformen.

## <a name="create-issues"></a>Erstellen von Problemen

Wenn Sie Auslassungen oder Ungenauigkeiten in einem Artikel gefunden haben, erstellen Sie ein Problem für diesen Artikel. Die einfachste Möglichkeit zum Auffinden des richtigen Orts besteht darin, in Ihrem Browser auf die Schaltfläche „Bearbeiten“ zu klicken, über die Sie an den Quelltext des Artikels im richtigen öffentlichen GitHub-Repository gelangen. An diesem Ort können Sie die URL für den Quelltext des Artikels in der Adressleiste ersehen. Klicken Sie auf "Problem erstellen", um ein neues Problem für den Artikel zu erstellen.

> [!NOTE]
> Wenn Sie Probleme finden, die sich mit kleinen Bearbeitungen beheben lassen, wie etwa Rechtschreib- oder Grammatikfehler, können Sie sich und uns Zeit sparen, wenn Sie den Browser verwenden, um die Quelle zu bearbeiten und [die Korrektur zu übermitteln](#quick-edits).

Die meisten unserer öffentlichen Repositorys enthalten Vorlagen für neue Probleme, die Sie dazu anleiten, die zum Beheben des Problems benötigten Informationen bereitzustellen.

Ferner können Sie neue Probleme melden, zu denen Ihnen die benötigten Informationen fehlen. Die Vorgehensweise ist die gleiche: Erstellen Sie ein neues Problem in einem der Repositorys für öffentliche Dokumente. Teilen Sie uns mit, wonach Sie gesucht haben, was Sie ausführen wollten und warum die von Ihnen gefundenen Artikel Ihnen nicht in der erwarteten Weise weitergeholfen haben.

## <a name="review-new-articles"></a>Überprüfen neuer Artikel

Wenn Sie mit neuer Software arbeiten, möglicherweise im CTP- oder Betastadium, erstellen wir wahrscheinlich die Dokumentation, während Sie die Technologie kennenlernen. Sie finden die noch in Bearbeitung befindlichen Dokumente in unseren öffentlichen Repositorys. Mit Ihren Kommentaren können Sie uns helfen, die Dokumente vor ihrer Veröffentlichung zu verbessern.

Neue Artikel werden öffentlich mithilfe des [GitHub-Flussprozesses](https://guides.github.com/introduction/flow/) überprüft. Sehen Sie sich eins unserer Dokumentreporitorys an, und überprüfen Sie die offenen Pull Requests (PRs). Wir freuen uns über Kommentare und Rezensionen zu allen offenen Pull Requests. Das hilft uns, bei der Erstveröffentlichung bessere Inhalte herauszubringen, statt auf Feedback nach der Veröffentlichung zu warten.

Wir suchen nach Möglichkeiten, die technische Genauigkeit, die Klarheit der Beschreibungen und die grammatische Exaktheit zu verbessern.

## <a name="quick-edits"></a>Schnelle Bearbeitungen

Schnelle Bearbeitungen sind ein Verfahren zum Vornehmen von kleinen Korrekturen mithilfe des browserbasierten Editors. Wenn Sie kleine Rechtschreib- oder Grammatikfehler oder falsch bezeichnete APIs finden, können Sie das Erstellen eines Problems überspringen, indem Sie die Bearbeitung vornehmen und einen PR einreichen.

Klicken Sie in jedem Artikel auf die Schaltfläche „Edit“ (Bearbeiten; normalerweise in der Nähe der oberen rechten Ecke der Seite), nehmen Sie Ihre Bearbeitungen vor, und klicken Sie unten auf der Seite auf „Submit PR“ (PR einreichen). Wir überprüfen den PR und mergen ihn im Rahmen unserer täglichen PR-Überprüfung.

## <a name="create-new-articles"></a>Erstellen neuer Artikel

Wenn Sie sich für bestimmte Konzepte besonders engagieren und sie anderen näherbringen möchten, können Sie Artikel erstellen und einen PR einreichen.

Das Erstellen neuer Artikel ist zeitaufwändig, und wir schätzen Ihre Zeit und Ihre Beiträge. Wir möchten frühzeitig in den Prozess einbezogen werden, um sicherzustellen, dass Sie sich von Anfang an an unseren Richtlinien und unserem Stil orientieren. Wir empfehlen die folgenden Schritte:

1. [Erstellen Sie ein Problem](#create-issues), das beschreibt, was fehlt und wie Sie das lösen möchten.
1. Kommentieren Sie das Problem, teilen Sie uns mit, dass Sie daran arbeiten möchten, und schlagen Sie eine Gliederung und einen kurzen Abriss für den Artikel vor.
1. Wir antworten mit Vorschlägen. Diese können Links zu verwandten Artikeln, Vorschläge für Beispiele oder Anregungen zur Struktur des Artikels enthalten.
1. Sobald wir uns über die Gliederung geeinigt haben, forken Sie das Repository, und beginnen Sie mit der Arbeit.
1. Öffnen Sie früh im Prozess einen PR, dessen Titel mit „[WIP]“ beginnt.
1. Einer der Kernmitwirkenden gibt Ihnen das erste Feedback.
1. Schreiben Sie weiter, und @-mention Sie die Person, die den ersten Entwurf geprüft hatte, wenn Sie für weiteres Feedback bereit sind.
1. Entfernen Sie das „[WIP]“, wenn Sie für die abschließende Überprüfung bereit sind.
1. Antworten auf das Feedback
1. Die Kernmitwirkenden mergen Ihren PR.

Einige Punkte auf dieser Liste sind es wert, genauer beleuchtet zu werden. Im Allgemeinen folgen wir dem [GitHub-Flussprozess](https://guides.github.com/introduction/flow/), um Inhalte so früh wie möglich zu überprüfen. Auf diese Weise stimmen wir uns darüber ab, an welcher Stelle ein Artikel im Inhaltsverzeichnis aufgeführt werden soll, welchen Nutzen der Leser aus dem neuen Artikel ziehen kann und in welchem Umfang Sie Beispiele für den Artikel erstellen. Wir können alle erforderlichen Kurskorrekturen frühzeitig vornehmen, bevor Sie in nennenswertem Umfang Zeit in das Schreiben investiert haben.

## <a name="update-samples"></a>Aktualisieren von Beispielen

Einige Beispiele wurden möglicherweise schon mehrere Versionen früher erstellt und verwenden z.B. Praktiken, die nicht mehr empfohlen werden. Vielleicht möchten Sie uns helfen, diese Beispiele zu aktualisieren. Oder Ihnen fällt auf, dass sich die Klarheit einer Erläuterung durch das einfache Ändern eines Variablennamens steigern lässt.

Der in den einzelnen Artikeln angezeigte Beispielcode ist Teil von Programmen, die unter unserem CI-System erstellt und oft auch getestet werden.

Um kleine Änderungen vorzunehmen, suchen Sie den Code im entsprechenden Repository, nehmen die Codeänderung im Browser vor, und reichen einen PR ein. Unser CI-System erstellt die Änderungen, und wir mergen den PR nach dem Abschluss.

Für Änderungen in größerem Maßstab forken Sie das Repository und nehmen die Änderungen in Ihrer bevorzugten Entwicklungsumgebung vor. Führen Sie unter allen Umständen Tests durch, um sicherzustellen, dass Ihre Änderungen wie erwartet funktionieren. Reichen Sie einen PR ein, und wir werden ihn überprüfen.

Halten Sie sich bei allen Codeänderungen an die bestehenden Codekonventionen für den Beispielcode, den Sie ändern. Die Standards zur Codeerstellung in unseren Beispielrepositorys spiegeln die Standards der zugehörigen Produktteams wider. Überprüfen Sie jedes Repository auf spezifische Anleitungen.

> [!NOTE]
> Wir bemühen uns unsererseits um eine möglichst genaue Einhaltung dieser Anleitungen. Einige der Beispiele sind älter als unsere aktuellen Standards und wurden noch nicht aktualisiert. Wir arbeiten auf das Ziel hin, dass jeglicher Beispielcode aus funktionierenden, getesteten Beispielen angezeigt wird.

## <a name="create-samples"></a>Erstellen von Beispielen

Sie können auch neue Beispiele erstellen, die Konzepte oder Szenarien veranschaulichen. Alle Beispiele müssen durch einen Artikel begleitet werden, der die Schlüsselinformationen aus dem Beispiel erläutert.

Wenn Ihr neues Beispiel einen vorhandenen Artikel ergänzt, fügen Sie in dem betreffenden Artikel einen Verweis auf das Beispiel ein. Ist das nicht der Fall, arbeiten Sie mit uns zusammen, um [den Artikel zu schreiben](#create-new-articles), der das Beispiel begleitet.

In allen Fällen muss unser Beispielcode den Konventionen zur Codeerstellung folgen, die von den zugehörigen Produktteams verwendet werden. Eine Ausnahme besteht darin, dass wir zugunsten größerer Deutlichkeit mit großer Wahrscheinlichkeit explizit typisierte Variablen anstelle von implizit typisierten (mit `var` deklarierten) Variablen verwenden, wenn der Artikel solche Deklarationen enthält.

Befolgen Sie den Beispielprozess, der im früheren Abschnitt für[neue Artikel](#create-new-articles) umrissen wurde, damit wird den Code frühzeitig im Entwicklungsprozess überprüfen können.
