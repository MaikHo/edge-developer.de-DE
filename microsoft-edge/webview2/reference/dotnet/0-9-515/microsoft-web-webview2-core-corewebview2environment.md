---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: be8f475d4c1a886a92b46144f2bffde2d49dc9d4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654025"
---
# <span data-ttu-id="82b11-104">Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse</span><span class="sxs-lookup"><span data-stu-id="82b11-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="82b11-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="82b11-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="82b11-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="82b11-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="82b11-107">Dies stellt die WebView2-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="82b11-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="82b11-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="82b11-108">Summary</span></span>

 <span data-ttu-id="82b11-109">Member</span><span class="sxs-lookup"><span data-stu-id="82b11-109">Members</span></span>                        | <span data-ttu-id="82b11-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="82b11-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82b11-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="82b11-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="82b11-112">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="82b11-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="82b11-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="82b11-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="82b11-114">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="82b11-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="82b11-115">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="82b11-115">CreateAsync</span></span>](#createasync) | <span data-ttu-id="82b11-116">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="82b11-116">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="82b11-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="82b11-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="82b11-118">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="82b11-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="82b11-119">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="82b11-119">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="82b11-120">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="82b11-120">Create a new web resource response object.</span></span>

<span data-ttu-id="82b11-121">Webansichten, die aus einer Umgebung erstellt wurden, die im Browser Prozess ausgeführt wird, der mit Umgebungsparametern und aus einer Umgebung erstellten Objekten erstellt wurde, sollten in derselben Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82b11-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="82b11-122">Die Verwendung in unterschiedlichen Umgebungen ist nicht garantiert kompatibel und kann fehlerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="82b11-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="82b11-123">Member</span><span class="sxs-lookup"><span data-stu-id="82b11-123">Members</span></span>

#### <span data-ttu-id="82b11-124">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="82b11-124">BrowserVersionString</span></span> 

<span data-ttu-id="82b11-125">Die Browser Versionsinformationen des aktuellen CoreWebView2Environment, einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="82b11-125">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="82b11-126">public String [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="82b11-126">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="82b11-127">Dies entspricht dem Format der GetAvailableCoreWebView2BrowserVersionString-API.</span><span class="sxs-lookup"><span data-stu-id="82b11-127">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="82b11-128">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="82b11-128">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="82b11-129">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="82b11-129">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="82b11-130">Das NewBrowserVersionAvailable-Ereignis wird ausgelöst, wenn eine neuere Version des Edge-Browsers installiert ist und über WebView2 zur Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="82b11-130">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="82b11-131">public event EventHandler<-Objekt > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="82b11-131">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="82b11-132">Wenn Sie die neuere Version des Browsers verwenden möchten, müssen Sie eine neue Umgebung und WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="82b11-132">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="82b11-133">Dieses Ereignis wird nur für eine neue Version aus dem gleichen Edge-Kanal ausgelöst, von dem aus der Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82b11-133">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="82b11-134">Wenn Sie nicht mit installiertem Edge ausgeführt wird, wird kein Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="82b11-134">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="82b11-135">Da ein benutzerdatenordner nur von einem Browserprozess gleichzeitig verwendet werden kann, wenn Sie denselben benutzerdatenordner in den Webansichten mithilfe der neuen Browserversion verwenden möchten, müssen Sie die Umgebung und Webansichten schließen, die zuerst die ältere Version des Browsers verwenden.</span><span class="sxs-lookup"><span data-stu-id="82b11-135">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="82b11-136">Oder fordern Sie den Benutzer einfach auf, die APP neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="82b11-136">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="82b11-137">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="82b11-137">CreateAsync</span></span> 

<span data-ttu-id="82b11-138">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="82b11-138">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="82b11-139">Public Async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Optionen)</span><span class="sxs-lookup"><span data-stu-id="82b11-139">public async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="82b11-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="82b11-140">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="82b11-141">Der relative Pfad zu dem Ordner, in dem sich der eingebettete Edge befindet.</span><span class="sxs-lookup"><span data-stu-id="82b11-141">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="82b11-142">userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="82b11-142">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="82b11-143">Optionen zum Erstellen der WebView2-Umgebung</span><span class="sxs-lookup"><span data-stu-id="82b11-143">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="82b11-144">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="82b11-144">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="82b11-145">Erstellen Sie einen neuen WebView asynchron.</span><span class="sxs-lookup"><span data-stu-id="82b11-145">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="82b11-146">Public Async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="82b11-146">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="82b11-147">ParentWindow ist das HWND, in dem die WebView-Ansicht angezeigt werden soll und von der die Eingabe empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b11-147">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="82b11-148">Die WebView fügt dem bereitgestellten Fenster während der Erstellung von WebView ein untergeordnetes Fenster hinzu.</span><span class="sxs-lookup"><span data-stu-id="82b11-148">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="82b11-149">Die Z-Reihenfolge und andere Elemente, die von der Reihenfolge der nebengeordneten Fenster beeinflusst werden, sind dementsprechend betroffen.</span><span class="sxs-lookup"><span data-stu-id="82b11-149">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="82b11-150">Es wird empfohlen, die Anwendungsbenutzer Modell-ID für den Prozess oder das Anwendungsfenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="82b11-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="82b11-151">Wenn None gesetzt ist, wird bei der Erstellung von WebView eine generierte Anwendungsbenutzer Modell-ID auf das Stammfenster von ParentWindow eingestellt.</span><span class="sxs-lookup"><span data-stu-id="82b11-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="82b11-152">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="82b11-152">CreateWebResourceResponse</span></span> 

<span data-ttu-id="82b11-153">Erstellen Sie ein neues Webressourcen-Antwortobjekt.</span><span class="sxs-lookup"><span data-stu-id="82b11-153">Create a new web resource response object.</span></span>

> <span data-ttu-id="82b11-154">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int Statuscode, String ReasonPhrase, String Headers)</span><span class="sxs-lookup"><span data-stu-id="82b11-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="82b11-155">Die Kopfzeilen ist die unformatierte Antwortheader Zeichenfolge, die durch einen Zeilenumbruch getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="82b11-155">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="82b11-156">Es ist auch möglich, dieses Objekt mit einer leeren Headerzeichenfolge zu erstellen und dann die Kopfzeilen Zeile für Zeile mithilfe der CoreWebView2HttpResponseHeaders zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="82b11-156">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="82b11-157">Informationen zu anderen Parametern finden Sie unter CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="82b11-157">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>
