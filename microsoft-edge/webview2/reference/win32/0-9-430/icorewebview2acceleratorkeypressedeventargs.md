---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 280df2816696ce4abce118976b3eb9abf76267e3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884414"
---
# 0.9.430-Interface-ICoreWebView2AcceleratorKeyPressedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Ereignis-args für das AcceleratorKeyPressed-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_KeyEventKind](#get_keyeventkind) | Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.
[get_VirtualKey](#get_virtualkey) | Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.
[get_KeyEventLParam](#get_keyeventlparam) | Der lParam-Wert, der die Fenstermeldung begleitet hat.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.
[get_Handled](#get_handled) | Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.
[put_Handled](#put_handled) | Legt die Handled-Eigenschaft fest.

## Member

#### get_KeyEventKind 

Der Key-Ereignistyp, der bewirkt hat, dass das Ereignis ausgelöst wird.

> Public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_VirtualKey 

Der virtuelle Win32-Tastencode des Schlüssels, der gedrückt oder freigegeben wurde.

> Public HRESULT [get_VirtualKey](#get_virtualkey)(uint * VirtualKey)

Hierbei handelt es sich um eine der virtuellen Win32-Schlüssel Konstanten wie VK_RETURN oder einen (Großbuchstaben) ASCII-Wert wie "A". Sie können überprüfen, ob STRG oder ALT gedrückt werden, indem Sie GetKeyState (VK_CONTROL) oder GetKeyState (VK_MENU) aufrufen.

#### get_KeyEventLParam 

Der lParam-Wert, der die Fenstermeldung begleitet hat.

> Public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * LPARAM)

Lesen Sie die Dokumentation zu den WM_KEYDOWN-und WM_KEYUP-Nachrichten.

#### get_PhysicalKeyStatus 

Eine Struktur, die die im LParam der Fenstermeldung übergebenen Informationen darstellt.

> Public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_Handled 

Während des AcceleratorKeyPressedEvent-Handler-Aufrufs wird die WebView-Warteschlange blockiert, wenn die Zugriffstaste vom Host verarbeitet wird oder nicht.

> öffentliche HRESULT- [get_Handled](#get_handled)(bool * Handled)

Wenn die Handled-Eigenschaft auf true festgelegt ist, wird dadurch verhindert, dass die WebView die Standardaktion für diese Zugriffstaste ausführt. Andernfalls führt WebView die Standardaktion für die Zugriffstasten Taste aus.

#### put_Handled 

Legt die Handled-Eigenschaft fest.

> öffentliche HRESULT- [put_Handled](#put_handled)(bool Handled)

