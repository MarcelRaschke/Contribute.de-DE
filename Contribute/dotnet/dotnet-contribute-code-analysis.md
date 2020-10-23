---
title: Beitragen von Dokumenten für .NET-Codeanalyseregeln zum .NET-Dokumentationsrepository
description: In diesem Artikel wird der Prozess zum Beitragen zu den Artikeln und Codebeispielen für .NET-Codeanalyseregeln im .NET Dokumentationsrepository beschrieben.
author: mavasani
ms.author: mavasani
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 10/09/2020
ms.openlocfilehash: 27ae1a31c55c41aa1c97bf1f88dbf28bec35a80a
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "91957052"
---
# <a name="contribute-docs-for-net-code-analysis-rules-to-the-net-docs-repository"></a>Beitragen von Dokumenten für .NET-Codeanalyseregeln zum .NET-Dokumentationsrepository

Die Analysetools für die .NET-Compilerplattform (Roslyn) untersuchen Ihren C#- oder Visual Basic-Code auf Probleme hinsichtlich Codequalität und Codeformat. Ab .NET 5.0 sind diese Analysetools im [.NET SDK](/dotnet/fundamentals/code-analysis/overview) enthalten.

- [Analyse der Codequalität („CAxxxx“-Regeln)](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis):
  - [Hier](https://github.com/dotnet/roslyn-analyzers/tree/master/src/NetAnalyzers) im `dotnet/roslyn-analyzers`-Repository implementiert.
  - [Hier](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) im `dotnet/docs`-Repository dokumentiert. Weitere Informationen finden Sie unter [Beitragen von Dokumenten für „CAxxxx“-Regeln](#contribute-docs-for-caxxxx-rules).
- [Analyse des Codeformats („IDExxxx“-Regeln)](/dotnet/fundamentals/code-analysis/overview#code-style-analysis):
  - [Hier](https://github.com/dotnet/roslyn/tree/master/src/Analyzers) im `dotnet/roslyn`-Repository implementiert.
  - [Hier](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) im `dotnet/docs`-Repository dokumentiert. Weitere Informationen finden Sie unter [Beitragen von Dokumenten für „IDExxxx“-Regeln](#contribute-docs-for-idexxxx-rules).

## <a name="contribute-docs-for-caxxxx-rules"></a>Beitragen von Dokumenten für „CAxxxx“-Regeln

Befolgen Sie die folgenden Schritte, um Dokumentationen zu Analyseregeln für die Codequalität zum Repository [dotnet/docs](https://github.com/dotnet/docs) beizutragen:

1. Bestimmen Sie `Rule ID` und `Category`: Stellen Sie sicher, dass Sie die „CAxxxx“-Regel-ID und die Kategorie für die zu dokumentierende Regel kennen. Das bedeutet, dass entweder Ihr CA-Analysetool im Repository [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) zusammengeführt wurde, oder Sie verfügen über einen offenen PR mit einer genehmigten ID und Kategorie, die der Regel zugewiesen wurde.
2. Hinzufügen einer Regeldokumentation:
   1. Klonen Sie eine vorhandene CA-Regeldatei unter dem [Stammordner](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules), z. B. `ca1000.md`, und benennen Sie sie um.
   2. Aktualisieren Sie den Inhalt der Datei entsprechend.
3. Fügen Sie den folgenden Tabellen einen Eintrag für die Regel hinzu:
   - In der [Inhaltsverzeichnis](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)-Datei unter der Regelkategorieliste. Suchen Sie z. B. für eine CA-Regel mit der Kategorie `Performance` nach dem Begriff `- name: Performance rules` in der Datei, und fügen Sie der Liste einen Eintrag hinzu. Wenn keine vorhanden ist, erstellen Sie eine neue Kategorieliste unter `- name: Code quality rules`.
   - In der [Regelindexdatei auf oberster Ebene](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules/index.md).
   - In der auf `category` basierenden Regelindexdatei:
     1. Identifizieren Sie die kategoriebasierte Indexdatei unter dem [Stammordner](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules). Für eine CA-Regel mit der Kategorie `Performance` erhält diese Datei z. B. die Bezeichnung `performance-warnings.md`. Wenn keine vorhanden ist, erstellen Sie eine neue kategoriebasierte Indexdatei durch Klonen einer vorhandenen Datei.
     2. Fügen Sie in dieser Datei einen Eintrag für die Regel-ID hinzu.

> [!TIP]
> Führen Sie eine Repositorysuche im `dotnet/docs`-Repository nach einer bekannten, bestehenden CA-Regel-ID durch, um potenzielle Speicherorte zu identifizieren, die möglicherweise einer Aktualisierung bedürfen. Ein Beispiel finden Sie unter <https://github.com/dotnet/docs/search?q=CA2000>.

## <a name="contribute-docs-for-idexxxx-rules"></a>Beitragen von Dokumenten für „IDExxxx“-Regeln

Befolgen Sie die folgenden Schritte, um Dokumentationen zu Analyseregeln für das Codeformat zum Repository [dotnet/docs](https://github.com/dotnet/docs) beizutragen:

1. Bestimmen Sie `Rule ID` und Codeformatoptionen, falls vorhanden: Stellen Sie sicher, dass Sie die „IDExxxx“-Regel-ID und die Codeformatoptionen für die zu dokumentierende Regel kennen. Das bedeutet, dass entweder das IDE-Analysetool im Repository [dotnet/roslyn](https://github.com/dotnet/roslyn) zusammengeführt wurde, oder Sie verfügen über einen offenen PR mit einer genehmigten ID und Codeformatoptionen, die der Regel zugewiesen wurden.
2. Bestimmen Sie die Regel `subcategory`: IDE-Regeln besitzen die Kategorie `Style`. Identifizieren Sie die Regelunterkategorie, indem Sie den einleitenden Abschnitt von [Codeformatregeln](/dotnet/fundamentals/code-analysis/style-rules/index) durchlesen. Die meisten der IDE-Codeformatregeln befinden sich unter der `Language`-Unterkategorie.
3. Bestimmen Sie die Regel `preference group`: Identifizieren Sie die `preference group` für die Regel, indem Sie die Überschriften zu den Voreinstellungen [hier](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules) durchlesen.
   - Wenn die Regel bekannte, zugeordnete Codeformatoptionen aufweist, stimmt die Voreinstellungsgruppe mit der in der Deklaration der Codeformatoptionen angegebenen `OptionGroup` überein.
   - Andernfalls bestimmen Sie, ob die Regel zu einer bestehenden Voreinstellungsgruppe gehört oder eine neue Voreinstellungsgruppe benötigt.
4. Hinzufügen einer Regeldokumentation:
   1. Klonen Sie eine vorhandene IDE-Regeldatei unter dem [Stammordner](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules), z. B. `ide0011.md`, und benennen Sie sie um.
   2. Aktualisieren Sie den Inhalt der Datei entsprechend.
5. Fügen Sie in den folgenden Tabellen einen Eintrag für die IDE-Regel und/oder Codeformatoptionen hinzu:
   - In der [Inhaltsverzeichnis](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml)-Datei unter der Unterkategorie der Regel und der Voreinstellungsliste. Suchen Sie z. B. für eine IDE-Codeformatregel mit der Unterkategorie `Language` und der Gruppe `Modifier preferences` nach dem Begriff `- name: Language rules` und einem untergeordneten Knoten `- name: Modifier preferences` in der Datei, und fügen Sie der Liste einen Eintrag hinzu. Wenn entweder die Liste der Unterkategorien oder die Voreinstellungsliste unter der Unterkategorie nicht vorhanden ist, erstellen Sie eine neue Liste unter `- name: Code style rules`.
   - In der [auf der Codeformatoption basierende Indexdatei](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/language-rules.md).
   - In der [auf der Regel-ID basierenden Indexdatei](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/index.md).
   - In der auf `preferences group` basierenden Regelindexdatei:
     1. Identifizieren Sie die auf Voreinstellungsgruppen basierende Indexdatei unter [Stammordner](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules). Bei einer IDE-Regel für `Modifier preferences` erhält diese Datei z. B. den Namen `modifier-preferences.md`. Wenn keine vorhanden ist, erstellen Sie eine neue auf der Voreinstellungsgruppe basierende Indexdatei durch Klonen einer vorhandenen Datei.
     2. Fügen Sie in dieser Datei einen Eintrag für die Regel-ID hinzu.

> [!TIP]
> Führen Sie eine Repositorysuche im `dotnet/docs`-Repository nach einer bekannten, bestehenden IDE-Regel und/oder Codeformatoptionen durch, um potenzielle Speicherorte zu identifizieren, die möglicherweise einer Aktualisierung bedürfen. Beispielsweise unter <https://github.com/dotnet/docs/search?q=IDE0011> und <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>.

## <a name="see-also"></a>Siehe auch

- [Mitwirken an den Repositorys der .NET-Dokumentation](dotnet-contribute.md)
