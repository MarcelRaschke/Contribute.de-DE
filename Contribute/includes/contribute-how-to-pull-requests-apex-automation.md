---
ms.openlocfilehash: b64e8dd4c62ca05b6e04ef404ebf98a618d0171e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "66391364"
---
Durch die Kommentarautomatisierung können Benutzer mit Leserechten (Benutzer, die keine Schreibrechte für ein Repository haben) eine Aktion mit Schreibrechten durchführen, indem Sie die entsprechende Bezeichnung einem Pull Request zuweisen. Wenn Sie in einem Repository arbeiten, in dem die Kommentarautomatisierung implementiert wurde, verwenden Sie die Hashtagkommentare, die in der folgenden Tabelle aufgeführt sind, um Bezeichnungen zuzuweisen, zu ändern, oder um einen Pull Request zu schließen. Microsoft-Mitarbeiter werden auch per E-Mail über die Überprüfung und Freigabe öffentlicher Repository-Pull Requests informiert, wenn Änderungen für Artikel vorgeschlagen werden, für die Sie der Autor sind.

| Hashtagkommentar | Funktionsbeschreibung | Repository-Verfügbarkeit |
| --- | --- | --- |
| `#sign-off` |Wenn der Autor eines Artikels den Kommentar `#sign-off` in den Kommentarstream eingibt, wird die Bezeichnung **ready-to-merge** zugewiesen. Diese Bezeichnung lässt die Bearbeiter im Repository wissen, wann ein Pull Request zur Überprüfung bzw. zum Zusammenführen bereit ist. <br/><br/> Wenn ein Mitwirkender, der *nicht* der aufgelistete Autor ist, versucht, einen öffentlichen Pull Request mithilfe des Kommentars `#sign-off` zu genehmigen, wird eine Nachricht im Pull Request angezeigt, dass nur der Autor diese Bezeichnung zuweisen kann. |Öffentlich und privat |
| `#hold-off` |Autoren können `#hold-off` in einen PR-Kommentar eingeben, um die Bezeichnung **ready-to-merge** zu entfernen, im Fall, dass sie ihre Meinung geändert oder einen Fehler gemacht haben. Im privaten Repository wird die Bezeichnung **do-not-merge** zugewiesen. |Öffentlich und privat |
| `#please-close` |Autoren können `#please-close` in den Kommentarstream eingeben, um den Pull Request zu schließen, wenn sie sich dazu entscheiden, die Änderungen nicht zu mergen. |Öffentlich |
