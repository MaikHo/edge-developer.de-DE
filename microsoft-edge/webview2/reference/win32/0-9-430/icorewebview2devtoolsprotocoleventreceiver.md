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
ms.openlocfilehash: 4c2c859525753a386134b2ae0145f4fdca4c37ae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653785"
---
# <span data-ttu-id="88345-104">Schnittstellen ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="88345-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

> [!NOTE]
> <span data-ttu-id="88345-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="88345-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="88345-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="88345-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="88345-107">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt, und Sie können dieses Ereignis abonnieren und abmelden.</span><span class="sxs-lookup"><span data-stu-id="88345-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubsribe from that event.</span></span>

## <span data-ttu-id="88345-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="88345-108">Summary</span></span>

 <span data-ttu-id="88345-109">Member</span><span class="sxs-lookup"><span data-stu-id="88345-109">Members</span></span>                        | <span data-ttu-id="88345-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="88345-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88345-111">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="88345-111">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="88345-112">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="88345-112">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="88345-113">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="88345-113">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="88345-114">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="88345-114">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="88345-115">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="88345-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="88345-116">Member</span><span class="sxs-lookup"><span data-stu-id="88345-116">Members</span></span>

#### <span data-ttu-id="88345-117">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="88345-117">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="88345-118">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="88345-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="88345-119">öffentliche HRESULT- [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="88345-119">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="88345-120">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="88345-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="88345-121">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="88345-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="88345-122">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="88345-122">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="88345-123">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="88345-123">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="88345-124">Public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="88345-124">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>
