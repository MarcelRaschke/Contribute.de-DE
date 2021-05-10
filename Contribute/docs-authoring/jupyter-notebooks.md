---
title: 'Abrufen von Inhalt von Jupyter-Notebooks: Docs Authoring Pack'
description: Hier erfahren Sie, wie Sie Inhalt von einem Jupyter-Notebook in Ihr Dokument mithilfe des Docs Authoring Pack, einer Visual Studio Code-Erweiterung, einfügen und aktualisieren.
author: sdgilley
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 01/19/2021
ms.author: sgilley
ms.openlocfilehash: c2b21d260c9e3bd90fbffed9a28afbebd76e2831
ms.sourcegitcommit: f174f438ad2cdb7f2acc5acc73bf5389074c44c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98811969"
---
# <a name="insert-and-update-content-from-a-jupyter-notebook"></a>Einfügen und Aktualisieren von Inhalten aus einem Jupyter-Notebook

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

> [!IMPORTANT]
> Das Einfügen und Aktualisieren aus einer Jupyter Notebook-Funktionalität funktioniert derzeit nicht auf dem Mac.

## <a name="summary"></a>Zusammenfassung

Jupyter Notebook-Instanzen sind eine interaktive Standardmethode zum Erstellen und Freigeben von Code in der Python-Welt.  Das Notebook enthält eine Kombination aus Python-Code, Markdown und optional der Ausgabe aus dem Code.


Die Docs Authoring Pack-Erweiterung enthält Funktionen, mit denen eine statische Markdownversion eines Jupyter-Notebooks in Ihr Dokument eingefügt werden kann:

**Docs: Einfügen des Jupyter-Notebooks:** Geben Sie die URL des Notebooks ein. Eine Markdownversion des Notebooks wird dem Dokument an der Position Ihres Cursors hinzugefügt. Ändern Sie keine Start- oder Endtags. Diese werden von der nächsten Funktion zum Aktualisieren des Notebooks verwendet.

**Docs: Aktualisieren des Jupyter-Notebooks:** Diese Funktion ersetzt den zuvor eingefügten Notebook-Inhalt zwischen dem Start und dem Ende durch die neueste Version. Die URL muss nicht eingegeben werden, sie wird im Starttag aufgezeichnet.  Die Updatefunktion geht davon aus, dass sich ein einzelnes Notebook im Dokument befindet.  Fügen Sie nicht mehrere Notebooks zu einem einzelnen Dokument hinzu.

## <a name="in-action"></a>In Aktion

Nachstehend sehen Sie eine kurze Demo dieses Features.

[![Jupyter-Notebook einfügen](media/insertnotebook.gif)](media/insertnotebook.gif#lightbox)

## <a name="troubleshooting"></a>Problembehandlung

> [!IMPORTANT]
> Das Einfügen und Aktualisieren aus einer Jupyter Notebook-Funktionalität funktioniert derzeit nicht auf dem Mac.

Für diese Funktionen müssen Python, `jupyter`und `nbconvert` auf dem Computer installiert sein.

Um festzustellen, ob Python installiert ist, öffnen Sie ein VS Code-Terminal, und führen Sie Folgendes aus:

* Windows – `where python`
* Linux/Mac: `which python`

Wenn die Rückgabe mindestens einen Pfad enthält, ist Python installiert.  Wenn nicht, dann [installieren Sie Python jetzt](https://www.python.org/downloads/).

Stellen Sie als Nächstes sicher, dass `jupyter` installiert ist:

* Windows – `where jupyter`
* Linux/Mac: `which jupyter`

Wenn kein Pfad zurückgegeben wird, installieren Sie `jupyter`:

```bash
pip install --upgrade jupyter
```

Sobald sowohl Python als auch `jupyter` installiert sind, installieren Sie `nbconvert`:

```bash
pip install --upgrade nbconvert
```
