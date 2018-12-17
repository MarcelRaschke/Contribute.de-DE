## <a name="pull-request-processing"></a>Verarbeitung des Pull Requests

Im vorherigen Abschnitt wurden Sie durch den Prozess zur Übermittlung vorgeschlagener Änderungen durch Bündeln dieser Änderungen in einem neuen Pull Request (PR) geführt, der zur PR-Warteschlange des Zielrepositorys hinzugefügt wurde. Ein Pull Request aktiviert das Modell der Zusammenarbeit von GitHub, indem er anfordert, dass die Änderungen von Ihrem Arbeitsbranch mithilfe von Pull in einen anderen Branch übertragen und darin zusammengeführt werden. In den meisten Fällen ist dieser andere Branch der Standard-/„Master“-Branch im Hauptrepository.

### <a name="validation"></a>Überprüfung

Bevor Ihr Pull Request in seinem Zielbranch zusammengeführt werden kann, ist es möglicherweise notwendig, einen oder mehrere PR-Überprüfungsvorgänge zu durchlaufen. Überprüfungsprozesse können je nach Umfang der vorgeschlagenen Änderungen und den Regeln des Zielrepositorys variieren. Nachdem Ihr Pull Request übermittelt wurde, können Sie erwarten, dass eines der folgenden Ereignisse eintritt:

- **Zusammenführbarkeit:** Ein grundlegender Test für GitHub wird zunächst durchgeführt,bei dem geprüft wird, ob das Mergen möglich ist. Es wird überprüft, ob die vorgeschlagenen Änderungen in Ihrem Branch in Konflikt mit dem Zielbranch stehen oder nicht. Wenn der Pull Request darauf hinweist, dass der Test fehlgeschlagen ist, müssen Sie den Inhalt ausgleichen, der den Konflikt beim Zusammenführen verursacht, bevor die Verarbeitung fortgeführt werden kann.
- **CLA:** Wenn Sie zu einem öffentlichen Repository beitragen und nicht bei Microsoft angestellt sind, werden Sie je nach Ausmaß der vorgeschlagenen Änderungen möglicherweise aufgefordert, eine kurze Lizenzvereinbarung für Mitwirkende (Contribution License Agreement, CLA) abzuschließen, wenn Sie das erste Mal einen Pull Request für dieses Repository absenden. Nachdem der CLA-Schritt gelöscht wurde, wird Ihr Pull Request verarbeitet.
- **Bezeichnung:** Bezeichnungen werden automatisch Ihrem Pull Request zugeordnet. Diese werden verwendet, um den Status Ihres Pull Requests anzugeben, wenn er den Validierungsworkflow durchläuft. Beispielsweise erhalten neue Pull Requests womöglich automatisch die Bezeichnung „do-not-merge“ (nicht zusammenführen), was anzeigt, dass der Pull Request die Schritte zur Validierung, Überprüfung und Abmeldung noch nicht abgeschlossen hat.
- **Prüfung und Erstellung:** Automatische Prüfungen verifizieren, ob Ihre Änderungen die Validierungstests bestehen. Die Validierungstests ergeben womöglich Warnungen oder Fehler. Sie müssen deshalb Änderungen an mindestens einer Datei in Ihrem Pull Request vornehmen, bevor dieser zusammengeführt werden kann. Die Testergebnisse der Validierung werden Ihrem Pull Request als Kommentar zur Überprüfung hinzugefügt und werden Ihnen möglicherweise auch via E-Mail übermittelt.
- **Staging:** Die Artikelseiten, die von Ihren Änderungen betroffen sind, können bei erfolgreicher Validierung und Erstellung automatisch in einer Stagingumgebung zur Überprüfung bereitgestellt werden. Vorschau-URLs erscheinen in einem PR-Kommentar.
- **Automatisch mergen:** Der Pull Request wird möglicherweise automatisch gemergt, wenn er die Validierungstests besteht und bestimmte Kriterien erfüllt. In diesem Fall sind keine weiteren Schritte nötig.

### <a name="review-and-sign-off"></a>Überprüfen und Abmelden

Nachdem die gesamte PR-Verarbeitung abgeschlossen wurde, überprüfen Sie die Ergebnisse (PR-Kommentare, Vorschau-URLs usw.), um zu bestimmen, ob weitere Änderungen an diesen Dateien nötig sind, bevor Sie sich für die Zusammenführung abmelden. Wenn ein PR-Prüfer Ihren Pull Request überprüft hat, kann der Prüfer auch mithilfe von Kommentaren Feedback geben, falls es ausstehende Probleme bzw. Fragen vor dem Zusammenführen gibt.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Wenn der Pull Request fehlerfrei und abgemeldet ist, werden Ihre Änderungen von einem übergeordneten Branch zusammengeführt, und der Pull Request wird geschlossen.

### <a name="publishing"></a>Veröffentlichung

Denken Sie daran, dass Ihr Pull Request von einem PR-Prüfer zusammengeführt werden muss, bevor die Änderungen im nächsten geplanten Veröffentlichungsdurchlauf eingeschlossen werden können. Pull Requests werden normalerweise in der Reihenfolge überprüft bzw. zusammengeführt, in der sie übermittelt wurden. Wenn Ihr Pull Request eine Zusammenführung für einen bestimmten Veröffentlichungsdurchlauf erfordert, müssen Sie mit Ihrem PR-Prüfer vorzeitig daran arbeiten, um sicherzustellen, dass die Zusammenführung vor der Veröffentlichung ausgeführt wird.

Nachdem Ihre Beiträge genehmigt und zusammengeführt wurden, werden Sie vom Veröffentlichungsprozess von docs.microsoft.com übernommen. Die Veröffentlichungszeiten können je nach Team, das das Repository verwaltet, zu dem Sie beitragen, variieren. Artikel, die unter folgenden Pfaden veröffentlicht werden, werden normalerweise um 10:30 Uhr und 15:30 Uhr (UTC) von Montag bis Freitag veröffentlicht.

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Es kann bis zu 45 Minuten dauern, bis Artikel nach der Veröffentlichung online erscheinen. Nachdem Ihr Artikel veröffentlicht wurde, können Sie Ihre Änderungen unter folgender URL überprüfen: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
