# Lecture 5 Lab 3 — Storyboard ID

In this lab, we programmatically connect to a view controller that is in the storyboard file but not connected by any segues.

----
## Objectives

1. Get the instance of a particular view controller from a storyboard.
2. Programmatically show any view controller from storyboard.
----
## Background / Scenario

There are cases that we cannot specific an automatically storyboard connection. For example, when we need to present the login view controller whenever the user session expires. We don’t have a specific route for the login view. In such case, we can programmatically instantiate a view controller from the storyboard.

----
## Required Resources

- macOS and Xcode
- Download the [Storyboard ID](./labs/ios-lab-storyboard-id.zip) lab project file.

----

## Part 1: Define the `chocie` instance variable

1. In the `SecondViewController.swift`, add a `choice` instance variable under class definition.
  `var choice = 0`
2. In the `viewDidLoad` method, add the following line of code that displays the label.
  `outputLabel.text = "Selected \(choice)"`

----

## Part 2: Storyboard

3. In the `Main.storyboard`, select the Second View Controller. On the right panel, select the 3rd tab “Identity Inspector”.
4. In the `Storyboard ID`, input `SecondViewController`.
5. Still in the `Main.storyboard`, select the default view controller.
6. Select the 4 choice buttons. Set the tag to 1, 2, 3, 4 correspondingly.
7. Open “Assistant Editor” if it is not enabled yet.
8. Control-drag the first choice button to `ViewController.swift` to create action and name it `selectChoice`.
9. Control-drag the other choice buttons to the same IBAction.
10. Change the `sender: Any` in IBAction argument to `sender: UIButton`.
11. Add the following code to the `selectChoice` IBAction.

```swift
let viewController = storyboard?.instantiateViewController(withIdentifier: "SecondViewController") as? SecondViewController
if viewController != nil {
    viewController!.choice = sender.tag
    navigationController?.pushViewController(viewController!, animated: true)
}
```

----

## Part 3: Reflection

Storyboard provides a `instantiateViewController(withIdentifier:` method for us to fetch any view controller in program. The only requirement is that we have set the `Storyboard ID` in the storyboard file and the identifier is string. The return value is a generic `UIViewController` so we need to cast it into our desired view controller, for example `SecondViewController` in this project. The identifier is string means we cannot guarantee to find a view controller. So we need to check if the return value is `nil` before using it.

Whenever we are inside a navigation controller controlled view controller, we can use `navicationController?.pushViewController` method to push in the next view controller.