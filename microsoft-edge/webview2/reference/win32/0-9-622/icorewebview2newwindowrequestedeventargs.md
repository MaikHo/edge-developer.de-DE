---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: d1cf39fe71c4b00f10a14da8a65428eb24daa71f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012128"
---
# <span data-ttu-id="06b69-104">Schnittstellen ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="06b69-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="06b69-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="06b69-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="06b69-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="06b69-106">Summary</span></span>

 <span data-ttu-id="06b69-107">Member</span><span class="sxs-lookup"><span data-stu-id="06b69-107">Members</span></span>                        | <span data-ttu-id="06b69-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="06b69-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06b69-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="06b69-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="06b69-110">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="06b69-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="06b69-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06b69-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="06b69-112">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="06b69-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="06b69-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b69-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="06b69-114">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="06b69-114">Gets the new window.</span></span>
[<span data-ttu-id="06b69-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06b69-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="06b69-116">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b69-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="06b69-117">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="06b69-117">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="06b69-118">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06b69-118">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="06b69-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06b69-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="06b69-120">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="06b69-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="06b69-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="06b69-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="06b69-122">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="06b69-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="06b69-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b69-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="06b69-124">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="06b69-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="06b69-125">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="06b69-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="06b69-126">Member</span><span class="sxs-lookup"><span data-stu-id="06b69-126">Members</span></span>

#### <span data-ttu-id="06b69-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="06b69-127">get_Handled</span></span> 

<span data-ttu-id="06b69-128">Ruft ab, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="06b69-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="06b69-129">öffentliche HRESULT- [get_Handled](#get_handled)(bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="06b69-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="06b69-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06b69-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="06b69-131">IsUserInitiated ist wahr, wenn die neue Fenster Anforderung durch eine Benutzergeste initiiert wurde, beispielsweisedurch klicken auf ein Anchor-Tag mit target.</span><span class="sxs-lookup"><span data-stu-id="06b69-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="06b69-132">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="06b69-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="06b69-133">Der Edge-Popupblocker ist für WebView deaktiviert, damit die APP dieses Flag verwenden kann, um nicht vom Benutzer initiierte Popups zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="06b69-133">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="06b69-134">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b69-134">get_NewWindow</span></span> 

<span data-ttu-id="06b69-135">Ruft das neue Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="06b69-135">Gets the new window.</span></span>

> <span data-ttu-id="06b69-136">öffentliche HRESULT- [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="06b69-136">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="06b69-137">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06b69-137">get_Uri</span></span> 

<span data-ttu-id="06b69-138">Der Ziel-URI des NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="06b69-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="06b69-139">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="06b69-139">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="06b69-140">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="06b69-140">get_WindowFeatures</span></span> 

<span data-ttu-id="06b69-141">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06b69-141">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="06b69-142">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="06b69-142">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="06b69-143">Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="06b69-143">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="06b69-144">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06b69-144">GetDeferral</span></span> 

<span data-ttu-id="06b69-145">Rufen Sie ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt ab, und setzen Sie das Ereignis in einen verzögerten Zustand.</span><span class="sxs-lookup"><span data-stu-id="06b69-145">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="06b69-146">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="06b69-146">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="06b69-147">Sie können das [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt verwenden, um die geöffnete Fenster Anforderung zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="06b69-147">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="06b69-148">Während dieses Ereignis verzögert wird, wird das Opener-Fenster eine WindowProxy zu einem unnavigierten Fenster zurückgegeben, das nach Abschluss der Verzögerungszeit navigiert.</span><span class="sxs-lookup"><span data-stu-id="06b69-148">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="06b69-149">put_Handled</span><span class="sxs-lookup"><span data-stu-id="06b69-149">put_Handled</span></span> 

<span data-ttu-id="06b69-150">Legt fest, ob die NewWindowRequestedEvent vom Host verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="06b69-150">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="06b69-151">öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)</span><span class="sxs-lookup"><span data-stu-id="06b69-151">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="06b69-152">Wenn dies falsch ist und kein Fenster festgelegt ist, wird die WebView ein Popupfenster geöffnet und als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06b69-152">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="06b69-153">Wenn Sie auf "true" festgelegt ist und kein Fenster für einen Window. Open-Aufruf festgelegt ist, wird das geöffnete WindowProxy-Objekt für ein Dummy Window-Objekt und es wird kein Fenster geladen.</span><span class="sxs-lookup"><span data-stu-id="06b69-153">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="06b69-154">Der Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="06b69-154">Default is false.</span></span>

#### <span data-ttu-id="06b69-155">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="06b69-155">put_NewWindow</span></span> 

<span data-ttu-id="06b69-156">Legt eine WebView als Ergebnis des NewWindowRequest fest.</span><span class="sxs-lookup"><span data-stu-id="06b69-156">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="06b69-157">öffentliche HRESULT- [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \*-Fenster)</span><span class="sxs-lookup"><span data-stu-id="06b69-157">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="06b69-158">Die Ziel-WebView sollte nicht navigiert werden.</span><span class="sxs-lookup"><span data-stu-id="06b69-158">The target WebView should not be navigated.</span></span> <span data-ttu-id="06b69-159">Wenn das Fenster "Fenster" eingestellt ist, wird das Fenster der obersten Ebene als geöffnetes WindowProxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06b69-159">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>
