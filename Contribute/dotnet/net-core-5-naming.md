---
title: Verweisen auf .NET in Dokumenten
description: Hier erfahren Sie, wie Sie in Dokumenten auf .NET Core, .NET 5 und höhere Versionen verweisen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/28/2021
ms.openlocfilehash: 102c782215ea6daa033b4fa4e996d89cf587c86b
ms.sourcegitcommit: ac9c26c336b6886b6970e8d85b1e79faad0db4b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "99477324"
---
# <a name="how-to-refer-to-net-in-docs"></a>Verweisen auf .NET in Dokumenten

## <a name="recommended-terminology"></a>Empfohlene Terminologie

**Im Titel des Dokuments und in der ersten Überschrift (H1):**

- „.NET“ (ohne Angabe von „5“ oder „Core“)

**Erster Verweis in Artikeltext:**

- „.NET“ für Dokumente zu Core bzw. 5 und höher, die für Benutzer hilfreich sind, die in .NET einsteigen.
- „.NET 5“ (und .NET Core) und höhere Versionen, falls es erforderlich ist, „Core“ bzw. „5“ (und höher) als spezifische .NET-Implementierung hervorzuheben.

**Nachfolgende Verweise:**

- „.NET“ für Dokumente, die Core bzw. 5 und höhere Versionen für Benutzer erläutern, die noch nicht mit .NET vertraut sind, oder wenn der Verweis auf Core bzw. 5 (und höher) im Kontext klar ist.
- „.NET 5 und höhere Versionen“ bei denen es erforderlich ist, zwischen Core bzw. 5 (und höher) aus anderen .NET-Implementierungen zu unterscheiden.

**Hinweise:**

- Andere berücksichtigte Optionen:
  - „.NET 5 (und .NET Core 2.1/3.1) und höhere Versionen“: die Core-Versionsnummern scheinen unnötig zu sein und machen den Ausdruck länger als er sein müsste.
  - „.NET 5 und höhere Versionen (zuvor als .NET Core bezeichnet)“ könnten Verwirrung verursachen, da „5 und höher“ die Versionen 2.1–3.1 ausschließt.
  - „.NET 5 und höhere Versionen (einschließlich .NET Core 2.1–3.1)“ bringt ein ähnliches Problem mit sich, da „2.1–3.1“ so klingt, als sollten diese Versionen unter „höhere Versionen“ vermerkt werden.
  - „.NET 5+“ ist eine kürzere Alternative zu „.NET 5 und höhere Versionen“, es gibt jedoch Bedenken, dass dies nicht universell verständlich ist.
- „.NET 5 und höhere Versionen“ bleibt nach der Veröffentlichung von Version 6 und späteren Versionen eine akkurate Bezeichnung. Schließlich ist jedoch verständlich, dass mit „.NET“ die Version 5+ gemeint ist, deshalb ist es vielleicht möglich, in einigen Kontexten „5 und höhere Versionen“ wegzulassen.

## <a name="examples"></a>Beispiele

### <a name="changes-that-affect-compatibility"></a>[Änderungen, die sich auf die Kompatibilität auswirken](/dotnet/core/compatibility/)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Im Laufe seines Bestehens hat .NET versucht, ein hohes Maß an Kompatibilität von Version zu Version und zwischen den verschiedenen Varianten von.NET aufrechtzuerhalten. Dies gilt auch für .NET Core. Obwohl .NET Core als eine von .NET Framework unabhängige neue Technologie betrachtet werden kann, schränken zwei wesentliche Faktoren die Möglichkeit von .NET Core ein, von .NET Framework abzuweichen: | Seit der erstmaligen Veröffentlichung wurde immer versucht, in .NET ein hohes Maß an versions- und implementierungsübergreifender Kompatibilität zu gewährleisten. Obwohl .NET 5 (und .NET Core) sowie höhere Versionen im Vergleich zum .NET Framework als neue Technologie angesehen werden können, gibt es zwei Hauptfaktoren, die eine Umstellung vom .NET Framework auf diese .NET-Variante einschränken: |
| .NET Standard-Bibliotheksprojekte ermöglichen es Entwicklern, Bibliotheken zu erstellen, die auf gemeinsame APIs ausgerichtet sind, die von .NET Core und .NET Framework gemeinsam genutzt werden. | .NET Standard-Bibliotheksprojekte ermöglichen es Entwicklern, Bibliotheken zu erstellen, die auf gemeinsame APIs ausgerichtet sind, die vom .NET Framework sowie von .NET 5 und höheren Versionen (sowie von .NET Core) gemeinsam genutzt werden. |
| Dieser Artikel enthält keine vollständige Liste mit Breaking Changes zwischen .NET Framework und .NET Core. | Dieser Artikel enthält keine umfassende Liste von Breaking Changes in .NET 5 (und .NET Core) und höheren Versionen, verglichen mit .NET Framework. |
| Die folgenden APIs lösen immer eine `PlatformNotSupportedException` für .NET Core aus. | Die folgenden APIs lösen immer eine `PlatformNotSupportedException` für .NET 5 (und .NET Core) sowie höhere Versionen aus. |

### <a name="install-net-on-windows"></a>[Installieren von .NET unter Windows](/dotnet/core/install/windows)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Titel/H1: Installieren von .NET Core unter Windows | Titel/H1: Installieren von .NET unter Windows |
| In diesem Artikel wird erläutert, wie Sie .NET Core unter Windows installieren. .NET Core besteht aus der Runtime und dem SDK. Die Runtime wird zum Ausführen von .NET Core-Apps verwendet und ist möglicherweise bereits in der App enthalten. Dies ist allerdings keine Voraussetzung. Das SDK wird zum Erstellen von .NET Core-Apps und -Bibliotheken verwendet. Die .NET Core-Runtime wird immer mit dem SDK installiert. | In diesem Artikel erfahren Sie, wie Sie .NET 5 (und .NET Core) und höhere Versionen unter Windows installieren. .NET besteht aus der Runtime und dem SDK. Die Runtime wird zum Ausführen von .NET-Apps verwendet und ist möglicherweise bereits in der App enthalten. Das SDK wird zum Erstellen von .NET-Apps und -Bibliotheken verwendet. Die .NET-Runtime wird immer mit dem SDK installiert. |

### <a name="how-to-check-that-net-is-already-installed"></a>[Überprüfen, ob .NET bereits installiert ist](/dotnet/core/install/how-to-detect-installed-versions)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Titel/H1: Überprüfen, ob .NET Core bereits installiert ist | Titel/H1: Überprüfen, ob .NET bereits installiert ist |
| In diesem Artikel erfahren Sie, wie Sie überprüfen, welche Versionen der .NET Core-Runtime und des .NET Core SDK auf Ihrem Computer installiert sind. .NET Core wurde möglicherweise bereits installiert, wenn Sie eine integrierte Entwicklungsumgebung wie z. B. Visual Studio oder Visual Studio für Mac besitzen. | In diesem Artikel erfahren Sie, wie Sie überprüfen, welche Versionen der Runtime und des SDK für .NET 5 (und .NET Core) und für höhere Versionen auf Ihrem Computer installiert sind. Die Runtime und das SDK wurden möglicherweise bereits installiert, wenn Sie eine integrierte Entwicklungsumgebung wie Visual Studio oder Visual Studio für Mac besitzen. |

### <a name="tutorial-create-a-net-console-application-using-visual-studio"></a>[Tutorial: Erstellen einer .NET-Konsolenanwendung mit Visual Studio](/dotnet/core/tutorials/with-visual-studio)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Titel/H1: Tutorial: Erstellen einer .NET Core-Konsolenanwendung mit Visual Studio | Titel/H1: Tutorial: Erstellen einer .NET-Konsolenanwendung mit Visual Studio |
| In diesem Tutorial wird gezeigt, wie Sie eine .NET Core-Konsolenanwendung in Visual Studio 2019 erstellen und ausführen. | In diesem Tutorial wird gezeigt, wie Sie eine .NET-Konsolenanwendung in Visual Studio 2019 erstellen und ausführen. |
| Voraussetzungen: Visual Studio 2019 Version 16.6 oder höher mit installierter plattformübergreifenden .NET Core-Entwicklungsumgebung. Das .NET Core 3.1 SDK wird automatisch installiert, wenn Sie diese Workload auswählen. | Visual Studio 2019 Version 16.6 oder höher mit installierter plattformübergreifender .NET-Entwicklungsworkload. Das .NET SDK wird automatisch installiert, wenn Sie diese Workload auswählen. |


### <a name="tutorial-create-an-item-template"></a>[Tutorial: Erstellen einer Elementvorlage](/dotnet/core/tutorials/cli-templates-create-item-template)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Title/h1:Tutorial: Erstellen einer Elementvorlage | Title/h1:Tutorial: Erstellen einer Elementvorlage |
| Mit .NET Core können Sie Vorlagen erstellen und bereitstellen, die Projekte, Dateien und sogar Ressourcen generieren. | Mit .NET können Sie Vorlagen erstellen und bereitstellen, die Projekte, Dateien und sogar Ressourcen generieren. |
| Voraussetzungen: .NET Core 2.2 SDK oder eine höhere Version. | Voraussetzungen: .NET Core 2.2 SDK oder eine höhere Version (einschließlich .NET 5 und höhere Versionen). |

### <a name="net-sdk-overview"></a>[.NET Core SDK – Übersicht](/dotnet/core/sdk)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Title/H1: Übersicht über .NET Core SDK | Title/H1: Übersicht über .NET SDK |
| „das SDK“ im Text | keine Änderung |

### <a name="net-cli-overview"></a>[Übersicht über die .NET Core-CLI](/dotnet/core/tools)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Title/H1: Übersicht über die .NET Core-CLI | Title/H1: Übersicht über die .NET-CLI |
| Die .NET Core-Befehlszeilenschnittstelle (CLI) ist eine plattformübergreifende Toolkette zum Entwicklung, Erstellen, Ausführen und Veröffentlichen von .NET Core-Anwendungen. | Die .NET-Befehlszeilenschnittstelle (CLI) ist eine plattformübergreifende Toolkette zum Entwicklung, Erstellen, Ausführen und Veröffentlichen von .NET-Anwendungen. |

### <a name="net-application-publishing-overview"></a>[Übersicht über die .NET-Anwendungsveröffentlichung](/dotnet/core/deploying/)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| Titel/H1: Übersicht über die .NET Core-Anwendungsveröffentlichung | Titel/H1: Übersicht über die .NET-Anwendungsveröffentlichung |
| Mit .NET Core erstellte Anwendungen können in zwei verschiedenen Modi veröffentlicht werden, und der gewählte Modus beeinflusst, wie ein Benutzer Ihre App ausführt. | Die mit .NET 5 (und .NET Core) sowie mit späteren Versionen erstellten Anwendungen können in zwei verschiedenen Modi veröffentlicht werden, und der gewählte Modus beeinflusst, wie ein Benutzer Ihre App ausführt. |
| Die Veröffentlichung als eigenständige App erzeugt eine Anwendung, die die .NET Core-Runtime und die Bibliotheken, Ihre Anwendung und zugehörige Abhängigkeiten enthält. Benutzer der Anwendung können diese auf einem Computer ausführen, auf dem die .NET Core-Runtime nicht installiert ist. | Die Veröffentlichung als eigenständige App erzeugt eine Anwendung, die die .NET-Runtime und die Bibliotheken, Ihre Anwendung und zugehörige Abhängigkeiten enthält. Benutzer der Anwendung können diese auf einem Computer ausführen, auf dem die .NET-Runtime nicht installiert ist. |

### <a name="dotnet-new"></a>[dotnet new](/dotnet/core/tools/dotnet-new)

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| **Dieser Artikel gilt für:** ✔️ .NET Core 2.1 SDK und höhere Versionen | **Dieser Artikel gilt für:** ✔️ .NET Core 2.1 SDK und höhere Versionen (einschließlich .NET 5 SDK und höhere Versionen) |
| **`--dry-run`** Es wird eine Zusammenfassung dazu angezeigt, was passiert, wenn der jeweilige Befehl ausgeführt wird und sich eine Vorlagenerstellung ergibt. Verfügbar ab .NET Core 2.2 SDK. | Keine Änderung („Verfügbar seit .NET Core 2.2. SDK“ beibehalten) |

### <a name="applies-to-link-text-in-api-ref-docs"></a>„Gilt für“-Linktext in API-Verweisdokumenten

| Vor .NET 5 | Aktuelle Empfehlung |
| --- | --- |
| \<exception cref="T:System.PlatformNotSupportedException"\>Nur .NET Core: in allen Fällen\</exception\> | \<exception cref="T:System.PlatformNotSupportedException"\>.NET 5 (und .NET Core) und spätere Versionen: in allen Fällen\</exception\> |
