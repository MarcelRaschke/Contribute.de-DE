---
title: Mitwirken an den Repositorys der PowerShell-Dokumentation
description: Dieser Artikel ist Teil der Repositorys, aus denen die PowerShell-Dokumentation besteht.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290171"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="f599f-103">Mitwirken an der PowerShell-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f599f-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="f599f-104">Vielen Dank für Ihr Interesse an der PowerShell-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f599f-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="f599f-105">In diesem Artikel erfahren Sie, wie Sie an Artikeln und Codebeispielen der PowerShell-Dokumentation mitwirken können.</span><span class="sxs-lookup"><span data-stu-id="f599f-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="f599f-106">Bei Änderungen kann es sich nur um das Korrigieren von Tippfehlern oder sogar um das Hinzufügen neuer Artikel handeln.</span><span class="sxs-lookup"><span data-stu-id="f599f-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="f599f-107">Die PowerShell-Dokumentation besteht aus mehreren Repositorys, die mindestens ein Docset enthalten:</span><span class="sxs-lookup"><span data-stu-id="f599f-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="f599f-108">[PowerShell-Konzepte & Cmdlet-Referenz][psdocs]</span><span class="sxs-lookup"><span data-stu-id="f599f-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="f599f-109">Codebeispiele für das PowerShell SDK: Privates Repository mit Beispielen, die in Artikeln zum SDK verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f599f-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="f599f-110">[Referenz zum PowerShell .NET SDK:](/dotnet/api/?view=pscore-6.2.0) aus PowerShell-Quellcode generierte Inhalte des privaten Repositorys.</span><span class="sxs-lookup"><span data-stu-id="f599f-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="f599f-111">Probleme für diese Inhalte werden im Repository [PowerShell-Docs][docsrepo] dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="f599f-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="f599f-112">Repository-Struktur</span><span class="sxs-lookup"><span data-stu-id="f599f-112">Repository Structure</span></span>

<span data-ttu-id="f599f-113">Das Repository „PowerShell-Docs“ besteht aus drei Docsets, die in [Microsoft-Dokumentationen][psdocs] veröffentlicht sind. Die Docsets befinden sich in den folgenden Ordnern:</span><span class="sxs-lookup"><span data-stu-id="f599f-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="f599f-114">[/reference/:][ref] enthält die PowerShell-Cmdlet-Referenz für die in PowerShell enthaltenen Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f599f-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="f599f-115">Die Referenz wird in verschiedenen Versionsordnern erfasst (3.0, 4.0, 5.0, 5.1, 6 und 7).</span><span class="sxs-lookup"><span data-stu-id="f599f-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="f599f-116">Dieses Docset enthält nicht die Referenz für die in Windows oder anderen Microsoft-Produkten enthaltenen Module.</span><span class="sxs-lookup"><span data-stu-id="f599f-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="f599f-117">[/reference/docs-conceptual:][conceptual] enthält das Konzept der PowerShell-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f599f-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="f599f-118">Dies umfasst Anweisungen für das Setup, Beispielskripts, Anleitungen und mehr.</span><span class="sxs-lookup"><span data-stu-id="f599f-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="f599f-119">[/developer/:][SDK] enthält das Konzept der PowerShell SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f599f-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
