---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 21c78d88237e525f6e0ff8d9c604cd023209599c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653801"
---
# <span data-ttu-id="55c1f-104">Schnittstellen ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="55c1f-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="55c1f-105">Ereignis-args für das NavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="55c1f-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="55c1f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="55c1f-106">Summary</span></span>

 <span data-ttu-id="55c1f-107">Member</span><span class="sxs-lookup"><span data-stu-id="55c1f-107">Members</span></span>                        | <span data-ttu-id="55c1f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="55c1f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="55c1f-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="55c1f-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="55c1f-110">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="55c1f-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="55c1f-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="55c1f-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="55c1f-112">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="55c1f-112">The ID of the navigation.</span></span>
[<span data-ttu-id="55c1f-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="55c1f-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="55c1f-114">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="55c1f-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="55c1f-115">Member</span><span class="sxs-lookup"><span data-stu-id="55c1f-115">Members</span></span>

#### <span data-ttu-id="55c1f-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="55c1f-116">get_IsSuccess</span></span> 

<span data-ttu-id="55c1f-117">"True", wenn die Navigation erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="55c1f-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="55c1f-118">öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool \* issuccess)</span><span class="sxs-lookup"><span data-stu-id="55c1f-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="55c1f-119">Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="55c1f-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="55c1f-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="55c1f-120">get_NavigationId</span></span> 

<span data-ttu-id="55c1f-121">Die ID der Navigation.</span><span class="sxs-lookup"><span data-stu-id="55c1f-121">The ID of the navigation.</span></span>

> <span data-ttu-id="55c1f-122">Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="55c1f-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="55c1f-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="55c1f-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="55c1f-124">Der Fehlercode, wenn die Navigation fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="55c1f-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="55c1f-125">öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="55c1f-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>
