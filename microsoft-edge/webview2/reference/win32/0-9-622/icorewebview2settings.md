---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012125"
---
# Schnittstellen ICoreWebView2Settings 

```
interface ICoreWebView2Settings
  : public IUnknown
```

Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.
[get_AreHostObjectsAllowed](#get_arehostobjectsallowed) | Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.
[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled) | Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.
[get_IsScriptEnabled](#get_isscriptenabled) | Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Festlegen der AreDefaultContextMenusEnabled-Eigenschaft
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Festlegen der AreDevToolsEnabled-Eigenschaft
[put_AreHostObjectsAllowed](#put_arehostobjectsallowed) | Festlegen der AreHostObjectsAllowed-Eigenschaft
[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled) | Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft
[put_IsScriptEnabled](#put_isscriptenabled) | Festlegen der IsScriptEnabled-Eigenschaft
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Festlegen der IsStatusBarEnabled-Eigenschaft
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Festlegen der IsWebMessageEnabled-Eigenschaft
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Festlegen der IsZoomControlEnabled-Eigenschaft

Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.

## Member

#### get_AreDefaultContextMenusEnabled 

Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.

> öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool * enabled)

Standardmäßig ist dies der Fall.

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled wird beim Laden eines neuen HTML-Dokuments verwendet.

> Public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Wenn Sie auf "false" festgelegt ist, rendert WebView das Standarddialogfeld für JavaScript nicht (insbesondere diejenigen, die durch die JavaScript-Benachrichtigung, Bestätigungs-, Eingabe Aufforderungs Funktionen und beforeunload-Ereignis angezeigt werden). Wenn ein Ereignishandler über add_ScriptDialogOpening festgesetzt wird, sendet WebView ein Ereignis, das alle Informationen für das Dialogfeld enthält, und es der Host-App gestatten, eine eigene benutzerdefinierte Benutzeroberfläche anzuzeigen. Standardmäßig ist dies der Fall.

#### get_AreDevToolsEnabled 

AreDevToolsEnabled steuert, ob der Benutzer das Kontextmenü oder Tastenkombinationen verwenden kann, um das devtools-Fenster zu öffnen.

> Public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool * AreDevToolsEnabled)

Standardmäßig ist dies der Fall.

#### get_AreHostObjectsAllowed 

Die AreHostObjectsAllowed-Eigenschaft wird verwendet, um zu steuern, ob auf Hostobjekte über die Seite in WebView zugegriffen werden kann.

> öffentliche HRESULT- [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(bool * zulässig)

Standardmäßig ist dies der Fall.

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsBuiltInErrorPageEnabled 

Die IsBuiltInErrorPageEnabled-Eigenschaft wird verwendet, um die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler zu deaktivieren.

> öffentliche HRESULT- [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(bool * enabled)

Standardmäßig ist dies der Fall. Wenn diese Option deaktiviert ist, wird leere Seite angezeigt, wenn ein verwandter Fehler auftritt.

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsScriptEnabled 

Steuert, ob die JavaScript-Ausführung in allen zukünftigen Navigationselementen in der WebView aktiviert ist.

> Public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool * IsScriptEnabled)

Dies wirkt sich nur auf Skripts im Dokument aus. mit executeScript injizierte Skripts werden auch dann ausgeführt, wenn das Skript deaktiviert ist. Standardmäßig ist dies der Fall.

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### get_IsStatusBarEnabled 

IsStatusBarEnabled steuert, ob die Statusleiste angezeigt wird.

> Public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool * IsStatusBarEnabled)

Die Statusleiste wird normalerweise in der unteren linken Ecke der WebView angezeigt und zeigt Elemente wie den URI eines Links an, wenn der Benutzer darüber schwebt, und weitere Informationen. Standardmäßig ist dies der Fall.

#### get_IsWebMessageEnabled 

Die IsWebMessageEnabled-Eigenschaft wird beim Laden eines neuen HTML-Dokuments verwendet.

> Public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool * IsWebMessageEnabled)

Wenn Sie auf "true" festgelegt ist, ist die Kommunikation zwischen dem Host und dem HTML-Dokument der obersten Ebene der WebView über das PostWebMessageAsJson-, PostWebMessageAsString-und Window. Chrome. WebView-Nachrichtenereignis zulässig (Weitere Informationen finden Sie in der PostWebMessageAsJson-Dokumentation). Die Kommunikation vom HTML-Dokument der WebView-Oberfläche zum Host ist über die Funktion "PostMessage" von Window. Chrome. WebView und die add_WebMessageReceived-Methode möglich (Weitere Informationen finden Sie unter add_WebMessageReceived-Dokumentation). Wenn Sie auf "false" festgelegt ist, ist die Kommunikation nicht zulässig. Bei PostWebMessageAsJson und PostWebMessageAsString tritt ein Fehler auf, wenn E_ACCESSDENIED und Window. Chrome. WebView. PostMessage fehlschlägt, indem Sie eine Instanz eines Error-Objekts auslösen. Standardmäßig ist dies der Fall.

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### get_IsZoomControlEnabled 

Die IsZoomControlEnabled-Eigenschaft wird verwendet, um zu verhindern, dass der Benutzer den Zoom des WebView-Effekts beeinflusst.

> öffentliche HRESULT- [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(bool * enabled)

Standardmäßig ist dies der Fall. Wenn diese Option deaktiviert ist, kann der Benutzer nicht mehr mit STRG +/-oder STRG + Mausrad zoomen, aber der Zoom kann über die ZoomFactor-API eingestellt werden.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Festlegen der AreDefaultContextMenusEnabled-Eigenschaft

> öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)

#### put_AreDefaultScriptDialogsEnabled 

Festlegen der AreDefaultScriptDialogsEnabled-Eigenschaft

> Public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(bool AreDefaultScriptDialogsEnabled)

#### put_AreDevToolsEnabled 

Festlegen der AreDevToolsEnabled-Eigenschaft

> Public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(bool AreDevToolsEnabled)

#### put_AreHostObjectsAllowed 

Festlegen der AreHostObjectsAllowed-Eigenschaft

> öffentliche HRESULT- [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(bool Allowed)

#### put_IsBuiltInErrorPageEnabled 

Festlegen der IsBuiltInErrorPageEnabled-Eigenschaft

> öffentliche HRESULT- [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(bool enabled)

#### put_IsScriptEnabled 

Festlegen der IsScriptEnabled-Eigenschaft

> Public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(bool IsScriptEnabled)

#### put_IsStatusBarEnabled 

Festlegen der IsStatusBarEnabled-Eigenschaft

> Public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(bool IsStatusBarEnabled)

#### put_IsWebMessageEnabled 

Festlegen der IsWebMessageEnabled-Eigenschaft

> Public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(bool IsWebMessageEnabled)

#### put_IsZoomControlEnabled 

Festlegen der IsZoomControlEnabled-Eigenschaft

> öffentliche HRESULT- [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(bool enabled)

