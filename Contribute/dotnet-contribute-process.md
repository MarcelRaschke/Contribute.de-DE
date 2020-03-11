---
title: Mitwirken an Repositorys der .NET-Dokumentation
description: In diesem Artikel erhalten Sie eine Einführung in das Mitwirken an den Repositorys der .NET-Dokumentation. Sie lernen die verwendeten Repositorys, die Vorgehensweise für das Ordnen von Inhalten und die Richtlinien für das Verwalten von Codebeispielen und anderen Ressourcen kennen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 161f831bf3f31428f78d3a828b12b4c9ecaffb0e
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331763"
---
# <a name="process-for-contributing-to-net-docs"></a>Mitwirken an der .NET-Dokumentation

Wir schätzen Beiträge zur Dokumentation, die aus der Community kommen. Im Folgenden sind einige Leitlinien aufgelistet, die Sie beachten sollten, wenn Sie an der .NET-Dokumentation mitwirken:

- **Keine** unvermittelten großen Pull Requests. Eröffnen Sie stattdessen ein Issue, und beginnen Sie eine Diskussion, sodass sich die Teilnehmer auf eine Richtung einigen können, bevor Sie viel Zeit investieren.
- **Befolgen Sie** diese Anweisungen und die Richtlinien für [Sprache und Stil](dotnet-voice-tone.md).
- **Verwenden Sie** die [Vorlage](dotnet-style-guide.md) als Ausgangspunkt für Ihre Arbeit.
- **Erstellen Sie** einen separaten Branch in Ihrer Fork, bevor Sie an einem Artikel arbeiten.
- **Befolgen Sie** den [Workflow für GitHub Flow](https://guides.github.com/introduction/flow/).
- **Bloggen oder twittern Sie** regelmäßig über Ihre Beiträge.

Durch diese Richtlinien wird der Ablauf für Sie und für uns erleichtert.

## <a name="make-a-contribution-to-net-docs"></a>So tragen Sie zur .NET-Dokumentation bei

**Schritt 1:** Überspringen Sie diesen Schritt, wenn es sich um kleine Änderungen handelt. Wenn Sie neue Inhalte erstellen oder bestehenden Inhalt überprüfen, öffnen Sie ein [Issue](https://github.com/dotnet/docs/issues), in dem Sie beschreiben, was Sie vorhaben.

Der Inhalt im Ordner **docs** ist in Abschnitte unterteilt, die im Inhaltsverzeichnis erfasst werden. Definieren Sie, wo im Inhaltsverzeichnis sich das Thema befinden soll. Holen Sie Feedback zu Ihrem Vorschlag ein.

Alternative:

Sie können ein bestehendes Issue auswählen, für das Beiträge aus der Community gewünscht werden. Unter [Projects for .NET Community contributors (Projekte für Mitwirkende aus der .NET-Community)](https://github.com/dotnet/docs/projects/35) finden Sie viele Issues, die für Mitwirkende aus der Community verfügbar sind. Je nachdem, was Sie interessiert und wie viel Zeit Sie investieren möchten, können Sie Issues aus folgenden Kategorien auswählen:

- **Korrekturen:** Zu dieser Kategorie zählen einfache Beiträge, z.B. das Korrigieren von fehlerhaften Links, das Hinzufügen von fehlenden Codebeispielen oder das Beheben von Problemen mit beschränktem Inhalt. Manchmal können diese Probleme viele Dateien betreffen. In diesem Fall sollten Sie uns darüber informieren, woran Sie arbeiten möchten, bevor Sie damit beginnen. Fügen Sie einen Kommentar zum Issue hinzu, um uns mitzuteilen, dass Sie daran arbeiten.

- **Inhaltsaktualisierung:** Durch die Größe der Dokumentation kann der Inhalt schnell veralten und muss überprüft werden. Außerdem sind manche Inhalte doppelt oder dreifach vorhanden. Beim Aktualisieren des Inhalts müssen Sie sicherstellen, dass einzelne Artikel aktuell sind oder den Inhalt in einem Featurebereich überprüfen, um Duplizierungen zu entfernen und sicherzustellen, dass einmaliger Inhalt in der kleineren Dokumentation beibehalten wird.

- **Erstellen neuer Inhalte:** Wenn Sie einen neuen Artikel erstellen möchten, finden Sie in diesen Issues die Themen, von denen bekannt ist, dass sie in einem Docset noch fehlen. Sie sollten uns allerdings mitteilen, dass Sie an einem Artikel arbeiten möchten, bevor Sie damit beginnen. Wenn Sie einen Artikel erstellen möchten, der nicht aufgeführt ist, eröffnen Sie ein Issue.

Sie können ebenfalls die Liste [open issues (Offene Issues)](https://github.com/dotnet/docs/issues) ansehen und an einem Issue mitwirken, der Sie interessiert. Mit der Bezeichnung [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) werden Issues gekennzeichnet, an denen die Community mitwirken kann. Für diese ist normalerweise nicht viel Kontext erforderlich, wodurch sie für den Einstieg gut geeignet sind. Erfahrenen Mitwirkenden aus der Community wird empfohlen, die Issues durchzugehen, die für sie von Interesse sind. Wenn Sie ein entsprechendes Issue finden, fügen Sie einen Kommentar hinzu, um zu fragen, ob es noch offen ist.

Sobald Sie einen Artikel ausgewählt haben, an dem Sie arbeiten möchten, befolgen Sie den [Leitfaden für die ersten Schritte](get-started-setup-github.md), um ein GitHub-Konto zu erstellen und Ihre Umgebung einzurichten.

**Schritt 2:** Forken Sie nach Bedarf die Repositorys `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` oder `dotnet/ml-api-docs`, und erstellen Sie einen Branch für Ihre Änderungen.

Wenn Sie nur kleine Änderungen vornehmen müssen, finden Sie die entsprechenden Anweisungen für das Bearbeiten in GitHub auf der [Startseite](index.md#quick-edits-to-existing-documents) des Leitfadens für Mitwirkende.

**Schritt 3:** Nehmen Sie Änderungen an diesem neuen Branch vor.

Wenn es sich um einen neuen Artikel handelt, können Sie diese [Vorlage](dotnet-style-guide.md) als Ausgangspunkt verwenden. Diese enthält die Richtlinien für das Schreiben und erläutert die Metadaten, die für jeden Artikel erforderlich sind, z.B. Informationen zum Autor.

Navigieren Sie zu dem Ordner, der der Position im Inhaltsverzeichnis entspricht, die Sie in Schritt 1 für Ihren Artikel festgelegt haben. Dieser Ordner enthält die Markdowndateien für alle Artikel in diesem Abschnitt. Erstellen Sie bei Bedarf einen neuen Ordner, in dem Sie die Dateien speichern können, aus denen Ihr Inhalt besteht. Der Hauptartikel für diesen Abschnitt heißt *index.md*. Erstellen Sie für Bilder und andere statische Ressourcen einen Unterordner namens **media** in dem Ordner, der Ihren Artikel enthält (falls noch nicht vorhanden). Erstellen Sie im Ordner **media** einen Unterordner mit dem Namen des Artikels (außer für die Indexdatei). Beispielcode sollte sich im Repository `dotnet/samples` befinden. Dies wird im Abschnitt zu [Beispielen](#contributing-to-samples) erläutert.

Stellen Sie sicher, dass Sie die richtige Markdownsyntax verwenden. Beispiele zu bewährten Methoden finden Sie im [Spickzettel zu Vorlagen und Markdown](dotnet-style-guide.md).

## <a name="example-structure"></a>Beispielstruktur

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**Schritt 4:** Senden Sie einen Pull Request (PR) von Ihrem Branch zum Masterbranch.

> [!IMPORTANT]
> Die [Kommentarautomatisierung](how-to-write-workflows-major.md#review-and-sign-off) ist derzeit nicht für die Repositorys für die .NET-Dokumentation verfügbar. Die Mitglieder des Teams für die .NET-Dokumentation überprüfen und mergen Ihren Pull Request.

Jeder Pull Request sollte in der Regel nur ein Problem beheben. Mit einem Pull Request können eine oder mehrere Dateien geändert werden. Wenn Sie mehrere Probleme in verschiedenen Dateien beheben, sollten Sie mehrere Pull Requests erstellen. Wenn Sie Beispiele erstellen und Markdown aktualisieren, müssen Sie für die Beispiele einen separaten Pull Request erstellen.

Wenn Ihr Pull Request ein vorhandenes Problem behebt, fügen Sie das Schlüsselwort `Fixes #Issue_Number` zur Commitnachricht oder zur Beschreibung des Pull Requests hinzu. Dadurch wird das Issue automatisch geschlossen, wenn der Pull Request gemerget wurde. Weitere Informationen finden Sie unter [Closing issues via commit messages (Schließen von Issues über Commitnachrichten)](https://help.github.com/articles/closing-issues-via-commit-messages/).

Das .NET-Team überprüft Ihren Pull Request anschließend und teilt Ihnen mit, ob weitere Änderungen nötig sind, um diesen zu genehmigen.

**Schritt 5:** Nehmen Sie gemäß der Absprache mit dem Team die erforderlichen Änderungen an Ihrem Branch vor.

Die Verwalter mergen Ihren Pull Request in den Masterbranch, sobald das Feedback umgesetzt und die Änderung genehmigt wurde.

Wir pushen alle Commits an den Masterbranch regelmäßig in den Livebranch. Dann können Sie Ihren Beitrag unter https://docs.microsoft.com/dotnet/ ansehen. Diese Veröffentlichungen finden werktags in der Regel täglich statt. Durch Wartungsaktivitäten können sich diese jedoch um einige Tage verzögern.

## <a name="contributing-to-samples"></a>So tragen Sie zu den Beispielen bei

Das Repository [dotnet/samples](https://github.com/dotnet/samples) enthält den Beispielcode für alle Artikel in der .NET-Dokumentation. Es gibt einige verschiedene Projekte, die in Unterordnern organisiert sind. Die Organisation dieser Unterordner ähnelt der Organisation der Dokumente für die .NET-Dokumentation.

Der Code in unserem Repository wird folgendermaßen kategorisiert:

- Samples (Beispiele): Leser können die Beispiele herunterladen und ausführen. Bei den Beispielen sollte es sich immer um vollständige Anwendungen oder Bibliotheken handeln. Wenn ein Beispiel eine Bibliothek erstellt, sollte dieses Komponententests oder eine Anwendung enthalten, mit denen der Leser den Code ausführen kann. Häufig werden mehrere Technologien, Features oder Toolkits verwendet. Die Datei „readme.md“ für jedes Beispiel verweist auf den Artikel, sodass Sie sich über die Konzepte informieren können, mit denen sich die Beispiele befassen.
- Snippets (Codeausschnitte): Diese stellen weniger umfangreiche Konzepte oder Tasks dar. Sie können zwar kompiliert werden, sind jedoch keine vollständigen Anwendungen. Sie sollten ordnungsgemäß ausgeführt werden können, sind jedoch keine Beispielanwendungen für ein bestimmtes Szenario. Codeausschnitte sollen so klein wie möglich sein, um ein einzelnes Konzept oder Feature zu veranschaulichen. Dabei sollte nicht mehr Code enthalten sein, als auf einen üblichen Bildschirm passt.

Der Code befindet sich im Repository [dotnet/samples](https://github.com/dotnet/samples). Wir arbeiten an einer Lösung, damit die Struktur des Ordners „samples“ zukünftig der Struktur des Ordners „docs“ entspricht. Es gibt folgende Standards zu beachten:

- Der Ordner *snippets* auf oberster Ebene enthält Codeausschnitte für kleine, präzise Beispiele.
- Beispiele für API-Referenzen werden in einem Ordner gespeichert, der folgendem Muster entspricht: *snippets/\<Sprache>/api/\<Namespace>/\<API-Name>* .
- Die anderen Ordner auf oberster Ebene entsprechen den Ordnern, die sich im Repository *docs* auf oberster Ebene befinden. Das Repository „docs“ enthält beispielsweise den Ordner *machine-learning/tutorials*, und die Beispiele für diese Tutorials für das maschinelle Lernen befinden sich im Ordner *samples/machine-learning/tutorials*.

Außerdem sollten alle Beispiele, die sich in den Ordnern *core* und *standard* befinden, auf allen Plattformen, die .NET Core unterstützt, erstellt und ausgeführt werden können. Dies wird durch unser CI-Buildsystem erzwungen. Der Ordner *framework* auf oberster Ebene enthält Beispiele, die nur unter Windows erstellt und überprüft werden.

Beispielprojekte sollten dem Szenario entsprechend auf so vielen Plattformen wie möglich ausgeführt können. In der Praxis bedeutet das, dass Sie nach Möglichkeit auf .NET Core basierende Konsolenanwendungen erstellen sollten. Beispielen, die für Web- oder Benutzeroberflächenframeworks gelten, sollten diese Tools bei Bedarf hinzugefügt werden. Dazu zählen unter anderem Webanwendungen, mobile Apps und WPF- oder WinForms-Apps.

Wir arbeiten an einem CI-System für jeden Code. Wenn Sie Beispiele aktualisieren, sollten Sie sicherstellen, dass jedes Update Teil eines erstellbaren Projekts ist. Fügen Sie den Beispielen im Idealfall auch Tests auf Richtigkeit hinzu.

Jedes vollständige Beispiel sollte die Datei *readme.md* enthalten. In dieser Datei sollte eine kurze Beschreibung des Beispiels enthalten sein (ein bis zwei Absätze). Die Datei *readme.md* soll den Lesern vermitteln, was sie durch dieses Beispiel lernen können. Die Datei *readme.md* sollte ebenfalls einen Link zur Dokumentation auf der Website der [.NET-Dokumentation](https://docs.microsoft.com/dotnet/welcome) enthalten. Wenn Sie festlegen möchten, wo eine bestimmte Datei im Repository dieser Website zugeordnet wird, ersetzen Sie `/docs` im Repositorypfad durch `https://docs.microsoft.com/dotnet`.

Ihr Artikel sollte zudem Links zum Beispiel enthalten. Der Link sollte direkt zu dem Ordner auf GitHub führen, in dem sich das Beispiel befindet.

### <a name="writing-a-new-snippet-or-sample"></a>Schreiben eines neuen Codeausschnitts oder Beispiels

1. Ihr Beispiel **muss Teil eines erstellbaren Projekts sein**. Die Projekte sollten nach Möglichkeit auf allen Plattformen erstellt werden können, die von .NET Core unterstützt werden. Davon ausgenommen sind Beispiele, die plattformspezifische Features oder Tools veranschaulichen.

2. Ihr Beispiel sollte aus Gründen der Konsistenz dem [corefx-Codierungsstil](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) entsprechen.

    - Zudem sollten Sie `static`-Methoden anstelle von Instanzmethoden verwenden, wenn Sie etwas veranschaulichen möchten, für das die Instanziierung von Objekten nicht erforderlich ist.

3. Ihre Beispiele sollten eine **angemessene Ausnahmebehandlung** umfassen. Diese sollte alle Ausnahmen behandeln, die im Kontext des Beispiels wahrscheinlich ausgelöst werden. In ein Beispiel, in dem die Methode [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) aufgerufen wird, um die Benutzereingabe abzurufen, sollte beispielsweise eine angemessene Ausnahmebehandlung eingefügt werden, die verwendet werden kann, wenn die Eingabezeichenfolge als Argument an eine Methode übergeben wird. Wenn ihr Beispiel erwartet, dass ein Methodenaufruf fehlschlägt, muss ebenfalls die Ausnahme behandelt werden, die ausgelöst wird. Sie sollten immer die Ausnahmen behandeln, die von der Methode ausgelöst werden, nicht die Ausnahmen der Basisklassen wie [Exception](https://docs.microsoft.com/dotnet/api/system.exception) oder [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. Wenn Ihr Beispiel ein eigenständiges Paket erstellt, müssen Sie die Runtimes einfügen, die von unserem CI-Buildsystem verwendet werden, und alle Runtimes, die von Ihrem Beispiel verwendet werden:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

Bald ist ein CI-System verfügbar, um diese Projekte zu erstellen.

So erstellen Sie ein Beispiel:

1. Eröffnen Sie ein [Issue](https://github.com/dotnet/docs/issues), oder fügen Sie einen Kommentar zu einem vorhandenen Issue hinzu, der aussagt, dass Sie an diesem arbeiten.
2. Schreiben Sie einen Artikel, der die Konzepte erläutert, die in Ihrem Beispiel veranschaulicht werden (z.B. `docs/standard/linq/where-clause.md`).
3. Schreiben Sie Ihr Beispiel (z.B. `WhereClause-Sample1.cs`).
4. Erstellen Sie die Datei „Program.cs“ mit einem Haupteinstiegspunkt, der Ihr Beispiel aufruft. Wenn diese bereits vorhanden ist, fügen Sie den Aufruf zum Beispiel hinzu:

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

Codeausschnitte oder Beispiele für .NET Core werden mithilfe der .NET Core-CLI erstellt, die mit dem [.NET Core SDK](https://www.microsoft.com/net/download) installiert werden kann. So können Sie ein Beispiel erstellen und ausführen:

1. Navigieren Sie zum Ordner des Beispiels, und führen Sie „dotnet build“ aus, um diesen auf Fehler zu überprüfen:

    ```console
    dotnet build
    ```
2. Führen Sie Ihr Beispiel aus:

    ```console
    dotnet run
    ```

3. Fügen Sie die Datei „readme.md“ zum Stammverzeichnis Ihres Beispiels hinzu.

   Diese sollte eine kurze Beschreibung des Codes und einen Verweis auf den Artikel enthalten, zu dem das Beispiel gehört.

Wenn es nicht anders angegeben ist, werden alle Beispiele auf von .NET Core unterstützten Plattformen über die Befehlszeile erstellt. Es gibt einige Beispiele, die speziell für Visual Studio erstellt wurden. Für diese ist Visual Studio 2017 oder höher erforderlich. Außerdem behandeln einige Beispiele plattformspezifische Features. Für diese ist eine bestimmte Plattform erforderlich. Andere Beispiele und Codeausschnitte werden unter Windows ausgeführt und benötigen .NET Framework sowie das Developer Pack für die Zielversion des Frameworks.

## <a name="the-c-interactive-experience"></a>Die interaktive C#-Benutzeroberfläche

Für alle Beispiele, die in einem Artikel enthalten sind, wird ein [Sprachtag](code-in-docs.md) verwendet, um die Quellsprache anzugeben. Für kurze Codebeispiele in C# kann das Sprachtag `csharp-interactive` verwendet werden, um ein C#-Beispiel anzugeben, das im Browser ausgeführt wird. (Für Inlinecodebeispiele wird das Tag `csharp-interactive` verwendet und für Codebeispiele, die über die Quelle hinzugefügt werden, das Tag `code-csharp-interactive`.) Diese Codebeispiele stellen im Artikel ein Codefenster und ein Ausgabefenster dar. Das Ausgabefenster zeigt die Ausgabe an, die aus dem interaktiven Code entsteht, sobald der Benutzer das Beispiel ausgeführt hat.

Durch die interaktive C#-Benutzeroberfläche wird das Arbeiten mit Beispielen verändert und verbessert. Leser können das Beispiel ausführen, um die Ergebnisse anzuzeigen. Es gibt einige Faktoren, anhand derer Sie entscheiden können, ob das Beispiel oder der zugehörige Text Informationen zur Ausgabe enthalten sollte.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Wann die erwartete Ausgabe ohne Ausführung des Beispiels erkennbar sein sollte

- In Artikeln für Einsteiger sollte die Ausgabe enthalten sein, sodass die Leser die Ausgabe Ihres Codes mit der erwarteten Ausgabe vergleichen können.
- In Beispielen, bei denen die Ausgabe eine wichtige Rolle für den Artikel spielt, sollte diese enthalten sein. Bei Artikeln über formatierten Text sollte das Textformat ersichtlich sein, ohne das Beispiel auszuführen.
- Wenn das Beispiel und die erwartete Ausgabe kurz sind, sollten Sie die Ausgabe ebenfalls einfügen. Das spart dem Leser etwas Zeit.
- In Artikeln, die thematisieren, wie die aktuelle Kultur oder invariante Kultur sich auf die Ausgabe auswirken, sollte die erwartete Ausgabe erläutert werden. Die interaktive REPL (read–eval–print-Loop) wird auf einem Linux-basierten Host ausgeführt. Die Standardkultur und die invariante Kultur erzeugen auf unterschiedlichen Betriebssystemen und Computern verschiedene Ausgaben. Die Ausgabe sollte in solchen Artikeln für Windows-, Linux- und Mac-Systeme erläutert werden.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Wann die erwartete Ausgabe nicht im Beispiel enthalten sein sollte

- Bei Artikeln mit einem Beispiel, das eine große Ausgabe generiert, sollte diese nicht in den Kommentaren enthalten sein. Der Code wird dadurch unübersichtlich, sobald das Beispiel ausgeführt wurde.
- Bei Artikeln mit einem Beispiel, das ein Thema veranschaulicht, bei dem die Ausgabe für das Verständnis nicht relevant ist. Wenn beispielsweise Code enthalten ist, der eine LINQ-Abfrage ausführt, um die Syntax von Abfragen zu veranschaulichen, muss nicht jedes in der Ausgabe vorhandene Element aufgeführt werden.

> [!NOTE]
> Sie werden feststellen, dass einige Artikel den hier ausgeführten Richtlinien nicht entsprechen. Wir arbeiten an der Konsistenz der Website. Hier finden Sie die Liste der [offenen Issues](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22), die derzeit auf diesen Punkt überprüft werden.

## <a name="contributor-license-agreement"></a>Lizenzvereinbarung für Mitwirkende

Sie müssen die [Lizenzvereinbarung der .NET Foundation für Mitwirkende (Contribution License Agreement, CLA)](https://cla.dotnetfoundation.org) unterschreiben, bevor Ihr Pull Request gemergt wird. Für Projekte der .NET Foundation ist dies nur einmalig nötig. Weitere Informationen zu [Lizenzvereinbarungen für Mitwirkende (Contribution License Agreement, CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) finden Sie auf Wikipedia.

Hier finden Sie die Lizenzvereinbarung: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

Sie müssen diese nicht im Voraus unterschreiben. Sie können Ihren Pull Request wie gewohnt klonen, forken und senden. Wenn Ihr Pull Request erstellt wird, wird dieser von einem CLA-Bot klassifiziert. Wenn es sich nur um eine geringfügige Änderung handelt (z.B. das Korrigieren eines Tippfehlers), wird der Pull Request mit `cla-not-required` gekennzeichnet. Andernfalls wird er als `cla-required` klassifiziert. Sobald Sie die Lizenzvereinbarung für Mitwirkende (CLA) unterschrieben haben, werden alle aktuellen und zukünftigen Pull Requests als `cla-signed` gekennzeichnet.
