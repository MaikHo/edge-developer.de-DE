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
ms.openlocfilehash: 1041cd0f7dd38ed19adde19a4b7203141651d955
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654147"
---
# <span data-ttu-id="052bb-104">Schnittstellen IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="052bb-104">interface IWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="052bb-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="052bb-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="052bb-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="052bb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="052bb-107">Der Aufrufer implementiert diese Schnittstelle, um das NavigationStarting-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="052bb-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="052bb-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="052bb-108">Summary</span></span>

 <span data-ttu-id="052bb-109">Member</span><span class="sxs-lookup"><span data-stu-id="052bb-109">Members</span></span>                        | <span data-ttu-id="052bb-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="052bb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="052bb-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="052bb-111">Invoke</span></span>](#invoke) | <span data-ttu-id="052bb-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="052bb-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="052bb-113">Member</span><span class="sxs-lookup"><span data-stu-id="052bb-113">Members</span></span>

#### <span data-ttu-id="052bb-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="052bb-114">Invoke</span></span> 

<span data-ttu-id="052bb-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="052bb-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="052bb-116">öffentlicher HRESULT- [Aufruf](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="052bb-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationStartingEventArgs](IWebView2NavigationStartingEventArgs.md) \* args)</span></span>
