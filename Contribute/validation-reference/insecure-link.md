---
title: insecure-link
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528846"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln. **Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .

## <a name="suggestion"></a>Vorschlag

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Diese Meldung bedeutet, dass Sie entweder einen expliziten Markdownlink mit `http` oder eine Rohdaten-URL wie beispielsweise `www.microsoft.com` verwendet haben. Rohdaten-URLs werden bei der Veröffentlichung in Microsoft-Dokumentation in unsichere Links konvertiert und sollten nicht verwendet werden.

## <a name="resolution"></a>Lösung

Ändern Sie alle URLs auf Microsoft-Websites, um `https` anstelle von `http` zu verwenden.

Wenn Ihr Link eine Rohdaten-URL ist, ändern Sie diesen wie im folgenden Beispiel in einen expliziten Markdownlink, der mit `https` beginnt:

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links. Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten. So führen Sie das Skript aus:
>
> 1. Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.
> 1. Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.
> 1. Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.

In einigen Fällen müssen Sie möglicherweise Webadressen dokumentieren, z. B. vollqualifizierte Domänennamen, die keine klickbaren Links sein sollen. Diese sollten wie im folgenden Beispiel als Inlinecode formatiert werden:

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
