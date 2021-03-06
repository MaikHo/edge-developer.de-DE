---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012177"
---
# Schnittstellen ICoreWebView2EnvironmentOptions 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

Optionen zum Erstellen der WebView2-Umgebung

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_AdditionalBrowserArguments](#get_additionalbrowserarguments) | AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.
[get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount) | Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.
[get_Language](#get_language) | Die Standardsprache, mit der WebView ausgeführt wird.
[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion) | Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.
[put_AdditionalBrowserArguments](#put_additionalbrowserarguments) | Festlegen der AdditionalBrowserArguments-Eigenschaft
[put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount) | Festlegen der AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft
[put_Language](#put_language) | Festlegen der Language-Eigenschaft
[put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion) | Festlegen der TargetCompatibleBrowserVersion-Eigenschaft

Eine Standardimplementierung wird in WebView2EnvironmentOptions. h bereitgestellt.

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## Member

#### get_AdditionalBrowserArguments 

AdditionalBrowserArguments kann angegeben werden, um das Verhalten von WebView zu ändern.

> Public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR *-Wert)

Diese werden als Teil der Befehlszeile an den Browserprozess übergeben. Weitere Informationen zu Befehlszeilen wechseln in den Browserprozess finden Sie unter [Ausführen von Chrom mit Flags](https://aka.ms/RunChromiumWithFlags) . Wenn die APP mit einem Befehlszeilen Schalter gestartet wird, `--edge-webview-switches=xxx` wird der Wert dieses Schalters (xxx im obigen Beispiel) auch an die Befehlszeile des Browser Prozesses angefügt. Bestimmte Schalter wie `--user-data-dir` sind intern und wichtig für WebView. Diese Schalter werden ignoriert, auch wenn Sie angegeben werden. Wenn dieselben Schalter mehrmals angegeben werden, gewinnt der letzte. Es wird nicht versucht, die verschiedenen Werte desselben Schalters zusammenzuführen, mit Ausnahme von deaktivierten und aktivierten Features. Die Features, die von `--enable-features` und `--disable-features` mit einfacher Logik zusammengeführt werden: die Features sind die Vereinigung der angegebenen Features und integrierten Features, und wenn ein Feature deaktiviert ist, wird es aus der Liste der aktivierten Features entfernt. Der Befehlszeilenwert des App-Prozesses `--edge-webview-switches` wird verarbeitet, nachdem der additionalBrowserArguments-Parameter verarbeitet wurde. Bestimmte Features sind intern deaktiviert und können nicht aktiviert werden. Wenn die Analyse bei den angegebenen Schaltern fehlgeschlagen ist, werden Sie ignoriert. Standardmäßig wird der Browserprozess ohne zusätzliche Flags ausgeführt.

#### get_AllowSingleSignOnUsingOSPrimaryAccount 

Die AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft wird verwendet, um die einmalige Anmeldung mit Azure Active Directory (AAD)-Ressourcen in WebView unter Verwendung des angemeldeten Windows-Kontos und des einmaligen Anmeldens bei Websites zu aktivieren, die das Microsoft-Konto verwenden, das mit dem Anmeldenamen im Windows-Konto verknüpft ist.

> öffentliche HRESULT- [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(bool * Allow)

Standard ist deaktiviert. Universelle Windows-Plattform-apps müssen auch die [Eingeschränkte](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO-Funktion für das einmalige Anmelden deklarieren.

#### get_Language 

Die Standardsprache, mit der WebView ausgeführt wird.

> Public HRESULT [get_Language](#get_language)(LPWSTR *-Wert)

Sie bezieht sich auf Browser-UIs wie Kontextmenüs und Dialogfelder. Sie gilt auch für den HTTP-Header Accept-Languages, der von WebView an Websites gesendet wird. Das Format von `language[-country]` Where `language` ist der 2-Buchstaben-Code von ISO 639 und `country` der 2-Buchstaben-Code von ISO 3166.

#### get_TargetCompatibleBrowserVersion 

Die Version der Edge-WebView2-Runtime-Binärdateien, die für die Kompatibilität mit der aufrufenden Anwendung erforderlich sind.

> Public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR *-Wert)

Dies ist standardmäßig die Edge WebView2-Laufzeitversion, die der Version des SDK entspricht, das die Anwendung verwendet. Das Format dieses Werts entspricht dem Format der BrowserVersionString-Eigenschaft und anderen Browserversion-Werten. Nur der Versions Teil des Browserversion-Werts wird berücksichtigt. Wenn es vorhanden ist, wird das Kanal Suffix ignoriert. Die Version der tatsächlich verwendeten Edge-WebView2-Runtime-Binärdateien kann sich vom angegebenen TargetCompatibleBrowserVersion unterscheiden. Sie sind nur garantiert kompatibel. Sie können die aktuelle Version auf der BrowserVersionString-Eigenschaft auf der ICoreWebView2Environment-Eigenschaft überprüfen.

#### put_AdditionalBrowserArguments 

Festlegen der AdditionalBrowserArguments-Eigenschaft

> Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR-Wert)

#### put_AllowSingleSignOnUsingOSPrimaryAccount 

Festlegen der AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft

> öffentliche HRESULT- [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(bool Allow)

#### put_Language 

Festlegen der Language-Eigenschaft

> Public HRESULT [put_Language](#put_language)(LPCWSTR-Wert)

#### put_TargetCompatibleBrowserVersion 

Festlegen der TargetCompatibleBrowserVersion-Eigenschaft

> Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR-Wert)

