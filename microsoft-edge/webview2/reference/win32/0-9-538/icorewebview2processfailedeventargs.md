---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879345"
---
# <span data-ttu-id="97521-104">Schnittstellen ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="97521-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="97521-105">Ereignis-args für das ProcessFailed-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="97521-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="97521-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97521-106">Summary</span></span>

 <span data-ttu-id="97521-107">Member</span><span class="sxs-lookup"><span data-stu-id="97521-107">Members</span></span>                        | <span data-ttu-id="97521-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="97521-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97521-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="97521-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="97521-110">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="97521-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="97521-111">Member</span><span class="sxs-lookup"><span data-stu-id="97521-111">Members</span></span>

#### <span data-ttu-id="97521-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="97521-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="97521-113">Der Typ des aufgetretenen Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="97521-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="97521-114">Public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="97521-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

