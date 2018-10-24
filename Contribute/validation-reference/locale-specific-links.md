# <a name="locale-specific-links"></a>Gebietsschemaspezifische Links

Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein. Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt. Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.

Entfernen Sie lokale Codes aus Links zu Microsoft-Websites. Dies ist ein Beispiel:

Vorher:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Nachher:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

Diese Überprüfung soll für die folgenden Websites durchgeführt werden:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com