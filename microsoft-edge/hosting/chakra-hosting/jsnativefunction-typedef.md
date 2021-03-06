---
description: Ein Funktions Rückruf.
title: JsNativeFunction typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567220"
---
# JsNativeFunction typedef
Ein Funktions Rückruf.  
  
## Syntax  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Parameter  
 angerufenen  
 Ein `Function` Objekt, das die aufgerufene Funktion darstellt.  
  
 isConstructCall  
 Gibt an, ob es sich um einen regulären Anruf oder einen "neuen" Anruf handelt.  
  
 arguments  
 Die Argumente für den Anruf.  
  
 argumentCount  
 Die Anzahl von Argumenten.  
  
## Eigenschaftswert/Rückgabewert  
 Das Ergebnis des Anrufs (sofern vorhanden).  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)