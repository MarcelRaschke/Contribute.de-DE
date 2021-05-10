---
title: Erläuterung der Bezeichnungen, Projekte und Meilensteine
description: In diesem Artikel wird erläutert, wie Bezeichnungen, Projekte und Meilensteine im dotnet/docs-Repository verwendet werden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 02/10/2021
ms.openlocfilehash: e053f09f7502cbe6f711488959de910298d3a456
ms.sourcegitcommit: f9a92d1cc70e46fae100dbc698e1d2196e0df7c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "100335739"
---
# <a name="labels-projects-and-milestones-roadmap"></a>Erläuterung der Bezeichnungen, Projekte und Meilensteine

Das .NET-Dokumentationsteam macht umfassend Gebrauch von [GitHub-Bezeichnungen](https://github.com/dotnet/docs/labels), um die Arbeit zu organisieren. Indem wir nach Bezeichnungen filtern, können wir uns schnell auf wichtige Bereiche auf der [.NET-Dokumentationswebsite](https://docs.microsoft.com/dotnet) konzentrieren. Sie könnten beispielsweise mit der Abfrage [is:issue is:open label:"dotnet-architecture/prod"](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) nach allen offenen Issues für Architekturleitfäden filtern.

Wir verwenden [GitHub-Projekte](https://github.com/dotnet/docs/projects), um Sprints und andere zielorientierte Epics zu organisieren. Wir verwenden auch [GitHub-Meilensteine](https://github.com/dotnet/docs/milestones), um die Arbeit nachzuverfolgen. Projekte dienen der Planung (Issues), Meilensteine der laufenden Arbeit (Pull Requests).

Diese Roadmap erläutert, wie wir diese Organisationstools verwenden und enthält Links zu praktischen Filtern, die wir verwenden, um relevante Bereiche zu finden.

## <a name="labels"></a>Bezeichnungen

Wenn Sie zum ersten Mal etwas zu [dotnet/docs](https://github.com/dotnet/docs) beitragen, sollten Sie mit den [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-Issues beginnen. Dabei handelt es sich um Issues, die sich stärker auf einen Bereich konzentrieren. Sie eignen sich besonders für Ihren ersten Beitrag. In der Ansicht „up-for-grabs“ können Sie basierend auf Bereich und Priorität nach Issues filtern. Mithilfe von [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) konnten wir Issues identifizieren, die sich für Anfänger eignen und mit denen Sie Ihren ersten kleinen Beitrag leisten können.

Wir verwenden Bezeichnungen, um Issues auf verschiedene Art und Weise zu klassifizieren:

- [.NET-Leitfäden](#find-issues-for-a-single-net-guide) und [Abschnitte eines Leitfadens](#find-issues-for-one-section-of-a-guide)
- [Zielrelease](#releases)
- [Priority](#priority)

Sie können eine Bezeichnung aus jedem Bereich kombinieren (guide, release, priority), um genau die Issues zu finden, an denen Sie arbeiten möchten.

### <a name="find-issues-for-a-single-net-guide"></a>Ermitteln von Issues für einen .NET-Leitfaden

Wir verwenden Bezeichnungen für die einzelnen Architektur-E-Books und für jeden .NET-Leitfaden. Alle E-Books werden mit der Bezeichnung [dotnet-architecture/prod](https://github.com/dotnet/docs/labels/dotnet-architecture%2Fprod) versehen. Jedes E-Book verfügt über eine eindeutige Bezeichnung, die mit `/tech` endet.

.NET-Leitfäden erkennen Sie am Suffix [`/prod`](https://github.com/dotnet/docs/labels?q=prod) und einem blaugrauen Hintergrund. Hier werden aktuelle Issues für die einzelnen .NET-Leitfäden gefiltert.

- [.NET-Leitfaden: `dotnet/prod`](https://github.com/dotnet/docs/labels/dotnet%2Fprod)
- [Leitfaden für .NET-Grundlagen (zuvor .NET Standard-Leitfaden): `dotnet-fundamentals/prod`](https://github.com/dotnet/docs/labels/dotnet-fundamentals%2Fprod)
- [Leitfaden für .NET-Grundlagen (zuvor .NET Core-Leitfaden): `dotnet-core/prod`](https://github.com/dotnet/docs/labels/dotnet-core%2Fprod)
- [.NET Framework-Leitfaden: `dotnet-framework/prod`](https://github.com/dotnet/docs/labels/dotnet-framework%2Fprod)
- [API-Referenz: `dotnet-api/prod`](https://github.com/dotnet/docs/labels/dotnet-api%2Fprod)
- [C#-Leitfaden: `dotnet-csharp/prod`](https://github.com/dotnet/docs/labels/dotnet-csharp%2Fprod)
- [F#-Leitfaden: `dotnet-fsharp/prod`](https://github.com/dotnet/docs/labels/dotnet-fsharp%2Fprod)
- [Visual Basic-Leitfaden: `dotnet-visualbasic/prod](https://github.com/dotnet/docs/labels/dotnet-visualbasic%2Fprod)
- [ML.NET-Leitfaden: `dotnet-ml/prod`](https://github.com/dotnet/docs/labels/dotnet-ml%2Fprod)
- [Azure .NET SDK: `azure-dotnet/prod`](https://github.com/dotnet/docs/labels/azure-dotnet%2Fprod)
- [.NET for Apache Spark-Leitfaden: `dotnet-spark/prod`](https://github.com/dotnet/docs/labels/dotnet-spark%2Fprod)
- [.NET Desktop-Leitfaden: `dotnet-desktop/prod`](https://github.com/dotnet/docs/labels/dotnet-desktop%2Fprod)

Andere Produktbezeichnungen werden für Bereiche definiert, die sich in mehreren Repositorys befinden.

#### <a name="find-issues-for-one-section-of-a-guide"></a>Ermitteln von Issues für einen Abschnitt eines Leitfadens

Die .NET-Leitfäden sind groß, sodass diese Bezeichnungen den Bereich durch einen Abschnitt eines Leitfadens weiter einschränken. Unterbereiche eines .NET-Leitfadens erkennen Sie am Suffix [`/tech`](https://github.com/dotnet/docs/labels?q=tech) und einem hellblauen Hintergrund. Viele dieser Bezeichnungen gelten für mehrere Leitfäden, während andere in nur einem Leitfaden aufgeführt sind. Fügen Sie nach dem Filtern nach einem Bereich eine dieser Bezeichnungen hinzu, um den Umfang des Issues weiter einzuschränken.

### <a name="releases"></a>Releases

![„:checkered_flag: Release:“ auf dunkelgelbem Hintergrund](./media/labels-projects/release.png "Präfix für Releasebezeichnungen")

Issues mit Tags für ein bestimmtes Release erkennen Sie am Präfix [`:checkered_flag: Release:`](https://github.com/dotnet/docs/labels?q=%3Acheckered_flag%3A+Release) und einem dunkelgelben Hintergrund.

### <a name="priority"></a>Priorität

Bei Prioritätsbezeichnungen folgt auf `Pri` eine einzelne Ziffer. Niedrigere Zahlen stehen für eine höhere Priorität.

- Pri0: kritische Priorität

  Sicherheitsissue oder aus Compliancegründen gesetzlich vorgeschrieben. Wir kümmern uns mit oberster Priorität um eine Lösung.
  
- Pri1: hohe Priorität

  Essenziell für gängige Szenarien oder ein auffälliger Fehler in einem häufig aufgerufenen Artikel. Solche Issues korrigieren wir, bevor wir an P2- oder P3-Issues arbeiten.
  
- Pri2: mittlere Priorität

  Hilfreich für gängige Szenarien, aber kein Issue, das Prozesse blockiert.  Wir korrigieren solche Issues entweder schnell zwischendurch oder während im gleichen Artikel ein P1-Issue behoben wird.
  
- Pri3: niedrige Priorität

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
