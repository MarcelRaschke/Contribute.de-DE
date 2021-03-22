---
title: Grundlegende Informationen zu Git und GitHub für die Dokumentation
description: In diesem Artikel erhalten Sie einen Überblick über Git und das GitHub-Repository, die Organisation des Inhalts und die für docs.microsoft.com verwendeten Namenskonventionen.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/30/2017
ms.openlocfilehash: 038b181fee8465c9503f8a157ea90346b72d273f
ms.sourcegitcommit: 48d9a16cd3854cdf3c8c492dab1675edcdfbbd7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103481347"
---
# <a name="git-and-github-essentials-for-docs"></a>Grundlegende Informationen zu Git und GitHub für die Dokumentation

## <a name="overview"></a>Übersicht

Sie interagieren als Mitwirkender an Dokumentationsinhalten mit verschiedenen Tools und Vorgängen. Sie arbeiten mit anderen Mitwirkenden parallel an demselben Projekt zusammen – teilweise sogar an denselben Inhalten und zur selben Zeit. Möglich wird all dies durch die Software Git und GitHub.

Git ist ein Open-Source-System für die Versionskontrolle. Es ermöglicht derartige Projektzusammenarbeiten durch *verteilte Versionskontrolle* der in den *Repositorys* enthaltenen Dateien. Im Wesentlichen können mit Git Streams integriert werden, die im Laufe der Zeit von verschiedenen Mitwirkenden für ein bestimmtes Repository erstellt wurden.

GitHub ist ein webbasierter Hostingdienst für Git-Repositorys, die beispielsweise zum Speichern von [docs.microsoft.com](https://docs.microsoft.com)-Inhalten eingesetzt werden. GitHub hostet für alle Projekte das Hauptrepository, über das Mitwirkende Kopien für Ihre eigene Arbeit erstellen können.

## <a name="git"></a>Git

Wenn Ihnen die Arbeit mit zentralen Versionskontrollsystemen (z.B. Team Foundation Server, SharePoint oder Visual SourceSafe) bekannt ist, werden Sie feststellen, dass Git über einen einzigartigen Mitwirkungsworkflow und eine einzigartige Terminologie zur Unterstützung des verteilten Modells verfügt. So ist beispielsweise keine Dateisperrung verfügbar, die bei Auscheck-/Eincheckvorgängen üblich ist. Bei Git werden Änderungen sogar noch ausführlicher behandelt, indem Dateien byteweise miteinander verglichen werden.

Git basiert ebenfalls auf einer mehrstufigen Struktur zur Speicherung und Verwaltung von Inhalten für ein Projekt:

- Repository: Dies ist die größte Speichereinheit. Ein Repository enthält mindestens einen Branch.
- *Branch*: Diese Speichereinheit enthält die Dateien und Ordner, die den gesamten Inhalt eines Projekts bilden. Branches werden zur Trennung der Streams (in der Regel als Versionen bezeichnet) verwendet. Beiträge werden immer für einen bestimmten Branch erstellt und diesem zugeordnet. Alle Repositorys enthalten einen Standardbranch, der in der Regel als „Mainbranch“ bezeichnet wird, und mindestens einen weiteren Branch, der mit dem Standardbranch zusammengeführt werden soll. Der Standardbranch dient für das Projekt als aktuelle und allgemeingültige Version. Er ist der übergeordnete Branch, aus dem alle anderen Branches in dem Repository erstellt werden.

Mit Git aktualisieren und bearbeiten Mitwirkende Repositorys auf der lokalen und der GitHub-Ebene:

- Lokal mit Tools wie der Git Bash-Konsole, die Git-Befehle für die Verwaltung lokaler Repositorys und die Kommunikation mit GitHub-Repositorys unterstützt.
- Über die Website [www.github.com](https://www.github.com), welche Git zum Verwalten des Abgleichs von Beiträgen integriert, die an das Hauptrepository zurückgeführt werden.

## <a name="github"></a>GitHub

> [!NOTE]
> Die Anweisungen in der Dokumentation beziehen sich zwar auf die Verwendung von GitHub, jedoch hosten einige Teams Git-Repositorys mithilfe von Visual Studio Team Services. Der Visual Studio Team Explorer-Client enthält eine GUI für die Interaktion mit Team Services-Repositorys, die eine Alternative zur Verwendung von Git-Befehlen über eine Befehlszeile darstellen.
> </br>
> Zudem wurden viele der folgenden Richtlinien als bewährte Methoden basierend auf jahrelangen Erfahrungen beim Hosting von Azure-Dienstinhalten in GitHub entwickelt. Sie sind in einigen Dokumentationsrepositorys möglicherweise erforderlich.

Alle Workflows beginnen und enden auf GitHub-Ebene, auf der das Hauptrepository für jedes Dokumentationsprojekts gespeichert ist. Die von den Mitwirkenden erstellten Kopien werden über mehrere Computer hinweg verteilt. Diese Kopien werden letztendlich mit dem GitHub-Hauptrepository in Einklang gebracht.

### <a name="directory-organization"></a>Organisation von Verzeichnissen

Wie zuvor bereits erwähnt wurde, stellt der Standardbranch eines Projekts die aktuelle Version der Projektinhalte dar. Der Inhalt im Standardbranch (und in den daraus erstellten Branches) wird mit der Organisation der Artikel auf den entsprechenden Dokumentationsseiten abgestimmt. Unterverzeichnisse werden zur Trennung von ähnlichen Inhalten (z.B. Diensten), Medieninhalten (z.B. Bilddateien) und „Include“-Dateien verwendet, die eine Wiederverwendung der Inhalte ermöglichen.

Üblicherweise finden Sie ein `articles`-Hauptverzeichnis des Repositorystamms. Das Artikelverzeichnis enthält einige Unterverzeichnisse. Artikel in den Unterverzeichnissen werden als Markdowndateien mit *MD*-Erweiterung formatiert. Einige Repositorys, die mehrere Dienste unterstützen, verwenden ein generisches `/articles`-Unterverzeichnis, z.B. das Repository [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs). Andere verwenden möglicherweise einen dienstspezifischen Namen, z.B. das Repository [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs), das `/IntuneDocs` verwendet.

Im Stamm dieses Verzeichnisses finden Sie allgemeine Artikel, die mit dem allgemeinen Dienst oder Produkt im Zusammenhang stehen. Zudem können Sie üblicherweise weitere Unterverzeichnisse finden, die zu Features bzw. Diensten oder allgemeinen Szenarios passen. Azure-Artikel zu virtuellen Computern befinden sich beispielsweise im Unterverzeichnis `/virtual-machines`, während die Intune-Artikel im Bereich „Understand and Explore“ („Verstehen und Erkunden“) im Unterverzeichnis `/understand-explore` enthalten sind.

### <a name="media-subdirectory"></a>Unterverzeichnis für Mediendateien

Jedes Artikelverzeichnis enthält ein Unterverzeichnis `/media` für entsprechende Mediendateien. Mediendateien enthalten Bilder, die von Artikeln mit Bildverweisen verwendet werden.

### <a name="includes-subdirectory"></a>Unterverzeichnis für Includes

Wenn es wiederverwendbaren Inhalt gibt, der von mindestens einem Artikeln genutzt wird, wird dieser im Unterverzeichnis `/includes` des `articles`-Hauptartikelverzeichnisses abgelegt. In einer Markdowndatei, die die Includedatei verwenden soll, wird die entsprechende Markdownerweiterung „include“ an die Stelle platziert, an der auf die Includedatei verwiesen werden soll.

Weitere Anleitungen finden Sie unter [Einbezogene Markdowndateien](markdown-reference.md#included-markdown-files).

### <a name="markdown-file-template"></a>Markdown-Vorlagendatei

Der Einfachheit halber enthält das Stammverzeichnis jedes Repositorys üblicherweise eine Markdownvorlagendatei namens `template.md`. Sie können diese Vorlagendatei als Ausgangsdatei nutzen, wenn Sie einen neuen Artikel für die Übermittlung an das Repository erstellen müssen. Die Datei enthält Folgendes:

- Einen **Metadatenheader** am Anfang der Datei, der durch zwei Zeilen mit drei Bindestrichen getrennt wird. Er enthält die verschiedenen Tags, die zur Nachverfolgung von Informationen verwendet werden, die im Zusammenhang mit dem Artikel stehen. Metadaten zu Artikeln sind Voraussetzungen für bestimmte Funktionen wie die Zuordnung von Autoren und Mitwirkenden, die Brotkrümelnavigation und Beschreibungen von Artikeln. Zudem enthalten Sie SEO-Optimierungen und Vorgänge zur Berichterstattung, die Microsoft verwendet, um die Leistung eines Inhalts zu bewerten. Daher sind die Metadaten wichtig.
- Den **Abschnitt „Metadaten“** , in dem die verschiedenen Metadatentags und Werte beschrieben werden. Wenn Sie nicht sicher sind, welche Werte in den Metadatenabschnitt gehören, können Sie sie leer lassen oder mit einem führenden Hashtag (#) kommentieren. Der Prüfer des Pull Requests für das Repository überprüft bzw. vervollständigt diese anschließend.
- Verschiedene **Beispiele für die Verwendung des Markdownformats** zum Formatieren der Elemente eines Artikels.
- Allgemeine **Anweisungen für die Verwendung von Markdownerweiterungen**, die für verschiedene Arten von Benachrichtigungen verwendet werden können
- Beispiele für das **Einbetten von Videos** mithilfe eines IFrames
- Allgemeine **Anweisungen für die Verwendung von Erweiterungen für docs.microsoft.com**, die Sie für spezielle Steuerelemente wie Schaltflächen und Selektoren verwenden können.

## <a name="pull-requests"></a>Pull Requests

Ein *Pull Request* stellt eine praktische Methode für einen Mitwirkenden dar, um eine Reihe von Änderungen vorzuschlagen, die auf den Standardbranch angewendet werden sollen. Die Änderungen, auch als *Commits* bezeichnet, werden im Branch eines Mitwirkenden gespeichert, wodurch GitHub die Auswirkungen der *Zusammenführung* zuerst im Standardbranch modellieren kann. Ein Pull Request dient auch als Methode, um dem Mitwirkenden Feedback über einen Build- bzw. Validierungsprozess bereitzustellen, dem Prüfer des Pull Requests. Damit sollen vor der Zusammenführung der Änderungen im Standardbranch mögliche Probleme oder Fragen behoben bzw. geklärt werden.

Es gibt zwei Möglichkeiten, über einen Pull Request mitzuwirken, deren Anwendung davon abhängig ist, wie groß die Veränderungen sind, die Sie vorschlagen möchten. Dies wird weiter unten in den Abschnitten zum [GitHub-Workflow](how-to-write-workflows-major.md) dieses Leitfadens ausführlicher beschrieben.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
