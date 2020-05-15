---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a9cc4c9e2bd13509c25fa5f5faaa9fe65634b47b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653943"
---
# <span data-ttu-id="ef021-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef021-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ef021-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ef021-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ef021-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ef021-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="ef021-107">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ef021-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="ef021-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ef021-108">Summary</span></span>

 <span data-ttu-id="ef021-109">Member</span><span class="sxs-lookup"><span data-stu-id="ef021-109">Members</span></span>                        | <span data-ttu-id="ef021-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ef021-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef021-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef021-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ef021-112">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef021-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ef021-113">Member</span><span class="sxs-lookup"><span data-stu-id="ef021-113">Members</span></span>

#### <span data-ttu-id="ef021-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ef021-114">Invoke</span></span> 

<span data-ttu-id="ef021-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef021-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ef021-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ef021-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>
