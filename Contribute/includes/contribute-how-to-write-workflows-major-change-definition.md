---
ms.openlocfilehash: 55b3034f4375bc2b9ec68e8aa47ff828b91f8e39
ms.sourcegitcommit: 48d9a16cd3854cdf3c8c492dab1675edcdfbbd7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103481303"
---
 - **Tragen Sie Wesentliches bei**. Sie können beispielsweise Beiträge (Hinzufügungen, Änderungen oder Löschungen) einreichen, die mehrere Artikel betreffen, müssen als eine Arbeitseinheit in einem einzigen Pull Request committet oder getestet werden. 
 - **Einen neuen Artikel erstellen oder veröffentlichen**, was normalerweise einen robusteren lokalen Editor erfordert. 
 - **Neue Bilder hinzufügen oder Bilder aktualisieren**, erfordert in der Regel die gleichzeitige Erstellung eines neuen `media`-Unterverzeichnisses, Bilddateien, Updates für Bildverknüpfungen in Artikeln und das Anzeigen einer Vorschau von Markdowndateien in einem lokalen Editor, um Bildrendering zu testen.
 - **Einen Artikel vor der Veröffentlichung über einen Zeitraum von Tagen aktualisieren**. In diesen Fällen müssen Sie normalerweise eine reguläre Integration anderer Änderungen durchführen, die in diesem Standardbranch vorkommen. Diese Integration lässt sich leichter über Git Bash oder durch lokale Bearbeitung vornehmen. Es besteht dabei auch das Risiko, Ihre Änderungen zu verlieren, falls Sie diesen Prozess mithilfe der GitHub-Benutzeroberfläche durchführen. Warten Sie, bevor Sie für die Änderungen ein Commit ausführen.
 - **Fortwährende Updates für denselben Artikel durchführen, nachdem ein Pull Request geöffnet wurde** (es sei denn, Sie möchten dies lieber über die GitHub-Benutzeroberfläche tun). Die GitHub-Benutzeroberfläche hat das Potential, mehrere herausragende Pull Requests für die gleiche Datei zu erstellen, was zu einem Konflikt mit einer anderen führen kann. 