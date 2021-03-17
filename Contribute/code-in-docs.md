---
title: 'Gewusst wie: Einbinden von Code in Dokumenten'
description: Erfahren Sie, wie Sie Codeelemente und -ausschnitte in Artikeln auf docs.microsoft.com veröffentlichen.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: ddd0463840769f02724423583efaa6ffa69d5d33
ms.sourcegitcommit: 48d9a16cd3854cdf3c8c492dab1675edcdfbbd7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103481358"
---
# <a name="how-to-include-code-in-docs"></a>Gewusst wie: Einbinden von Code in Dokumenten

Es gibt mehrere Methoden zum Einbinden von Code in einem Artikel, der auf docs.microsoft.com veröffentlicht wird:

* Einzelne Elemente (Wörter) innerhalb einer Zeile

  Es folgt ein Beispiel für das `code`-Format.

  Verwenden Sie Codeformat, wenn Sie auf benannte Parameter und Variablen in einem in der Nähe befindlichen Codeblock im Text verweisen. Codeformat kann auch für Eigenschaften, Methoden, Klassen und Sprachschlüsselwörter verwendet werden. Weitere Informationen finden Sie unter [Codeelemente](#code-elements) weiter unten in diesem Artikel.

* Codeblöcke in der Markdowndatei des Artikels

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Verwenden Sie Inlinecodeblöcke, wenn es nicht praktikabel ist, Code durch einen Verweis auf eine Codedatei anzuzeigen. Weitere Informationen finden Sie unter [Codeblöcke](#inline-code-blocks) weiter unten in diesem Artikel.

* Codeblöcke durch einen Verweis auf eine Codedatei im lokalen Repository

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Weitere Informationen finden Sie unter [Verweise auf Ausschnitte in Repositorys](#in-repo-snippet-references) weiter unten in diesem Artikel.

* Codeblöcke durch einen Verweis auf eine Codedatei in einem anderen Repository

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Weitere Informationen finden Sie unter [Verweise auf Ausschnitte außerhalb des Repositorys](#out-of-repo-snippet-references) weiter unten in diesem Artikel.
  
* Codeblöcke, mit denen der Benutzer Code im Browser ausführen kann

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Weitere Informationen finden Sie unter [Interaktive Codeausschnitte](#interactive-code-snippets) weiter unten in diesem Artikel.

Neben einer Erläuterung des Markdown für jede dieser Methoden zum Einbinden von Code enthält der Artikel einige [allgemeine Hinweise für alle Codeblöcke](#code-blocks).

## <a name="code-elements"></a>Codeelemente

Als „Codeelement“ wird in der Programmiersprache z.B. ein Schlüsselwort, Klassenname oder Eigenschaftsname bezeichnet. Es ist nicht immer offensichtlich, was als Code gilt. Beispielsweise sollten NuGet-Paketnamen als Code behandelt werden. Im Zweifelsfall schauen Sie in den [Textformatierungsrichtlinien](text-formatting-guidelines.md) nach.

### <a name="inline-code-style"></a>Inlinecodeformat

Um ein Codeelement in den Artikeltext einzubinden, umgeben Sie es mit Graviszeichen (\`), um das Codeformat anzugeben.
Beim Inlinecodeformat sollte nicht das Format mit Dreifach-Graviszeichen verwendet werden.

|Markdown |Gerendert |
|---------|---------|
|Standardmäßig interpretiert das Entity Framework eine Eigenschaft mit dem Namen \`Id\` oder \`ClassnameI\` als Primärschlüssel.|Standardmäßig interpretiert das Entity Framework eine Eigenschaft mit dem Namen `Id` oder `ClassnameID` als Primärschlüssel.|

Wenn ein Artikel lokalisiert (in andere Sprachen übersetzt) wird, bleibt der als Code formatierte Text unübersetzt. Wenn Sie die Lokalisierung ohne Codeformat verhindern möchten, finden Sie Informationen dazu unter [Nicht lokalisierte Zeichenfolgen](markdown-reference.md#non-localized-strings).

### <a name="bold-style"></a>Fettformatierung

Einige ältere Styleguides geben vor, dass Inlinecode fett zu formatieren ist. Fett ist eine Option, wenn das Codeformat so störend ist, dass die Lesbarkeit beeinträchtigt wird. Beispielsweise könnte eine Markdowntabelle, in der sich größtenteils Codeelemente befinden, durch die Codeformatierung etwas überfrachtet aussehen. Wenn Sie Fettformatierung verwenden möchten, nutzen Sie die [Syntax für nicht lokalisierte Zeichenfolgen](markdown-reference.md#non-localized-strings), um sicherzustellen, dass der Code nicht lokalisiert wird.

### <a name="links"></a>Links

In einigen Kontexten ist ein Link zu einer Referenzdokumentation möglicherweise hilfreicher als Codeformat. Wenn Sie einen Link verwenden, wenden Sie kein Codeformat auf den Linktext an. Einen Link als Code zu formatieren, kann dazu führen, dass man den Text nicht als Link erkennt.

Wenn Sie einen Link verwenden und später im gleichen Kontext auf dasselbe Element verweisen, verwenden Sie für die nachfolgenden Instanzen Codeformat und keine Links.

### <a name="placeholders"></a>Platzhalter

Wenn Sie möchten, dass der Benutzer einen Abschnitt des angezeigten Codes durch eigene Werte ersetzt, verwenden Sie Platzhaltertext, der durch spitze oder geschweifte Klammern gekennzeichnet ist. Beispiel: `az group delete -n <ResourceGroupName>`. Weisen Sie darauf hin, dass die Klammern beim Ersetzen durch echte Werte entfernt werden müssen.

## <a name="code-blocks"></a>Codeblöcke

Die Syntax für das Einbinden von Code in einem Dokument hängt davon ab, wo sich der Code befindet:

* [In der Markdowndatei des Artikels](#inline-code-blocks)
* [In einer Codedatei im selben Repository](#in-repo-snippet-references)
* [In einer Codedatei in einem anderen Repository](#out-of-repo-snippet-references)

Die folgenden Richtlinien gelten für alle drei Arten von Codeblöcken:

* [Automatisieren Sie die Codeüberprüfung.](#code-validation)
* [Heben Sie wichtige Codezeilen hervor.](#highlighting)
* [Vermeiden Sie horizontale Scrollleisten.](#horizontal-scroll-bars)

### <a name="screenshots"></a>Screenshots

Alle im vorherigen Abschnitt aufgeführten Methoden führen zu verwendbaren Codeblöcken:

* Sie können daraus kopieren und einfügen.
* Sie werden von Suchmaschinen indiziert.
* Sprachausgaben können darauf zugreifen.

Dies sind nur einige der Gründe, warum IDE-Screenshots nicht als Methode zum Einbinden von Code in einen Artikel empfohlen werden. Verwenden Sie IDE-Screenshots nur dann für Code, wenn Sie etwas über die IDE selbst, z. B. IntelliSense, zeigen. Verwenden Sie Screenshots nicht, um lediglich Farbgebung und Hervorhebung anzuzeigen.

### <a name="code-validation"></a>Codeüberprüfung

In einigen Repositorys wird der gesamte Beispielcode durch implementierte Prozesse automatisch kompiliert, um ihn auf Fehler zu prüfen. Dies ist beim .NET-Repository der Fall. Weitere Informationen finden Sie im .NET-Repository unter [Contributing](https://github.com/dotnet/docs/blob/main/CONTRIBUTING.md) (Beitrag).

Wenn Sie Codeblöcke aus einem anderen Repository einbinden, erarbeiten Sie zusammen mit den Besitzern eine Wartungsstrategie für den Code, damit Ihr eingebundener Code nicht unterbrochen wird oder veraltet, sobald neue Versionen der vom Code verwendeten Bibliotheken geliefert werden.

### <a name="highlighting"></a>Hervorhebung

Ausschnitte enthalten in der Regel mehr Code als nötig, um den Kontext darzustellen. Die Lesbarkeit wird erleichtert, wenn Sie die wichtigen Zeilen im Codeausschnitt hervorheben, wie z.B. in diesem Beispiel:

![Beispiel mit hervorgehobenem Code](media/code-in-docs/highlighted-code.png)

Sie können den Code nicht hervorheben, wenn Sie ihn in der Markdowndatei des Artikels einbinden. Dies funktioniert nur für Codeausschnitte, die durch Verweis auf eine Codedatei eingebunden werden.

### <a name="horizontal-scroll-bars"></a>Horizontale Scrollleisten

Fügen Sie Umbrüche in langen Zeilen ein, um horizontale Scrollleisten zu vermeiden. Die Verwendung von Scrollleisten bei Codeblöcken erschwert das Lesen des Codes. Sie sind besonders problematisch bei längeren Codeblöcken, bei denen es nicht möglich ist, die Scrollleiste und die zu lesende Zeile gleichzeitig anzuzeigen.

Eine gute Vorgehensweise zur Minimierung horizontaler Scrollleisten in Codeblöcken ist es, in Codezeilen mit mehr als 85 Zeichen einen Umbruch einzufügen. Denken Sie jedoch daran, dass das Vorhandensein oder Fehlen einer Scrollleiste nicht das einzige Kriterium für Lesbarkeit ist. Wenn der Umbruch von Zeilen vor dem 85. Zeichen zu schlechterer Lesbarkeit oder Schwierigkeiten beim Kopieren und Einfügen führt, können Sie auch mehr als 85 Zeichen in der Zeile belassen.

## <a name="inline-code-blocks"></a>Inlinecodeblöcke

Verwenden Sie Inlinecodeblöcke nur, wenn es nicht praktikabel ist, Code durch einen Verweis auf eine Codedatei anzuzeigen. Inlinecode ist im Allgemeinen schwieriger zu testen und auf dem neuesten Stand zu halten als eine Codedatei, die Teil eines vollständigen Projekts ist.  Außerdem wird beim Inlinecode möglicherweise Kontext ausgelassen, der dem Entwickler dabei helfen könnte, den Code zu verstehen und zu verwenden. Diese Überlegungen gelten vor allem für Programmiersprachen. Inlinecodeblöcke können auch für Ausgaben und Eingaben (z. B. JSON), Abfragesprachen (z. B. SQL) und Skriptsprachen (z. B. PowerShell) verwendet werden.
  
Es gibt zwei Möglichkeiten, einen Textabschnitt in einer Artikeldatei als Codeblock anzuzeigen: durch *Fencing* (Umklammern) dieses Abschnitts mit Dreifach-Graviszeichen (\`\`\`) oder durch Einrücken. Fencing wird bevorzugt, weil Sie dadurch die Sprache festlegen können. Vermeiden Sie das Einrücken, da hierbei zu leicht Fehler gemacht werden und es für einen anderen Autor schwierig sein kann, Ihre Absicht zu verstehen, wenn der Artikel bearbeitet werden muss.

Die Sprachindikatoren werden unmittelbar nach den sich öffnenden Dreifach-Graviszeichen platziert, wie im folgenden Beispiel zu sehen:

Markdown:

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

Gerendert:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Informationen zu den Werten, die Sie als Sprachindikatoren verwenden können, finden Sie unter [Sprachnamen und Aliase](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

Wenn Sie nach den Dreifach-Graviszeichen (\`\`\`) ein nicht unterstütztes Sprach- oder Umgebungswort verwenden, wird dieses Wort in der Titelleiste des Codeabschnitts auf der gerenderten Seite angezeigt. Verwenden Sie nach Möglichkeit einen Sprach- oder Umgebungsindikator in den Inlinecodeblöcken.

> [!NOTE]
> Wenn Sie Code aus einem Word-Dokument kopieren und einfügen, vergewissern Sie sich, dass er keine „geschweiften Anführungszeichen“ enthält, die in Code nicht gültig sind (z. B. `“` und `’`). Wenn das der Fall ist, ändern Sie diese wieder in normale Anführungszeichen (`'` und `"`). Alternativ können Sie auch die [Funktion für den Austausch typografischer Anführungszeichen](docs-authoring/smart-quote-replacement.md) im Docs Authoring Pack nutzen.

## <a name="in-repo-snippet-references"></a>Verweise auf Ausschnitte in Repositorys

Die bevorzugte Methode, Codeausschnitte für Programmiersprachen in Dokumente einzubinden, ist der Verweis auf eine Codedatei. Diese Methode bietet Ihnen die Möglichkeit, Codezeilen hervorzuheben, und stellt den Entwicklern den größeren Kontext des Codeausschnitts auf GitHub zur Verwendung bereit. Sie können Code mithilfe des Formats mit drei Doppelpunkten (:\:\:) entweder manuell oder in Visual Studio Code mit Unterstützung durch das [Authoring Pack für docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) einbinden.

1. Drücken Sie in Visual Studio Code <kbd>ALT+M</kbd> oder <kbd>WAHLTASTE+M</kbd>, und klicken Sie auf „Codeausschnitt“.
2. Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen. Wählen Sie „Full Search“ (Vollständige Suche) aus, wenn Sie lokal suchen möchten.
3. Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen. Wählen Sie die Datei aus, wenn sie gefunden wurde.
4. Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen. Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).
5. Geben Sie je nach Auswahl in Schritt 4 einen Wert an.

Die gesamte Codedatei wird angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Ein Teil einer Codedatei wird durch Angabe von Zeilennummern angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Ein Teil einer Codedatei wird durch Angabe eines Ausschnittnamens angezeigt:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

In den folgenden Abschnitten werden diese Beispiele erläutert:

* [Verwenden eines relativen Pfads zur Codedatei](#path-to-code-file)
* [Ausschließliches Einbinden ausgewählter Zeilennummern](#selected-line-numbers)
* [Verweisen auf benannten Codeausschnitt](#named-snippet)
* [Hervorheben ausgewählter Zeilen](#highlighting-selected-lines)

Weitere Informationen finden Sie unter [Verweissyntax für Codeausschnitte](#snippet-syntax-reference) weiter unten in diesem Artikel.

### <a name="path-to-code-file"></a>Pfad zur Codedatei

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Das Beispiel stammt aus der Artikeldatei [aspnetcore/data/ef-mvc/crud.md](https://github.com/dotnet/AspNetCore.Docs/blob/main/aspnetcore/data/ef-mvc/crud.md) des ASP.NET-Dokumentenrepositorys. Auf die Codedatei wird über einen relativen Pfad zu [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/dotnet/AspNetCore.Docs/blob/main/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) im selben Repository verwiesen.

### <a name="selected-line-numbers"></a>Ausgewählte Zeilennummern

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

In diesem Beispiel werden nur die Zeilen 2–24 und 26 der Codedatei *StudentController.cs* angezeigt.

Bevorzugen Sie benannte Codeausschnitte gegenüber hartcodierten Zeilennummern, wie im nächsten Abschnitt erläutert.

### <a name="named-snippet"></a>Benannter Codeausschnitt

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Verwenden Sie für den Namen nur Buchstaben und Unterstriche.

Das Beispiel zeigt den Abschnitt `snippet_Create` der Codedatei. Die Codedatei für dieses Beispiel enthält Codeausschnitttags in Kommentaren im C#-Code:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Wenn möglich, sollten Sie immer auf einen benannten Abschnitt verweisen anstatt Zeilennummern anzugeben. Zeilennummernverweise sind fehleranfällig, weil sich Codedateien zwangsläufig in einer Weise ändern, die die Zeilennummern verändern.
Über solche Änderungen werden Sie nicht unbedingt informiert. In Ihrem Artikel werden dann die falschen Zeilen angezeigt, und Sie haben keine Ahnung, dass sich überhaupt etwas geändert hat.

### <a name="highlighting-selected-lines"></a>Hervorheben ausgewählter Zeilen

Beispiel:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

Im Beispiel werden die Zeilen 2 und 5 hervorgehoben, gezählt vom Anfang des angezeigten Ausschnitts. Bei hervorzuhebenden Zeilennummern wird mit dem Zählen nicht am Anfang der Codedatei begonnen. Die Zeilen 3 und 6 der Codedatei werden also hervorgehoben.

## <a name="out-of-repo-snippet-references"></a>Verweise auf Ausschnitte außerhalb des Repositorys

Wenn sich die Codedatei, auf die verwiesen werden soll, in einem anderen Repository befindet, richten Sie das Coderepository als *abhängiges Repository* ein. Geben Sie in diesem Fall einen Namen dafür an. Dieser Name verhält sich dann wie ein Ordnername für Codeverweise.

Zum Beispiel lautet das Dokumentenrepository *Azure/azure-docs* und das Coderepository *Azure/azure-functions-durable-extension*.

Fügen Sie im Stammordner von *azure-docs* den folgenden Abschnitt in *.openpublishing.publish.config.json* hinzu:

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

Wenn Sie nun auf *samples-durable-functions* verweisen, als wäre es ein Ordner in *azure-docs*, verweisen Sie tatsächlich jedoch auf den Stammordner im Repository *azure-functions-durable-extension*.

Sie können Code mithilfe des Formats mit drei Doppelpunkten (:\:\:) entweder manuell oder in Visual Studio Code mit Unterstützung durch das [Authoring Pack für docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) einbinden.

1. Drücken Sie in Visual Studio Code <kbd>ALT+M</kbd> oder <kbd>WAHLTASTE+M</kbd>, und klicken Sie auf „Codeausschnitt“.
2. Nachdem Sie auf „Codeausschnitt“ geklickt haben, werden Sie dazu aufgefordert, zwischen „Full Search“ (Vollständige Suche), „Scoped Search“ (Bereichsbezogene Suche) oder „Cross-Repository Reference“ (Repositoryübergreifender Verweis) auszuwählen. Wählen Sie „Cross-Repository Reference“ (Repositoryübergreifender Verweis) aus, um repositoryübergreifend zu suchen.
3. Daraufhin wird eine Auswahl der Repositorys angezeigt, die sich in *.openpublishing.publish.config.json* befinden. Wählen Sie ein Repository aus.
4. Geben Sie einen Suchbegriff ein, um nach der Datei zu suchen. Wählen Sie die Datei aus, wenn sie gefunden wurde.
5. Wählen Sie dann eine Option aus, um festzulegen, welche Codezeile(n) im Codeausschnitt enthalten sein sollen. Folgende Optionen sind verfügbar: **ID**, **Range** (Bereich) und **None** (Keine).
6. Geben Sie je nach Auswahl in Schritt 5 einen Wert an.

Ihr Codeausschnittverweis sieht folgendermaßen aus:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

Im Repository *azure-functions-durable-extension* befindet sich diese Codedatei im Ordner *samples/csx/shared*. Wie [oben](#highlighting-selected-lines) erwähnt, sind die Zeilennummern für die Hervorhebung relativ zum Anfang des Codeausschnitts und nicht zum Anfang der Datei.

> [!NOTE]
> Der Name, den Sie dem abhängigen Repository zuweisen, ist relativ zum Stamm des Hauptrepositorys, aber die Tilde (~) verweist auf den Stamm des Docsets. Der Stamm des Docsets wird durch `build_source_folder` in *.openpublishing.publish.config.json* bestimmt. Der Pfad zum Codeausschnitt im vorherigen Beispiel wird im Repository „azure-docs“ verwendet, da `build_source_folder` auf den Repositorystamm (`.`) verweist. Wenn für `build_source_folder` der Wert `articles` angegeben wäre, würde der Pfad mit `~/../samples-durable-functions` anstelle von `~/samples-durable-functions` beginnen.

## <a name="snippets-in-a-jupyter-notebook"></a>Codeausschnitte in einem Jupyter-Notebook

Sie können auf eine Zelle in einem Jupyter-Notebook als Codeausschnitt verweisen. So verweisen Sie auf die Zelle:

1. Fügen Sie dem Notebook Zellenmetadaten hinzu, auf die Sie verweisen möchten.
1. Richten Sie den Zugriff auf das Repository ein.
1. Verwenden Sie die Syntax für den Jupyter-Notebook-Ausschnitt in Ihrer Markdowndatei.

### <a name="add-metadata-to-notebook"></a>Hinzufügen von Metadaten zur Notebook-Instanz

1. Benennen Sie die Zelle, indem Sie Zellenmetadaten im Jupyter-Notebook hinzufügen.  

    * In Jupyter können Sie [Zellmetadaten bearbeiten](https://jupyterbook.org/advanced/advanced.html#adding-tags-using-notebook-interfaces), indem Sie zuerst die Zellensymbolleiste aktivieren:  **Ansicht > Zellensymbolleiste > Metadaten bearbeiten**
    * Nachdem die Zellensymbolleiste aktiviert ist, wählen Sie **Metadaten bearbeiten** in der Zelle aus, die Sie benennen möchten.
    * Alternativ können Sie die Metadaten direkt in der JSON-Struktur des Notebooks bearbeiten.

1.  Fügen Sie in den Zellenmetadaten ein „name“-Attribut hinzu:
 
    ```json
    "metadata": {"name": "<name>"},
    ```
  
    Beispiel:

    ```json
    "metadata": {"name": "workspace"},
    ```

    > [!TIP]
    > Sie können weitere Metadaten hinzufügen, die Ihnen helfen können, nachzuverfolgen, wo die Zelle verwendet wird.  Beispiel:
    >
    > ```json
    >     "metadata": {
    >       "name": "workspace",
    >       "msdoc": "how-to-track-experiments.md"
    >     },
    > ```

### <a name="set-up-repository-access"></a>Einrichten des Repositoryzugriffs

Wenn sich die die Notebook-Datei, auf die verwiesen werden soll, in einem anderen Repository befindet, richten Sie das Coderepository als [abhängiges Repository](#out-of-repo-snippet-references) ein.

### <a name="jupyter-notebook-snippet-syntax-reference"></a>Referenz zur Syntax für den Jupyter-Notebook-Ausschnitt

 Wenn Ihr Notebook die erforderlichen Metadaten enthält, verweisen Sie in Ihrer Markdowndatei darauf. Verwenden Sie den `<cell-name-value>`, den Sie dem Notebook hinzugefügt haben, sowie den `<path>` (Pfad), den Sie als Ihr abhängiges Repository eingerichtet haben.

```markdown
[!notebook-<language>[] (<path>/<notebook-name.ipynb>?name=<cell-name-value>)]
```

Beispiel:

```markdown
[!notebook-python[] (~/MachineLearningNotebooks/train-on-local.ipynb?name=workspace)]
```

> [!IMPORTANT]
> Diese Syntax ist ein Blockmarkdown-Erweiterung. Sie muss in einer eigenen Zeile verwendet werden.

Verwenden Sie für den `<language>`-Bezeichner eine der [unterstützten Programmiersprachen](#supported-languages).

## <a name="interactive-code-snippets"></a>Interaktive Codeausschnitte

### <a name="inline-interactive-code-blocks"></a>Interaktive Inlinecodeblöcke

Für die folgenden Sprachen können Codeausschnitte im Browserfenster ausführbar gemacht werden:

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Wenn der interaktive Modus aktiviert ist, verfügen die gerenderten Codeboxen über die Schaltflächen **Try It** (Testen) und **Run** (Ausführen). Beispiel:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

wird wie folgt gerendert:

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Um dieses Feature für einen bestimmten Codeblock zu aktivieren, verwenden Sie eine spezielle Sprachen-ID. Folgende Optionen sind verfügbar:

* `azurepowershell-interactive`: Aktiviert wie im vorherigen Beispiel PowerShell für Azure Cloud Shell
* `azurecli-interactive`: Aktiviert Azure Cloud Shell
* `csharp-interactive`: Aktiviert C#-REPL

Für Azure Cloud Shell und PowerShell Cloud Shell können Benutzer Befehle nur für ihr eigenes Azure-Konto ausführen.

### <a name="code-snippets-included-by-reference"></a>Durch einen Verweis eingebundene Codeausschnitte

Sie können den interaktiven Modus für Codeausschnitte aktivieren, die per Verweis eingebunden werden. Hier finden Sie Beispiele:

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Verwenden Sie das Attribut `interactive`, um dieses Feature für einen bestimmten Codeblock zu aktivieren. Folgende Attributwerte sind verfügbar:

* `cloudshell-powershell`: Aktiviert wie im vorherigen Beispiel PowerShell für Azure Cloud Shell
* `cloudshell-bash`: Aktiviert Azure Cloud Shell
* `try-dotnet`: Aktiviert .NET Interactive
* `try-dotnet-class`: Aktiviert .NET Interactive mit Klassengerüst
* `try-dotnet-method`: Aktiviert .NET Interactive mit Methodengerüst

Für Azure Cloud Shell und PowerShell Cloud Shell können Benutzer Befehle nur für ihr eigenes Azure-Konto ausführen.

Für die .NET Interactive-Erfahrung hängt der Inhalt Ihres Codeblocks davon ab, welche der drei Gerüstumgebungen Sie auswählen:

* *Kein Gerüstbau* (`try-dotnet`): Der Codeblock sollte einen vollständigen Programmtext darstellen. Die Datei *Program.cs*, die von `dotnet new console` generiert wird, wäre z. B. gültig. Diese sind am nützlichsten, um ein ganzes kleines Programm anzuzeigen, einschließlich der erforderlichen `using`-Direktiven. Anweisungen auf oberster Ebene werden derzeit nicht unterstützt.
* *Methodengerüst* (`try-dotnet-method`): Der Codeblock sollte den Inhalt einer `Main`-Methode in einer Konsolenanwendung darstellen. Sie können die von der `dotnet new console`-Vorlage hinzugefügten `using`-Direktiven annehmen. Diese Einstellung ist am nützlichsten für kurze Codeausschnitte, die ein Feature veranschaulichen.
* *Klassengerüst* (`try-dotnet-class`): Der Codeblock sollte eine Klasse mit einer `Main`-Methode als Programmeinstiegspunkt darstellen. Diese können verwendet werden, um zu zeigen, wie die Member einer Klasse interagieren.

## <a name="snippet-syntax-reference"></a>Verweissyntax für Codeausschnitte

Syntax:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Diese Syntax ist ein Blockmarkdown-Erweiterung. Sie muss in einer eigenen Zeile verwendet werden.

* `<language>` (*optional*)
  * Sprache des Codeausschnitts. Weitere Informationen finden Sie im Abschnitt [Unterstützte Sprachen](#supported-languages) weiter unten in diesem Artikel.

* `<path>` (*obligatorisch*)
  * Relativer Pfad im Dateisystem, der die Codeausschnittdatei angibt, auf die verwiesen wird.

* `<attribute>` und `<attribute-value>` (*optional*)

  Zusammen verwendet, um anzugeben, wie der Code aus der Datei abgerufen und wie er angezeigt werden soll:

  * `range`: `1,3-5` Ein Bereich von Zeilen. Dieses Beispiel enthält die Zeilen 1, 3, 4 und 5.
  * `id`: `snippet_Create`: Die ID des Codeausschnitts, der aus der Codedatei eingefügt werden soll. Dieser Wert kann nicht gleichzeitig mit „range“ vorhanden sein.
  * `highlight`: `2-4,6`: Der Bereich und/oder die Zeilennummern, die im generierten Codeausschnitt hervorgehoben werden sollen. Die Nummerierung ist relativ zu den angezeigten Zeilen (gemäß Bereich oder ID) und nicht zur Datei.
  * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method`: Der Zeichenfolgenwert legt fest, welche Arten von Interaktivität aktiviert sind.
  * Details zur Darstellung des Tagnamens in den Quelldateien des Codeausschnitts pro Sprache finden Sie unter [DocFX-Richtlinien](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

## <a name="supported-languages"></a>Unterstützte Sprachen

Das [Docs Authoring Pack](how-to-write-docs-auth-pack.md) enthält eine Funktion, die Anweisungsvervollständigung und eine Überprüfung der verfügbaren Sprachen-IDs für Codefence-Blöcke bietet.

### <a name="fenced-code-blocks"></a>Umgrenzte Codeblöcke

| Name                           | Gültige Aliase                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core-CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Zugriffsprotokolle                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| ARM assembler                  | `armasm`, `arm`                                                                |
| ARM assembler                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure Powershell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Standard                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| DNS Zone file                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (Device Tree)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| BEHEBUNG                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Lenkstangen                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Kleiner                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| Managed Object Format          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective-C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Plaintext no highlight         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Verarbeitung                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Eigenschaften                     | `properties`                                                                   |
| Protokollpuffer               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Python profiler results        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| RPM spec files                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Schema                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Shell                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Structured Text                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Eingabestift                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| x86 Assembly                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> Wenn mehrere Aliase verfügbar sind, verwendet die [Funktion zur Vervollständigung von Entwicklungssprachen](docs-authoring/dev-lang-completion.md) im Docs Authoring Pack den ersten gültigen Alias.

## <a name="next-steps"></a>Nächste Schritte

Informationen zur Textformatierung für andere Inhaltstypen als Code finden Sie in den [Textformatierungsrichtlinien](text-formatting-guidelines.md).
