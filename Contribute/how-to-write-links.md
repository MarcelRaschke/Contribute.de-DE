---
title: Verwenden von Links in der Dokumentation
description: Dieser Artikel enthält Anleitungen zum Erstellen von Links, die auf Inhalte von docs.microsoft.com verweisen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: 94ba4cefd9aff70b38502aa397a3761127c8089f
ms.sourcegitcommit: 9852045bac75fd5d90c0ffc88d2a17dd45ba015f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2020
ms.locfileid: "85107111"
---
# <a name="use-links-in-documentation"></a>Verwenden von Links in der Dokumentation

In diesem Artikel erfahren Sie, wie Sie Links von Seiten verwenden, die auf docs.microsoft.com gehostet werden. Links können mit wenigen unterschiedlichen Konventionen auf einfache Weise in Markdown eingefügt werden. Benutzer werden über Links auf Inhalte derselben Seite, auf benachbarten Seiten oder auf externen Websites und URLs verwiesen.

Das Back-End der Website „docs.microsoft.com“ nutzt Open Publishing Services (OPS). Dadurch wird [CommonMark][]-konformes Markdown unterstützt, das durch die [Markdig][]-Engine analysiert wird. Diese Markdownvariante ist meistens mit [GitHub Flavored Markdown (GFM)][GFM] kompatibel, da die meisten Dokumentationen auf GitHub gespeichert und auch dort bearbeitet werden können. Weitere Funktionalität wird über Markdown-Erweiterungen hinzugefügt.

> [!IMPORTANT]
> Alle Links müssen sicher sein (`https` statt `http`), sofern das Ziel dies unterstützt (dies sollte meistens der Fall sein).

## <a name="link-text"></a>Linktext

Die im Linktext verwendeten Begriffe sollten benutzerfreundlich sein. Das bedeutet, es sollten geläufige Begriffe oder der Titel einer Seite sein, auf die Sie verweisen.

> [!IMPORTANT]
> Verwenden Sie nicht die Formulierung „Hier klicken“. Diese ist im Hinblick auf die Suchmaschinenoptimierung suboptimal und beschreibt das Linkziel nicht ausreichend.

**Richtig:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**Falsch:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Links in einem Artikel zum anderen Artikel

Das Veröffentlichungssystem unterstützt zwei Arten von Hyperlinks: **URLs** und **Dateilinks**.

Bei einem URL-Link kann es sich um einen URL-Pfad handeln, der relativ zum Stammverzeichnis von docs.microsoft.com ist, oder um eine absolute URL, die die vollständige URL-Syntax enthält (z. B. `https://github.com/MicrosoftDocs/PowerShell-Docs`).

- Verwenden Sie URL-Links, wenn Sie Inhalt außerhalb des aktuellen _Docsets_ oder zwischen automatisch generierten Referenz- und Konzeptartikeln innerhalb des Docsets verlinken.
- Die einfachste Möglichkeit zum Erstellen eines relativen Links besteht darin, die URL aus Ihrem Browser zu kopieren und dann `https://docs.microsoft.com/en-us` aus dem Wert zu entfernen, den Sie in den Markdowncode einfügen.
   - URLs für Microsoft-Eigenschaften sollten keine Gebietsschemas enthalten. Entfernen Sie also beispielsweise „/de-de“ aus der URL.

Ein Dateilink wird verwendet, um einen Artikel mit einem anderen innerhalb des Docsets zu verlinken.

- Für alle Dateipfade müssen Schrägstriche (`/`) anstelle von umgekehrten Schrägstrichen verwendet werden.
- Einem Artikel wird ein Link zu einem anderen Artikel im selben Verzeichnis hinzugefügt:

  `[link text](article-name.md)`

- Ein Artikel verweist auf einen Artikel im übergeordneten Verzeichnis des aktuellen Verzeichnisses:

  `[link text](../article-name.md)`

- Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des aktuellen Verzeichnisses:

  `[link text](directory/article-name.md)`

- Ein Artikel verweist auf einen Artikel in einem Unterverzeichnis des übergeordneten Verzeichnisses des aktuellen Verzeichnisses:

  `[link text](../directory/article-name.md)`

> [!NOTE]
> In keinem der oben stehenden Beispiele wird `~/` als Teil des Links verwendet. Wenn Sie auf einen absoluten Pfad verweisen möchten, der im Stammverzeichnis des Repositorys beginnt, beginnen Sie den Link mit `/`. Wenn Sie ein `~/` einfügen, wird dadurch beim Navigieren in den Quellrepositorys auf GitHub ein ungültiger Link erstellt. Wenn der Pfad mit `/` beginnt, kann der Link ordnungsgemäß aufgelöst werden.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>Linkstruktur auf docs.microsoft.com

Auf docs.microsoft.com veröffentlichte Inhalte weisen folgende URL-Struktur auf:

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

Beispiele:

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>`: gibt die Sprache des Artikels an (Beispiel: de-de oder en-us)
- `<product-service>`: gibt den Namen des Produkts oder Diensts an (Beispiel: powershell, dotnet oder azure)
- `[<feature-service>]` (optional): gibt den Featurenamen oder Subdienst des Produkts an (Beispiel: csharp oder load-balancer)
- `[<subfolder>]` (optional): der Name eines Unterordners innerhalb eines Features
- `<topic>`: der Name der Artikeldatei für das Thema (Beispiel: load-balancer-overview oder overview)
- `[?view=\<view-name>]` (optional): der Ansichtsname, der von der Versionsauswahl für Inhalt mit mehreren verfügbaren Versionen verwendet wird (Beispiel: azps-3.5.0)

> [!TIP]
> Artikel im selben _Docset_ besitzen meistens das gleiche `<product-service>`-URL-Fragment. Beispiel:
> - Gleiches Docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - Anderes Docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>Lesezeichenlinks

Verwenden Sie ein Hashsymbol gefolgt von der Überschrift in Kleinbuchstaben, um einen Lesezeichenlink zu einer Überschrift in der *aktuellen* Datei zu erstellen. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche:

```markdown
[Managed Disks](#managed-disks)
```

Wenn Sie eine Lesezeichenüberschrift in einem anderen Artikel verlinken möchten, verwenden Sie einen datei- oder websitebezogenen Link und ein Hashsymbol gefolgt von der Überschrift. Entfernen Sie Satzzeichen aus der Überschrift, und ersetzen Sie Leerzeichen durch Bindestriche:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Sie können auch den Lesezeichenlink aus der URL kopieren. Zeigen Sie mit der Maus auf die Kopfzeile von docs.microsoft.com, um zur URL zu gelangen. Das Linksymbol sollte angezeigt werden:

![Linksymbol in Artikelüberschrift](media/how-to-write-links/bookmark-link.png)

Klicken Sie auf das Linksymbol, und kopieren Sie dann den Ankertext des Lesezeichens aus der URL (d. h. den Teil nach dem Hash).

> [!NOTE]
> Die Docs-Erweiterung bietet auch Tools zum Erstellen von Links.

### <a name="explicit-anchor-links"></a>Explizite Ankerlinks

Es ist nicht erforderlich und wird nicht empfohlen, explizite Ankerlinks mit dem HTML-Tag `<a>` hinzufügen (Ausnahmen: im Hub und auf der Landing Page). Verwenden Sie stattdessen wie unter [Lesezeichenlinks](#bookmark-links) beschrieben die automatisch generierten Lesezeichen. Deklarieren Sie folgendermaßen Anker für den Hub und die Landing Page:

```markdown
## <a id="anchortext" />Header text
```

oder

```markdown
## <a name="anchortext" />Header text
```

So können Sie einen Link zum Anker erstellen:

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> Ankertext muss immer aus Kleinbuchstaben bestehen und darf keine Leerzeichen enthalten.

## <a name="xref-cross-reference-links"></a>XRef-Links (Querverweise)

Es wird empfohlen, XRef-Links zum Verlinken mit APIs zu verwenden, da diese zur Buildzeit überprüft werden. Verwenden Sie XRef-Links mit der eindeutigen ID ([UID](#determine-the-uid)) des Typs oder Members, um automatisch generierte Links zu API-Referenzen im aktuellen Docset oder in anderen Docsets hinzuzufügen.

> [!TIP]
> Sie können die [Docs-Markdownerweiterung für Visual Studio Code][docsextension] (im Docs Authoring Pack enthalten) verwenden, um .NET-XRef-Links einzufügen, die im [.NET-API-Browser][] angezeigt werden.

Überprüfen Sie, ob die API, die Sie verlinken möchten, sich auf [docs.microsoft.com][docs] befindet, indem Sie ihren Namen ganz oder teilweise in den [.NET-API-Browser][] oder das [UWP][] eingeben. Wenn keine Ergebnisse angezeigt werden, ist sie noch nicht auf docs.microsoft.com vorhanden.

Sie können eine der folgenden Syntaxvarianten auswählen:

- Automatische Links:

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   Standardmäßig zeigt der Linktext nur den Member- oder Typnamen an. Der optionale Abfrageparameter `displayProperty=nameWithType` erzeugt einen vollqualifizierten Linktext, der **namespace.typ** für Typen und **typ.member** für Typmember (inklusive Enumerationstypenmember) lautet.

- Markdownlinks:

   ```markdown
   [link text](xref:UID)
   ```

   Verwenden Sie Markdownlinks für XRef, wenn Sie den angezeigten Linktext anpassen möchten.

Beispiele:

- **\<xref:System.String>** wird als <xref:System.String> angezeigt.

- **\<xref:System.String?displayProperty=nameWithType>** wird als <xref:System.String?displayProperty=nameWithType> angezeigt.

- **\[String-Klasse](xref:System.String)** wird als [String-Klasse](xref:System.String) angezeigt.

Der Abfrageparameter `displayProperty=fullName` funktioniert genau wie `displayProperty=nameWithType` für Klassen. Der Linktext wird also zu **namespace.klassenname**. Für Member wird der Linktext jedoch als **namespace.klassenname.membername** angezeigt. Das ist möglicherweise nicht erwünscht.

> [!NOTE]
> Bei UIDs wird die Groß-/Kleinschreibung berücksichtigt. Beispielsweise wird `<xref:System.Object>` ordnungsgemäß aufgelöst, `<xref:system.object>` jedoch nicht.

### <a name="xref-build-warnings-and-incremental-builds"></a>XRef-Buildwarnungen und inkrementelle Builds

Bei einem inkrementellen Build werden nur Dateien erstellt, die geändert wurden oder von einer Änderung betroffen sind. Wenn eine Buildwarnung zu einem ungültigen XRef-Link angezeigt wird, der Link aber eigentlich gültig ist, kann das daran liegen, dass es sich um einen inkrementellen Build handelt. Die Datei, die die Warnung verursacht hat, wurde nicht geändert und deshalb nicht erstellt, sodass frühere Warnungen wiederholt angezeigt wurden. Die Warnung wird nicht mehr angezeigt, wenn die Datei geändert wird oder Sie einen vollständigen Build initiieren (über ops.microsoft.com). Das ist ein Nachteil von inkrementellen Builds, da DocFX keine Datenupdates im XRef-Dienst erkennt.

### <a name="determine-the-uid"></a>Ermitteln der UID

Die UID entspricht in der Regel dem vollqualifizierten Klassen- oder Membernamen. Es gibt mindestens zwei Möglichkeiten, die UID zu ermitteln:

- Rechtsklicken Sie auf die Seite [Dokumentation][docs] eines Typs oder Members, klicken Sie dann auf **Quelltext anzeigen**, und kopieren Sie den **content**-Wert von **ms.assetid**:

  ![ms.assetid im Quelltext der Webseite](media/how-to-write-links/ms-assetid.png)

- Nutzen Sie die [automatische Vervollständigung][], indem Sie den Typnamen ganz oder teilweise an die URL anfügen. Wenn Sie beispielsweise `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in die Adressleiste Ihres Browsers eingeben, werden alle Typen und Methoden angezeigt, die **Writeline** im Namen enthalten, sowie die jeweilige UID.

#### <a name="verify-the-uid"></a>Überprüfen der UID

Sie können testen, ob die UID korrekt ist, indem Sie **System.String** in der folgenden URL durch Ihre UID ersetzen und diese dann in die Adressleiste eines Browsers einfügen:

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> Bei der UID in der URL wird die Groß-/Kleinschreibung beachtet. Vermeiden Sie zudem Leerzeichen zwischen den Parametertypen, wenn Sie eine Methodenüberladungs-UID überprüfen.

Wenn die Ausgabe der folgenden ähnelt, ist die UID korrekt:

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

Wenn auf der Seite nur `[]` angezeigt wird, ist die UID nicht korrekt.

### <a name="percent-encoding-of-urls"></a>Prozentcodierung von URLs

Sonderzeichen in der UID müssen folgendermaßen HTML-codiert werden:

| Zeichen | HTML-Codierung |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

Hier finden Sie eine vollständige Liste der [Prozentcodierungen](https://en.wikipedia.org/wiki/Percent-encoding).

Codierungsbeispiele:

- ``System.Threading.Tasks.Task`1`` wird als `System.Threading.Tasks.Task%601` codiert (Vergleich: [Abschnitt zu generischen Typen](#generic-types)).

- `System.Exception.#ctor` wird als `System.Exception.%23ctor` codiert.

- `System.Object.Equals*` wird als `System.Object.Equals%2A` codiert.

### <a name="generic-types"></a>Generische Typen

Bei generischen Typen handelt es sich um Typen wie `System.Collections.Generic.List<T>`. Wenn Sie einen solchen Typ im [.NET-API-Browser](https://docs.microsoft.com/dotnet/api/) suchen, stellen Sie bei der URL fest, dass `<T>` im Format `-1` dargestellt wird und somit eigentlich für **`1** steht:

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

Für eine Verlinkung mit einem generischen Typ wie **List\<T>** müssen Sie das Backtickzeichen **\`** wie im folgenden Beispiel dargestellt als **%60** codieren:

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>Methoden

Für die Verlinkung mit einer Methode können Sie entweder einen Link zur allgemeinen Methodenseite erstellen, indem Sie ein Sternchen (`*`) an den Methodennamen anfügen, oder zu einer bestimmten Überladung. Verwenden Sie die allgemeine Seite beispielsweise, wenn Sie einen Link zur `<xref:System.Object.Equals%2A?displayProperty=nameWithType>`-Methode ohne bestimmte Parametertypen erstellen möchten. Das Sternchen wird als `%2A` codiert. Beispiel:

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` verlinkt zu <xref:System.Object.Equals%2A?displayProperty=nameWithType>.

Für eine Verlinkung zu einer bestimmten Überladung müssen Sie nach dem Methodennamen Klammern einfügen und dort die vollständigen Namen der einzelnen Parameter eingeben. Fügen Sie kein Leerzeichen zwischen den Typnamen ein, da der Link andernfalls nicht funktioniert. Beispiel:

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` verlinkt zu <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>.

## <a name="links-from-includes"></a>Links von Includes

Da sich include-Dateien in einem anderen Verzeichnis befinden, müssen Sie längere relative Pfade verwenden. Verwenden Sie zum Erstellen eines Links zu einem Artikel aus einer include-Datei folgendes Format:

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> Mit dem Erweiterung [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) für Visual Studio Code können Sie relative Links und Lesezeichenlinks korrekt einfügen, ohne sich um den Pfad Gedanken machen zu müssen.

## <a name="links-in-selectors"></a>Links in Selektoren

Ein Selektor ist eine Komponente zum Navigieren, die in einem Dokumentationsartikel als Dropdownliste angezeigt wird. Wenn ein Leser einen Wert in der Dropdownliste auswählt, wird der ausgewählte Artikel im Browser geöffnet. In der Regel enthält die Selektorliste Links zu Artikeln, die in engem Zusammenhang stehen, z.B. der gleiche Inhalt in mehreren Programmiersprachen oder eine zusammenhängende Reihe von Artikeln.

Wenn Sie in einer Includedatei eingebettete Selektoren verwenden, verwenden Sie folgende Linkstruktur:

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>Verweislinks

Zur besseren Lesbarkeit Ihres Quellinhalts können Sie Verweislinks verwenden. Die Verweislinks ersetzen die Syntax des Inlinelinks durch eine vereinfachte Syntax, mit der Sie lange URLs an das Ende des Artikels verschieben können. Im Folgenden wird ein Beispiel aus dem Blog [Daring Fireball](https://daringfireball.net/projects/markdown/) vorgestellt:

Inlinetext:

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Linkverweise am Ende des Artikels:

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

Achten Sie darauf, dass Sie nach dem Doppelpunkt und vor dem Link ein Leerzeichen einfügen. Wenn Sie einen Link zu anderen technischen Artikeln einfügen und das Leerzeichen vergessen, ist der Link im veröffentlichten Artikel fehlerhaft.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Link zu Seiten außerhalb der technischen Dokumentation

Zum Erstellen eines Links zu einer Seite zu einer anderen Microsoft-Eigenschaft (z.B. einer Seite mit Preisen oder der SLA oder einer anderen Seite, die kein Dokumentationsartikel ist), verwenden Sie eine absolute URL, wobei Sie jedoch das Gebietsschema auslassen. Hierdurch soll die Funktionsfähigkeit von Links in GitHub und auf der gerenderten Website sichergestellt werden:

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>Links zu Websites von Drittanbietern

Um eine ideale Benutzererfahrung sicherzustellen, sollten Benutzer so selten wie möglich an andere Websites verwiesen werden. Daher sollten beim Hinzufügen von Links zu Websites von Drittanbietern, was gelegentlich notwendig ist, folgende Punkte berücksichtigt werden:

- **Verantwortlichkeit**: Links zu Inhalten von Drittanbietern, wenn die Informationen, die geteilt werden sollen, von Drittanbietern stammen. Beispielsweise liegt es nicht im Zuständigkeitsbereich von Microsoft, Benutzer über die Verwendung von Android-Entwicklertools zu informieren – dies ist die Aufgabe von Google. Bei Bedarf können wir erläutern, wie Android-Entwicklertools im Zusammenhang *mit* Azure zu verwenden sind. Doch die allgemeine Erläuterung bezüglich der Verwendung dieser Tools obliegt Google.
- **Freigabe durch einen PM**: Stellen Sie die Anforderung, dass Inhalte von Drittanbietern durch Microsoft freigegeben werden. Durch die Erstellung von Links zu diesen Inhalten drücken wir unser Vertrauen in diese Inhalte aus und müssen gewisse Pflichten erfüllen, wenn Benutzer die Anweisungen befolgen.
- **Prüfung der Aktualität**: Stellen Sie sicher, dass Informationen von Drittanbietern nach wie vor aktuell, korrekt und relevant sind und dass sich der Link nicht geändert hat.
- **Hinweis auf Umleitung an externe Websites**: Benutzer müssen darauf hingewiesen werden, dass sie auf eine andere Website umgeleitet werden. Wenn sich dies nicht eindeutig aus dem Kontext ergibt, fügen Sie einen entsprechenden Hinweis hinzu. Beispiel: „Zu den Voraussetzungen zählen die Android-Entwicklertools. Diese können Sie über die Android Studio-Website herunterladen.“
- **Nächste Schritte**: Im Abschnitt „Nächste Schritte“ können Sie beispielsweise einen Link zu einem Blog von einem MVP hinzufügen. Auch hier müssen Benutzer lediglich darauf hingewiesen werden, dass sie im Begriff sind, die Website zu verlassen.
- **Rechtliche Hinweise**: Durch die **Nutzungsbedingungen** in der Fußzeile jeder microsoft.com-Seite sind wir in Bezug auf **Links zu Websites von Drittanbietern** rechtlich geschützt.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[.NET-API-Browser]: https://docs.microsoft.com/dotnet/api/
[UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Automatische Vervollständigung]: https://xref.docs.microsoft.com/autocomplete?text=
