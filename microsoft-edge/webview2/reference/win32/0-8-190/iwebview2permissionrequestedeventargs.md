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
ms.openlocfilehash: 9d16f1c72a3921b220bd0046e78ed0c6b32a718a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653933"
---
# <span data-ttu-id="f7c5b-104">Schnittstellen IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f7c5b-104">interface IWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f7c5b-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f7c5b-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f7c5b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f7c5b-107">Ereignis-args für das PermissionRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="f7c5b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="f7c5b-108">Summary</span></span>

 <span data-ttu-id="f7c5b-109">Member</span><span class="sxs-lookup"><span data-stu-id="f7c5b-109">Members</span></span>                        | <span data-ttu-id="f7c5b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f7c5b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7c5b-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f7c5b-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f7c5b-112">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="f7c5b-113">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="f7c5b-113">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="f7c5b-114">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="f7c5b-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f7c5b-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="f7c5b-116">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="f7c5b-117">get_State</span><span class="sxs-lookup"><span data-stu-id="f7c5b-117">get_State</span></span>](#get_state) | <span data-ttu-id="f7c5b-118">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="f7c5b-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="f7c5b-119">put_State</span><span class="sxs-lookup"><span data-stu-id="f7c5b-119">put_State</span></span>](#put_state) | <span data-ttu-id="f7c5b-120">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-120">Set the State property.</span></span>
[<span data-ttu-id="f7c5b-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f7c5b-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f7c5b-122">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-122">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="f7c5b-123">Member</span><span class="sxs-lookup"><span data-stu-id="f7c5b-123">Members</span></span>

#### <span data-ttu-id="f7c5b-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f7c5b-124">get_Uri</span></span> 

<span data-ttu-id="f7c5b-125">Der Ursprung des Webinhalts, der die Berechtigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="f7c5b-126">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f7c5b-127">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="f7c5b-127">get_PermissionType</span></span> 

<span data-ttu-id="f7c5b-128">Der Typ der angeforderten Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="f7c5b-129">Public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-129">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="f7c5b-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f7c5b-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="f7c5b-131">"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="f7c5b-132">Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="f7c5b-133">Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="f7c5b-134">get_State</span><span class="sxs-lookup"><span data-stu-id="f7c5b-134">get_State</span></span> 

<span data-ttu-id="f7c5b-135">Der Status einer Berechtigungs Anfrage, also</span><span class="sxs-lookup"><span data-stu-id="f7c5b-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="f7c5b-136">Public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-136">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="f7c5b-137">Gibt an, ob die Anforderung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-137">whether the request is granted.</span></span> <span data-ttu-id="f7c5b-138">Der Standardwert ist WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-138">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="f7c5b-139">put_State</span><span class="sxs-lookup"><span data-stu-id="f7c5b-139">put_State</span></span> 

<span data-ttu-id="f7c5b-140">Legt die State-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-140">Set the State property.</span></span>

> <span data-ttu-id="f7c5b-141">Public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE Wert)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-141">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="f7c5b-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f7c5b-142">GetDeferral</span></span> 

<span data-ttu-id="f7c5b-143">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-143">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="f7c5b-144">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="f7c5b-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f7c5b-145">Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.</span><span class="sxs-lookup"><span data-stu-id="f7c5b-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>
