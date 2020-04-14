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
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="d44e7-103">Roadmap für Bezeichnungen und Projekte</span><span class="sxs-lookup"><span data-stu-id="d44e7-103">Labels and projects roadmap</span></span>

<span data-ttu-id="d44e7-104">Das .NET-Dokumentationsteam macht umfassend Gebrauch von [GitHub-Bezeichnungen](https://github.com/dotnet/docs/labels), um die Arbeit zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="d44e7-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="d44e7-105">Indem wir nach Bezeichnungen filtern, können wir uns schnell auf wichtige Bereiche auf der [.NET-Dokumentationswebsite](https://docs.microsoft.com/dotnet) konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="d44e7-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="d44e7-106">Außerdem verwenden wir [GitHub-Projekte](https://github.com/dotnet/docs/projects), um Sprints und andere zielorientierte Epics zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="d44e7-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="d44e7-107">In dieser Roadmap wird erläutert, wie wir diese Organisationstools nutzen. Zudem sind Links zu praktischen Filtern enthalten, mit denen wir nach relevanten Bereichen suchen.</span><span class="sxs-lookup"><span data-stu-id="d44e7-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="d44e7-108">Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="d44e7-108">Labels</span></span>

<span data-ttu-id="d44e7-109">Wenn Sie zum ersten Mal an [dotnet/docs](https://github.com/dotnet/docs) mitwirken, sollten Sie mit den [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs)-Issues beginnen.</span><span class="sxs-lookup"><span data-stu-id="d44e7-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="d44e7-110">Diese Issues haben bereits einen klaren Umfang.</span><span class="sxs-lookup"><span data-stu-id="d44e7-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="d44e7-111">Sie sind gut für Ihren ersten Beitrag geeignet.</span><span class="sxs-lookup"><span data-stu-id="d44e7-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="d44e7-112">In der up-for-grabs-Ansicht können Sie die Issues weiter nach Bereich und Priorität filtern.</span><span class="sxs-lookup"><span data-stu-id="d44e7-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="d44e7-113">Wir haben für Einsteiger geeignete Issues mit [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) gekennzeichnet, falls Sie sich zunächst an einem kleineren Beitrag versuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d44e7-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="d44e7-114">Wir verwenden Bezeichnungen, um Issues unter anderem nach folgenden Kriterien zu klassifizieren:</span><span class="sxs-lookup"><span data-stu-id="d44e7-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="d44e7-115">[.NET-Leitfäden](#find-a-single-net-guide) und [Abschnitte eines Leitfadens](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="d44e7-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="d44e7-116">Zielrelease</span><span class="sxs-lookup"><span data-stu-id="d44e7-116">Target release</span></span>](#releases)
- [<span data-ttu-id="d44e7-117">Priorität</span><span class="sxs-lookup"><span data-stu-id="d44e7-117">Priority</span></span>](#priority)

<span data-ttu-id="d44e7-118">Sie können eine Bezeichnung jeder Kategorie (Leitfaden, Release, Priorität) kombinieren, um Ihren Fokus für Issues zu präzisieren, an denen Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d44e7-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="d44e7-119">Suchen eines einzelnen .NET-Leitfadens</span><span class="sxs-lookup"><span data-stu-id="d44e7-119">Find a single .NET guide</span></span>

<span data-ttu-id="d44e7-120">Für verwenden Bezeichnungen für jedes Architektur-E-Book und jeden .NET-Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="d44e7-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="d44e7-121">![„:book: guide“ auf hellgrünem Hintergrund](./media/labels-projects/guide.png "Präfix für Bezeichnungen für Architekturleitfäden")</span><span class="sxs-lookup"><span data-stu-id="d44e7-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="d44e7-122">Architektur-E-Books erkennen Sie am Präfix `:book: guide` und einem hellgrünen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="d44e7-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="d44e7-123">Hierbei handelt es sich um die übergeordneten Bereiche, in denen empfohlene Architekturen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d44e7-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="d44e7-124">Hier finden Sie aktuelle Issues, die nach den einzelnen .NET-Architekturleitfäden gefiltert wurden:</span><span class="sxs-lookup"><span data-stu-id="d44e7-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="d44e7-125">ASP.NET Core web apps</span><span class="sxs-lookup"><span data-stu-id="d44e7-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="d44e7-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="d44e7-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="d44e7-127">Cloud Native</span><span class="sxs-lookup"><span data-stu-id="d44e7-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="d44e7-128">Docker lifecycle</span><span class="sxs-lookup"><span data-stu-id="d44e7-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="d44e7-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="d44e7-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="d44e7-130">Modernizing w/ Windows containers</span><span class="sxs-lookup"><span data-stu-id="d44e7-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="d44e7-131">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="d44e7-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="d44e7-132">Serverless apps</span><span class="sxs-lookup"><span data-stu-id="d44e7-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="d44e7-133">Diese Bezeichnungen werden auch auf [Leitfäden zum Frameworkentwurf](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines) angewendet.</span><span class="sxs-lookup"><span data-stu-id="d44e7-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="d44e7-134">Die Bezeichnungen in diesem Bereich sind gleich gestaltet, es wird jedoch von PRs aus der Community abgeraten.</span><span class="sxs-lookup"><span data-stu-id="d44e7-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="d44e7-135">Dieses Material wird mit Genehmigung neu herausgegeben und sollte nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d44e7-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="d44e7-136">![„:books: Area“ auf dunkelblauem Hintergrund](./media/labels-projects/area.png "Präfix für Bezeichnungen für .NET-Leitfäden")</span><span class="sxs-lookup"><span data-stu-id="d44e7-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="d44e7-137">.NET-Leitfäden erkennen Sie am Präfix `:books: Area` und einem dunkelblauen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="d44e7-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="d44e7-138">Hier finden Sie aktuelle Issues, die nach den einzelnen .NET-Leitfäden gefiltert wurden:</span><span class="sxs-lookup"><span data-stu-id="d44e7-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="d44e7-139">API Reference</span><span class="sxs-lookup"><span data-stu-id="d44e7-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="d44e7-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="d44e7-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="d44e7-141">C# Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="d44e7-142">Desktop Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="d44e7-143">F# Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="d44e7-144">ML.NET Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="d44e7-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) (wird möglicherweise entfernt)</span><span class="sxs-lookup"><span data-stu-id="d44e7-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="d44e7-146">.NET Core Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="d44e7-147">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="d44e7-148">.NET Framework Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="d44e7-149">.NET Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="d44e7-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) (wird möglicherweise entfernt)</span><span class="sxs-lookup"><span data-stu-id="d44e7-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="d44e7-151">Visual Basic Guide</span><span class="sxs-lookup"><span data-stu-id="d44e7-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="d44e7-152">Durchsuchen eines Abschnitts eines Leitfadens</span><span class="sxs-lookup"><span data-stu-id="d44e7-152">Search one section of a guide</span></span>

<span data-ttu-id="d44e7-153">![„:card_file_box: Area“ auf hellblauem Hintergrund](./media/labels-projects/technology.png "Präfix für Bezeichnungen für Unterbereiche von .NET-Leitfäden")</span><span class="sxs-lookup"><span data-stu-id="d44e7-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="d44e7-154">Die .NET-Leitfäden sind sehr umfangreich, deshalb schränken diese Bezeichnungen den Umfang nach Abschnitt eines Leitfadens ein.</span><span class="sxs-lookup"><span data-stu-id="d44e7-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="d44e7-155">Unterbereiche eines .NET-Leitfadens erkennen Sie am Präfix `:card_file_box: Technology` und einem hellblauen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="d44e7-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="d44e7-156">Viele dieser Bezeichnungen gelten für mehrere Leitfäden, während andere in nur einem Leitfaden aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d44e7-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="d44e7-157">Wenn Sie nach einem Bereich gefiltert haben, können Sie eine dieser Bezeichnungen hinzufügen, um den Bereich der Issues weiter einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="d44e7-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="d44e7-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="d44e7-158">AppCompat</span></span>
- <span data-ttu-id="d44e7-159">Async Task</span><span class="sxs-lookup"><span data-stu-id="d44e7-159">Async Task</span></span>
- <span data-ttu-id="d44e7-160">C# Advanced concepts</span><span class="sxs-lookup"><span data-stu-id="d44e7-160">C# Advanced concepts</span></span>
- <span data-ttu-id="d44e7-161">C# compiler</span><span class="sxs-lookup"><span data-stu-id="d44e7-161">C# compiler</span></span>
- <span data-ttu-id="d44e7-162">C# Fundamentals</span><span class="sxs-lookup"><span data-stu-id="d44e7-162">C# Fundamentals</span></span>
- <span data-ttu-id="d44e7-163">C# Get Started</span><span class="sxs-lookup"><span data-stu-id="d44e7-163">C# Get Started</span></span>
- <span data-ttu-id="d44e7-164">C# Language Reference</span><span class="sxs-lookup"><span data-stu-id="d44e7-164">C# Language Reference</span></span>
- <span data-ttu-id="d44e7-165">C# Null safety</span><span class="sxs-lookup"><span data-stu-id="d44e7-165">C# Null safety</span></span>
- <span data-ttu-id="d44e7-166">C# What's new</span><span class="sxs-lookup"><span data-stu-id="d44e7-166">C# What's new</span></span>
- <span data-ttu-id="d44e7-167">CLI</span><span class="sxs-lookup"><span data-stu-id="d44e7-167">CLI</span></span>
- <span data-ttu-id="d44e7-168">Data Access</span><span class="sxs-lookup"><span data-stu-id="d44e7-168">Data Access</span></span>
- <span data-ttu-id="d44e7-169">Docker</span><span class="sxs-lookup"><span data-stu-id="d44e7-169">Docker</span></span>
- <span data-ttu-id="d44e7-170">Installers</span><span class="sxs-lookup"><span data-stu-id="d44e7-170">Installers</span></span>
- <span data-ttu-id="d44e7-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="d44e7-171">LINQ</span></span>
- <span data-ttu-id="d44e7-172">NCL</span><span class="sxs-lookup"><span data-stu-id="d44e7-172">NCL</span></span>
- <span data-ttu-id="d44e7-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="d44e7-173">.NET Standard</span></span>
- <span data-ttu-id="d44e7-174">Roslyn APIs</span><span class="sxs-lookup"><span data-stu-id="d44e7-174">Roslyn APIs</span></span>
- <span data-ttu-id="d44e7-175">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d44e7-175">Security</span></span>
- <span data-ttu-id="d44e7-176">WCF</span><span class="sxs-lookup"><span data-stu-id="d44e7-176">WCF</span></span>
- <span data-ttu-id="d44e7-177">WF</span><span class="sxs-lookup"><span data-stu-id="d44e7-177">WF</span></span>
- <span data-ttu-id="d44e7-178">WIF</span><span class="sxs-lookup"><span data-stu-id="d44e7-178">WIF</span></span>
- <span data-ttu-id="d44e7-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="d44e7-179">WinForms</span></span>
- <span data-ttu-id="d44e7-180">WPF</span><span class="sxs-lookup"><span data-stu-id="d44e7-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="d44e7-181">Releases</span><span class="sxs-lookup"><span data-stu-id="d44e7-181">Releases</span></span>

<span data-ttu-id="d44e7-182">![„:checkered_flag: Release:“ auf dunkelgelbem Hintergrund](./media/labels-projects/release.png "Präfix für Bezeichnungen für Releases")</span><span class="sxs-lookup"><span data-stu-id="d44e7-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="d44e7-183">Issues, die für ein bestimmtes Release gekennzeichnet sind, erkennen Sie am Präfix `:checkered_flag: Release:` und einem dunkelgelben Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="d44e7-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="d44e7-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="d44e7-184">.NET Core 2.2</span></span>
- <span data-ttu-id="d44e7-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="d44e7-185">.NET Core 3.0</span></span>
- <span data-ttu-id="d44e7-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="d44e7-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="d44e7-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="d44e7-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="d44e7-188">Priorität</span><span class="sxs-lookup"><span data-stu-id="d44e7-188">Priority</span></span>

<span data-ttu-id="d44e7-189">Prioritätsbezeichnungen weisen das Format `P` gefolgt von einer einzelnen Ziffer auf.</span><span class="sxs-lookup"><span data-stu-id="d44e7-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="d44e7-190">Je niedriger die Zahl, desto höher die Priorität:</span><span class="sxs-lookup"><span data-stu-id="d44e7-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="d44e7-191">P0</span><span class="sxs-lookup"><span data-stu-id="d44e7-191">P0</span></span>
- <span data-ttu-id="d44e7-192">P1</span><span class="sxs-lookup"><span data-stu-id="d44e7-192">P1</span></span>
- <span data-ttu-id="d44e7-193">P2</span><span class="sxs-lookup"><span data-stu-id="d44e7-193">P2</span></span>
- <span data-ttu-id="d44e7-194">P3</span><span class="sxs-lookup"><span data-stu-id="d44e7-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="d44e7-195">Weitere Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="d44e7-195">What about the other labels?</span></span>

<span data-ttu-id="d44e7-196">Es gibt viele weitere Bezeichnungen, die von den Inhaltsteams verwendet werden, um unterschiedliche Klassifizierungen für Issues zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d44e7-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="d44e7-197">Wenn Sie kein Mitglied des Inhaltsteams sind, können Sie diese anderen Bezeichnungen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="d44e7-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="d44e7-198">Projekte</span><span class="sxs-lookup"><span data-stu-id="d44e7-198">Projects</span></span>

<span data-ttu-id="d44e7-199">Projekte werden auf diese beiden Arten verwendet:</span><span class="sxs-lookup"><span data-stu-id="d44e7-199">We use projects in two ways:</span></span>

- <span data-ttu-id="d44e7-200">Projekttypen nach „Monat JJJJ“: Dabei handelt es sich um Scrum-Boards für den Arbeitsplan jedes Monats.</span><span class="sxs-lookup"><span data-stu-id="d44e7-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="d44e7-201">Epics mit langer Laufzeit: Diese werden verwendet, um Aufgaben für ein Ziel zu organisieren, wenn die Arbeit sich über mehrere Monate erstreckt.</span><span class="sxs-lookup"><span data-stu-id="d44e7-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
