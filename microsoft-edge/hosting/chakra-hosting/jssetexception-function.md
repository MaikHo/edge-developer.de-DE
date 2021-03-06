---
description: Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.
title: JsSetException-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568315"
---
# JsSetException-Funktion
Legt die Laufzeit des aktuellen Kontexts auf einen Ausnahmezustand fest.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Parameter  
 `exception`  
 Die JavaScript-Ausnahme, die für die Laufzeit des aktuellen Kontexts gesetzt werden soll.  
  
## Rückgabewert  
 `JsNoError` Wenn das Modul in einen Ausnahmezustand gesetzt wurde, wird andernfalls ein Fehlercode ausgelöst.  
  
## Hinweise  
 Wenn sich die Laufzeit des aktuellen Kontexts bereits in einem Ausnahmezustand befindet, gibt diese API zurück `JsErrorInExceptionState` .  
  
 Erfordert einen aktiven Skriptkontext.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)