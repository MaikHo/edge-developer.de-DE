---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 02128001f208f15d4e33c1f3f2cef6c8d662d357
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653991"
---
# <span data-ttu-id="536bf-104">Schnittstellen ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="536bf-104">interface ICoreWebView2Controller</span></span> 

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="536bf-105">Diese Schnittstelle ist der Besitzer des CoreWebView2-Objekts und bietet Unterstützung für die Größenänderung, das ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.</span><span class="sxs-lookup"><span data-stu-id="536bf-105">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="536bf-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="536bf-106">Summary</span></span>

 <span data-ttu-id="536bf-107">Member</span><span class="sxs-lookup"><span data-stu-id="536bf-107">Members</span></span>                        | <span data-ttu-id="536bf-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="536bf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="536bf-109">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="536bf-109">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="536bf-110">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-110">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="536bf-111">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-111">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="536bf-112">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-112">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="536bf-113">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-113">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="536bf-114">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-114">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="536bf-115">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="536bf-115">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="536bf-116">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-116">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="536bf-117">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-117">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="536bf-118">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-118">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="536bf-119">Schließen</span><span class="sxs-lookup"><span data-stu-id="536bf-119">Close</span></span>](#close) | <span data-ttu-id="536bf-120">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="536bf-120">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="536bf-121">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="536bf-121">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="536bf-122">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="536bf-122">The webview bounds.</span></span>
[<span data-ttu-id="536bf-123">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="536bf-123">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="536bf-124">Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-124">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="536bf-125">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="536bf-125">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="536bf-126">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="536bf-126">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="536bf-127">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="536bf-127">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="536bf-128">Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-128">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="536bf-129">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-129">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="536bf-130">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="536bf-130">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="536bf-131">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-131">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="536bf-132">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="536bf-132">Move focus into WebView.</span></span>
[<span data-ttu-id="536bf-133">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-133">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="536bf-134">Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="536bf-134">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="536bf-135">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="536bf-135">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="536bf-136">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="536bf-136">Set the Bounds property.</span></span>
[<span data-ttu-id="536bf-137">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="536bf-137">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="536bf-138">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="536bf-138">Set the IsVisible property.</span></span>
[<span data-ttu-id="536bf-139">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="536bf-139">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="536bf-140">Das übergeordnete Fenster für die WebView-Ansicht einrichten</span><span class="sxs-lookup"><span data-stu-id="536bf-140">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="536bf-141">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-141">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="536bf-142">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="536bf-142">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="536bf-143">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="536bf-143">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="536bf-144">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-144">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="536bf-145">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-145">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="536bf-146">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-146">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="536bf-147">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-147">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="536bf-148">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-148">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="536bf-149">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="536bf-149">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="536bf-150">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-150">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="536bf-151">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-151">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="536bf-152">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-152">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="536bf-153">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-153">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="536bf-154">Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="536bf-154">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="536bf-155">Die CoreWebView2Controller besitzt den CoreWebView2, und wenn alle Verweise auf die CoreWebView2Controller verschwindet, wird die WebView geschlossen.</span><span class="sxs-lookup"><span data-stu-id="536bf-155">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="536bf-156">Member</span><span class="sxs-lookup"><span data-stu-id="536bf-156">Members</span></span>

#### <span data-ttu-id="536bf-157">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="536bf-157">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="536bf-158">Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-158">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="536bf-159">Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-159">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="536bf-160">AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-160">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="536bf-161">Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:</span><span class="sxs-lookup"><span data-stu-id="536bf-161">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="536bf-162">STRG oder alt wird derzeit gehalten, oder</span><span class="sxs-lookup"><span data-stu-id="536bf-162">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="536bf-163">die Taste gedrückt wird einem Zeichen nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="536bf-163">the pressed key does not map to a character.</span></span> <span data-ttu-id="536bf-164">Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="536bf-164">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="536bf-165">Die Escape-Taste wird immer als Beschleuniger angesehen.</span><span class="sxs-lookup"><span data-stu-id="536bf-165">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="536bf-166">Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="536bf-166">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="536bf-167">Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="536bf-167">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="536bf-168">Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="536bf-168">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="536bf-169">Bis Sie Handle () für die Ereignis-args aufrufen oder der Ereignishandler zurückgibt, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl.</span><span class="sxs-lookup"><span data-stu-id="536bf-169">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="536bf-170">Allerdings funktionieren alle CoreWebView2-API-Methoden.</span><span class="sxs-lookup"><span data-stu-id="536bf-170">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="536bf-171">Im Fenstermodus wird der Ereignishandler asynchron aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="536bf-171">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="536bf-172">Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handle () aufgerufen wird, der Browserprozess selbst jedoch nicht blockiert wird und ausgehende com-Aufrufe normal funktionieren.</span><span class="sxs-lookup"><span data-stu-id="536bf-172">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="536bf-173">Es wird empfohlen, handle (true) so früh wie möglich aufzurufen, wenn Sie wissen, dass Sie die Zugriffstasten Taste behandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="536bf-173">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="536bf-174">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-174">add_GotFocus</span></span> 

<span data-ttu-id="536bf-175">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-175">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="536bf-176">Public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-176">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="536bf-177">GotFocus wird ausgelöst, wenn WebView den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="536bf-177">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="536bf-178">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-178">add_LostFocus</span></span> 

<span data-ttu-id="536bf-179">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-179">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="536bf-180">Public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-180">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="536bf-181">LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="536bf-181">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="536bf-182">In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-182">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="536bf-183">Der verlorene Fokus wird erst dann ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.</span><span class="sxs-lookup"><span data-stu-id="536bf-183">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="536bf-184">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="536bf-184">add_MoveFocusRequested</span></span> 

<span data-ttu-id="536bf-185">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-185">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="536bf-186">Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-186">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="536bf-187">MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="536bf-187">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="536bf-188">Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-188">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="536bf-189">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-189">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="536bf-190">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="536bf-190">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="536bf-191">Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-191">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="536bf-192">Das Ereignis wird ausgelöst, wenn die ZoomFactor-Eigenschaft des WebView geändert wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-192">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="536bf-193">Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat.</span><span class="sxs-lookup"><span data-stu-id="536bf-193">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="536bf-194">Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="536bf-194">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="536bf-195">WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu.</span><span class="sxs-lookup"><span data-stu-id="536bf-195">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="536bf-196">Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="536bf-196">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="536bf-197">Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem ContentLoading-Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="536bf-197">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="536bf-198">Schließen</span><span class="sxs-lookup"><span data-stu-id="536bf-198">Close</span></span> 

<span data-ttu-id="536bf-199">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="536bf-199">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="536bf-200">Public HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="536bf-200">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="536bf-201">Beim Bereinigen der Browserinstanz werden die Ressourcen freigegeben, die die WebView-Ansicht auslösen.</span><span class="sxs-lookup"><span data-stu-id="536bf-201">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="536bf-202">Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="536bf-202">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="536bf-203">Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="536bf-203">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="536bf-204">Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-204">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="536bf-205">Close wird implizit aufgerufen, wenn die CoreWebView2Controller den endgültigen Bezug verliert und zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-205">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="536bf-206">Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="536bf-206">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="536bf-207">Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="536bf-207">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="536bf-208">Durch das Aufrufen von Close wird dieser Zyklus unterbrochen, indem alle Ereignishandler freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="536bf-208">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="536bf-209">Um dies zu vermeiden, empfiehlt es sich, sowohl explizit Close für die WebView zu verwenden als auch einen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="536bf-209">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="536bf-210">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="536bf-210">get_Bounds</span></span> 

<span data-ttu-id="536bf-211">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="536bf-211">The webview bounds.</span></span>

> <span data-ttu-id="536bf-212">öffentliche HRESULT- [get_Bounds](#get_bounds)(Rect \* bounds)</span><span class="sxs-lookup"><span data-stu-id="536bf-212">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="536bf-213">Begrenzungen sind relativ zum übergeordneten HWND.</span><span class="sxs-lookup"><span data-stu-id="536bf-213">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="536bf-214">Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:</span><span class="sxs-lookup"><span data-stu-id="536bf-214">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="536bf-215">Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-215">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="536bf-216">Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll.</span><span class="sxs-lookup"><span data-stu-id="536bf-216">Position this window where the WebView should be.</span></span> <span data-ttu-id="536bf-217">Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).</span><span class="sxs-lookup"><span data-stu-id="536bf-217">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="536bf-218">Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND.</span><span class="sxs-lookup"><span data-stu-id="536bf-218">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="536bf-219">Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-219">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="536bf-220">Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.</span><span class="sxs-lookup"><span data-stu-id="536bf-220">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="536bf-221">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="536bf-221">get_CoreWebView2</span></span> 

<span data-ttu-id="536bf-222">Ruft das CoreWebView2 ab, das diesem CoreWebView2Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-222">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="536bf-223">Public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="536bf-223">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="536bf-224">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="536bf-224">get_IsVisible</span></span> 

<span data-ttu-id="536bf-225">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="536bf-225">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="536bf-226">öffentliche HRESULT- [get_IsVisible](#get_isvisible)(bool \* isVisible)</span><span class="sxs-lookup"><span data-stu-id="536bf-226">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="536bf-227">Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="536bf-227">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="536bf-228">Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateCoreWebView2Controller übergeben wurde).</span><span class="sxs-lookup"><span data-stu-id="536bf-228">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="536bf-229">Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="536bf-229">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="536bf-230">WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-230">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="536bf-231">Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-231">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="536bf-232">Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="536bf-232">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="536bf-233">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="536bf-233">get_ParentWindow</span></span> 

<span data-ttu-id="536bf-234">Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-234">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="536bf-235">öffentliche HRESULT- [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="536bf-235">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="536bf-236">Diese API gibt zunächst das Fenster zurück, das an CreateCoreWebView2Controller übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-236">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="536bf-237">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-237">get_ZoomFactor</span></span> 

<span data-ttu-id="536bf-238">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="536bf-238">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="536bf-239">öffentliche HRESULT- [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="536bf-239">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="536bf-240">Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann.</span><span class="sxs-lookup"><span data-stu-id="536bf-240">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="536bf-241">Ein Zoomfaktor, der vom Host durch Aufrufen von ZoomFactor angewendet wird, wird zum neuen Standardzoom für die WebView.</span><span class="sxs-lookup"><span data-stu-id="536bf-241">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="536bf-242">Dieser Zoomfaktor gilt für alle Navigationselemente und der Zoomfaktor WebView wird zurückgegeben, wenn der Benutzer STRG + 0 drückt.</span><span class="sxs-lookup"><span data-stu-id="536bf-242">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="536bf-243">Wenn der Zoomfaktor vom Benutzer geändert wird (was im App-Empfang ZoomFactorChanged), gilt dieser Zoom nur für die aktuelle Seite.</span><span class="sxs-lookup"><span data-stu-id="536bf-243">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="536bf-244">Der Zoom eines Benutzers, der angewendet wird, ist nur für die aktuelle Seite vorgesehen und wird in einer Navigation zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="536bf-244">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="536bf-245">Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="536bf-245">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="536bf-246">WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich.</span><span class="sxs-lookup"><span data-stu-id="536bf-246">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="536bf-247">Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="536bf-247">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="536bf-248">Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="536bf-248">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="536bf-249">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-249">MoveFocus</span></span> 

<span data-ttu-id="536bf-250">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="536bf-250">Move focus into WebView.</span></span>

> <span data-ttu-id="536bf-251">öffentliche HRESULT- [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON Grund)</span><span class="sxs-lookup"><span data-stu-id="536bf-251">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="536bf-252">WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-252">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="536bf-253">Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-253">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="536bf-254">Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="536bf-254">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="536bf-255">Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="536bf-255">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="536bf-256">WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste.</span><span class="sxs-lookup"><span data-stu-id="536bf-256">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="536bf-257">Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist.</span><span class="sxs-lookup"><span data-stu-id="536bf-257">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="536bf-258">Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="536bf-258">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="536bf-259">Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht.</span><span class="sxs-lookup"><span data-stu-id="536bf-259">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="536bf-260">Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.</span><span class="sxs-lookup"><span data-stu-id="536bf-260">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="536bf-261">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-261">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="536bf-262">Hierbei handelt es sich um eine Benachrichtigung, die sich von den Grenzen unterscheidet, die WebView das übergeordnete HWND (oder ein Vorgänger) verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="536bf-262">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="536bf-263">Public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="536bf-263">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="536bf-264">Dies ist für die Barrierefreiheit und bestimmte Dialogfelder in WebView erforderlich, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="536bf-264">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="536bf-265">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="536bf-265">put_Bounds</span></span> 

<span data-ttu-id="536bf-266">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="536bf-266">Set the Bounds property.</span></span>

> <span data-ttu-id="536bf-267">öffentliche HRESULT- [put_Bounds](#put_bounds)(Rect-Begrenzungen)</span><span class="sxs-lookup"><span data-stu-id="536bf-267">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="536bf-268">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="536bf-268">put_IsVisible</span></span> 

<span data-ttu-id="536bf-269">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="536bf-269">Set the IsVisible property.</span></span>

> <span data-ttu-id="536bf-270">öffentliche HRESULT- [put_IsVisible](#put_isvisible)(bool isVisible)</span><span class="sxs-lookup"><span data-stu-id="536bf-270">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="536bf-271">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="536bf-271">put_ParentWindow</span></span> 

<span data-ttu-id="536bf-272">Das übergeordnete Fenster für die WebView-Ansicht einrichten</span><span class="sxs-lookup"><span data-stu-id="536bf-272">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="536bf-273">Public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="536bf-273">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="536bf-274">Dies bewirkt, dass die WebView das Fenster des neu bereitgestellten Fensters erneut übermittelt.</span><span class="sxs-lookup"><span data-stu-id="536bf-274">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="536bf-275">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-275">put_ZoomFactor</span></span> 

<span data-ttu-id="536bf-276">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="536bf-276">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="536bf-277">öffentliche HRESULT- [put_ZoomFactor](#put_zoomfactor)(Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="536bf-277">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="536bf-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="536bf-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="536bf-279">Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="536bf-280">Public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="536bf-281">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-281">remove_GotFocus</span></span> 

<span data-ttu-id="536bf-282">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-282">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="536bf-283">Public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-283">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="536bf-284">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="536bf-284">remove_LostFocus</span></span> 

<span data-ttu-id="536bf-285">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-285">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="536bf-286">Public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-286">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="536bf-287">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="536bf-287">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="536bf-288">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-288">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="536bf-289">Public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-289">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="536bf-290">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="536bf-290">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="536bf-291">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="536bf-291">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="536bf-292">Public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="536bf-292">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="536bf-293">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="536bf-293">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="536bf-294">Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="536bf-294">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="536bf-295">öffentliche HRESULT- [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(Rect-Begrenzungen, Doppel ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="536bf-295">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="536bf-296">Dieser Vorgang ist aus der Perspektive des Hosts atomar.</span><span class="sxs-lookup"><span data-stu-id="536bf-296">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="536bf-297">Nach der Rückgabe von dieser Funktion werden die Bounds-Eigenschaft und die ZoomFactor-Eigenschaft beide aktualisiert, wenn die Funktion erfolgreich ist, oder keine wird aktualisiert, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="536bf-297">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="536bf-298">Wenn Grenz-und ZoomFactor sowohl auf der gleichen Skala aktualisiert werden (d. h., dass die Begrenzungen und ZoomFactor beide verdoppelt werden), wird der Seite keine Änderung in Window. InnereBreite/InnereHoehe angezeigt, und die WebView rendert den Inhalt mit der neuen Größe und zoomt ohne zwischen Renderings.</span><span class="sxs-lookup"><span data-stu-id="536bf-298">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="536bf-299">Diese Funktion kann auch verwendet werden, um nur eine von ZoomFactor oder Begrenzungen zu aktualisieren, indem der neue Wert für einen und der aktuelle Wert für den anderen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="536bf-299">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```
