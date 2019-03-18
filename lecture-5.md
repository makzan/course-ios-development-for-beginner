# Lecture 5 — Connecting Multiple View Controllers


----
3 ways to connect view controllers:

----

1. Storyboard connection with segue
2. Programmatically connecting to new view controller
3. Programmatically connecting a view controller within storyboard
----

# Code Snippets

----
^ Storyboard connection with segue

```swift
// In a storyboard-based application, you will often want to do a little preparation before navigation
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    // Get the new view controller using segue.destination.
    // Pass the selected object to the new view controller.

    let viewController = segue.destination as! ViewController
    viewController.selectedSite = selectedRow

}
```
----

^ Programmatically connecting a view controller within storyboard

```swift
let viewController = storyboard?.instantiateViewController(withIdentifier: "LoginViewController")
self.present(viewController, animated: true, completion: nil)
```

----
^ Programmatically presenting `UIActivityViewController`

```swift
let url = URL(string: "https://example.com")!
let viewController = UIActivityViewController(activityItems: [url], applicationActivities: nil)
self.present(viewController, animated: true, completion: nil)
```
----
^ Programmatically presenting `SFSafariViewController`

```swift
let viewController = SFSafariViewController(url: URL(string: "https://example.com")!)
self.present(viewController, animated: true, completion: nil)
```
----
# When to use Storyboard connection with segue?
----
^ When to use Storyboard connection with segue?

When we have fixed connection relationship between two view controllers, the easiest way is to define the connection in storyboard.
----
# When to use programmatically connection?

----
^ When to use programmatically connection?

1. When we need to present system-controlled view controllers.
2. When we need to dynamic present a view controller, even it is already defined in the storyboard.
----

^ When we need to present system-controlled view controllers

For example, presenting:

- `SFSafariViewController`
- `UIActivityViewController`
- `UIAlertController` for both alerts and action sheet.

----

^ When we need to dynamic present a view controller, even it is already defined in the storyboard

For example, when we have need logic to determine what is the next view.

----

## Example: Creating an app with static table view, UI view and web view

----

<iframe src="https://player.vimeo.com/video/324934415?color=ff9933&byline=0&portrait=0" width="640" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
