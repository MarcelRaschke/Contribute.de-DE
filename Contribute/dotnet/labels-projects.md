---
title: Erläuterung der Bezeichnungen, Projekte und Meilensteine
description: In diesem Artikel wird erläutert, wie Bezeichnungen, Projekte und Meilensteine im dotnet/docs-Repository verwendet werden.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b8e9f2a33f9b4a8025aa36a890bff1017cf132c6
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559261"
---
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="a2610-103">Erläuterung der Bezeichnungen, Projekte und Meilensteine</span><span class="sxs-lookup"><span data-stu-id="a2610-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="a2610-104">Das .NET-Dokumentationsteam macht umfassend Gebrauch von [GitHub-Bezeichnungen](https://github.com/dotnet/docs/labels), um die Arbeit zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="a2610-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="a2610-105">Indem wir nach Bezeichnungen filtern, können wir uns schnell auf wichtige Bereiche auf der [.NET-Dokumentationswebsite](https://docs.microsoft.com/dotnet) konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="a2610-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="a2610-106">Wir könnten beispielsweise mit folgender Abfrage nach allen offenen `P1`-Issues (Priorität 1) filtern: [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span><span class="sxs-lookup"><span data-stu-id="a2610-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="a2610-107">Wir verwenden [GitHub-Projekte](https://github.com/dotnet/docs/projects), um Sprints und andere zielorientierte Epics zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="a2610-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="a2610-108">Wir verwenden auch [GitHub-Meilensteine](https://github.com/dotnet/docs/milestones), um die Arbeit nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="a2610-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="a2610-109">Projekte dienen der Planung (Issues), Meilensteine der laufenden Arbeit (Pull Requests).</span><span class="sxs-lookup"><span data-stu-id="a2610-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="a2610-110">Diese Roadmap erläutert, wie wir diese Organisationstools verwenden und enthält Links zu praktischen Filtern, die wir verwenden, um relevante Bereiche zu finden.</span><span class="sxs-lookup"><span data-stu-id="a2610-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="a2610-111">Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="a2610-111">Labels</span></span>

<span data-ttu-id="a2610-112">Wenn Sie zum ersten Mal etwas zu [dotnet/docs](https://github.com/dotnet/docs) beitragen, sollten Sie mit den [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-Issues beginnen.</span><span class="sxs-lookup"><span data-stu-id="a2610-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="a2610-113">Dabei handelt es sich um Issues, die sich stärker auf einen Bereich konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="a2610-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="a2610-114">Sie eignen sich besonders für Ihren ersten Beitrag.</span><span class="sxs-lookup"><span data-stu-id="a2610-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="a2610-115">In der Ansicht „up-for-grabs“ können Sie basierend auf Bereich und Priorität nach Issues filtern.</span><span class="sxs-lookup"><span data-stu-id="a2610-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="a2610-116">Mithilfe von [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) konnten wir Issues identifizieren, die sich für Anfänger eignen und mit denen Sie Ihren ersten kleinen Beitrag leisten können.</span><span class="sxs-lookup"><span data-stu-id="a2610-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="a2610-117">Wir verwenden Bezeichnungen, um Issues auf verschiedene Art und Weise zu klassifizieren:</span><span class="sxs-lookup"><span data-stu-id="a2610-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="a2610-118">[.NET-Leitfäden](#find-a-single-net-guide) und [Abschnitte eines Leitfadens](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="a2610-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="a2610-119">Zielrelease</span><span class="sxs-lookup"><span data-stu-id="a2610-119">Target release</span></span>](#releases)
- [<span data-ttu-id="a2610-120">Priority</span><span class="sxs-lookup"><span data-stu-id="a2610-120">Priority</span></span>](#priority)

<span data-ttu-id="a2610-121">Sie können eine Bezeichnung aus jedem Bereich kombinieren (guide, release, priority), um genau die Issues zu finden, an denen Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="a2610-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="a2610-122">Suchen nach einzelnem .NET-Leitfaden</span><span class="sxs-lookup"><span data-stu-id="a2610-122">Find a single .NET guide</span></span>

<span data-ttu-id="a2610-123">Wir verwenden Bezeichnungen für die einzelnen Architektur-E-Books und für jeden .NET-Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="a2610-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="a2610-124">![:book: Leitfaden auf hellgrünem Hintergrund](./media/labels-projects/guide.png "Präfix für Architekturleitfadenbezeichnungen")</span><span class="sxs-lookup"><span data-stu-id="a2610-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="a2610-125">Architektur-E-Books enthalten das Präfix `:book: guide` und weisen einen hellgrünen Hintergrund auf.</span><span class="sxs-lookup"><span data-stu-id="a2610-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="a2610-126">Dies sind die langen Bereiche , die empfohlene Architektur abdecken.</span><span class="sxs-lookup"><span data-stu-id="a2610-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="a2610-127">Hier werden aktuelle Issues für die einzelnen .NET-Architekturleitfäden gefiltert.</span><span class="sxs-lookup"><span data-stu-id="a2610-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="a2610-128">ASP.NET Core web apps</span><span class="sxs-lookup"><span data-stu-id="a2610-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="a2610-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="a2610-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="a2610-130">Cloud Native</span><span class="sxs-lookup"><span data-stu-id="a2610-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="a2610-131">Docker-Lebenszyklus</span><span class="sxs-lookup"><span data-stu-id="a2610-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="a2610-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="a2610-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="a2610-133">Modernisieren von w/ Windows-Containern</span><span class="sxs-lookup"><span data-stu-id="a2610-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="a2610-134">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="a2610-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="a2610-135">Serverlose Apps</span><span class="sxs-lookup"><span data-stu-id="a2610-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="a2610-136">Diese Bezeichnung wird auch für die [Framework-Entwurfsrichtlinien](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines) angewendet.</span><span class="sxs-lookup"><span data-stu-id="a2610-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="a2610-137">Dieser Bereich weist das gleiche Bezeichnungsdesign auf, Community-PRs wird davon aber abgeraten.</span><span class="sxs-lookup"><span data-stu-id="a2610-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="a2610-138">Dies ist mit der Berechtigung neu gedrucktes Material und sollte nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a2610-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="a2610-139">![„:books: Area“ auf dunkelblauem Hintergrund](./media/labels-projects/area.png "Präfix für .NET-Leitfadenbereichsbezeichnungen")</span><span class="sxs-lookup"><span data-stu-id="a2610-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="a2610-140">Jeder .NET-Leitfaden ist mit dem Präfix `:books: Area` versehen und weist einen dunkelblauen Hintergrund auf.</span><span class="sxs-lookup"><span data-stu-id="a2610-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="a2610-141">Hier werden aktuelle Issues für die einzelnen .NET-Leitfäden gefiltert.</span><span class="sxs-lookup"><span data-stu-id="a2610-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="a2610-142">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="a2610-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="a2610-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="a2610-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="a2610-144">Leitfaden für C#</span><span class="sxs-lookup"><span data-stu-id="a2610-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="a2610-145">Desktopleitfaden</span><span class="sxs-lookup"><span data-stu-id="a2610-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="a2610-146">Leitfaden für F#</span><span class="sxs-lookup"><span data-stu-id="a2610-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="a2610-147">Leitfaden für ML.NET</span><span class="sxs-lookup"><span data-stu-id="a2610-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="a2610-148">[.NET-Architekturleitfaden:](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) Kann entfernt werden</span><span class="sxs-lookup"><span data-stu-id="a2610-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="a2610-149">Leitfaden für .NET Core</span><span class="sxs-lookup"><span data-stu-id="a2610-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="a2610-150">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="a2610-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="a2610-151">Leitfaden für .NET Framework</span><span class="sxs-lookup"><span data-stu-id="a2610-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="a2610-152">.NET Guide (Leitfaden für .NET)</span><span class="sxs-lookup"><span data-stu-id="a2610-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="a2610-153">[Roslyn-API-Referenz:](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) Kann entfernt werden</span><span class="sxs-lookup"><span data-stu-id="a2610-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="a2610-154">Leitfaden für Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a2610-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="a2610-155">Durchsuchen eines Abschnitts eines Leitfadens</span><span class="sxs-lookup"><span data-stu-id="a2610-155">Search one section of a guide</span></span>

<span data-ttu-id="a2610-156">![„:card_file_box: Area“ auf hellblauem Hintergrund](./media/labels-projects/technology.png "Präfix für Unterbereichbezeichnungen in .NET-Leitfäden")</span><span class="sxs-lookup"><span data-stu-id="a2610-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="a2610-157">Die .NET-Leitfäden sind groß, sodass diese Bezeichnungen den Bereich durch einen Abschnitt eines Leitfadens weiter einschränken.</span><span class="sxs-lookup"><span data-stu-id="a2610-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="a2610-158">Jeder Unterbereich eines .NET-Leitfadens ist mit dem Präfix `:card_file_box: Technology` versehen und weist einen mittelblauen Hintergrund auf.</span><span class="sxs-lookup"><span data-stu-id="a2610-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="a2610-159">Viele dieser Bezeichnungen gelten für mehrere Leitfäden, während andere in nur einem Leitfaden aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a2610-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="a2610-160">Fügen Sie nach dem Filtern nach einem Bereich eine dieser Bezeichnungen hinzu, um den Umfang des Issues weiter einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="a2610-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="a2610-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="a2610-161">AppCompat</span></span>
- <span data-ttu-id="a2610-162">asynchrone Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a2610-162">Async Task</span></span>
- <span data-ttu-id="a2610-163">erweiterte C#-Konzepte</span><span class="sxs-lookup"><span data-stu-id="a2610-163">C# Advanced concepts</span></span>
- <span data-ttu-id="a2610-164">C#-Compiler</span><span class="sxs-lookup"><span data-stu-id="a2610-164">C# compiler</span></span>
- <span data-ttu-id="a2610-165">C#-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="a2610-165">C# Fundamentals</span></span>
- <span data-ttu-id="a2610-166">Erste Schritte mit C#</span><span class="sxs-lookup"><span data-stu-id="a2610-166">C# Get Started</span></span>
- <span data-ttu-id="a2610-167">C#-Programmiersprachenreferenz</span><span class="sxs-lookup"><span data-stu-id="a2610-167">C# Language Reference</span></span>
- <span data-ttu-id="a2610-168">C# Null-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a2610-168">C# Null safety</span></span>
- <span data-ttu-id="a2610-169">Neuerungen in C#</span><span class="sxs-lookup"><span data-stu-id="a2610-169">C# What's new</span></span>
- <span data-ttu-id="a2610-170">Befehlszeilenschnittstelle (CLI)</span><span class="sxs-lookup"><span data-stu-id="a2610-170">CLI</span></span>
- <span data-ttu-id="a2610-171">Datenzugriff</span><span class="sxs-lookup"><span data-stu-id="a2610-171">Data Access</span></span>
- <span data-ttu-id="a2610-172">Docker</span><span class="sxs-lookup"><span data-stu-id="a2610-172">Docker</span></span>
- <span data-ttu-id="a2610-173">Installer</span><span class="sxs-lookup"><span data-stu-id="a2610-173">Installers</span></span>
- <span data-ttu-id="a2610-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="a2610-174">LINQ</span></span>
- <span data-ttu-id="a2610-175">NCL</span><span class="sxs-lookup"><span data-stu-id="a2610-175">NCL</span></span>
- <span data-ttu-id="a2610-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="a2610-176">.NET Standard</span></span>
- <span data-ttu-id="a2610-177">Roslyn-APIs</span><span class="sxs-lookup"><span data-stu-id="a2610-177">Roslyn APIs</span></span>
- <span data-ttu-id="a2610-178">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="a2610-178">Security</span></span>
- <span data-ttu-id="a2610-179">WCF</span><span class="sxs-lookup"><span data-stu-id="a2610-179">WCF</span></span>
- <span data-ttu-id="a2610-180">WF</span><span class="sxs-lookup"><span data-stu-id="a2610-180">WF</span></span>
- <span data-ttu-id="a2610-181">WIF</span><span class="sxs-lookup"><span data-stu-id="a2610-181">WIF</span></span>
- <span data-ttu-id="a2610-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="a2610-182">WinForms</span></span>
- <span data-ttu-id="a2610-183">WPF</span><span class="sxs-lookup"><span data-stu-id="a2610-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="a2610-184">Releases</span><span class="sxs-lookup"><span data-stu-id="a2610-184">Releases</span></span>

<span data-ttu-id="a2610-185">![„:checkered_flag: Release:“ auf dunkelgelbem Hintergrund](./media/labels-projects/release.png "Präfix für Releasebezeichnungen")</span><span class="sxs-lookup"><span data-stu-id="a2610-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="a2610-186">Issues, die für ein bestimmtes Release gekennzeichnet sind, werden mit dem Präfix `:checkered_flag: Release:` versehen und weisen einen dunkelgelben Hintergrund auf.</span><span class="sxs-lookup"><span data-stu-id="a2610-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="a2610-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="a2610-187">.NET Core 2.2</span></span>
- <span data-ttu-id="a2610-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="a2610-188">.NET Core 3.0</span></span>
- <span data-ttu-id="a2610-189">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="a2610-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="a2610-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="a2610-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="a2610-191">Priorität</span><span class="sxs-lookup"><span data-stu-id="a2610-191">Priority</span></span>

<span data-ttu-id="a2610-192">Bei Prioritätsbezeichnungen folgt auf `P` eine einzelne Ziffer.</span><span class="sxs-lookup"><span data-stu-id="a2610-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="a2610-193">Niedrigere Zahlen stehen für eine höhere Priorität.</span><span class="sxs-lookup"><span data-stu-id="a2610-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="a2610-194">P0: Issues oder Pull Requests mit kritischer Priorität</span><span class="sxs-lookup"><span data-stu-id="a2610-194">P0 - Indicates issues or PRs that are critical priority</span></span>
- <span data-ttu-id="a2610-195">P1: hohe Priorität</span><span class="sxs-lookup"><span data-stu-id="a2610-195">P1 - High priority</span></span>
- <span data-ttu-id="a2610-196">P2: mittlere Priorität</span><span class="sxs-lookup"><span data-stu-id="a2610-196">P2 - Medium priority</span></span>
- <span data-ttu-id="a2610-197">P3: niedrige Priorität</span><span class="sxs-lookup"><span data-stu-id="a2610-197">P3 - Low priority</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="a2610-198">Weitere Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="a2610-198">What about the other labels</span></span>

<span data-ttu-id="a2610-199">Es gibt viele andere Bezeichnungen, die von den Inhaltsteams verwendet werden, um unterschiedliche Klassifizierungen von Issues zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a2610-199">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="a2610-200">Wenn Sie nicht Teil des Inhaltsteams sind, können Sie diese anderen Bezeichnungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="a2610-200">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="a2610-201">Projekte</span><span class="sxs-lookup"><span data-stu-id="a2610-201">Projects</span></span>

<span data-ttu-id="a2610-202">Projekte dienen Planungszwecken, und die priorisierten Arbeitsaufgaben sind dabei über ein Kanban-Board automatisiert.</span><span class="sxs-lookup"><span data-stu-id="a2610-202">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="a2610-203">Projekte dürfen immer nur GitHub-Issues enthalten, _niemals_ Pull Requests.</span><span class="sxs-lookup"><span data-stu-id="a2610-203">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="a2610-204">In dieser Beziehung unterscheiden sich Projekte von Meilensteinen: Meilensteine enthalten nur Pull Requests.</span><span class="sxs-lookup"><span data-stu-id="a2610-204">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="a2610-205">Projekte werden auf diese beiden Arten verwendet:</span><span class="sxs-lookup"><span data-stu-id="a2610-205">We use projects in two ways:</span></span>

- <span data-ttu-id="a2610-206">Projekte vom Typ `Month YYYY`: Dies sind Kanban-Boards für den Arbeitsplan jedes einzelnen Monats.</span><span class="sxs-lookup"><span data-stu-id="a2610-206">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="a2610-207">Beispiele: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) usw.</span><span class="sxs-lookup"><span data-stu-id="a2610-207">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="a2610-208">Epics mit langer Laufzeit: Diese werden verwendet, um Aufgaben für ein Ziel zu organisieren, wenn die Arbeit sich über mehrere Monate erstreckt.</span><span class="sxs-lookup"><span data-stu-id="a2610-208">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="a2610-209">Beispiele: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106) usw.</span><span class="sxs-lookup"><span data-stu-id="a2610-209">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="a2610-210">Meilensteine</span><span class="sxs-lookup"><span data-stu-id="a2610-210">Milestones</span></span>

<span data-ttu-id="a2610-211">Meilensteine folgen in der Regel derselben Namenskonvention wie Projekte (`Month YYYY`), unterscheiden sich aber von Projekten.</span><span class="sxs-lookup"><span data-stu-id="a2610-211">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="a2610-212">Meilensteine dienen zum Nachverfolgen abgeschlossener Arbeitsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="a2610-212">We use milestones to track completed work.</span></span> <span data-ttu-id="a2610-213">Meilensteine dürfen _keine_ Issues (potenzielle Arbeitsaufgaben) enthalten, sondern ausschließlich Pull Requests.</span><span class="sxs-lookup"><span data-stu-id="a2610-213">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="a2610-214">Der aktuelle Meilenstein wird automatisch auf neue Pull Requests angewendet.</span><span class="sxs-lookup"><span data-stu-id="a2610-214">The current milestone is automatically applied to new pull requests.</span></span>
