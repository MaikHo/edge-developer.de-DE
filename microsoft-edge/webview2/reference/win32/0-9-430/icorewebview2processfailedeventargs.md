---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877737"
---
# <span data-ttu-id="6c30f-104">0.9.430-Interface-ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6c30f-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6c30f-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6c30f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6c30f-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6c30f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="6c30f-107">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6c30f-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="6c30f-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6c30f-108">Summary</span></span>

 <span data-ttu-id="6c30f-109">Member</span><span class="sxs-lookup"><span data-stu-id="6c30f-109">Members</span></span>                        | <span data-ttu-id="6c30f-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6c30f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c30f-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="6c30f-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="6c30f-112">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6c30f-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="6c30f-113">Member</span><span class="sxs-lookup"><span data-stu-id="6c30f-113">Members</span></span>

#### <span data-ttu-id="6c30f-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="6c30f-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="6c30f-115">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6c30f-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="6c30f-116">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="6c30f-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

