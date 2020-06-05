---
description: Ruft die interne Datengruppe in JsrtContext ab.
title: JsGetContextData-Funktion | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd85ccbc4008897643ec3840e8cdeca3611a50c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567268"
---
# <span data-ttu-id="dc30d-103">JsGetContextData-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc30d-103">JsGetContextData Function</span></span>
<span data-ttu-id="dc30d-104">Ruft die interne Datengruppe in JsrtContext ab.</span><span class="sxs-lookup"><span data-stu-id="dc30d-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="dc30d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc30d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="dc30d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc30d-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="dc30d-107">Der Kontext, aus dem die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc30d-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="dc30d-108">Der Zeiger auf die Daten, in die Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc30d-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="dc30d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc30d-109">Return Value</span></span>  
 <span data-ttu-id="dc30d-110">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dc30d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dc30d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc30d-111">Remarks</span></span>  
 <span data-ttu-id="dc30d-112">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="dc30d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dc30d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc30d-113">Requirements</span></span>  
 <span data-ttu-id="dc30d-114">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dc30d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dc30d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc30d-115">See Also</span></span>  
 [<span data-ttu-id="dc30d-116">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="dc30d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)