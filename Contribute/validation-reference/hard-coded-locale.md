---
title: hard-coded-locale
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – hard-coded-locale
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166834"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> Diese Regel war anfänglich als „Vorschlag“ aktiviert, um Inhaltsteams Zeit zu geben, die Auswirkung abzuschätzen und einen Plan zum Bereinigen ihrer Repositorys zu entwickeln. **Ab dem 20.12.2019 erfolgt eine Hochstufung zu einer „Warnung“** .

## <a name="suggestion"></a>Vorschlag

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein. Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt. Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.

Diese Überprüfung soll für die folgenden Websites durchgeführt werden:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com (ausgenommen social.msdn.com, wofür das Gebietsschema nötig ist, um sicherzustellen, dass das richtige Forum verknüpft ist)
- technet.microsoft.com

## <a name="resolution"></a>Lösung

Entfernen Sie lokale Codes aus Links zu Microsoft-Websites. Dies ist ein Beispiel:

Vorher:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Nachher:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> Die Markdownerweiterung für die Microsoft-Dokumentation für VS Code enthält ein Bereinigungsskript für Microsoft-Links. Das Skript überprüft alle Links zu Microsoft-Websites in einem Repository, um sicherzustellen, dass sie mit `https` anstelle von `http` beginnen und keine Codes für Gebietsschemas wie `en-us` enthalten. So führen Sie das Skript aus:
>
> 1. Installieren Sie die [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)-Erweiterung für VS Code.
> 1. Klicken Sie auf „ALT + M“, um das Markdownmenü zu öffnen.
> 1. Wählen Sie **Bereinigung** und dann **Microsoft-Links** aus.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
