---
title: Metadatenaktualisierungen – Docs Authoring Pack
description: Hier erfahren Sie, wie Sie Metadaten aus dem Docs Authoring Pack, Visual Studio Code-Erweiterung, aktualisieren.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336633"
---
# <a name="update-metadata"></a>Aktualisieren von Metadaten

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Zusammenfassung

In einer Markdowndatei ( *\*.MD*) gibt es zwei kontextbezogene Menüelemente, die für Metadaten spezifisch sind. Wenn Sie mit der rechten Maustaste auf eine beliebige Stelle im Text-Editor klicken, wird etwas wie die folgenden Menüelemente angezeigt:

:::image type="content" source="media/update-metadata-menu.png" alt-text="Kontextmenü „Metadaten aktualisieren“":::

## <a name="update-msdate-metadata-value"></a>Aktualisieren des Metadatenwerts `ms.date`

Wenn Sie die Option **Metadatenwert `ms.date` aktualisieren** auswählen, wird der aktuelle `ms.date`-Wert für die Markdowndateien auf das heutige Datum festgelegt. Falls das Dokument kein Metadatenfeld `ms.date` enthält, wird keine Aktion ausgeführt.

## <a name="update-implicit-metadata-values"></a>Aktualisieren von impliziten Metadatenwerten

Wenn Sie die Option **Implizite Metadatenwerte aktualisieren** auswählen, werden alle möglichen Metadatenwerte gefunden und ersetzt, die implizit angegeben werden könnten. Metadatenwerte werden implizit in der Datei *docfx.json* unter dem Knoten `build/fileMetadata` angegeben. Jedes Schlüssel-Wert-Paar im Knoten `fileMetadata` stellt Metadatenstandardwerte dar. Beispielsweise könnte eine Markdowndatei im Verzeichnis *top-level/sub-folder*, in dem der Metadatenwert `ms.author` ausgelassen wird, implizit einen Standardwert angeben, der im Knoten `fileMetadata` verwendet werden soll.

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

In diesem Fall würden alle Markdowndateien implizit den Metadatenwert `ms.author: dapine` übernehmen. Das Feature wird auf diese impliziten Einstellungen in der Datei *docfx.json* angewendet. Wenn eine Markdowndatei Metadaten mit Werten enthält, für die explizit etwas anderes als die impliziten Werte festgelegt wird, werden sie überschrieben.

Sehen Sie sich die folgenden Markdowndatei-Metadaten an, bei denen sich diese Markdowndatei in **top-level/sub-folder/includes/example.md** befindet:

```markdown
---
ms.author: someone-else
---

# Content
```

Wenn die Option **Implizite Metadatenwerte aktualisieren** für diese Datei ausgeführt wurde, würde der Metadatenwert bei dem vorstehenden angenommenen *docfx.json*-Inhalt auf `ms.author: dapine` aktualisiert.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Demo zum Aktualisieren von Metadaten](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
