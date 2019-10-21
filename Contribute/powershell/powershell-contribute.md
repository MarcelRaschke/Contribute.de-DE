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
# <a name="contributing-to-powershell-documentation"></a>Mitwirken an der PowerShell-Dokumentation

Vielen Dank für Ihr Interesse an der PowerShell-Dokumentation.

In diesem Artikel erfahren Sie, wie Sie an Artikeln und Codebeispielen der PowerShell-Dokumentation mitwirken können. Bei Änderungen kann es sich nur um das Korrigieren von Tippfehlern oder sogar um das Hinzufügen neuer Artikel handeln.

Die PowerShell-Dokumentation besteht aus mehreren Repositorys, die mindestens ein Docset enthalten:

- [PowerShell-Konzepte & Cmdlet-Referenz][psdocs]
- Codebeispiele für das PowerShell SDK: Privates Repository mit Beispielen, die in Artikeln zum SDK verwendet werden.
- [Referenz zum PowerShell .NET SDK:](/dotnet/api/?view=pscore-6.2.0) aus PowerShell-Quellcode generierte Inhalte des privaten Repositorys.

Probleme für diese Inhalte werden im Repository [PowerShell-Docs][docsrepo] dokumentiert.

## <a name="repository-structure"></a>Repository-Struktur

Das Repository „PowerShell-Docs“ besteht aus drei Docsets, die in [Microsoft-Dokumentationen][psdocs] veröffentlicht sind. Die Docsets befinden sich in den folgenden Ordnern:

- [/reference/:][ref] enthält die PowerShell-Cmdlet-Referenz für die in PowerShell enthaltenen Cmdlets. Die Referenz wird in verschiedenen Versionsordnern erfasst (3.0, 4.0, 5.0, 5.1, 6 und 7). Dieses Docset enthält nicht die Referenz für die in Windows oder anderen Microsoft-Produkten enthaltenen Module.
- [/reference/docs-conceptual:][conceptual] enthält das Konzept der PowerShell-Dokumentation. Dies umfasst Anweisungen für das Setup, Beispielskripts, Anleitungen und mehr.
- [/developer/:][SDK] enthält das Konzept der PowerShell SDK-Dokumentation.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
