---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 442bd26caeb78804ceb202b302123b0ee1127f09
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012136"
---
# <span data-ttu-id="2d83a-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="2d83a-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="2d83a-105">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2d83a-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="2d83a-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2d83a-106">Summary</span></span>

 <span data-ttu-id="2d83a-107">Member</span><span class="sxs-lookup"><span data-stu-id="2d83a-107">Members</span></span>                        | <span data-ttu-id="2d83a-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2d83a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d83a-109">Annehmen</span><span class="sxs-lookup"><span data-stu-id="2d83a-109">Accept</span></span>](#accept) | <span data-ttu-id="2d83a-110">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d83a-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="2d83a-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="2d83a-112">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="2d83a-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="2d83a-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="2d83a-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="2d83a-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="2d83a-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="2d83a-115">get_Message</span></span>](#get_message) | <span data-ttu-id="2d83a-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="2d83a-116">The message of the dialog box.</span></span>
[<span data-ttu-id="2d83a-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="2d83a-118">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="2d83a-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d83a-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2d83a-120">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2d83a-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="2d83a-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d83a-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2d83a-122">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d83a-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="2d83a-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="2d83a-124">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d83a-124">Set the ResultText property.</span></span>

## <span data-ttu-id="2d83a-125">Member</span><span class="sxs-lookup"><span data-stu-id="2d83a-125">Members</span></span>

#### <span data-ttu-id="2d83a-126">Annehmen</span><span class="sxs-lookup"><span data-stu-id="2d83a-126">Accept</span></span> 

<span data-ttu-id="2d83a-127">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d83a-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="2d83a-128">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="2d83a-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="2d83a-129">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="2d83a-130">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="2d83a-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="2d83a-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-131">get_DefaultText</span></span> 

<span data-ttu-id="2d83a-132">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="2d83a-133">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="2d83a-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="2d83a-134">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="2d83a-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="2d83a-135">get_Kind</span></span> 

<span data-ttu-id="2d83a-136">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="2d83a-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="2d83a-137">öffentliche HRESULT- [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="2d83a-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="2d83a-138">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="2d83a-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="2d83a-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="2d83a-139">get_Message</span></span> 

<span data-ttu-id="2d83a-140">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="2d83a-140">The message of the dialog box.</span></span>

> <span data-ttu-id="2d83a-141">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="2d83a-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="2d83a-142">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="2d83a-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="2d83a-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-143">get_ResultText</span></span> 

<span data-ttu-id="2d83a-144">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2d83a-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="2d83a-145">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="2d83a-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="2d83a-146">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2d83a-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="2d83a-147">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d83a-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="2d83a-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d83a-148">get_Uri</span></span> 

<span data-ttu-id="2d83a-149">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2d83a-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="2d83a-150">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2d83a-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2d83a-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2d83a-151">GetDeferral</span></span> 

<span data-ttu-id="2d83a-152">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d83a-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="2d83a-153">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="2d83a-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2d83a-154">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2d83a-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="2d83a-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="2d83a-155">put_ResultText</span></span> 

<span data-ttu-id="2d83a-156">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d83a-156">Set the ResultText property.</span></span>

> <span data-ttu-id="2d83a-157">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="2d83a-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>
