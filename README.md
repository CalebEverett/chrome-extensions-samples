# Chrome Extensions samples

Official samples for Chrome Extensions and the Chrome Apps platform.
Note that Chrome Apps are deprecated—learn more [on the Chromium blog](https://blog.chromium.org/2020/08/changes-to-chrome-app-support-timeline.html).

For more information on extensions, see [Chrome Developers](https://developer.chrome.com).

## Samples

The directory structure is as follows:

* api/ - extensions focused on a single API package
* howto/ - extensions that show how to perform a particular task
* tutorials/ - multi-step walkthroughs referenced inline in the docs
* extensions/ - full featured extensions spanning multiple API packages
* apps/ - deprecated Chrome Apps platform (not listed below)

To experiment with these samples, please clone this repo and use 'Load Unpacked Extension'.
Read more on [Getting Started](https://developer.chrome.com/extensions/getstarted).

Sample | Calls
--- | ---
[My Bookmarks](mv2-archive/api/bookmarks/basic)<br />A browser action with a popup dump of all bookmarks, including search, add, edit and delete. | <ul><li>bookmarks.create</li><li>bookmarks.getTree</li><li>bookmarks.remove</li><li>bookmarks.update</li><li>tabs.create</li></ul>
[Page Redder](mv2-archive/api/browserAction/make_page_red)<br />Make the current page red | <ul><li>browserAction.onClicked</li><li>tabs.executeScript</li></ul>
[Print this page](mv2-archive/api/browserAction/print)<br />Adds a print button to the browser. | <ul><li>browserAction.onClicked</li><li>tabs.executeScript</li></ul>
[A browser action which changes its icon when clicked](mv2-archive/api/browserAction/set_icon_path)<br />Click browser action icon to change color! | <ul><li>browserAction.onClicked</li><li>browserAction.setIcon</li><li>runtime.onInstalled</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[A browser action with a popup that changes the page color](mv2-archive/api/browserAction/set_page_color)<br />Change the current page color | <ul><li>tabs.executeScript</li></ul>
[BrowsingData API: Basics](mv2-archive/api/browsingData/basic)<br />A trivial usage example. | <ul><li>browsingData.remove</li></ul>
[Sample Extension Commands extension](mv2-archive/api/commands)<br />Press Ctrl+Shift+F to open the browser action popup, press Ctrl+Shift+Y to send an event. | <ul><li>commands.onCommand</li></ul>
[Content settings](mv2-archive/api/contentSettings)<br />Shows the content settings for the current site. | <ul><li>contentSettings.ContentSetting.get</li><li>contentSettings.ContentSetting.set</li><li>tabs.query</li></ul>
[Context Menus Sample](mv2-archive/api/contextMenus/basic)<br />Shows some of the features of the Context Menus API | <ul><li>contextMenus.create</li><li>extension.lastError</li></ul>
[Context Menus Sample (with Event Page)](mv2-archive/api/contextMenus/event_page)<br />Shows some of the features of the Context Menus API using an event page | <ul><li>contextMenus.create</li><li>contextMenus.onClicked</li><li>extension.lastError</li><li>runtime.onInstalled</li></ul>
[Global Google Search](mv2-archive/api/contextMenus/global_context_search)<br />Use the context menu to search a different country's Google | <ul><li>contextMenus.create</li><li>contextMenus.onClicked</li><li>contextMenus.remove</li><li>runtime.onInstalled</li><li>storage.onChanged</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.create</li></ul>
[Cookie API Test Extension](mv2-archive/api/cookies)<br />Testing Cookie API | <ul><li>browserAction.onClicked</li><li>cookies.getAll</li><li>cookies.onChanged</li><li>cookies.remove</li><li>extension.getURL</li><li>tabs.create</li><li>tabs.update</li><li>windows.getAll</li></ul>
[Live HTTP headers](mv2-archive/api/debugger/live-headers)<br />Displays the live log with the http requests headers | <ul><li>browserAction.onClicked</li><li>debugger.attach</li><li>debugger.detach</li><li>debugger.onEvent</li><li>debugger.sendCommand</li><li>runtime.lastError</li><li>windows.create</li></ul>
[JavaScript pause/resume](mv2-archive/api/debugger/pause-resume)<br />Pauses / resumes JavaScript execution | <ul><li>browserAction.onClicked</li><li>browserAction.setIcon</li><li>browserAction.setTitle</li><li>debugger.attach</li><li>debugger.detach</li><li>debugger.onDetach</li><li>debugger.onEvent</li><li>debugger.sendCommand</li><li>runtime.lastError</li></ul>
[Tab Flipper](mv2-archive/api/default_command_override)<br />Press Ctrl+Shift+Right or Ctrl+Shift+Left (Command+Shift+Right or Command+Shift+Left on a Mac) to flip through window tabs | <ul><li>commands.onCommand</li><li>tabs.query</li><li>tabs.update</li></ul>
[Desktop Capture Example](mv2-archive/api/desktopCapture)<br />Show desktop media picker UI | <ul><li>desktopCapture.cancelChooseDesktopMedia</li><li>desktopCapture.chooseDesktopMedia</li><li>runtime.onMessage</li><li>runtime.sendMessage</li></ul>
[My Devices](mv2-archive/api/deviceInfo/basic)<br />A browser action with a popup dump of all devices signed into the same account as the current profile. | <ul><li>signedInDevices.get</li><li>signedInDevices.onDeviceInfoChange</li></ul>
[FirePHP for Chrome](mv2-archive/api/devtools/network/chrome-firephp)<br />Extends the Developer Tools, adding support for parsing FirePHP messages from server | <ul><li>devtools.network.getHAR</li><li>devtools.network.onRequestFinished</li><li>extension.onRequest</li><li>extension.sendRequest</li><li>tabs.executeScript</li></ul>
[Chrome Query](mv2-archive/api/devtools/panels/chrome-query)<br />Extends the Developer Tools, adding a sidebar that displays the jQuery data associated with the selected DOM element. | <ul><li>devtools.panels.ElementsPanel.createSidebarPane</li><li>devtools.panels.ElementsPanel.onSelectionChanged</li></ul>
[tabCast](mv2-archive/api/displaySource/tabCast)<br />Creates a WiFi Display Session from the captured tab media stream using chrome.displaySource API. | <ul><li>displaySource.getAvailableSinks</li><li>displaySource.onSessionTerminated</li><li>displaySource.onSinksUpdated</li><li>displaySource.startSession</li><li>displaySource.terminateSession</li><li>extension.getBackgroundPage</li><li>runtime.lastError</li><li>runtime.onMessage</li><li>runtime.sendMessage</li><li>tabCapture.capture</li><li>tabs.getCurrent</li></ul>
[Document Scanning API Sample](mv2-archive/api/document_scan)<br /> | <ul><li>documentScan.scan</li><li>permissions.contains</li><li>permissions.request</li><li>runtime.lastError</li></ul>
[Download Filename Controller](mv2-archive/api/downloads/download_filename_controller)<br />Download Filename Controller | <ul><li>downloads.onDeterminingFilename</li></ul>
[Download Selected Links](mv2-archive/api/downloads/download_links)<br />Select links on a page and download them. | <ul><li>downloads.download</li><li>extension.onRequest</li><li>extension.sendRequest</li><li>tabs.executeScript</li><li>tabs.query</li><li>windows.getCurrent</li></ul>
[Download Manager Button](mv2-archive/api/downloads/download_manager)<br />Browser Action Download Manager User Interface for Google Chrome | <ul><li>browserAction.setIcon</li><li>downloads.acceptDanger</li><li>downloads.cancel</li><li>downloads.download</li><li>downloads.erase</li><li>downloads.getFileIcon</li><li>downloads.onChanged</li><li>downloads.onCreated</li><li>downloads.onErased</li><li>downloads.open</li><li>downloads.pause</li><li>downloads.removeFile</li><li>downloads.resume</li><li>downloads.search</li><li>downloads.setShelfEnabled</li><li>downloads.show</li><li>downloads.showDefaultFolder</li><li>i18n.getMessage</li><li>permissions.contains</li><li>permissions.request</li><li>runtime.onMessage</li><li>runtime.sendMessage</li><li>tabs.create</li></ul>
[Download and Open Button](mv2-archive/api/downloads/download_open)<br />Download and Open Context Menu Button | <ul><li>contextMenus.create</li><li>contextMenus.onClicked</li><li>downloads.download</li><li>downloads.onChanged</li><li>downloads.open</li><li>i18n.getMessage</li></ul>
[Downloads Overwrite Existing Files](mv2-archive/api/downloads/downloads_overwrite)<br />All downloads overwrite existing files instead of adding ' (1)', ' (2)', etc. | <ul><li>downloads.onDeterminingFilename</li></ul>
[Event Page Example](mv2-archive/api/eventPage/basic)<br />Demonstrates usage and features of the event page | <ul><li>alarms.create</li><li>alarms.onAlarm</li><li>bookmarks.onRemoved</li><li>browserAction.onClicked</li><li>browserAction.setBadgeText</li><li>commands.onCommand</li><li>declarativeWebRequest.RedirectRequest</li><li>declarativeWebRequest.RequestMatcher</li><li>runtime.onInstalled</li><li>runtime.onMessage</li><li>runtime.onSuspend</li><li>runtime.sendMessage</li><li>tabs.create</li><li>tabs.executeScript</li><li>tabs.query</li><li>tabs.sendMessage</li></ul>
[`extension.isAllowedFileSchemeAccess` and `extension.isAllowedIncognitoAccess` Example](mv2-archive/api/extension/isAllowedAccess)<br />Demonstrates the `extension.isAllowedFileSchemeAccess` and `extesion.isAllowedIncognitoAccess` APIs | <ul><li>extension.isAllowedFileSchemeAccess</li><li>extension.isAllowedIncognitoAccess</li></ul>
[Fake Archive Handler App](mv2-archive/api/fileSystemProvider/archive)<br />Demonstrate File System Provider API usage for apps. | <ul><li>fileSystemProvider.get</li><li>fileSystemProvider.mount</li><li>fileSystemProvider.onCloseFileRequested</li><li>fileSystemProvider.onGetMetadataRequested</li><li>fileSystemProvider.onOpenFileRequested</li><li>fileSystemProvider.onReadDirectoryRequested</li><li>fileSystemProvider.onReadFileRequested</li><li>fileSystemProvider.onUnmountRequested</li><li>fileSystemProvider.unmount</li><li>runtime.lastError</li><li>runtime.onStartup</li><li>runtime.onSuspend</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[File System Provider API Extension Example](mv2-archive/api/fileSystemProvider/basic)<br />Demonstrate features of the API like mounting, listing directories, etc for extensions. | <ul><li>fileSystemProvider.mount</li><li>fileSystemProvider.onCloseFileRequested</li><li>fileSystemProvider.onGetMetadataRequested</li><li>fileSystemProvider.onMountRequested</li><li>fileSystemProvider.onOpenFileRequested</li><li>fileSystemProvider.onReadDirectoryRequested</li><li>fileSystemProvider.onReadFileRequested</li><li>fileSystemProvider.onUnmountRequested</li><li>fileSystemProvider.unmount</li><li>runtime.lastError</li></ul>
[Advanced Font Settings](mv2-archive/api/fontSettings)<br />Customize per-script font settings. | <ul><li>fontSettings.clearDefaultFixedFontSize</li><li>fontSettings.clearDefaultFontSize</li><li>fontSettings.clearFont</li><li>fontSettings.clearMinimumFontSize</li><li>fontSettings.getDefaultFixedFontSize</li><li>fontSettings.getDefaultFontSize</li><li>fontSettings.getFont</li><li>fontSettings.getFontList</li><li>fontSettings.getMinimumFontSize</li><li>fontSettings.onDefaultFixedFontSizeChanged</li><li>fontSettings.onDefaultFontSizeChanged</li><li>fontSettings.onFontChanged</li><li>fontSettings.onMinimumFontSizeChanged</li><li>fontSettings.setDefaultFixedFontSize</li><li>fontSettings.setDefaultFontSize</li><li>fontSettings.setFont</li><li>fontSettings.setMinimumFontSize</li></ul>
[History Override](mv2-archive/api/history/historyOverride)<br />Overrides the History Page | <ul><li>history.deleteAll</li><li>history.deleteUrl</li><li>history.search</li></ul>
[Typed URL History](mv2-archive/api/history/showHistory)<br />Reads your history, and shows the top ten pages you go to by typing the URL. | <ul><li>history.getVisits</li><li>history.search</li><li>tabs.create</li></ul>
[CLD](mv2-archive/api/i18n/cld)<br />Displays the language of a tab | <ul><li>browserAction.setBadgeText</li><li>tabs.detectLanguage</li><li>tabs.onSelectionChanged</li><li>tabs.onUpdated</li><li>tabs.query</li></ul>
[Detect Language](mv2-archive/api/i18n/detectLanguage)<br />Detects up to 3 languages and their percentages of the provided string | <ul><li>i18n.detectLanguage</li></ul>
[AcceptLanguage](mv2-archive/api/i18n/getMessage)<br />Returns accept languages of the browser | <ul><li>i18n.getAcceptLanguages</li><li>i18n.getMessage</li></ul>
[Minimal Localized Hosted App](mv2-archive/api/i18n/localizedHostedApp)<br />This is the minimal set of data required to upload a localized hosted application to the web store. | <ul></ul>
[Idle - Simple Example](mv2-archive/api/idle/idle_simple)<br />Demonstrates the Idle API | <ul><li>browserAction.onClicked</li><li>extension.getBackgroundPage</li><li>idle.onStateChanged</li><li>idle.queryState</li></ul>
[Test IME](mv2-archive/api/input.ime/basic)<br />A simple IME that converts all keystrokes to upper case. | <ul><li>input.ime</li><li>input.ime.commitText</li><li>input.ime.onActivate</li><li>input.ime.onBlur</li><li>input.ime.onDeactivated</li><li>input.ime.onFocus</li><li>input.ime.onKeyEvent</li></ul>
[Message Timer](mv2-archive/api/messaging/timer)<br />Times how long it takes to send a message to a content script and back. | <ul><li>runtime.onConnect</li><li>runtime.onMessage</li><li>tabs.connect</li><li>tabs.query</li><li>tabs.sendMessage</li></ul>
[Native Messaging Example](mv2-archive/api/nativeMessaging/app)<br />Send a message to a native application. | <ul><li>runtime.connectNative</li></ul>
[Notification Demo](mv2-archive/api/notifications)<br />Shows off desktop notifications, which are "toast" windows that pop up on the desktop. | <ul></ul>
[Omnibox New Tab Search](mv2-archive/api/omnibox/newtab_search)<br />Type 'nt' plus a search term into the Omnibox to open search in new tab. | <ul><li>omnibox.onInputEntered</li><li>tabs.create</li></ul>
[Omnibox Example](mv2-archive/api/omnibox/simple-example)<br />To use, type 'omnix' plus a search term into the Omnibox. | <ul><li>omnibox.onInputChanged</li><li>omnibox.onInputEntered</li></ul>
[Blank new tab page](mv2-archive/api/override/blank_ntp)<br />Override the new tab page with a blank one | <ul></ul>
[iGoogle new tab page](mv2-archive/api/override/override_igoogle)<br />Override the new tab page with iGoogle | <ul></ul>
[Page action by content](mv2-archive/api/pageAction/pageaction_by_content)<br />Shows a page action for HTML pages containing a video | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>runtime.onInstalled</li></ul>
[Page action by URL](mv2-archive/api/pageAction/pageaction_by_url)<br />Shows a page action for urls which have the letter 'g' in them. | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>runtime.onInstalled</li></ul>
[Animated Page Action](mv2-archive/api/pageAction/set_icon)<br />This extension adds an animated browser action to the toolbar. | <ul><li>pageAction.hide</li><li>pageAction.onClicked</li><li>pageAction.setIcon</li><li>pageAction.setTitle</li><li>pageAction.show</li><li>tabs.onSelectionChanged</li><li>tabs.query</li></ul>
[Top Chrome Extension Questions](mv2-archive/api/permissions/extension-questions)<br />Sample demonstration of the optional permissions API. | <ul><li>permissions.contains</li><li>permissions.onAdded</li><li>permissions.onRemoved</li><li>permissions.remove</li><li>permissions.request</li><li>tabs.create</li></ul>
[Keep Awake](mv2-archive/api/power)<br />Override system power-saving settings. | <ul><li>browserAction.onClicked</li><li>browserAction.setIcon</li><li>browserAction.setTitle</li><li>i18n.getMessage</li><li>power.releaseKeepAwake</li><li>power.requestKeepAwake</li><li>runtime.onInstalled</li><li>runtime.onStartup</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[Block/allow third-party cookies API example extension](mv2-archive/api/preferences/allowThirdPartyCookies)<br />Sample extension which demonstrates how to access a preference. | <ul><li>extension.isAllowedIncognitoAccess</li></ul>
[Block/allow referrer API example extension](mv2-archive/api/preferences/enableReferrer)<br />Sample extension which demonstrates how to access a preference. | <ul><li>extension.isAllowedIncognitoAccess</li></ul>
[Print Extension](mv2-archive/api/printing)<br />Sends print job directly to the printers installed on the Chromebook | <ul><li>printing.getPrinterInfo</li><li>printing.getPrinters</li><li>printing.submitJob</li><li>runtime.lastError</li></ul>
[Print Job History](mv2-archive/api/printingMetrics)<br />Reads your print history and displays the recent print jobs. | <ul><li>browserAction.setBadgeText</li><li>printingMetrics.getPrintJobs</li><li>printingMetrics.onPrintJobFinished</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[Process Monitor](mv2-archive/api/processes/process_monitor)<br />Adds a browser action that monitors resource usage of all browser processes. | <ul><li>processes.onUpdatedWithMemory</li><li>processes.terminate</li></ul>
[Show Tabs in Process](mv2-archive/api/processes/show_tabs)<br />Adds a browser action showing which tabs share the current tab's process. | <ul><li>processes.getProcessIdForTab</li><li>tabs.query</li><li>tabs.update</li><li>windows.getAll</li><li>windows.getCurrent</li><li>windows.update</li></ul>
[Stylizr](mv2-archive/api/storage/stylizr)<br />Spruce up your pages with custom CSS. | <ul><li>extension.getURL</li><li>runtime.lastError</li><li>storage.local</li><li>storage.StorageArea.clear</li><li>storage.StorageArea.get</li><li>storage.StorageArea.remove</li><li>storage.StorageArea.set</li><li>tabs.insertCSS</li></ul>
[Tab Capture Example](mv2-archive/api/tabCapture)<br />Capture a tab and play in a | <ul><li>browserAction.onClicked</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabCapture.capture</li><li>tabCapture.getMediaStreamId</li></ul>
[Tab Inspector](mv2-archive/api/tabs/inspector)<br />Utility for working with the extension tabs api | <ul><li>browserAction.onClicked</li><li>extension.getURL</li><li>tabs.create</li><li>tabs.get</li><li>tabs.getAllInWindow</li><li>tabs.move</li><li>tabs.onAttached</li><li>tabs.onCreated</li><li>tabs.onDetached</li><li>tabs.onMoved</li><li>tabs.onRemoved</li><li>tabs.onSelectionChanged</li><li>tabs.onUpdated</li><li>tabs.query</li><li>tabs.remove</li><li>tabs.update</li><li>windows.create</li><li>windows.get</li><li>windows.getAll</li><li>windows.getCurrent</li><li>windows.getLastFocused</li><li>windows.onCreated</li><li>windows.onFocusChanged</li><li>windows.onRemoved</li><li>windows.remove</li><li>windows.update</li></ul>
[Keyboard Pin](mv2-archive/api/tabs/pin)<br />Creates a keyboard shortcut (Alt + Shift + P) to toggle the pinned state of the currently selected tab | <ul><li>commands.onCommand</li><li>tabs.query</li><li>tabs.update</li></ul>
[Test Screenshot Extension](mv2-archive/api/tabs/screenshot)<br />Demonstrate screenshot functionality in the chrome.tabs api. | <ul><li>browserAction.onClicked</li><li>extension.getURL</li><li>extension.getViews</li><li>tabs.captureVisibleTab</li><li>tabs.create</li><li>tabs.onUpdated</li></ul>
[Tabs Zoom API Demo](mv2-archive/api/tabs/zoom)<br />This extension allows the user to explore features of the new tabs zoom api. | <ul><li>runtime.lastError</li><li>tabs.getZoom</li><li>tabs.getZoomSettings</li><li>tabs.onZoomChange</li><li>tabs.query</li><li>tabs.setZoom</li><li>tabs.setZoomSettings</li></ul>
[Top Sites](mv2-archive/api/topsites/basic)<br />Shows the top sites in a browser action | <ul><li>tabs.create</li><li>topSites.get</li></ul>
[NTP prototyping extension](mv2-archive/api/topsites/magic8ball)<br />extension to prototype new NTP designs | <ul><li>topSites.get</li></ul>
[Console TTS Engine](mv2-archive/api/ttsEngine/console_tts_engine)<br />A "silent" TTS engine that prints text to a small window rather than synthesizing speech. | <ul><li>extension.getViews</li><li>ttsEngine.onSpeak</li><li>ttsEngine.onStop</li><li>windows.create</li><li>windows.getCurrent</li><li>windows.onRemoved</li></ul>
[Drink Water Event Popup](mv2-archive/api/water_alarm_notification)<br />Demonstrates usage and features of the event page by reminding user to drink water | <ul><li>alarms.clearAll</li><li>alarms.create</li><li>alarms.onAlarm</li><li>browserAction.setBadgeText</li><li>notifications.create</li><li>notifications.onButtonClicked</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[WebNavigation Tech Demo](mv2-archive/api/webNavigation/basic)<br />Demonstration of the WebNavigation extension API. | <ul><li>i18n.getMessage</li><li>runtime.onMessage</li><li>runtime.onStartup</li><li>runtime.sendMessage</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>webNavigation.onBeforeNavigate</li><li>webNavigation.onCommitted</li><li>webNavigation.onCompleted</li><li>webNavigation.onCreatedNavigationTarget</li><li>webNavigation.onErrorOccurred</li><li>webNavigation.onHistoryStateUpdated</li><li>webNavigation.onReferenceFragmentUpdated</li></ul>
[Webview transparency](mv2-archive/api/webview/capturevisibleregion)<br />Sample of the webview.captureVisibleRegion api | <ul></ul>
[WebView Extension Communications Demo: App](mv2-archive/api/webview/comm_demo_app)<br /> | <ul><li>runtime.connect</li></ul>
[WebView Extension Communications Demo: Extension](mv2-archive/api/webview/comm_demo_ext)<br />Provides content scripts to an app hosting a WebView. | <ul><li>runtime.id</li><li>runtime.onConnectExternal</li></ul>
[Merge Windows](mv2-archive/api/windows/merge_windows)<br />Merges all of the browser's windows into the current window | <ul><li>browserAction.onClicked</li><li>tabs.getAllInWindow</li><li>tabs.move</li><li>windows.getAll</li><li>windows.getCurrent</li></ul>
[Simple Background App](mv2-archive/apps/background-simple)<br /> | <ul></ul>
[Calculator](mv2-archive/apps/calculator/app)<br />A simple calculator. | <ul></ul>
[App Launcher](mv2-archive/extensions/app_launcher)<br />Get access to your apps in a browser action | <ul><li>extension.getURL</li><li>management.getAll</li><li>management.launchApp</li><li>tabs.create</li></ul>
[Chromium Buildbot Monitor](mv2-archive/extensions/buildbot)<br />Displays the status of the Chromium buildbot in the toolbar. Click to see more detailed status in a popup. | <ul><li>browserAction.setBadgeBackgroundColor</li><li>browserAction.setBadgeText</li><li>browserAction.setTitle</li><li>extension.getBackgroundPage</li><li>extension.getURL</li><li>extension.getViews</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[Google Calendar Checker (by Google)](mv2-archive/extensions/calendar)<br />Quickly see the time until your next meeting from any of your calendars. Click on the button to be taken to your calendar. | <ul><li>browserAction.onClicked</li><li>browserAction.setBadgeBackgroundColor</li><li>browserAction.setBadgeText</li><li>i18n.getMessage</li><li>management.uninstallSelf</li><li>notifications.clear</li><li>notifications.create</li><li>notifications.onButtonClicked</li><li>notifications.onClicked</li><li>runtime.getURL</li><li>runtime.id</li><li>runtime.onInstalled</li><li>tabs.create</li></ul>
[CatBlock](mv2-archive/extensions/catblock)<br />I can't has cheezburger! | <ul><li>webRequest.onBeforeRequest</li></ul>
[Catifier](mv2-archive/extensions/catifier)<br />Moar cats! | <ul><li>declarativeWebRequest.IgnoreRules</li><li>declarativeWebRequest.RedirectRequest</li><li>declarativeWebRequest.RequestMatcher</li><li>runtime.lastError</li><li>runtime.onInstalled</li></ul>
[Chromium Search](mv2-archive/extensions/chrome_search)<br />Add support to the omnibox to search the Chromium source code. | <ul><li>omnibox.onInputCancelled</li><li>omnibox.onInputChanged</li><li>omnibox.onInputEntered</li><li>omnibox.onInputStarted</li><li>omnibox.setDefaultSuggestion</li><li>tabs.query</li><li>tabs.update</li></ul>
[Constant Context](mv2-archive/extensions/constant_context)<br />Highlights elements with keywords on developer.chrome | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>runtime.onInstalled</li><li>storage.StorageArea.clear</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.executeScript</li></ul>
[Download Images](mv2-archive/extensions/download_images)<br />Displays all webpage images and allows user to download | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>downloads.download</li><li>runtime.lastError</li><li>runtime.onInstalled</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.create</li><li>tabs.executeScript</li></ul>
[Email this page (by Google)](mv2-archive/extensions/email_this_page)<br />This extension adds an email button to the toolbar which allows you to email the page link using your default mail client or Gmail. | <ul><li>browserAction.onClicked</li><li>runtime.connect</li><li>runtime.onConnect</li><li>tabs.create</li><li>tabs.executeScript</li><li>tabs.update</li></ul>
[Chrome Sounds](mv2-archive/extensions/fx)<br />Enjoy a more magical and immersive experience when browsing the web using the power of sound. | <ul><li>bookmarks.onCreated</li><li>bookmarks.onMoved</li><li>bookmarks.onRemoved</li><li>extension.getBackgroundPage</li><li>extension.onRequest</li><li>extension.sendRequest</li><li>tabs.get</li><li>tabs.onAttached</li><li>tabs.onCreated</li><li>tabs.onDetached</li><li>tabs.onMoved</li><li>tabs.onRemoved</li><li>tabs.onSelectionChanged</li><li>tabs.onUpdated</li><li>windows.onCreated</li><li>windows.onFocusChanged</li><li>windows.onRemoved</li></ul>
[Google Document List Viewer](mv2-archive/extensions/gdocs)<br />Demonstrates how to use OAuth to connect the Google Documents List Data API. | <ul><li>extension.getBackgroundPage</li><li>extension.getURL</li><li>tabs.create</li><li>tabs.onUpdated</li><li>tabs.query</li><li>tabs.remove</li></ul>
[Google Mail Checker](mv2-archive/extensions/gmail)<br />Displays the number of unread messages in your Google Mail inbox. You can also click the button to open your inbox. | <ul><li>alarms.create</li><li>alarms.get</li><li>alarms.onAlarm</li><li>browserAction.onClicked</li><li>browserAction.setBadgeBackgroundColor</li><li>browserAction.setBadgeText</li><li>browserAction.setIcon</li><li>i18n.getMessage</li><li>runtime.onInstalled</li><li>runtime.onStartup</li><li>runtime.onStartup</li><li>tabs.create</li><li>tabs.getAllInWindow</li><li>tabs.onUpdated</li><li>tabs.update</li><li>webNavigation.onDOMContentLoaded</li><li>webNavigation.onDOMContentLoaded</li><li>webNavigation.onReferenceFragmentUpdated</li><li>webNavigation.onReferenceFragmentUpdated</li><li>windows.onCreated</li></ul>
[Imageinfo](mv2-archive/extensions/imageinfo)<br />Get image info for images, including EXIF data | <ul><li>contextMenus.create</li><li>tabs.getCurrent</li><li>windows.create</li><li>windows.update</li></ul>
[Chromium IRC App](mv2-archive/extensions/irc/app)<br /> | <ul></ul>
[Managed Bookmarks](mv2-archive/extensions/managed_bookmarks)<br />Adds bookmarks configured by your system administrator to Chrome. | <ul><li>bookmarks.create</li><li>bookmarks.getChildren</li><li>bookmarks.move</li><li>bookmarks.onChanged</li><li>bookmarks.onMoved</li><li>bookmarks.onRemoved</li><li>bookmarks.remove</li><li>bookmarks.removeTree</li><li>bookmarks.update</li><li>runtime.onInstalled</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>storage.StorageArea.get</li><li>storage.onChanged</li></ul>
[Mappy](mv2-archive/extensions/mappy)<br />Finds addresses in the web page you're on and pops up a map window. | <ul><li>pageAction.setTitle</li><li>pageAction.show</li><li>runtime.onMessage</li><li>runtime.sendMessage</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[Google Maps](mv2-archive/extensions/maps_app)<br /> | <ul></ul>
[News Reader (by Google)](mv2-archive/extensions/news)<br />Displays the latest stories from Google News in a popup. | <ul><li>extension.getURL</li><li>i18n.getMessage</li><li>tabs.create</li></ul>
[News Reader](mv2-archive/extensions/news_a11y)<br />Displays the first 5 items from the 'Google News - top news' RSS feed in a popup. | <ul><li>tabs.create</li></ul>
[News Reader](mv2-archive/extensions/news_i18n)<br />Displays the first 5 items from the '$Google$ News - top news' RSS feed in a popup. | <ul></ul>
[No Cookies](mv2-archive/extensions/no_cookies)<br />Removes 'Cookie' and 'Set-Cookie' headers. | <ul><li>webRequest.onBeforeSendHeaders</li><li>webRequest.onHeadersReceived</li></ul>
[Sample - OAuth Contacts](mv2-archive/extensions/oauth_contacts)<br />Uses OAuth to connect to Google's contacts service and display a list of your contacts. | <ul><li>browserAction.onClicked</li><li>browserAction.setIcon</li><li>extension.getBackgroundPage</li><li>extension.getURL</li><li>tabs.create</li><li>tabs.onUpdated</li><li>tabs.query</li><li>tabs.remove</li></ul>
[Optional Permissions New Tab](mv2-archive/extensions/optional_permissions)<br />Demonstrates optional permissions in extensions | <ul><li>permissions.contains</li><li>permissions.request</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>topSites.get</li></ul>
[Per-plugin content settings](mv2-archive/extensions/plugin_settings)<br />Customize your content setting for different plugins. | <ul><li>contentSettings.plugins</li><li>contentSettings.ContentSetting.clear</li><li>contentSettings.ContentSetting.getResourceIdentifiers</li><li>contentSettings.ContentSetting.set</li><li>i18n.getMessage</li><li>runtime.lastError</li></ul>
[Proxy Extension API Sample](mv2-archive/extensions/proxy_configuration)<br />Set Chrome-specific proxies; a demonstration of Chrome's Proxy API | <ul><li>browserAction.setBadgeBackgroundColor</li><li>browserAction.setBadgeText</li><li>browserAction.setTitle</li><li>extension.isAllowedIncognitoAccess</li><li>extension.onRequest</li><li>extension.sendRequest</li><li>i18n.getMessage</li><li>proxy.onProxyError</li><li>runtime.lastError</li></ul>
[Speak Selection](mv2-archive/extensions/speak_selection)<br />Speaks the current selection out loud. | <ul><li>browserAction.onClicked</li><li>browserAction.setIcon</li><li>extension.getURL</li><li>extension.onRequest</li><li>extension.sendRequest</li><li>tabs.create</li><li>tabs.executeScript</li><li>tabs.sendRequest</li><li>tts.getVoices</li><li>tts.speak</li><li>tts.stop</li><li>windows.getAll</li></ul>
[Talking Alarm Clock](mv2-archive/extensions/talking_alarm_clock)<br />A clock with two configurable alarms that will play a sound and speak a phrase of your choice. | <ul><li>browserAction.setIcon</li><li>runtime.connect</li><li>runtime.onConnect</li><li>tts.getVoices</li><li>tts.speak</li><li>tts.stop</li></ul>
[TTS Debug](mv2-archive/extensions/ttsdebug)<br />Tool for developers of Chrome TTS engine extensions to help them test their engines are implementing the API correctly. | <ul><li>tts.getVoices</li><li>tts.speak</li><li>tts.stop</li></ul>
[TTS Demo](mv2-archive/extensions/ttsdemo)<br />Demo Chrome's synthesized text-to-speech capabilities. | <ul><li>runtime.lastError</li><li>tts.getVoices</li><li>tts.isSpeaking</li><li>tts.speak</li><li>tts.stop</li></ul>
[Sandboxed Frame](mv2-archive/howto/sandbox)<br />Demonstrate use of handlebars inside a sandboxed frame | <ul><li>browserAction.onClicked</li></ul>
[Tab Shortcuts](mv2-archive/howto/tab_shortcuts)<br />Allows pinning and duplication of tabs via keyboard shortcuts. | <ul><li>commands.onCommand</li><li>tabs.duplicate</li><li>tabs.update</li></ul>
[Event Tracking with Google Analytics](mv2-archive/tutorials/analytics)<br />A sample extension which uses Google Analytics to track usage. | <ul></ul>
[Broken Background Color](mv2-archive/tutorials/broken_background_color)<br />Fix an Extension! | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.executeScript</li></ul>
[Getting Started Example](mv2-archive/tutorials/get_started)<br />Build an Extension! | <ul><li>runtime.onInstalled</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li></ul>
[Getting Started Example](mv2-archive/tutorials/get_started_complete)<br />Build an Extension! | <ul><li>declarativeContent.PageStateMatcher</li><li>declarativeContent.ShowPageAction</li><li>runtime.onInstalled</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.executeScript</li><li>tabs.query</li></ul>
[Getting started example](mv2-archive/tutorials/getstarted)<br />This extension allows the user to change the background color of the current page. | <ul><li>runtime.lastError</li><li>storage.local</li><li>storage.sync</li><li>storage.StorageArea.get</li><li>storage.StorageArea.set</li><li>tabs.executeScript</li><li>tabs.query</li></ul>
[Hello Extensions](mv2-archive/tutorials/hello_extensions)<br />Base Level Extension | <ul></ul>
[OAuth Tutorial FriendBlock](mv2-archive/tutorials/oauth_starter)<br />Uses OAuth to connect to Google's People API and display contacts photos. | <ul><li>browserAction.onClicked</li><li>identity.getAuthToken</li><li>tabs.create</li></ul>
[OAuth Tutorial FriendBlock](mv2-archive/tutorials/oauth_tutorial_complete)<br />Uses OAuth to connect to Google's People API and display contacts photos. | <ul><li>browserAction.onClicked</li><li>identity.getAuthToken</li><li>tabs.create</li></ul>
