---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 37a7d89dbd7d13befe5a07c72fc8baa750775108
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012150"
---
# <span data-ttu-id="5dbab-104">Globals</span><span class="sxs-lookup"><span data-stu-id="5dbab-104">Globals</span></span> 

## <span data-ttu-id="5dbab-105">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5dbab-105">Summary</span></span>

 <span data-ttu-id="5dbab-106">Member</span><span class="sxs-lookup"><span data-stu-id="5dbab-106">Members</span></span>                        | <span data-ttu-id="5dbab-107">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="5dbab-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dbab-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="5dbab-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="5dbab-109">Diese Methode ist für alle Personen, die die Version richtig vergleichen möchten, um zu ermitteln, welche Version neuer, älter oder gleich ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="5dbab-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="5dbab-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="5dbab-111">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="5dbab-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="5dbab-112">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="5dbab-112">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="5dbab-113">DLL-Export zum Erstellen einer WebView2-Umgebung mit einer benutzerdefinierten Version von Edge, Benutzerdatenverzeichnis und/oder zusätzlichen Optionen.</span><span class="sxs-lookup"><span data-stu-id="5dbab-113">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="5dbab-114">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="5dbab-114">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="5dbab-115">Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.</span><span class="sxs-lookup"><span data-stu-id="5dbab-115">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="5dbab-116">Member</span><span class="sxs-lookup"><span data-stu-id="5dbab-116">Members</span></span>

#### <span data-ttu-id="5dbab-117">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="5dbab-117">CompareBrowserVersions</span></span> 

> <span data-ttu-id="5dbab-118">Public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="5dbab-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="5dbab-119">Diese Methode ist für alle Personen, die die Version richtig vergleichen möchten, um zu ermitteln, welche Version neuer, älter oder gleich ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-119">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="5dbab-120">Sie kann verwendet werden, um zu ermitteln, ob webview2 oder eine bestimmte featurebasis auf Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dbab-120">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="5dbab-121">Legt den Wert des Ergebnisses auf-1, 0 oder 1 fest, wenn version1 kleiner als, gleich oder größer als Version2 ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-121">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="5dbab-122">Gibt E_INVALIDARG zurück, wenn keine der Versionszeichenfolgen analysiert werden kann oder ein Eingabeparameter NULL ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-122">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="5dbab-123">Die Eingabe kann die von GetAvailableCoreWebView2BrowserVersionString abgerufene VERSIONINFO direkt verwenden, Kanalinformationen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5dbab-123">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="5dbab-124">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="5dbab-124">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="5dbab-125">Public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="5dbab-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span></span>

<span data-ttu-id="5dbab-126">Erstellt eine immergrüne WebView2-Umgebung unter Verwendung der installierten Edge-Version.</span><span class="sxs-lookup"><span data-stu-id="5dbab-126">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="5dbab-127">Dies entspricht dem Aufruf von CreateCoreWebView2EnvironmentWithOptions mit nullptr für browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="5dbab-127">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="5dbab-128">Weitere Informationen finden Sie unter CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="5dbab-128">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="5dbab-129">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="5dbab-129">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="5dbab-130">Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentoptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="5dbab-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span></span>

<span data-ttu-id="5dbab-131">DLL-Export zum Erstellen einer WebView2-Umgebung mit einer benutzerdefinierten Version von Edge, Benutzerdatenverzeichnis und/oder zusätzlichen Optionen.</span><span class="sxs-lookup"><span data-stu-id="5dbab-131">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="5dbab-132">Die WebView2-Umgebung und alle anderen WebView2-Objekte sind Single-Threading und haben Abhängigkeiten von Windows-Komponenten, für die com für ein Single-Thread-Apartment initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5dbab-132">The WebView2 environment and all other WebView2 objects are single threaded and have dependencies on Windows components that require COM to be initialized for a single-threaded apartment.</span></span> <span data-ttu-id="5dbab-133">Es wird erwartet, dass die Anwendung CoInitializeEx anruft, bevor CreateCoreWebView2EnvironmentWithOptions aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-133">The application is expected to call CoInitializeEx before calling CreateCoreWebView2EnvironmentWithOptions.</span></span>

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

<span data-ttu-id="5dbab-134">Wenn CoInitializeEx nicht aufgerufen wurde oder zuvor mit COINIT_MULTITHREADED aufgerufen wurde, schlägt CreateCoreWebView2EnvironmentWithOptions mit einem der folgenden Fehler fehl.</span><span class="sxs-lookup"><span data-stu-id="5dbab-134">If CoInitializeEx was not called or has been previously called with COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions will fail with one of the following errors.</span></span>

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

<span data-ttu-id="5dbab-135">Verwenden Sie `browserExecutableFolder` diese Option, um anzugeben, ob WebView2-Steuerelemente eine feste oder installierte Version der WebView2-Laufzeit verwenden, die auf einem Clientcomputer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-135">Use `browserExecutableFolder` to specify whether WebView2 controls use a fixed or installed version of the WebView2 Runtime that exists on a client machine.</span></span> <span data-ttu-id="5dbab-136">Wenn Sie eine feste Version der WebView2-Laufzeit verwenden möchten, übergeben Sie den relativen Pfad des Ordners, in dem sich die feste Version der WebView2-Laufzeit befindet `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="5dbab-136">To use a fixed version of the WebView2 Runtime, pass the relative path of the folder that contains the fixed version of the WebView2 Runtime to `browserExecutableFolder`.</span></span> <span data-ttu-id="5dbab-137">Zum Erstellen von WebView2-Steuerelementen, die die installierte Version der WebView2-Runtime verwenden, die auf Clientcomputern vorhanden ist, übergeben Sie eine NULL oder eine leere Zeichenfolge an `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="5dbab-137">To create WebView2 controls that use the installed version of the WebView2 Runtime that exists on client machines, pass a null or empty string to `browserExecutableFolder`.</span></span> <span data-ttu-id="5dbab-138">In diesem Szenario versucht die API, eine kompatible Version der WebView2-Laufzeit zu finden, die auf dem Clientcomputer installiert ist (zuerst auf Computerebene und dann pro Benutzer), wobei die ausgewählte Kanaleinstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-138">In this scenario, the API tries to find a compatible version of the WebView2 Runtime that is installed on the client machine (first at the machine level, and then per user) using the selected channel preference.</span></span> <span data-ttu-id="5dbab-139">Der Pfad einer festen Version der WebView2-Laufzeit sollte nicht enthalten `\Edge\Application\` .</span><span class="sxs-lookup"><span data-stu-id="5dbab-139">The path of fixed version of the WebView2 Runtime should not contain `\Edge\Application\`.</span></span> <span data-ttu-id="5dbab-140">Wenn ein solcher Pfad verwendet wird, schlägt die API mit ERROR_NOT_SUPPORTED fehl.</span><span class="sxs-lookup"><span data-stu-id="5dbab-140">When such a path is used, the API will fail with ERROR_NOT_SUPPORTED.</span></span>

<span data-ttu-id="5dbab-141">Die standardmäßige Kanal Suchreihenfolge ist die WebView2-Laufzeit, Beta, dev und Canary.</span><span class="sxs-lookup"><span data-stu-id="5dbab-141">The default channel search order is the WebView2 Runtime, Beta, Dev, and Canary.</span></span> <span data-ttu-id="5dbab-142">Wenn eine WEBVIEW2_RELEASE_CHANNEL_PREFERENCE Umgebungsvariable oder ein anwendbarer releaseChannelPreference-Registrierungswert mit dem Wert 1 überschrieben wird, wird die Kanal Suchreihenfolge umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="5dbab-142">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="5dbab-143">userDataFolder kann angegeben werden, um den Standardspeicherort des Benutzerdatenordners für WebView2 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5dbab-143">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="5dbab-144">Der Pfad kann ein absoluter Dateipfad oder ein relativer Dateipfad sein, der als relativ zur ausführbaren Datei des aktuellen Prozesses interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-144">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="5dbab-145">Andernfalls ist der standardmäßige benutzerdatenordner für UWP-apps der APP-Datenordner für das Paket. bei nicht-UWP-apps wird der standardmäßige benutzerdatenordner `{Executable File Name}.WebView2` im gleichen Verzeichnis neben der ausführbaren App erstellt.</span><span class="sxs-lookup"><span data-stu-id="5dbab-145">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="5dbab-146">Bei der WebView2-Erstellung kann ein Fehler auftreten, wenn die ausführbare Datei in einem Verzeichnis ausgeführt wird, in dem der Prozess keine Berechtigung zum Erstellen eines neuen Ordners aufweist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-146">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="5dbab-147">Die APP ist dafür verantwortlich, ihren benutzerdatenordner zu bereinigen, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="5dbab-147">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="5dbab-148">Beachten Sie, dass ein Browserprozess möglicherweise für Webansichten freigegeben wird, wenn die WebView-Erstellung mit HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) fehlschlägt, wenn die angegebenen Optionen nicht den Optionen der Webansichten entsprechen, die derzeit im freigegebenen Browserprozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-148">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="5dbab-149">environmentCreatedHandler ist das Ergebnis des Handlers für den asynchronen Vorgang, der die WebView2Environment enthält, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5dbab-149">environmentCreatedHandler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="5dbab-150">Die browserExecutableFolder-, userDataFolder-und additionalBrowserArguments-Werte von environmentoptions können von Werten überschrieben werden, die entweder in Umgebungsvariablen oder in der Registrierung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5dbab-150">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="5dbab-151">Beim Erstellen eines WebView2Environment werden die folgenden Umgebungsvariablen überprüft:</span><span class="sxs-lookup"><span data-stu-id="5dbab-151">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="5dbab-152">Wenn eine Außerkraftsetzungs Umgebungsvariable gefunden wird, verwenden wir die browserExecutableFolder-und userDataFolder-Werte als Ersatz für die entsprechenden Werte in CreateCoreWebView2EnvironmentWithOptions-Parametern.</span><span class="sxs-lookup"><span data-stu-id="5dbab-152">If an override environment variable is found then we use the browserExecutableFolder and userDataFolder values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span> <span data-ttu-id="5dbab-153">Wenn additionalBrowserArguments in der Umgebungsvariablen oder in der Registrierung angegeben ist, wird es an die nötige-Werte in CreateCoreWebView2EnvironmentWithOptions-Parametern angefügt.</span><span class="sxs-lookup"><span data-stu-id="5dbab-153">If additionalBrowserArguments specified in environment variable or in the registry, it will be appended to the correspinding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="5dbab-154">Zwar werden keine strengen Außerkraftsetzungen vorhanden, es gibt jedoch zusätzliche Umgebungsvariablen, die festgesetzt werden können:</span><span class="sxs-lookup"><span data-stu-id="5dbab-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="5dbab-155">Wenn Sie mit einem nicht leeren Wert gefunden wird, deutet dies darauf hin, dass die WebView unter einem Skriptdebugger gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="5dbab-156">In diesem Fall gibt die WebView einen `Page.waitForDebugger` CDP-Befehl aus, der dazu führt, dass die Skriptausführung in der WebView beim Start angehalten wird, bis ein Debugger einen entsprechenden CDP-Befehl ausgibt, `Runtime.runIfWaitingForDebugger` um die Ausführung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5dbab-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="5dbab-157">Hinweis: Es gibt keine Entsprechung dieser Umgebungsvariablen für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5dbab-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="5dbab-158">Wenn Sie mit einem nicht leeren Wert gefunden wird, deutet dies darauf hin, dass die WebView unter einem Skriptdebugger gestartet wird, der auch Hostanwendungen unterstützt, die mehrere Webansichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="5dbab-159">Der Wert wird als Bezeichner für eine Named Pipe verwendet, die geöffnet und geschrieben wird, wenn eine neue WebView von der Hostanwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="5dbab-160">Die Nutzlast entspricht der des JSON-Ziels "Remotedebuggen-Port" und kann vom externen Debugger zum Anfügen an eine bestimmte WebView-Instanz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="5dbab-161">Das Format der vom Debugger erstellten Pipe sollte wie folgt lauten: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}`</span><span class="sxs-lookup"><span data-stu-id="5dbab-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="5dbab-162">ist der Dateiname der Host-Anwendung exe, beispielsweise WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="5dbab-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="5dbab-163">ist der Wert, der für WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5dbab-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="5dbab-164">Um das Debuggen der von der JSON angegebenen Ziele zu aktivieren, müssen Sie auch die WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS Umgebungsvariable so festlegen, dass Sie gesendet wird, `--remote-debugging-port={port_num}` wobei:</span><span class="sxs-lookup"><span data-stu-id="5dbab-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="5dbab-165">ist der Port, an dem der CDP-Server gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="5dbab-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="5dbab-166">Beachten Sie, dass das Festlegen der Umgebungsvariablen WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER und WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS dazu führt, dass die in Ihrer Anwendung gehosteten Webansichten und deren Inhalte für Anwendungen von Drittanbietern wie Debuggern verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="5dbab-167">Hinweis: Es gibt keine Entsprechung dieser Umgebungsvariablen für den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5dbab-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="5dbab-168">Wenn keine dieser Umgebungsvariablen vorhanden ist, wird die Registrierung als nächstes überprüft.</span><span class="sxs-lookup"><span data-stu-id="5dbab-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="5dbab-169">Die folgenden Registrierungswerte werden überprüft:</span><span class="sxs-lookup"><span data-stu-id="5dbab-169">The following registry values are checked:</span></span>

```
[{Root}]\Software\Policies\Microsoft\Edge\WebView2\browserExecutableFolder
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\releaseChannelPreference
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\additionalBrowserArguments
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\userDataFolder
"{AppId}"=""
```

<span data-ttu-id="5dbab-170">browserExecutableFolder und releaseChannelPreference können mithilfe von Gruppenrichtlinien unter Administrative Vorlagen > Microsoft Edge-WebView2 konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-170">browserExecutableFolder and releaseChannelPreference can be configured using group policy under Administrative Templates > Microsoft Edge WebView2.</span></span> <span data-ttu-id="5dbab-171">Der alte Registrierungsspeicherort wird in Kürze veraltet sein:</span><span class="sxs-lookup"><span data-stu-id="5dbab-171">The old registry location will be deprecated soon:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="5dbab-172">In dem unwahrscheinlichen Szenario, in dem einige Instanzen von WebView während eines Browser Updates geöffnet sind, könnten wir das Löschen von alten Edge-Browsern blockieren.</span><span class="sxs-lookup"><span data-stu-id="5dbab-172">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="5dbab-173">Um zu vermeiden, dass der Speicherplatz knapp wird, schlägt eine neue WebView-Erstellung mit dem nächsten Fehler fehl, wenn erkannt wird, dass viele alte Versionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5dbab-173">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="5dbab-174">Die maximal zulässige Standardanzahl von Edge-Versionen beträgt 20.</span><span class="sxs-lookup"><span data-stu-id="5dbab-174">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="5dbab-175">Die maximal zulässige Anzahl Alter Edge-Versionen kann mit dem Wert der folgenden Umgebungsvariablen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5dbab-175">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="5dbab-176">Wenn die WebView von einem installierten Edge abhängt und deinstalliert wird, schlägt die spätere Erstellung mit dem nächsten Fehler fehl</span><span class="sxs-lookup"><span data-stu-id="5dbab-176">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="5dbab-177">Als erstes überprüfen wir root als HKLM und dann HKCU.</span><span class="sxs-lookup"><span data-stu-id="5dbab-177">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="5dbab-178">Die Anwendungs-ID des aufrufenden Prozesses wird zunächst auf die Anwendungsbenutzer Modell-ID festgesetzt, und wenn kein entsprechender Registrierungsschlüssel vorhanden ist, wird die APP auf den ausführbaren Namen des Prozesses des Aufrufers festgesetzt, oder wenn es sich nicht um einen Registrierungsschlüssel handelt, "\*".</span><span class="sxs-lookup"><span data-stu-id="5dbab-178">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="5dbab-179">Wenn ein Registrierungsschlüssel für die Überschreibung gefunden wird, verwenden wir die Registrierungswerte browserExecutableFolder und userDataFolder als Ersatz und fügen additionalBrowserArguments Registrierungswerte für die entsprechenden Werte in CreateCoreWebView2EnvironmentWithOptions-Parametern an.</span><span class="sxs-lookup"><span data-stu-id="5dbab-179">If an override registry key is found, then we use the browserExecutableFolder and userDataFolder registry values as replacements and append additionalBrowserArguments registry values for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="5dbab-180">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="5dbab-180">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="5dbab-181">Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="5dbab-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="5dbab-182">Rufen Sie die Browser Versionsinformationen einschließlich des Kanal namens ab, wenn es sich nicht um den stabilen Kanal oder den eingebetteten Edge handelt.</span><span class="sxs-lookup"><span data-stu-id="5dbab-182">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="5dbab-183">Kanalnamen sind Beta, dev und Canary.</span><span class="sxs-lookup"><span data-stu-id="5dbab-183">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="5dbab-184">Wenn für die browserExecutableFolder oder die Kanaleinstellung eine Überschreibung vorhanden ist, wird die Außerkraftsetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dbab-184">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="5dbab-185">Wenn keine Überschreibung vorhanden ist, wird der an GetAvailableCoreWebView2BrowserVersionString übergebene Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dbab-185">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>
