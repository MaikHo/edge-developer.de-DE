---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 5d906c85cf36ccf270d9af342e329e1d969ff494
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012153"
---
# <span data-ttu-id="e2708-104">Schnittstellen ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e2708-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e2708-105">Der Aufrufer implementiert diese Schnittstelle, um das PermissionRequested-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e2708-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="e2708-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e2708-106">Summary</span></span>

 <span data-ttu-id="e2708-107">Member</span><span class="sxs-lookup"><span data-stu-id="e2708-107">Members</span></span>                        | <span data-ttu-id="e2708-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e2708-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e2708-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2708-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e2708-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2708-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e2708-111">Member</span><span class="sxs-lookup"><span data-stu-id="e2708-111">Members</span></span>

#### <span data-ttu-id="e2708-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e2708-112">Invoke</span></span> 

<span data-ttu-id="e2708-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2708-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e2708-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e2708-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>
