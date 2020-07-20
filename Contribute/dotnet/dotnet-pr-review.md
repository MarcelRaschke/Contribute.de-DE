---
title: Pull Request-Überprüfungsprozess für .NET-Dokumentationsartikel
description: Für die .NET-Dokumentationsartikel sind die PR-Zusammenführungswebhooks nicht aktiviert. In diesem Artikel wird der PR-Prozess für diese Repositorys beschrieben.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/24/2020
ms.openlocfilehash: 7a494b00c05251e70b74d874d13653db9ba9f6e9
ms.sourcegitcommit: 5f5fc0fc2ff64610cc19a4b40cb3313adbc152cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "86290978"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>Pull Request-Überprüfungsprozess für die Repositorys der .NET-Dokumentationsartikel

Für einige Repositorys, einschließlich .NET-Repositorys, ist kein Webhook für die PR-Zusammenführung („PR Merger“) aktiviert, der automatisch kleinere Pull Requests (PRs) zusammengeführt. In diesem Artikel ist der PR-Überprüfungsprozess für diese Repositorys beschrieben. Der PR-Überprüfungsprozess wurde mit diesen Zielen konzipiert:

- Veröffentlichen hochwertiger Inhalte von unserem Team, den Mitgliedern des Produktteams und den Communitymitgliedern
- Zeitnahe und konsistente Weitergabe von umsetzbarem Feedback an die Autoren
- Erleichtern der Diskussion zwischen Autoren und Reviewern

Während die Teams Innovationen für eine immer ausgereiftere Plattform bereitstellen, entwickeln sich auch die Prozesse weiter.

## <a name="reviewers"></a>Reviewer

Ein Mitglied des Inhaltsteams überprüft jeden PR. Die Mitglieder des Inhaltsteams können von den einzelnen Mitgliedern des Produktteams eine Überprüfung der technischen Richtigkeit verlangen. Das Inhaltsteam verwendet das Code Ownership-Feature von GitHub, um automatisch Überprüfungen von Mitgliedern des Inhaltsteams anzufordern. Als Teil dieses Prozesses kann ein Reviewer andere Teammitglieder für die Überprüfung interner PRs kennzeichnen. Teammitglieder sehen angeforderte Überprüfungen von Team- und Communitymitgliedern in derselben Warteschlange.

Communitymitglieder können PRs überprüfen und auch Feedback geben. Mindestens ein Mitglied des Kernteams für Inhalte muss jedoch jeden PR vor der Zusammenführung genehmigen.

## <a name="review-process"></a>Überprüfungsprozess

Überprüfungen gehen einen von drei Wegen, abhängig vom PR:

- **Kleine PRs**: Kleine PRs sind einzelne Fehlerkorrekturen: Tippfehler, fehlerhafte Links, kleine Codeänderungen oder ähnliche Änderungen.
- **Hauptbeiträge**: Hauptbeiträge sind bedeutende Änderungen an einem bestehenden Artikel, neue Artikel oder Änderungen an einer Reihe von Artikeln.
- **In Bearbeitung**: Autoren können einen PR erstellen, der als noch nicht für die Überprüfung bereit gekennzeichnet ist, indem Sie einen Pull Request-*Entwurf* öffnen.

Die Verarbeitung durch den Contributor License Agreement-Bot (CLA) ist eine gute Richtlinie für die Unterscheidung zwischen „kleinen“ und „großen“ Beiträgen. PRs, die keine Unterzeichnung der CLA erfordern, sind wahrscheinlich „klein“. PRs, die die CLA erfordern, sind wahrscheinlich „groß“.

### <a name="small-prs"></a>Kleine PRs

Die Änderungen in kleinen PRs werden auf ihre Richtigkeit überprüft und mithilfe des Builds auf Reviewerseite überprüft. Da sie klein sind, lösen diese PRs keine Überprüfung des gesamten Artikels aus. 

Reviewer können andere kleine Änderungen anmerken, die einen Artikel verbessern würden. Wenn es sich ebenfalls um kleine Änderungen handelt, schlagen Sie sie als Reviewerkommentare vor. Wenn die vorgeschlagenen Änderungen eine größere Überprüfung erforderlich machen, öffnen Sie ein Problem und gehen später darauf ein. 

### <a name="larger-changes"></a>Größere Änderungen

Größere PRs werden einer gründlicheren Überprüfung unterzogen. Dabei werden alle folgenden Punkte überprüft:

- Der Beispielcode muss im PR, im Quelltext und als herunterladbare ZIP-Datei enthalten sein.
- Der Beispielcode wird ordnungsgemäß kompiliert und ausgeführt.
- Der Artikel beschreibt klar die Ziele für den Leser, und diese Ziele werden erreicht.
- Der Artikel erfüllt die [Stil- und Grammatikrichtlinien](dotnet-style-guide.md) und befolgt unsere [Richtlinien für Sprache und Stil](dotnet-voice-tone.md).
- Alle Links werden korrekt aufgelöst.

Die Mitglieder des Inhaltsteams werden den PR überprüfen und das Ergebnis mit Kommentaren einreichen. Werden nur geringfügige Änderungen gewünscht, können die Teammitglieder den PR mit dem Feedback „genehmigen“. Der Autor kann dann auf das Feedback eingehen und den PR zusammenführen. Nach den meisten Überprüfungen sind Änderungen erforderlich. Sobald diese eingearbeitet wurden, führt der Reviewer erneut eine Überprüfung durch.

Wenn die Änderungen eine technische Überprüfung erfordern, wird der Reviewer des Inhaltsteams eine Überprüfung vom entsprechenden Produktteammitglied anfordern.

### <a name="review-draft-pull-requests"></a>Überprüfen von Pull Request-Entwürfen

Sie wünschen sich vielleicht schon früher ein Feedback. Öffnen Sie einen Pull Request-Entwurf, und fügen Sie einen Kommentar hinzu, der eine frühzeitige Überprüfung anfordert. Solche Vorabüberprüfungen konzentrieren sich auf die Struktur des Artikels: die Gliederung, den Gesamtinhalt und die Beispiele. Diese Überprüfungen beinhalten keine gründliche Prüfung auf Grammatik und korrekte Links.

## <a name="respond-to-reviews"></a>Reagieren auf Überprüfungen

Der Autor aktualisiert den PR, um auf Kommentare zu antworten. Dabei kennzeichnet er jeden abgearbeiteten Kommentar mit „+1“, um zu zeigen, dass er diesen gesehen hat. Wenn der Autor mit dem Kommentar nicht einverstanden ist, oder den Kommentar in einem anderen Pull Request bearbeitet, fügt er einen Kommentar hinzu, in dem er die Änderung erklärt.

Der Autor @-mentions den ursprünglichen Reviewer (d.h., er erwähnt dessen Namen hinter einem @-Zeichen) in einem Kommentar, um eine neue Überprüfung anzufordern. 

## <a name="response-time-expectations"></a>Erwartete Reaktionszeiten

Die Mitglieder des Inhaltsteams überprüfen neue PRs in der Regel in weniger als zwei Werktagen. Sollte die Überprüfung länger dauern, fügt eines der Teammitglieder einen Kommentar hinzu, um den PR zu bestätigen und eine erwartete Bearbeitungsdauer anzugeben.

Sobald eine Überprüfung eingereicht wurde, sollten die Autoren versuchen, auf Kommentare innerhalb einer Woche zu antworten. Freiwillige können diese Erwartungen aufgrund anderer Verpflichtungen möglicherweise nicht erfüllen. In diesen Fällen fragen die Teammitglieder, ob der Communityautor den PR aktualisieren wird. Anderenfalls wird der PR von einem Teammitglied aktualisiert und zusammengeführt.
