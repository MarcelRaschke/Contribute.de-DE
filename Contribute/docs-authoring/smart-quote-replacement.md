---
title: Automatischer Austausch typografischer Anführungszeichen – Docs Authoring Pack
description: Hier erfahren Sie, wie typografische Anführungszeichen mithilfe des Docs Authoring Packs, Visual Studio Code-Erweiterung, automatisch ausgetauscht werden.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336702"
---
# <a name="smart-quote-replacement"></a>Austausch typografischer Anführungszeichen

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

Inhaltsentwickler sind für die Erstellung einiger der fortschrittlichsten Features moderner Technologie und Intelligenz zuständig, doch unsere Tools bevorzugen heutzutage in Markdown die Verwendung von einfachen (') oder doppelten einfachen Anführungszeichen ("). Das Gegenteil dazu sind die typografischen Anführungszeichen („“). Typografische Anführungszeichen sind in idealen Typografien üblich, werden bei Markdown und gerendertem HTML aber nicht bevorzugt.

Ein Beispiel: Bei Ihrer Arbeit an einem Microsoft Word-Dokument haben Sie vielleicht Folgendes bemerkt: Wenn Sie die <kbd>UMSCHALTTASTE</kbd> gedrückt halten und ein <kbd>"</kbd> eingeben, ersetzt Word das Zeichen `"` schnell durch ein dem typografischen Anführungszeichen entsprechendes Zeichen `“`.

| Beschreibung        | Unicode  | Typografisches Anführungszeichen | Austausch durch |
|--------------------|----------|-------------|-------------|
| Doppeltes linkes Anführungszeichen  | `\u201c` | `“`         | `"`         |
| Doppeltes rechtes Anführungszeichen | `\u201d` | `”`         | `"`         |
| Einfaches linkes Anführungszeichen  | `\u2018` | `‘`         | `'`         |
| Einfaches rechtes Anführungszeichen | `\u2019` | `’`         | `'`         |

Wenn Sie in einer Markdowndatei ( *\*.MD*) Text einfügen oder Inhalte aktualisieren, wertet dieses Feature den Inhalt aktiv aus und tauscht Werte automatisch entsprechend aus.

> [!NOTE]
> Das Feature zum Austausch von typografischen Anführungszeichen tauscht auch andere Zeichen aus, z. B. unter anderem: `©, ™, ®, •`, tiefgestellte und hochgestellte Zeichen. Dies ist hilfreich beim Einfügen von Text aus Word-Dokumenten.

## <a name="preferences"></a>Einstellungen

Dieses Feature ist optional; der Standardwert lautet aber `true`. So schalten Sie dieses Feature ein oder aus:

1. Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.
1. Schalten Sie die Einstellung im Abschnitt **Markdown: Replace Smart Quotes** (Typografische Anführungszeichen austauschen) ein.

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zum Austausch typografischer Anführungszeichen](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
