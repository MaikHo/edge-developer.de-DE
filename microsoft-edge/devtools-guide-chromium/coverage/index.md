---
title: Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601719"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="9b4ba-103">Suchen von nicht verwendetem Javascript und CSS-Code mit der Registerkarte "Coverage" in Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9b4ba-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="9b4ba-104">Die Registerkarte Coverage in Microsoft Edge devtools hilft Ihnen, ungenutzte JavaScript-und CSS-Codes zu finden.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="9b4ba-105">Wenn Sie nicht verwendeten Code entfernen, können Sie das Laden der Seite beschleunigen und Ihre mobilen Benutzer mobil Daten speichern.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

> ##### <span data-ttu-id="9b4ba-106">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="9b4ba-106">Figure 1</span></span>  
> <span data-ttu-id="9b4ba-107">Analysieren der Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="9b4ba-107">Analyzing code coverage</span></span>  
> ![Analysieren der Codeabdeckung][ImageExample]  

> [!WARNING]
> <span data-ttu-id="9b4ba-109">Das Auffinden unbenutzten Codes ist relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="9b4ba-110">Das Umgestalten einer CodeBase, damit jede Seite nur das JavaScript und das CSS liefert, die Sie benötigt, ist möglicherweise schwierig.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="9b4ba-111">In diesem Leitfaden wird nicht behandelt, wie Sie eine CodeBase umgestalten, um nicht verwendeten Code zu vermeiden, da diese umgestalten in hohem Maße von Ihrem Technologiestapel abhängen.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="9b4ba-112">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9b4ba-112">Overview</span></span>   

<span data-ttu-id="9b4ba-113">Das Versenden unbenutzter JavaScript-oder CSS-Probleme ist ein häufiges Problem in der Webentwicklung.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="9b4ba-114">Nehmen wir beispielsweise an, dass Sie die [Bootstrap-Schaltflächenkomponente][BootstrapButtons] auf der Seite verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="9b4ba-115">Um die Button-Komponente zu verwenden, müssen Sie einen Link zum Bootstrap-Stylesheet in Ihrem HTML-Code hinzufügen, wie hier:</span><span class="sxs-lookup"><span data-stu-id="9b4ba-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="9b4ba-116">Dieses Stylesheet enthält nicht nur den Code für die Schaltflächenkomponente.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="9b4ba-117">Sie enthält das CSS für **alle** Bootstrap-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="9b4ba-118">Sie verwenden jedoch keine der anderen Bootstrap-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="9b4ba-119">Ihre Seite lädt also eine Reihe von CSS herunter, die nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="9b4ba-120">Dieses extra-CSS ist aus den folgenden Gründen ein Problem.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="9b4ba-121">Der zusätzliche Code verlangsamt das Laden der Seite.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-121">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="9b4ba-122">Wenn ein Benutzer auf die Seite auf einem mobilen Gerät zugreift, verwendet der zusätzliche Code Ihre zellularen Daten.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="9b4ba-123">Öffnen der Registerkarte "Abdeckung"</span><span class="sxs-lookup"><span data-stu-id="9b4ba-123">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="9b4ba-124">[Öffnen des Befehlsmenüs][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="9b4ba-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="9b4ba-125">Beginnen `coverage` Sie mit der Eingabe, wählen Sie den Befehl **Coverage anzeigen** aus, und drücken Sie dann `Enter` , um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-125">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="9b4ba-126">Die Registerkarte **Coverage** wird im **Einzug**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-126">The **Coverage** tab opens in the **Drawer**.</span></span>  

    > ##### <span data-ttu-id="9b4ba-127">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="9b4ba-127">Figure 2</span></span>  
    > <span data-ttu-id="9b4ba-128">Die Registerkarte " **Coverage** "</span><span class="sxs-lookup"><span data-stu-id="9b4ba-128">The **Coverage** tab</span></span>  
    > ![Die Registerkarte "Coverage"][ImageCoverage]  

## <span data-ttu-id="9b4ba-130">Aufzeichnen von Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="9b4ba-130">Record code coverage</span></span>   

1.  <span data-ttu-id="9b4ba-131">Klicken Sie auf der Registerkarte **Coverage** auf eine der folgenden Schaltflächen:</span><span class="sxs-lookup"><span data-stu-id="9b4ba-131">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="9b4ba-132">Klicken Sie auf **Instrumentations Abdeckung starten und Seiten** ![ Anfang Instrumentations Abdeckung und Reload erneut laden, ][ImageReloadIcon] Wenn Sie sehen möchten, welcher Code zum Laden der Seite erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-132">Click **Start Instrumenting Coverage And Reload Page** ![Start Instrumenting Coverage And Reload Page][ImageReloadIcon] if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="9b4ba-133">Klicken Sie auf **Instrument** Coverage ![ Instrumentation Coverage ][ImageRecordIcon] , wenn Sie sehen möchten, welcher Code nach der Interaktion mit der Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-133">Click **Instrument Coverage** ![Instrument Coverage][ImageRecordIcon] if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="9b4ba-134">Klicken Sie auf **Instrumentations Abdeckung beenden und Ergebnisse anzeigen** , ![ um die Abdeckung der Instrumentation zu beenden und Ergebnisse anzuzeigen, ][ImageStopIcon] Wenn Sie die Aufzeichnung der Codeabdeckung beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-134">Click **Stop Instrumenting Coverage And Show Results** ![Stop Instrumenting Coverage And Show Results][ImageStopIcon] when you want to stop recording code coverage.</span></span>  

## <span data-ttu-id="9b4ba-135">Analysieren der Codeabdeckung</span><span class="sxs-lookup"><span data-stu-id="9b4ba-135">Analyze code coverage</span></span>   

<span data-ttu-id="9b4ba-136">Die Tabelle auf der Registerkarte **Coverage** zeigt Ihnen, welche Ressourcen analysiert wurden und wie viel Code innerhalb der einzelnen Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-136">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span> <span data-ttu-id="9b4ba-137">Klicken Sie auf eine Zeile, um diese Ressource im **Quellen** Panel zu öffnen, und sehen Sie eine zeilenweise Aufschlüsselung von verwendetem Code und nicht verwendetem Code.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-137">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

> ##### <span data-ttu-id="9b4ba-138">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="9b4ba-138">Figure 3</span></span>  
> <span data-ttu-id="9b4ba-139">Code Coverage-Bericht</span><span class="sxs-lookup"><span data-stu-id="9b4ba-139">A code coverage report</span></span>  
> ![Code Coverage-Bericht][ImageExample]  

*   <span data-ttu-id="9b4ba-141">Die **URL** -Spalte ist die URL der Ressource, die analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-141">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="9b4ba-142">In der Spalte **Typ** wird angegeben, ob die Ressource CSS, JavaScript oder beides enthält.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-142">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="9b4ba-143">Die Spalte " **Gesamt Bytes** " gibt die Gesamtgröße der Ressource in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-143">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="9b4ba-144">Die Spalte "nicht **verwendete Bytes** " gibt die Anzahl der Bytes an, die nicht verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-144">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="9b4ba-145">Die letzte, unbenannte Spalte ist eine Visualisierung der Spalten **Gesamt Bytes** und **nicht verwendete Bytes** .</span><span class="sxs-lookup"><span data-stu-id="9b4ba-145">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="9b4ba-146">Der Rote Bereich der Leiste ist nicht verwendete Bytes.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-146">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="9b4ba-147">Der grüne Abschnitt wird in Bytes verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-147">The green section is used bytes.</span></span>  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Abbildung 1: Analysieren der Codeabdeckung"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Abbildung 2: Registerkarte "Coverage""  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Abbildung 3: ein Code Coverage-Bericht"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Schaltflächen – Bootstrap"  

> [!NOTE]
> <span data-ttu-id="9b4ba-153">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-153">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9b4ba-154">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/coverage/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b4ba-154">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="9b4ba-156">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b4ba-156">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  