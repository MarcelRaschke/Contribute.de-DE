---
title: Richtlinien zu Sprache und Stil für .NET-Dokumentationen
description: Erlernen Sie die Richtlinien für Sprache und Stil anhand von Beispielen im Vergleich zu Beispielen, die sich nicht an die Richtlinien halten.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 4108019ac50d703c6dd509eca7a6394cc1c9dc18
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288481"
---
# <a name="voice-and-tone-guidelines"></a>Richtlinien für Sprache und Stil

Eine große Anzahl an Personen, darunter IT-Experten und Entwickler, lesen Ihre Dokumentationen, um .NET zu erlernen und für ihre reguläre Arbeit zu verwenden. Ihr Ziel ist es, eine großartige Dokumentation zu erstellen, die den Lesern hilft. Diese Richtlinien sollen Ihnen dabei helfen. Der Styleguide enthält folgende Empfehlungen:

In diesem Styleguide sind Beispiele zu den einzelnen Empfehlungen enthalten. Dieser Leitfaden wurde gemäß der Richtlinien verfasst, um Ihnen Beispiele zu bieten, an denen Sie sich beim Erstellen einer .NET-Dokumentation orientieren können. Außerdem werden Beispiele gegenübergestellt, damit Sie sehen können, wie Artikel aussehen, die sich nicht an den Richtlinien orientieren.

## <a name="use-a-conversational-tone"></a>Verwenden eines Gesprächstons

### <a name="appropriate-style"></a>Angemessener Stil

Die Dokumentation soll in einem Gesprächston geschrieben werden. Sie sollen sich beim Lesen der Tutorials oder Erklärungen so fühlen, als wären Sie im Gespräch mit dem Autor. Die Dokumentation sollte für Sie informell, dialogorientiert und informativ sein. Als Leser sollten Sie sich fühlen, als würden Sie dem Autor beim Erklären der Konzepte zuhören.

### <a name="inappropriate-style"></a>Unangemessener Stil

Im Kontrast zum Gesprächsstil steht der Stil, der für gewöhnlich bei wissenschaftlichen Behandlungen technischer Themen verwendet wird. Diese Ressourcen sind zwar sehr hilfreich, allerdings schreiben die Autoren solcher Artikel in einem Stil, der sich stark von Microsoft-Dokumentationen unterscheidet. Wenn man eine wissenschaftliche Zeitschrift liest, trifft man auf einen ganz anderen Schreibstil. Man fühlt sich eher, als würde man einen langweiligen Bericht zu einer trockenen Thematik lesen.  

Der erste Paragraph oben hält sich an den empfohlenen Gesprächsstil. Der zweite hält sich eher an einen akademischen Stil. Sie sehen den Unterschied sofort. 

## <a name="write-in-second-person"></a>Schreiben in der zweiten Person

### <a name="appropriate-style"></a>Angemessener Stil

Sie sollten Ihre Artikel schreiben, als würden Sie direkt mit dem Leser reden. Wie in diesen zwei Sätzen sollten Sie die zweite Person häufig verwenden. Das heißt nicht, dass Sie immer das Wort „Sie“ verwenden sollen. Schreiben Sie direkt an den Leser. Schreiben Sie Sätze im Imperativ. Erzählen Sie dem Leser, was er lernen soll.

### <a name="inappropriate-style"></a>Unangemessener Stil

Ein Autor könnte sich auch dazu entscheiden, in dritter Person zu schreiben. In diesem Modell, muss der Autor ein Pronomen oder Nomen finden, mit dem er sich auf den Leser beziehen kann. Leser empfinden diesen Stil meist als weniger ansprechend und weniger unterhaltsam.

Im ersten Paragraph wird der empfohlene Stil verwendet. Im zweiten wird die dritte Person verwendet. Schreiben Sie in der zweiten Person. Sie fanden dies vermutlich viel einfacher zu lesen.

## <a name="use-active-voice"></a>Verwenden von Aktiv

Schreiben Sie Ihre Artikel im Aktiv. Das heißt, das Subjekt des Satzes führt die Aktion (das Verb) im Satz aus. Dies steht im Gegensatz zum Passiv, bei dem der Satz so aufgebaut ist, dass die Aktion sich auf das Subjekt auswirkt. Vergleichen Sie die folgenden zwei Beispiele:

>Der Compiler transformiert den Quellcode in eine ausführbare Datei.

>Der Quellcode wurde vom Compiler in eine ausführbare Datei transformiert.

Im ersten Satz wird das Aktiv verwendet. Der zweite Satz wurde im Passiv geschrieben. (Beide Sätze stellen ein weiteres Beispiel der jeweiligen Stile dar.)

Das Aktiv wird empfohlen, da es einfacher zu lesen ist. Das Passiv kann schwerer zu lesen sein.

## <a name="target-a-fifth-grade-reading-level"></a>Schreiben auf Fünftklässlerniveau

Diese letzte Richtlinie wird verordnet, weil die Muttersprache vieler Leser nicht Englisch ist. Ihre Artikel erreichen eine internationale Zielgruppe. Denken Sie daran, dass sie möglicherweise nicht über das gleiche Vokabular wie Sie verfügen.

Allerdings schreiben Sie für technische Experten. Sie können davon ausgehen, dass Ihre Leser über Programmierkenntnisse und das spezifische Vokabular von Programmierbegriffen verfügen. Die Begriffe objektorientierte Programmierung, Klasse, Objekt, Funktion und Methode sind alle bekannt. Dennoch besitzt nicht jeder Leser einen Abschluss als Diplominformatiker. Begriffe wie „idempotent“ sollten Sie definieren, wenn Sie sie verwenden:

>Die Methode `Close()` ist idempotent, das heißt, wenn Sie sie wiederholt aufrufen, bleibt die Auswirkung unverändert.

## <a name="avoid-future-tense"></a>Vermeiden von Futur

In einigen Sprachen entspricht das Konzept des Zukunftstempus nicht dem Englischen. Die Verwendung des Zukunftstempus kann das Lesen Ihrer Dokumentationen erschweren. Wenn Sie das Futur verwenden, stellt sich außerdem an einem Punkt die Wann-Frage. Wenn Sie schreiben „PowerShell zu lernen, wird sich für Sie lohnen“, stellt der Leser sich natürlich die Frage „Wann wird es sich lohnen?“. Schreiben Sie stattdessen „Es lohnt sich, PowerShell zu lernen“.

## <a name="what-is-it---so-what"></a>Was ist es, und was tut es?

Immer, wenn Sie den Lesern ein neues Konzept vorstellen, definieren Sie zunächst das Konzept, bevor Sie erklären, inwiefern es nützlich ist. Für die Leser ist es wichtig, zu verstehen, was etwas ist, bevor sie die Vorteile (oder andere Aspekte) verstehen können.
