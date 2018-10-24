# <a name="locale-specific-links"></a><span data-ttu-id="044bf-101">Gebietsschemaspezifische Links</span><span class="sxs-lookup"><span data-stu-id="044bf-101">Locale-specific links</span></span>

<span data-ttu-id="044bf-102">Lokale Codes wie `en-us` sollten nicht in Links zu bestimmten Microsoft-Websites enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="044bf-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="044bf-103">Wenn Sie einen lokalen Code in einen Link mit englischem Inhalt einfügen, wird dieser auch in lokalisierten Links enthalten sein, was zu einer schlechten Lokalisierung führt.</span><span class="sxs-lookup"><span data-stu-id="044bf-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="044bf-104">Wenn beispielsweise ein Link in einem nach Deutsch lokalisierten Inhalt `en-us` enthält, werden deutsche Kunden zum englischen Artikel weitergeleitet, obwohl eine deutsche Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="044bf-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="044bf-105">Entfernen Sie lokale Codes aus Links zu Microsoft-Websites.</span><span class="sxs-lookup"><span data-stu-id="044bf-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="044bf-106">Dies ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="044bf-106">The following is an example.</span></span>

<span data-ttu-id="044bf-107">Vorher:</span><span class="sxs-lookup"><span data-stu-id="044bf-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="044bf-108">Nachher:</span><span class="sxs-lookup"><span data-stu-id="044bf-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="044bf-109">Diese Überprüfung soll für die folgenden Websites durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="044bf-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="044bf-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="044bf-110">azure.microsoft.com</span></span>
- <span data-ttu-id="044bf-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="044bf-111">docs.microsoft.com</span></span>
- <span data-ttu-id="044bf-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="044bf-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="044bf-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="044bf-113">technet.microsoft.com</span></span>