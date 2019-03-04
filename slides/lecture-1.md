# Lecture 1

CM420-03-2019-c

---

# Agenda

1. Join the classroom
2. Who is Makzan
3. iOS 開發背景
4. 使用 Storybaord

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

# iOS Simulator

![](/slides/images/ios-simulator.jpg)

---

在我們落實體機試之前，我們一般會利用 Xcode 跟來的模擬器進行測試。

---

![](/slides/images/ios-simulator-choices.jpg)

---

iOS Simulator 模擬器讓我們選擇不同畫面尺寸，方便測試應用在不同畫面的運行情況。



---

# Xcode 介面介紹

---

![Xcode IDE](/slides/images/xcode-ide.jpg)

---

掌握 **左中右**的基本功能便可以開始 iOS 編程

---

- 左邊：檔案 Tab
- 中間：主要編輯區域
- 右邊：與主編輯項目有關的屬性

---

![](/slides/images/3-panel-toggles.jpg)

---
![](/slides/images/3-panel-toggles-explain.jpg)

---

# 開發 iOS App，我應該選擇 Objective-C 還是 Swift 語言？

![](/slides/images/languages.jpg)

---

Objective-C 提倡 Message Passing，即 Call function 是溝通，而不是命令。

所以用 Objective-C 寫出來的語句很像在說英文。例如：

```objc
[gameObject placeAtX: 123 andY: 456];
```

---

為了更好地推廣編程學習，蘋果便於數年前推出了 Swift 語言。
現在 Swift 語言已經趨向穩定成熟，而且網上的新教材基本上都使用 Swift 語言了。

---

所以，如果現在開始學寫 iOS 應用，直接選擇 Swift 是擁抱未來的好選擇。

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

# Agenda 4: 使用 Storybaord

---

# 使用 Storybaord 建立 App Prototype

---

![](/slides/images/storyboard-example.jpg)

---

在撰寫第一行代碼之前，
我們可以純用 Storyboard 生成頗為完整的原型 Prototype。
當然，有條件判斷的 Prototype 還是須要寫少量代碼的。

---

# Storyboard 的前世今生

NIB → XIB → Storyboard


---

<iframe src="https://player.vimeo.com/video/293524239?color=ff9933&byline=0&portrait=0" width="800" height="548" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>


---

<iframe src="https://player.vimeo.com/video/293523608?color=ff9933&byline=0&portrait=0" width="800" height="549" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

---

# 包剪揼例子

<iframe src="https://player.vimeo.com/video/259699882?color=ff9933&byline=0&portrait=0" width="800" height="514" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

---

# 製作包剪揼小應用

---

^成果預覽

![](https://onionslides.com/system/media/uploads/000/000/214/original/4416-Screen_Shot_2018-03-13_at_1.43.22_AM.png)

---

^選擇新項目後，選擇 Single View App

![](https://onionslides.com/system/media/uploads/000/000/001/large/xcode-new-single-view-app.png)

---

^在新專案中，輸入應用名稱，Identifier 通常是網址。如沒有，也可以是個人名稱

![](https://onionslides.com/system/media/uploads/000/000/215/original/4456-xcode-new-project-detail.png)

---

^在左上方的控制中，我們可以執行應用。亦可以選擇在不同的摸擬器中執行

![](https://onionslides.com/system/media/uploads/000/000/216/original/4448-xcode-choose-view-controller.png)

---

^在左面的檔案列表中，選擇 Main.storyboard

![](https://onionslides.com/system/media/uploads/000/000/217/original/4443-xcode-choose-main-storyboard.png)

---

^在右下方的介面元件列表中，找出 Navigation Controller

![](https://onionslides.com/system/media/uploads/000/000/218/original/4444-xcode-choose-navigation-controller.png)

---
^將 Navigation Controller 拖進 Storyboard

![](https://onionslides.com/system/media/uploads/000/000/219/original/4454-xcode-drag-navigation-controller-to-storyboard.png)

---
^現在畫面多了，可以 zoom out 來一覽全部介面，需要時再 zoom in 特定介面進行設定

![](https://onionslides.com/system/media/uploads/000/000/220/original/4466-xcode-zoom-out-storyboard.png)

---

^拖進來後，將右邊的 View Controller 畫面刪除

![](https://onionslides.com/system/media/uploads/000/000/221/original/4451-xcode-delete-right-view-controller.png)

---

^將起始標記的箭頭，從原有畫面中拖拉到新拖進的 View Controller，表示應用一打開的起始介面

![](https://onionslides.com/system/media/uploads/000/000/222/original/xcode-drag-starting-arrow.gif)

---

^可以將兩個 View Controller 畫面並排在一起，方便管理

![](https://onionslides.com/system/media/uploads/000/000/223/original/4461-xcode-reposition.png)

---

^滑鼠右鍵拖拉，從 Navigation Controller 拖拉到原來 View Controller 畫面

![](https://onionslides.com/system/media/uploads/000/000/224/original/xcode-right-drag.gif)

---

^選擇 Root View

![](https://onionslides.com/system/media/uploads/000/000/225/original/4445-xcode-choose-root-view.png)

---

^在右下方介面元件列表中，找出 Button 按鈕。拖拉 3 個到畫面中

![](https://onionslides.com/system/media/uploads/000/000/226/original/4452-xcode-drag-3-buttons.png)

---

^將按鈕字句分別改為「包」「剪」「揼」

![](https://onionslides.com/system/media/uploads/000/000/227/original/4460-xcode-rename-buttons.png)

---

^將 3 個 View Controller 拖拉進 Storyboard

![](https://onionslides.com/system/media/uploads/000/000/228/original/4453-xcode-drag-3-view-controllers.png)

---

^利用滑鼠右鍵按住按鈕，再拖拉到新拖入的畫面

![](https://onionslides.com/system/media/uploads/000/000/229/original/4463-xcode-right-drag-button-to-view.png)

---

^在列表中，選擇第一個 Show

![](https://onionslides.com/system/media/uploads/000/000/230/original/4450-xcode-choose-show.png)

---

^分別連接三個新畫面

![](https://onionslides.com/system/media/uploads/000/000/231/original/4449-xcode-connect-all-3-views.png)

---

^在右下方的介面元件中，找出 Label，再分別拖到三個新畫面中

![](https://onionslides.com/system/media/uploads/000/000/232/original/4455-xcode-drag-label.png)

---

^我們可以將 Label 及 Button 的文字調整大一點

![](https://onionslides.com/system/media/uploads/000/000/233/original/4457-xcode-font-size.png)

---

^可以設定背景顏色

![](https://onionslides.com/system/media/uploads/000/000/234/original/4447-xcode-bg-color.jpg)

---

^這個是在模擬器運行的結果

![](https://onionslides.com/system/media/uploads/000/000/235/original/4462-xcode-result.jpg)



---
# Conclusion of Lecture 1

1. Join the classroom
2. Who is Makzan
3. iOS 開發背景
4. 使用 Storybaord

---
End of Lecture 1



