---
title: Vervollständigung von Entwicklungssprachen – Docs Authoring Pack
description: Hier erfahren Sie, wie die Vervollständigung von Entwicklungssprachen Mitwirkende im Docs Authoring Pack, Visual Studio Code-Erweiterung, unterstützt.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336794"
---
# <a name="dev-lang-completion"></a>Vervollständigung von Entwicklungssprachen

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

Mitwirkende benötigen Unterstützung bei der Ermittlung der gültigen Sprach-IDs (Entwicklungssprachen), die in einer Markdowndatei auf Dreifach-Graviszeichen (Codefenceöffnungen) folgen können. Leider gibt es keine Überprüfung von Entwicklungssprachen zur Buildzeit. Das Ergebnis deshalb: unterschiedliche Darstellungen einer einzelnen Sprache innerhalb desselben konzeptionellen Dokumentationssatzes (Docset).

Sehen Sie sich C# als Beispiel an. Mitwirkende haben unter anderem `c#`, `C#`, `cs`, `csharp` als Entwicklungssprachendarstellungen der Sprache verwendet. Welche der vorstehenden Darstellungen ist richtig?

Das Feature zur *Vervollständigung von Entwicklungssprachen* beseitigt die Möglichkeit einer Verwechslung durch die Anzeige einer Liste von bekannten Entwicklungssprachen. Nachdem Sie den Namen einer Entwicklungssprache aus IntelliSense ausgewählt haben, geschieht Folgendes:

* Der Codefence wird geschlossen.
* Der Textcursor wird im Codefence positioniert.

## <a name="preferences"></a>Einstellungen

Dieses Feature kann nicht deaktiviert werden. Die folgenden Einstellungen stehen zur Verfügung:

* [Häufig verwendete Entwicklungssprachen anzeigen](#display-commonly-used-dev-langs)
* [Alle bekannten Entwicklungssprachen anzeigen](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>Häufig verwendete Entwicklungssprachen anzeigen

In einem einzelnen Dokumentationssatz (Docset) wird nur eine Teilmenge der gültigen Entwicklungssprachen verwendet. So verbessern Sie die Benutzerleistung:

1. Öffnen Sie in Visual Studio Code den Dokumentationssatz im Stammverzeichnis.
1. Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.
1. Klicken Sie auf den Link **In „settings.json“ bearbeiten**  im Abschnitt **Markdown: Docset-Sprachen**.
1. Fügen Sie die folgende `markdown.docsetLanguages`-Eigenschaft zur Datei *settings.json* hinzu:

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Positionieren Sie den Textcursor im leeren Array der Eigenschaft, und aktivieren Sie IntelliSense (über <kbd>STRG</kbd> + <kbd>LEERTASTE</kbd>). Daraufhin wird eine Liste bekannter Namen von Entwicklungssprachen angezeigt.
1. Fügen Sie so viele Namen zum Array hinzu, bis Ihnen die Liste zusagt. Beispielsweise zeigt die folgende Liste dem Benutzer nach der Eingabe von Dreifach-Graviszeichen vier Namen von Entwicklungssprachen an:

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. Speichern Sie Ihre Änderungen an der Datei *settings.json*.

> [!WARNING]
> Ein leeres `markdown.docsetLanguages`-Array bewirkt, dass alle bekannten Entwicklungssprachen angezeigt werden.

### <a name="display-all-known-dev-langs"></a>Alle bekannten Entwicklungssprachen anzeigen

Standardmäßig werden in IntelliSense alle bekannten Namen von Entwicklungssprachen angezeigt. Diese Einstellung überschreibt die in [Häufig verwendete Entwicklungssprachen](#display-commonly-used-dev-langs) beschriebene Eigenschaft `markdown.docsetLanguages`.

So ändern Sie diese Einstellung:

1. Wählen Sie **Datei** > **Einstellungen** > **Einstellungen** aus, und filtern Sie nach *Docs-Markdownerweiterung*.
1. Schalten Sie die Einstellung im Abschnitt **Markdown: Alle verfügbaren Sprachen** um.

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features:

[![Vervollständigung von Entwicklungssprachen](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
