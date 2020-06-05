---
description: Erstellt ein neues JavaScript-URIError-Fehlerobjekt.
title: JsCreateURIError-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5188827cd0b89b1dd6b54af005f6e118c4ae4c94
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567278"
---
# <span data-ttu-id="5d518-103">JsCreateURIError-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d518-103">JsCreateURIError Function</span></span>
<span data-ttu-id="5d518-104">Erstellt ein neues JavaScript-URIError-Fehlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="5d518-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="5d518-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d518-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="5d518-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d518-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="5d518-107">Meldung für das Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d518-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="5d518-108">Das neue Error-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d518-108">The new error object.</span></span>  
  
## <span data-ttu-id="5d518-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d518-109">Return Value</span></span>  
 <span data-ttu-id="5d518-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5d518-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5d518-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d518-111">Remarks</span></span>  
 <span data-ttu-id="5d518-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="5d518-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5d518-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d518-113">Requirements</span></span>  
 <span data-ttu-id="5d518-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5d518-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5d518-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d518-115">See Also</span></span>  
 [<span data-ttu-id="5d518-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="5d518-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)