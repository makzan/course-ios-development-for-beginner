# Lecture 5 Lab 1 — Pushing SafariViewController

In this lab, we will show an external website by pushing in a Safari View Controller.
----
## Objectives

1. Programmatically show another view controller.
2. Use Safari View Controller to display external websites.
3. Configure the Safari View Controller for different purposes.
----
## Background / Scenario

In this lab, we will show an external website by pushing in a Safari View Controller. There are 3 view controllers that are related to displaying web content. They are `UIWebViewController`, `WKWebViewController` and `SFSafariViewController`.
----
## Required Resources

- macOS and Xcode
- Download project “[iOS Lab Safari View Controller](./labs/ios-lab-safari-view-controller.zip)”

----
## Part 1: Programmatically show Safari View Controller

We are given a project that comes with a single view controller. The interface is already configured with a button connected to the `ViewController.swift` code via IBAction.

1. Open the `ViewController.swift` in Xcode.
2. Add `import SafariServices` to the to top of the code, right below the `import UIKit` line of code.
3. Locate the `openExternalWebsite` IBAction.
4. Within the `openExternalWebsite` method, add the following code:
  `let viewController = SFSafariViewController(url: URL(string: "https://example.com")!)`
5. Continue on the `openExternalWebsite` method, add the following code after our previous line of code.
  `self.present(viewController, animated: true, completion: nil)`
6. Run the code into iOS Simulator.
7. When we tap on the button, we should see a Safari View Controller shows in with example.com loaded.
8. Try tapping on the links, we are able to go backward and forward as if we are in web browser.
9. We can tap action to share the URL to the other available services.
10. We can also tap the Safari icon on the bottom right tool bar to open the current page into Safari.
----
## Part 2: Configuring the Safari View Controller

We are already able to present the Safari View Controller. We want to further configure the `SFSafariViewController` to have more control on it.

1. Open the `ViewController.swift` in Xcode.
2. Locate the `openExternalWebsite` IBAction which we just added code in.
3. At the beginning of the IBAction, add the following line that init a configuration.
  `let configuration = SFSafariViewController.Configuration()`
4. Continue set the configuration by enabling reader mode if available:
  `configuration.entersReaderIfAvailable = true`
5. Continue set the configuration by disabling the bar collapsing feature:
  `configuration.barCollapsingEnabled = false`
6. Replace the line of code that we initialize SFSafariViewController to include the configuration we just set:
  `let viewController = SFSafariViewController(url: URL(string: "https://example.com")!, configuration: configuration)`
7. Run the code into iOS Simulator.
8. When we tap on the “More information” link on the example.com, reader mode automatically turns on.
9. When we scroll, the URL bar and tool bar stays and do not collapse.

----

## Part 3: Reflection

The Safari View Controller is useful when we want to display external website within the app. It comes with handy web browsing features including the backward, forward and sharing. It also comes with a built-in swipe-to-go-back gesture for consistent usage by iPhone users.