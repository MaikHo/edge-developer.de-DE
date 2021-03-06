---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: 0.9.515-WebView2 Win32 C++-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a4c354920022f344af44e887ec0a08b6ab892ab7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879954"
---
# 0.9.515 ⁠–⁠ Referenz (WebView2)  

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../webview2-api-reference.md) .

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webinhalte in Ihrer Anwendung unter Verwendung von [Microsoft Edge \ (Chrom \)](https://www.microsoftedgeinsider.com) als Rendering-Modul hosten.  Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge WebView2](../../index.md)) und [Erste Schritte mit WebView2](../../gettingstarted/win32.md).  [ICoreWebView2](0-9-488/ICoreWebView2.md) ist ein großartiger Ort, um mit dem Erlernen der Details der API zu beginnen.  

## Globals  

*   [Globals](0-9-488/webview2-idl.md)  

## Schnittstellen  
*   [ICoreWebView2](0-9-488/icorewebview2.md)
*   [ICoreWebView2Controller](0-9-488/icorewebview2controller.md)
*   [ICoreWebView2Deferral](0-9-488/icorewebview2deferral.md)
*   [ICoreWebView2DevToolsProtocolEventReceiver](0-9-488/icorewebview2devtoolsprotocoleventreceiver.md)
*   [ICoreWebView2Environment](0-9-488/icorewebview2environment.md)
*   [ICoreWebView2EnvironmentOptions](0-9-488/icorewebview2environmentoptions.md)
*   [ICoreWebView2HttpHeadersCollectionIterator](0-9-488/icorewebview2httpheaderscollectioniterator.md)
*   [ICoreWebView2HttpRequestHeaders](0-9-488/icorewebview2httprequestheaders.md)
*   [ICoreWebView2HttpResponseHeaders](0-9-488/icorewebview2httpresponseheaders.md)
*   [ICoreWebView2Settings](0-9-488/icorewebview2settings.md)
*   [ICoreWebView2WebResourceRequest](0-9-488/icorewebview2webresourcerequest.md)
*   [ICoreWebView2WebResourceResponse](0-9-488/icorewebview2webresourceresponse.md)

### Ereignisargumente

*   [ICoreWebView2AcceleratorKeyPressedEventArgs](0-9-488/icorewebview2acceleratorkeypressedeventargs.md)
*   [ICoreWebView2ContentLoadingEventArgs](0-9-488/icorewebview2contentloadingeventargs.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [ICoreWebView2MoveFocusRequestedEventArgs](0-9-488/icorewebview2movefocusrequestedeventargs.md)
*   [ICoreWebView2NavigationCompletedEventArgs](0-9-488/icorewebview2navigationcompletedeventargs.md)
*   [ICoreWebView2NavigationStartingEventArgs](0-9-488/icorewebview2navigationstartingeventargs.md)
*   [ICoreWebView2NewWindowRequestedEventArgs](0-9-488/icorewebview2newwindowrequestedeventargs.md)
*   [ICoreWebView2PermissionRequestedEventArgs](0-9-488/icorewebview2permissionrequestedeventargs.md)
*   [ICoreWebView2ProcessFailedEventArgs](0-9-488/icorewebview2processfailedeventargs.md)
*   [ICoreWebView2ScriptDialogOpeningEventArgs](0-9-488/icorewebview2scriptdialogopeningeventargs.md)
*   [ICoreWebView2SourceChangedEventArgs](0-9-488/icorewebview2sourcechangedeventargs.md)
*   [ICoreWebView2WebMessageReceivedEventArgs](0-9-488/icorewebview2webmessagereceivedeventargs.md)
*   [ICoreWebView2WebResourceRequestedEventArgs](0-9-488/icorewebview2webresourcerequestedeventargs.md)

### Delegaten

*   [ICoreWebView2AcceleratorKeyPressedEventHandler](0-9-488/icorewebview2acceleratorkeypressedeventhandler.md)
*   [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-9-488/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](0-9-488/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [ICoreWebView2CapturePreviewCompletedHandler](0-9-488/icorewebview2capturepreviewcompletedhandler.md)
*   [ICoreWebView2ContainsFullScreenElementChangedEventHandler](0-9-488/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [ICoreWebView2ContentLoadingEventHandler](0-9-488/icorewebview2contentloadingeventhandler.md)
*   [ICoreWebView2CreateCoreWebView2ControllerCompletedHandler](0-9-488/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](0-9-488/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventHandler](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [ICoreWebView2DocumentTitleChangedEventHandler](0-9-488/icorewebview2documenttitlechangedeventhandler.md)
*   [ICoreWebView2ExecuteScriptCompletedHandler](0-9-488/icorewebview2executescriptcompletedhandler.md)
*   [ICoreWebView2FocusChangedEventHandler](0-9-488/icorewebview2focuschangedeventhandler.md)
*   [ICoreWebView2HistoryChangedEventHandler](0-9-488/icorewebview2historychangedeventhandler.md)
*   [ICoreWebView2MoveFocusRequestedEventHandler](0-9-488/icorewebview2movefocusrequestedeventhandler.md)
*   [ICoreWebView2NavigationCompletedEventHandler](0-9-488/icorewebview2navigationcompletedeventhandler.md)
*   [ICoreWebView2NavigationStartingEventHandler](0-9-488/icorewebview2navigationstartingeventhandler.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventHandler](0-9-488/icorewebview2newbrowserversionavailableeventhandler.md)
*   [ICoreWebView2NewWindowRequestedEventHandler](0-9-488/icorewebview2newwindowrequestedeventhandler.md)
*   [ICoreWebView2PermissionRequestedEventHandler](0-9-488/icorewebview2permissionrequestedeventhandler.md)
*   [ICoreWebView2ProcessFailedEventHandler](0-9-488/icorewebview2processfailedeventhandler.md)
*   [ICoreWebView2ScriptDialogOpeningEventHandler](0-9-488/icorewebview2scriptdialogopeningeventhandler.md)
*   [ICoreWebView2SourceChangedEventHandler](0-9-488/icorewebview2sourcechangedeventhandler.md)
*   [ICoreWebView2WebMessageReceivedEventHandler](0-9-488/icorewebview2webmessagereceivedeventhandler.md)
*   [ICoreWebView2WebResourceRequestedEventHandler](0-9-488/icorewebview2webresourcerequestedeventhandler.md)
*   [ICoreWebView2WindowCloseRequestedEventHandler](0-9-488/icorewebview2windowcloserequestedeventhandler.md)
*   [ICoreWebView2ZoomFactorChangedEventHandler](0-9-488/icorewebview2zoomfactorchangedeventhandler.md)

### Experimentell

*   [ICoreWebView2ExperimentalCompositionController](0-9-488/icorewebview2experimentalcompositioncontroller.md)
*   [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](0-9-488/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [ICoreWebView2ExperimentalCursorChangedEventHandler](0-9-488/icorewebview2experimentalcursorchangedeventhandler.md)
*   [ICoreWebView2ExperimentalEnvironment](0-9-488/icorewebview2experimentalenvironment.md)
*   [ICoreWebView2ExperimentalPointerInfo](0-9-488/icorewebview2experimentalpointerinfo.md)
