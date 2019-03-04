# Lecture 1

CM420-03-2019-c

---

# Agenda

1. Join the classroom
2. Who is Makzan
3. iOS 開發背景

---

# Agenda 1: Join the classroom

---

# Join the classroom

https://makclass.com/join/cm420

---

# What is MakClass ?

派發教材、練習、交流的網上平台

---

# Agenda 2: Who is Makzan

---

# 關於 Makzan

自 2010 年推出 iPad 起投入開發 iOS 遊戲及應用程式。在 iPad 首發當天，我的第一隻遊戲就在 App Store 上架。

---

![Fish ball game screenshot](/slides/images/fishball.jpg)

---

![Chicken Rain game screenshot](/slides/images/chicken-rain.jpg)

---

# 過往開發亮點

- Fish Ball game
- Chicken Rain app
- 音樂 app
- Music Player app
- AR app
- Unity games
- Multiplayers game

---

# 你可以從以下途徑找到我：

- 網站：https://makzan.net
- Github：https://github.com/makzan
- 推特：https://twitter.com/makzan
- FB：https://fb.com/makzan

---

# Agenda 3: iOS 開發背景

---

# 製作 iOS 應用，須要什麼工具？

- Mac
- Xcode
- iOS Simulator
- Developer Apple ID

---

# 將 Xcode 上的 iOS 專案發佈到 iPhone / iPad 上

自從 iOS 9 以後，只要註冊免費 Apple ID 帳號，
就可以通過直接 USB 連接手機及 Xcode 暫寫中的應用程式直接放到手機上運行


---

# iOS 開發的歷史

---

![Xcode welcome screen](/slides/images/xcode-welcome-screen.jpg)

---

# 2007

Web App

---

# 2008

iOS 2.0 SDK

---

# iOS 系統背景

---

^ iOS 系統背景

# 底層 + UI

- macOS X 的 Darwin Unix 系統
- 加上專門為 Touch 而設計的 **UIKit**

---

# Prefix Namespace

蘋果系統的 Class 是使用 Prefix 來做 Namespacing 的

---

例如專門給 iOS 用的界面就是 UI 字開頭，
如 UIView, UILabel, UIButton 等

---

遊戲用的 SpriteKit 就有 SKView, SKScene, SKNode 等

---

位置相關的 CoreLocation 就有 CLLocationManager 等。

---

而數據類型 NSData, NSArray 等，
其 NS 則是遺傳自 Mac OS X 的前身：NextStep 電腦

---

在 Swift 世界，`NS` 字頭開始被無字頭取代。

- NSData → Data
- NSArray → Array
- NSUserDefaults → UserDefaults

---

注：這個去 NS 化過程，未必是等效的。例如 NSArray 及 Array 就是兩種不同的類型。

---

# iOS 系統版本與更新

一般最近兩代系統使用佔有率會[超過 95%](https://mixpanel.com/trends/#report/ios_12/from_date:-31,report_unit:week,to_date:0)

---

# Xcode 介面介紹

---

![Xcode IDE](/slides/images/xcode-ide.jpg)

---

掌握左中右最基本的功能便可以開始 iOS 編程。

---

- 左邊：檔案 Tab
- 中間：主要編輯區域
- 右邊：與主編輯項目有關的屬性

---

![](/slides/images/3-panel-toggles.jpg)

---
![](/slides/images/3-panel-toggles-explain.jpg)

---

# 一個項目的常用檔案

---

^ 一個項目的常用檔案

![](/slides/images/file-panel.jpg)

---

^ 一個項目的常用檔案

- `AppDelegate.swift` 負責控制檔案的 Life Cycle
- `Info.plist` 是應用程式的系統設定，例如於 Home Screen 顯示的名稱、需要的權限及說明文字
- `Main.storyboard` 是主要的介面檔案，如果是簡單的應用程式，這個檔案可以包含整個 App 的所有界面
- `LaunchScreen.storyboard` 是打開 App 時，未完成載入期間，用戶望到的第一個個畫面。
- `Assets.xcassets` 裝著一群群的圖片檔案，例如 App Icon，App Icon 有不同的尺寸以符合不同機種及使用情景。
- `ViewController.swift` 是預設 Single View App 的範本檔案，是第一個畫面背後的程序碼。

---

THE END



