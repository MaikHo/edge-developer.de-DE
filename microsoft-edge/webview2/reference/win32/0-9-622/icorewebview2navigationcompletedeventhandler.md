---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 3ff529c649eb455e8ea1b14ebbd25533631d2b99
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012140"
---
# <span data-ttu-id="cd5d6-104">Schnittstellen ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cd5d6-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="cd5d6-105">Der Aufrufer implementiert diese Schnittstelle, um das NavigationCompleted-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="cd5d6-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="cd5d6-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="cd5d6-106">Summary</span></span>

 <span data-ttu-id="cd5d6-107">Member</span><span class="sxs-lookup"><span data-stu-id="cd5d6-107">Members</span></span>                        | <span data-ttu-id="cd5d6-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="cd5d6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd5d6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cd5d6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cd5d6-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd5d6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="cd5d6-111">Member</span><span class="sxs-lookup"><span data-stu-id="cd5d6-111">Members</span></span>

#### <span data-ttu-id="cd5d6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cd5d6-112">Invoke</span></span> 

<span data-ttu-id="cd5d6-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd5d6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cd5d6-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="cd5d6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>
