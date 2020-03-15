---
title: Sortieren von Umleitungen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie Umleitungen mit dem Docs Authoring Pack, Visual Studio Code-Erweiterung, sortieren.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336679"
---
# <a name="sort-redirects"></a>Sortieren von Umleitungen

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

Bei der Entwicklung eines docs.Microsoft.com-Dokumentationssatzes (Docset) werden einige Markdowndateien letztlich gelöscht. Wenn eine Markdowndatei gelöscht wurde, müssen wir eine Umleitung bereitstellen, damit jeder Verweis auf den gelöschten Artikel über die Umleitung ordnungsgemäß aufgelöst wird. Umleitungen werden in der Datei *.openpublishing.redirection.json* angegeben.

1. Öffnen Sie die Befehlspalette, und drücken Sie <kbd>F1</kbd> (oder unter macOS <kbd>⇧⌘P</kbd>).
1. Geben Sie ein: **Docs: Masterumleitungsdatei sortieren**
1. Wählen Sie den Befehl zur Ausführung aus.
1. Beachten Sie Änderungen an der Datei *.openpublishing.redirection.json*.

## <a name="considerations"></a>Überlegungen

Das Konzept von „Daisy Chaining“ besteht darin, wie die Datei *.openpublishing.redirection.json* ursprünglich entworfen wurde. Im Laufe der Zeit veralten letztlich Dateien, die als Umleitung hinzugefügt wurden. Dies geschieht, wenn Datei A gelöscht wird und eine Umleitung zu Datei B erforderlich ist, später Datei B gelöscht wird und dann zu Datei C umgeleitet wird. Im Idealfall würden beide Einträge auf C verweisen, sodass A zu C umgeleitet wird und B unverändert bleibt. Dies ist ein geringfügiger Leistungsgewinn, und das Feature wird derzeit aktiv bearbeitet.

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zum Sortieren von Umleitungen](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
