---
description: Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.
title: JsConvertValueToObject-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6a8b1a8933cdcaaf250a2e28ed8fc758ea66cc0e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567316"
---
# <span data-ttu-id="268f7-103">JsConvertValueToObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="268f7-103">JsConvertValueToObject Function</span></span>
<span data-ttu-id="268f7-104">Konvertiert den Wert mit der standardmäßigen JavaScript-Semantik in Object.</span><span class="sxs-lookup"><span data-stu-id="268f7-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="268f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="268f7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="268f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="268f7-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="268f7-107">Der Wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="268f7-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="268f7-108">Der konvertierte Wert.</span><span class="sxs-lookup"><span data-stu-id="268f7-108">The converted value.</span></span>  
  
## <span data-ttu-id="268f7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="268f7-109">Return Value</span></span>  
 <span data-ttu-id="268f7-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="268f7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="268f7-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="268f7-111">Remarks</span></span>  
 <span data-ttu-id="268f7-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="268f7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="268f7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="268f7-113">Requirements</span></span>  
 <span data-ttu-id="268f7-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="268f7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="268f7-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="268f7-115">See Also</span></span>  
 [<span data-ttu-id="268f7-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="268f7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)