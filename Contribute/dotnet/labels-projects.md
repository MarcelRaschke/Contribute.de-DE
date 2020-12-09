---
title: Erläuterung der Bezeichnungen, Projekte und Meilensteine
description: In diesem Artikel wird erläutert, wie Bezeichnungen, Projekte und Meilensteine im dotnet/docs-Repository verwendet werden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b7c6e4058d802db2e9dc391bfebc9f66b27c4023
ms.sourcegitcommit: fe12c5eef9d05fa598e326c44248c2b9c68cca12
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/07/2020
ms.locfileid: "96755444"
---
# <a name="labels-projects-and-milestones-roadmap"></a>Erläuterung der Bezeichnungen, Projekte und Meilensteine

Das .NET-Dokumentationsteam macht umfassend Gebrauch von [GitHub-Bezeichnungen](https://github.com/dotnet/docs/labels), um die Arbeit zu organisieren. Indem wir nach Bezeichnungen filtern, können wir uns schnell auf wichtige Bereiche auf der [.NET-Dokumentationswebsite](https://docs.microsoft.com/dotnet) konzentrieren. Wir könnten beispielsweise mit folgender Abfrage nach allen offenen `P1`-Issues (Priorität 1) filtern: [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).

Wir verwenden [GitHub-Projekte](https://github.com/dotnet/docs/projects), um Sprints und andere zielorientierte Epics zu organisieren. Wir verwenden auch [GitHub-Meilensteine](https://github.com/dotnet/docs/milestones), um die Arbeit nachzuverfolgen. Projekte dienen der Planung (Issues), Meilensteine der laufenden Arbeit (Pull Requests).

Diese Roadmap erläutert, wie wir diese Organisationstools verwenden und enthält Links zu praktischen Filtern, die wir verwenden, um relevante Bereiche zu finden.

## <a name="labels"></a>Bezeichnungen

Wenn Sie zum ersten Mal etwas zu [dotnet/docs](https://github.com/dotnet/docs) beitragen, sollten Sie mit den [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-Issues beginnen. Dabei handelt es sich um Issues, die sich stärker auf einen Bereich konzentrieren. Sie eignen sich besonders für Ihren ersten Beitrag. In der Ansicht „up-for-grabs“ können Sie basierend auf Bereich und Priorität nach Issues filtern. Mithilfe von [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) konnten wir Issues identifizieren, die sich für Anfänger eignen und mit denen Sie Ihren ersten kleinen Beitrag leisten können.

Wir verwenden Bezeichnungen, um Issues auf verschiedene Art und Weise zu klassifizieren:

- [.NET-Leitfäden](#find-a-single-net-guide) und [Abschnitte eines Leitfadens](#search-one-section-of-a-guide)
- [Zielrelease](#releases)
- [Priority](#priority)

Sie können eine Bezeichnung aus jedem Bereich kombinieren (guide, release, priority), um genau die Issues zu finden, an denen Sie arbeiten möchten.

### <a name="find-a-single-net-guide"></a>Suchen nach einzelnem .NET-Leitfaden

Wir verwenden Bezeichnungen für die einzelnen Architektur-E-Books und für jeden .NET-Leitfaden.

![:book: Leitfaden auf hellgrünem Hintergrund](./media/labels-projects/guide.png "Präfix für Architekturleitfadenbezeichnungen")

Architektur-E-Books enthalten das Präfix `:book: guide` und weisen einen hellgrünen Hintergrund auf. Dies sind die langen Bereiche , die empfohlene Architektur abdecken. Hier werden aktuelle Issues für die einzelnen .NET-Architekturleitfäden gefiltert.

- [ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker-Lebenszyklus](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernisieren von w/ Windows-Containern](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Serverlose Apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Diese Bezeichnung wird auch für die [Framework-Entwurfsrichtlinien](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines) angewendet. Dieser Bereich weist das gleiche Bezeichnungsdesign auf, Community-PRs wird davon aber abgeraten. Dies ist mit der Berechtigung neu gedrucktes Material und sollte nicht bearbeitet werden.

![„:books: Area“ auf dunkelblauem Hintergrund](./media/labels-projects/area.png "Präfix für .NET-Leitfadenbereichsbezeichnungen")

Jeder .NET-Leitfaden ist mit dem Präfix `:books: Area` versehen und weist einen dunkelblauen Hintergrund auf. Hier werden aktuelle Issues für die einzelnen .NET-Leitfäden gefiltert.

- [API-Referenz](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [Leitfaden für C#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Leitfaden für F#](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [Leitfaden für ML.NET](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET-Architekturleitfaden:](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) Kann entfernt werden
- [Leitfaden für .NET Core](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [Leitfaden für .NET Framework](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide (Leitfaden für .NET)](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn-API-Referenz:](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) Kann entfernt werden
- [Leitfaden für Visual Basic](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Durchsuchen eines Abschnitts eines Leitfadens

![„:card_file_box: Area“ auf hellblauem Hintergrund](./media/labels-projects/technology.png "Präfix für Unterbereichbezeichnungen in .NET-Leitfäden")

Die .NET-Leitfäden sind groß, sodass diese Bezeichnungen den Bereich durch einen Abschnitt eines Leitfadens weiter einschränken. Jeder Unterbereich eines .NET-Leitfadens ist mit dem Präfix `:card_file_box: Technology` versehen und weist einen mittelblauen Hintergrund auf. Viele dieser Bezeichnungen gelten für mehrere Leitfäden, während andere in nur einem Leitfaden aufgeführt sind. Fügen Sie nach dem Filtern nach einem Bereich eine dieser Bezeichnungen hinzu, um den Umfang des Issues weiter einzuschränken.

- AppCompat
- asynchrone Aufgabe
- erweiterte C#-Konzepte
- C#-Compiler
- C#-Grundlagen
- Erste Schritte mit C#
- C#-Programmiersprachenreferenz
- C# Null-Sicherheit
- Neuerungen in C#
- Befehlszeilenschnittstelle (CLI)
- Datenzugriff
- Docker
- Installer
- LINQ
- NCL
- .NET Standard
- Roslyn-APIs
- Sicherheit
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Releases

![„:checkered_flag: Release:“ auf dunkelgelbem Hintergrund](./media/labels-projects/release.png "Präfix für Releasebezeichnungen")

Issues, die für ein bestimmtes Release gekennzeichnet sind, werden mit dem Präfix `:checkered_flag: Release:` versehen und weisen einen dunkelgelben Hintergrund auf.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Priorität

Bei Prioritätsbezeichnungen folgt auf `P` eine einzelne Ziffer. Niedrigere Zahlen stehen für eine höhere Priorität.

- P0: kritische Priorität

  Sicherheitsissue oder aus Compliancegründen gesetzlich vorgeschrieben. Wir kümmern uns mit oberster Priorität um eine Lösung.
  
- P1: hohe Priorität

  Essenziell für gängige Szenarien oder ein auffälliger Fehler in einem häufig aufgerufenen Artikel. Solche Issues korrigieren wir, bevor wir an P2- oder P3-Issues arbeiten.
  
- P2: mittlere Priorität

  Hilfreich für gängige Szenarien, aber kein Issue, das Prozesse blockiert.  Wir korrigieren solche Issues entweder schnell zwischendurch oder während im gleichen Artikel ein P1-Issue behoben wird.
  
- P3: niedrige Priorität

  Hilfreich für Grenzfälle, einfache Korrekturen für gängige Szenarien, nicht sehr häufig aufgerufene Artikel oder veraltete Technologien. Solche Korrekturen überlassen wir Communitybeiträgen. Ein P3-Issue kann geschlossen werden, wenn nach zwei Monaten keine Reaktion erfolgt ist.

### <a name="what-about-the-other-labels"></a>Weitere Bezeichnungen

Es gibt viele andere Bezeichnungen, die von den Inhaltsteams verwendet werden, um unterschiedliche Klassifizierungen von Issues zu verwalten. Wenn Sie nicht Teil des Inhaltsteams sind, können Sie diese anderen Bezeichnungen ignorieren.

## <a name="projects"></a>Projekte

Projekte dienen Planungszwecken, und die priorisierten Arbeitsaufgaben sind dabei über ein Kanban-Board automatisiert. Projekte dürfen immer nur GitHub-Issues enthalten, _niemals_ Pull Requests. In dieser Beziehung unterscheiden sich Projekte von Meilensteinen: Meilensteine enthalten nur Pull Requests.

Projekte werden auf diese beiden Arten verwendet:

- Projekte vom Typ `Month YYYY`: Dies sind Kanban-Boards für den Arbeitsplan jedes einzelnen Monats.
  - Beispiele: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) usw.
- Epics mit langer Laufzeit: Diese werden verwendet, um Aufgaben für ein Ziel zu organisieren, wenn die Arbeit sich über mehrere Monate erstreckt.
  - Beispiele: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) usw.

## <a name="milestones"></a>Meilensteine

Meilensteine folgen in der Regel derselben Namenskonvention wie Projekte (`Month YYYY`), unterscheiden sich aber von Projekten. Meilensteine dienen zum Nachverfolgen abgeschlossener Arbeitsaufgaben. Meilensteine dürfen _keine_ Issues (potenzielle Arbeitsaufgaben) enthalten, sondern ausschließlich Pull Requests. Der aktuelle Meilenstein wird automatisch auf neue Pull Requests angewendet.
