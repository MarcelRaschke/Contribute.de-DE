---
title: Roadmap für Bezeichnungen und Projekte
description: In diesem Artikel wird erläutert, wie Bezeichnungen und Projekte im dotnet/docs-Repository verwendet werden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760374"
---
# <a name="labels-and-projects-roadmap"></a>Roadmap für Bezeichnungen und Projekte

Das .NET-Dokumentationsteam macht umfassend Gebrauch von [GitHub-Bezeichnungen](https://github.com/dotnet/docs/labels), um die Arbeit zu organisieren. Indem wir nach Bezeichnungen filtern, können wir uns schnell auf wichtige Bereiche auf der [.NET-Dokumentationswebsite](https://docs.microsoft.com/dotnet) konzentrieren.

Außerdem verwenden wir [GitHub-Projekte](https://github.com/dotnet/docs/projects), um Sprints und andere zielorientierte Epics zu organisieren.

In dieser Roadmap wird erläutert, wie wir diese Organisationstools nutzen. Zudem sind Links zu praktischen Filtern enthalten, mit denen wir nach relevanten Bereichen suchen.

## <a name="labels"></a>Bezeichnungen

Wenn Sie zum ersten Mal an [dotnet/docs](https://github.com/dotnet/docs) mitwirken, sollten Sie mit den [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-Issues beginnen. Diese Issues haben bereits einen klaren Umfang. Sie sind gut für Ihren ersten Beitrag geeignet. In der up-for-grabs-Ansicht können Sie die Issues weiter nach Bereich und Priorität filtern. Wir haben für Einsteiger geeignete Issues mit [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) gekennzeichnet, falls Sie sich zunächst an einem kleineren Beitrag versuchen möchten.

Wir verwenden Bezeichnungen, um Issues unter anderem nach folgenden Kriterien zu klassifizieren:

- [.NET-Leitfäden](#find-a-single-net-guide) und [Abschnitte eines Leitfadens](#search-one-section-of-a-guide)
- [Zielrelease](#releases)
- [Priorität](#priority)

Sie können eine Bezeichnung jeder Kategorie (Leitfaden, Release, Priorität) kombinieren, um Ihren Fokus für Issues zu präzisieren, an denen Sie arbeiten möchten.

### <a name="find-a-single-net-guide"></a>Suchen eines einzelnen .NET-Leitfadens

Für verwenden Bezeichnungen für jedes Architektur-E-Book und jeden .NET-Leitfaden.

![„:book: guide“ auf hellgrünem Hintergrund](./media/labels-projects/guide.png "Präfix für Bezeichnungen für Architekturleitfäden")

Architektur-E-Books erkennen Sie am Präfix `:book: guide` und einem hellgrünen Hintergrund. Hierbei handelt es sich um die übergeordneten Bereiche, in denen empfohlene Architekturen behandelt werden. Hier finden Sie aktuelle Issues, die nach den einzelnen .NET-Architekturleitfäden gefiltert wurden:

- [ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizing w/ Windows containers](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Serverless apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Diese Bezeichnungen werden auch auf [Leitfäden zum Frameworkentwurf](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines) angewendet. Die Bezeichnungen in diesem Bereich sind gleich gestaltet, es wird jedoch von PRs aus der Community abgeraten. Dieses Material wird mit Genehmigung neu herausgegeben und sollte nicht bearbeitet werden.

![„:books: Area“ auf dunkelblauem Hintergrund](./media/labels-projects/area.png "Präfix für Bezeichnungen für .NET-Leitfäden")

.NET-Leitfäden erkennen Sie am Präfix `:books: Area` und einem dunkelblauen Hintergrund. Hier finden Sie aktuelle Issues, die nach den einzelnen .NET-Leitfäden gefiltert wurden:

- [API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Desktop Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) (wird möglicherweise entfernt)
- [.NET Core Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) (wird möglicherweise entfernt)
- [Visual Basic Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Durchsuchen eines Abschnitts eines Leitfadens

![„:card_file_box: Area“ auf hellblauem Hintergrund](./media/labels-projects/technology.png "Präfix für Bezeichnungen für Unterbereiche von .NET-Leitfäden")

Die .NET-Leitfäden sind sehr umfangreich, deshalb schränken diese Bezeichnungen den Umfang nach Abschnitt eines Leitfadens ein. Unterbereiche eines .NET-Leitfadens erkennen Sie am Präfix `:card_file_box: Technology` und einem hellblauen Hintergrund. Viele dieser Bezeichnungen gelten für mehrere Leitfäden, während andere in nur einem Leitfaden aufgeführt sind. Wenn Sie nach einem Bereich gefiltert haben, können Sie eine dieser Bezeichnungen hinzufügen, um den Bereich der Issues weiter einzugrenzen.

- AppCompat
- Async Task
- C# Advanced concepts
- C# compiler
- C# Fundamentals
- C# Get Started
- C# Language Reference
- C# Null safety
- C# What's new
- CLI
- Data Access
- Docker
- Installers
- LINQ
- NCL
- .NET Standard
- Roslyn APIs
- Sicherheit
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Releases

![„:checkered_flag: Release:“ auf dunkelgelbem Hintergrund](./media/labels-projects/release.png "Präfix für Bezeichnungen für Releases")

Issues, die für ein bestimmtes Release gekennzeichnet sind, erkennen Sie am Präfix `:checkered_flag: Release:` und einem dunkelgelben Hintergrund.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Priorität

Prioritätsbezeichnungen weisen das Format `P` gefolgt von einer einzelnen Ziffer auf. Je niedriger die Zahl, desto höher die Priorität:

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>Weitere Bezeichnungen

Es gibt viele weitere Bezeichnungen, die von den Inhaltsteams verwendet werden, um unterschiedliche Klassifizierungen für Issues zu verwalten. Wenn Sie kein Mitglied des Inhaltsteams sind, können Sie diese anderen Bezeichnungen ignorieren.

## <a name="projects"></a>Projekte

Projekte werden auf diese beiden Arten verwendet:

- Projekttypen nach „Monat JJJJ“: Dabei handelt es sich um Scrum-Boards für den Arbeitsplan jedes Monats.
- Epics mit langer Laufzeit: Diese werden verwendet, um Aufgaben für ein Ziel zu organisieren, wenn die Arbeit sich über mehrere Monate erstreckt.
