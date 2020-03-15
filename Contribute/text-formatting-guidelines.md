---
title: Richtlinien zum Formatieren von Text
description: Erfahren Sie, wie Sie Fett-, Kursiv-, Code- und andere Textformate in Artikeln für docs.microsoft.com verwenden können.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336494"
---
# <a name="text-formatting-guidelines"></a>Richtlinien zum Formatieren von Text

Die konsistente und angemessene Verwendung von Fett-, Kursiv- und Codeformatierungen von Textelementen verbessert die Lesbarkeit und hilft bei der Vermeidung von Missverständnissen.

## <a name="bold"></a>Fett

Schreiben Sie UI-Elemente wie Menüs, Dialogfeldnamen und Eingabefeldnamen fett.

### <a name="examples"></a>Beispiele

* **Richtig**: Klicken Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf den Projektknoten, und wählen Sie **Hinzufügen > Neues Element** aus.
* **Falsch**: Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den Projektknoten, und wählen Sie Hinzufügen > Neues Element aus.
* **Falsch**: Klicken Sie im *Projektmappen-Explorer* mit der rechten Maustaste auf den Projektknoten, und wählen Sie *Hinzufügen > Neues Element* aus.

## <a name="italics"></a>Kursiv

Verwenden Sie Kursivschrift für Folgendes:

* Einführung neuer Begriffe zusammen mit einer Definition oder Erläuterung.
* Dateinamen, Ordnernamen, Pfade.
* Benutzereingabe.

### <a name="examples"></a>Beispiele

* **Richtig**: In App Service wird eine App in einem *App Service-Plan* ausgeführt. Mit einem App Service-Plan werden mehrere Computeressourcen definiert, auf denen eine Web-App ausgeführt wird.
* **Falsch**: In App Service wird eine App in einem „App Service-Plan“ ausgeführt. Mit einem App Service-Plan werden mehrere Computeressourcen definiert, auf denen eine Web-App ausgeführt wird.
* **Richtig**: Ersetzen Sie den Code in *HttpTriggerCSharp.cs* durch den folgenden Code.
* **Falsch**: Ersetzen Sie den Code in `HttpTriggerCSharp.cs` durch den folgenden Code.
* **Richtig**: Geben Sie *ContosoUniversity* als **Name** ein, und wählen Sie **Hinzufügen** aus.
* **Falsch**: Geben Sie „ContosoUniversity“ als **Name** ein, und wählen Sie **Hinzufügen** aus.

## <a name="code-style"></a>Codeformat

Verwenden Sie das Codeformat für Folgendes:

* Codeelemente, z.B. Methodennamen, Eigenschaftennamen und Schlüsselwörter.
* SQL-Befehle
* NuGet-Paketnamen
* Befehlszeilenbefehle
* Datenbanktabellennamen und Datenbankspaltennamen
* Ressourcennamen, die nicht lokalisiert werden sollten (z. B. die Namen virtueller Computer)
* URLs, die nicht klickbar sein sollen

**Warum?** In älteren Styleguides wird für viele dieser Textelemente das Fettformat angegeben. Weil aber die meisten Artikel lokalisiert werden, zeigt das Codeformat dem Übersetzer/der Übersetzerin, dass dieser Teil des Texts nicht übersetzt wird.

Das Codeformat kann *inline* sein (umschlossen von \`) oder aus *umgrenzten* Codeblöcken bestehen (umschlossen von \`\`\`), die sich über mehrere Zeilen erstrecken. Fügen Sie längere Codeausschnitte und -pfade in umgrenzte Codeblöcke ein.

### <a name="examples-using-inline-styles"></a>Beispiele für die Verwendung von Inlineformaten

* **Richtig**: Standardmäßig interpretiert das Entity Framework eine Eigenschaft mit dem Namen `Id` oder `ClassnameID` als Primärschlüssel.
* **Falsch**: Standardmäßig interpretiert das Entity Framework eine Eigenschaft mit dem Namen *Id* oder *ClassnameI* als Primärschlüssel.
* **Richtig**: Das Paket `Microsoft.EntityFrameworkCore` bietet Laufzeitunterstützung für EF Core.
* **Falsch**: Das Paket *Microsoft.EntityFrameworkCore* bietet Laufzeitunterstützung für EF Core.

### <a name="examples-of-fenced-code-blocks"></a>Beispiele für umgrenzte Codeblöcke

* **Richtig**: Es werden keine Befehle von Anweisungen, die nur `IQueryable` ändern, an die Datenbank gesendet, wie z. B. im folgenden Code:

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **Falsch**: Es werden keine Befehle von Anweisungen, die nur **lQueryable** ändern, an die Datenbank gesendet, wie z. B. **var students = context.Students.Where(s => s.LastName == "Davolio")** .

* **Richtig**: Wenn Sie beispielsweise das Skript `Get-ServiceLog.ps1` im Verzeichnis `C:\Scripts` ausführen möchten, geben Sie Folgendes ein:

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **Falsch**: Wenn Sie beispielsweise das Skript **Get-ServiceLog.ps1** im Verzeichnis **C:\Scripts** ausführen möchten, geben Sie Folgendes ein: „C:\Scripts\Get-ServiceLog.ps1“.

* **Alle** umgrenzten Codeblöcke müssen ein genehmigtes Sprachtag haben. Eine Liste von unterstützten Sprachtags finden Sie unter [Einbinden von Code in Dokumenten](./code-in-docs.md#supported-languages).

## <a name="headings-and-link-text"></a>Überschriften und Linktext

Verwenden Sie kein Inlineformat wie Kursiv, Fett oder Code für Überschriften oder Linktext.

**Warum?**

Benutzer verlassen sich auf das Standardformat für Linktext, um Textelemente als klickbare Links zu identifizieren. Einen Link beispielsweise als Code zu formatieren, kann dazu führen, dass man den Text nicht als Link erkennt. Überschriften haben ihre eigenen Formate. Kombinieren Sie nicht mehrere Formate miteinander.

### <a name="examples"></a>Beispiele

* **Richtig**: Die Datei *function.json* wird mit dem NuGet-Paket [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) erstellt.
* **Falsch**: Die Datei *function.json* wird mit dem NuGet-Paket [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions) erstellt.

* **Richtig**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **Falsch**:

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>Tasten und Tastenkombinationen

Beachten Sie die folgenden Konventionen, wenn Sie auf Tasten oder Tastenkombinationen verweisen:

* Schreiben Sie Tastennamen groß.
* Wenden Sie kein Inlineformat wie Kursiv, Fett oder Code an.
* Verwenden Sie „+“ zum Verbinden von Tasten, die gleichzeitig gedrückt werden müssen.

### <a name="examples"></a>Beispiele

* **Richtig**: Drücken Sie ALT+STRG+S.
* **Falsch**: Drücken Sie **ALT+STRG+S**.
* **Falsch**: Drücken Sie `ALT+CTRL+S`.

Weitere Informationen finden Sie unter [Beschreiben von Interaktionen mit der Benutzeroberfläche](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472).

## <a name="exceptions"></a>Ausnahmen

Die Richtlinien des Styleguides sind keine strengen Regeln. Gehen Sie aber in einem Kontext, in dem diese Richtlinien die Lesbarbarkeit beeinträchtigen, anders vor. Zum Beispiel kann eine HTML-Tabelle, die überwiegend Codeelemente enthält, unübersichtlich sein, wenn überall das Codeformat verwendet wird. In diesem Kontext würde sich das Fettformat empfehlen.

Wenn Sie in Fällen, in denen normalerweise Code erforderlich ist, ein anderes Textformat verwenden, stellen Sie sicher, dass der Text in lokalisierten Versionen des Artikels übersetzt werden kann. Das Codeformat ist das einzige Format, das Übersetzungen automatisch verhindert. Bei Szenarien, in denen Sie die Lokalisierung ohne Codeformat verhindern möchten, finden Sie entsprechende Informationen unter [Nicht lokalisierte Zeichenfolgen](markdown-reference.md#non-localized-strings).
