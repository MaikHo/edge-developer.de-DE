---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: ee6886e32b32f4da4bbdc04fe6e866210a76488b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654150"
---
# <span data-ttu-id="320ee-104">Schnittstellen IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="320ee-104">interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="320ee-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="320ee-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="320ee-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="320ee-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="320ee-107">Ereignis-args für das NavigationStarting-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="320ee-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="320ee-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="320ee-108">Summary</span></span>

 <span data-ttu-id="320ee-109">Member</span><span class="sxs-lookup"><span data-stu-id="320ee-109">Members</span></span>                        | <span data-ttu-id="320ee-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="320ee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="320ee-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="320ee-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="320ee-112">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="320ee-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="320ee-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="320ee-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="320ee-114">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="320ee-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="320ee-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="320ee-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="320ee-116">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="320ee-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="320ee-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="320ee-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="320ee-118">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="320ee-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="320ee-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="320ee-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="320ee-120">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="320ee-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="320ee-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="320ee-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="320ee-122">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="320ee-122">Set the Cancel property.</span></span>

## <span data-ttu-id="320ee-123">Member</span><span class="sxs-lookup"><span data-stu-id="320ee-123">Members</span></span>

#### <span data-ttu-id="320ee-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="320ee-124">get_Uri</span></span> 

<span data-ttu-id="320ee-125">Der URI der angeforderten Navigation.</span><span class="sxs-lookup"><span data-stu-id="320ee-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="320ee-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="320ee-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="320ee-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="320ee-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="320ee-128">"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="320ee-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="320ee-129">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="320ee-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="320ee-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="320ee-130">get_IsRedirected</span></span> 

<span data-ttu-id="320ee-131">"True", wenn die Navigation umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="320ee-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="320ee-132">öffentliche HRESULT- [get_IsRedirected](#get_isredirected)(bool \* isumgeleitet)</span><span class="sxs-lookup"><span data-stu-id="320ee-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="320ee-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="320ee-133">get_RequestHeaders</span></span> 

<span data-ttu-id="320ee-134">Die HTTP-Anforderungsheader für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="320ee-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="320ee-135">Public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="320ee-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="320ee-136">Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="320ee-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="320ee-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="320ee-137">get_Cancel</span></span> 

<span data-ttu-id="320ee-138">Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="320ee-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="320ee-139">öffentliche HRESULT- [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="320ee-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="320ee-140">Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt.</span><span class="sxs-lookup"><span data-stu-id="320ee-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="320ee-141">Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert.</span><span class="sxs-lookup"><span data-stu-id="320ee-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="320ee-142">Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="320ee-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="320ee-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="320ee-143">put_Cancel</span></span> 

<span data-ttu-id="320ee-144">Festlegen der Cancel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="320ee-144">Set the Cancel property.</span></span>

> <span data-ttu-id="320ee-145">öffentliche HRESULT- [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="320ee-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>
