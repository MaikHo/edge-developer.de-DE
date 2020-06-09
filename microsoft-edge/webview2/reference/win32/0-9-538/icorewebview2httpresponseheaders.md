---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 508ecacc867330c73132ae7e446b7483ea002f83
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698898"
---
# Schnittstellen ICoreWebView2HttpResponseHeaders 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

HTTP-Antwortheader.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Fügt Headerzeile mit Name und Wert an.
[Contains](#contains) | Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.
[GetHeader](#getheader) | Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.
[GetHeaders](#getheaders) | Ruft die Überschriften Werte ab, die dem Namen entsprechen.
[GetIterator](#getiterator) | Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.

Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.

## Member

#### AppendHeader 

Fügt Headerzeile mit Name und Wert an.

> Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)

#### Contains 

Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.

> Public HRESULT [Contains](#contains)(LPCWSTR Name, bool * Contains)

#### GetHeader 

Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.

> Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR *-Wert)

#### GetHeaders 

Ruft die Überschriften Werte ab, die dem Namen entsprechen.

> öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)

#### GetIterator 

Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.

> öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)
