---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2018
---
# <a name="using-links-in-documentation"></a>Verwenden von Links in der Dokumentation
In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden. Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden. Benutzer werden über Links auf Inhalte derselben Seite, von benachbarten Seiten oder von externen Websites und URLs verwiesen.

Das Back-End der docs.microsoft.com-Website verwendet Open Publishing Services (OPS), worin DocFX Flavored Markdown (DFM) implementiert ist. DFM weist eine hohe Kompatibilität mit GitHub Flavored Markdown (GFM) auf und verfügt durch Markdownerweiterungen über zusätzliche Funktionen.

> [!IMPORTANT]
> Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).

## <a name="link-text"></a>Linktext

Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein. Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.

> [!IMPORTANT]
> Verwenden Sie nicht die Formulierung „Hier klicken“. Diese ist im Hinblick auf die SEO suboptimal und beschreibt das Linkziel nicht ausreichend.

**Richtig:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Falsch:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Links in einem Artikel zum anderen Artikel

Verwenden Sie zum Erstellen eines Inlinelinks in einem technischen Dokumentationsartikel zu einem anderen technischen Dokumentationsartikel innerhalb desselben Dokumentationssatzes die folgende Linksyntax:

- Einem Artikel in einem Verzeichnis wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:

  `[link text](article-name.md)`

- Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel im Stammverzeichnis hinzugefügt:

  `[link text](../article-name.md)`

- Einem Artikel im Stammverzeichnis wird ein Link in einem Artikel in einem Unterverzeichnis hinzugefügt:

  `[link text](./directory/article-name.md)`

- Einem Artikel in einem Unterverzeichnis wird ein Link zu einem Artikel in einem anderen Unterverzeichnis hinzugefügt:

  `[link text](../directory/article-name.md)`

- Einem Artikel wird ein Link zwischen verschiedenen Dokumentationssätzen hinzugefügt (auch wenn sie zum selben Repository gehören): `[link text](./directory/article-name)`
  
## <a name="links-to-anchors"></a>Links zu Verankerungen

Sie müssen keine Anker erstellen. Sie werden automatisch bei der Veröffentlichung aller H2-Überschriften generiert. Sie müssen lediglich Links zu den H2-Abschnitten erstellen.

- So erstellen Sie einen Link zu einer Überschrift im selben Artikel

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- So erstellen Sie einen Link zu einer Verankerung in einem anderen Artikel desselben Unterverzeichnisses

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- So erstellen Sie einen Link zu einer Verankerung in einem anderen Dienstunterverzeichnis

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Links von Includes

Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden. Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Links in Selektoren

Wenn Sie in einer include-Datei eingebettete Selektoren verwenden, wie es beim Azure-Dokumentationsteam der Fall ist, verwenden Sie folgende Linkstruktur:

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Text1 | Example1 )](../articles/folder/article-name1.md)
    - [(Text1 | Example2 )](../articles/folder/article-name2.md)
    - [(Text2 | Example3 )](../articles/folder/article-name3.md)
    - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Verweislinks

Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden. Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können. Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:

Inlinetext:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Linkverweise am Ende des Artikels:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen. Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Link zu Seiten außerhalb der technischen Dokumentation

Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen. Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Links zu Websites von Drittanbietern

Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden. Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:

- **Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen. Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google. Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.
- **Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden. Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.
- **Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.
- **Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden. Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu. Zum Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“
- **Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen. Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.
- **Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder „ms.com“-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.

## <a name="links-to-msdn-or-technet"></a>Links zu MSDN oder TechNet

Wenn Sie Links zu Websites von MSDN oder TechNet hinzufügen müssen, verwenden Sie den vollständigen Link zum Thema, und entfernen Sie das Sprachgebietsschema „en-us“ im Link.

## <a name="links-to-azure-powershell-reference-content"></a>Link zu weiterführenden Azure PowerShell-Inhalten

Seit November 2016 wurden verschiedene Änderungen an weiterführenden Azure PowerShell-Inhalten vorgenommen. Beachten Sie beim Erstellen von Links zu diesen Inhalten aus anderen Artikeln auf der Website „docs.microsoft.com“ die folgenden Richtlinien.

Struktur der URL:

* Für Cmdlets:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Für konzeptionelle Themen:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

Der Teil &lt;moniker-name&gt; ist optional. Wenn dieser ausgelassen wird, werden Sie zur aktuellen Version des Inhalts weitergeleitet. Der Teil &lt;service-name&gt; ist eines der Beispiele, das in den folgenden Basis-URLs gezeigt wird:

- Inhalt von Azure PowerShell (AzureRM): https://docs.microsoft.com/powershell/azure/
- Inhalt von Azure PowerShell (ASM): https://docs.microsoft.com/powershell/azure/ _servicemanagement_
- Inhalt von Azure Active Directory-PowerShell (Azure AD): https://docs.microsoft.com/powershell/azure/ _active-directory_
- Azure Service Fabric-PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_
- Azure Information Protection-PowerShell: https://docs.microsoft.com/powershell/azure/_aip_
- Azure PowerShell für Aufträge für die elastische Datenbank: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_

Wenn Sie diese URLs verwenden, werden Sie zur aktuellen Version des Inhalts umgeleitet. Auf diese Weise müssen Sie keinen Versionsmoniker angeben. Sie müssen bei Versionsänderungen auch keine Links zu konzeptionellen Inhalten aktualisieren.

Um den richtigen Link zu erstellen, suchen Sie nach der Seite, für die Sie einen Link in Ihren Browser einfügen möchten, und kopieren Sie die URL.
Entfernen Sie dann „https://docs.microsoft.com“ und die Gebietsschemainformationen.

Wenn Sie einen Link aus einem Inhaltsverzeichnis hinzufügen, müssen Sie die vollständige URL ohne Gebietsschemaangabe verwenden.

Beispiel für Markdown:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
