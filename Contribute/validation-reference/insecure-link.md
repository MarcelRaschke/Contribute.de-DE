---
title: insecure-link
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587673"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln. **Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .

## <a name="suggestion"></a>Vorschlag

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Diese Meldung bedeutet, dass Sie entweder einen expliziten Markdownlink mit `http` oder eine Rohdaten-URL wie beispielsweise `www.microsoft.com` verwendet haben. Rohdaten-URLs werden bei der Veröffentlichung in Microsoft-Dokumentation in unsichere Links konvertiert und sollten nicht verwendet werden.

## <a name="resolution"></a>Lösung

Ändern Sie alle URLs auf Microsoft-Websites, um `https` anstelle von `http` zu verwenden.

Wenn Ihr Link eine Rohdaten-URL ist, ändern Sie diesen in einen expliziten Markdownlink, der mit `https` beginnt.

> [!TIP]
> Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links. Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten. So führen Sie das Skript aus:
>
> 1. Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.
> 1. Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.
> 1. Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
