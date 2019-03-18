# Lecture 5 Lab 2 — Connecting Multiple View Controllers Storyboard

In this lab, we will use `segue` to pass variables into the second view controller.

----
## Objectives

1. Pass variables to the next view controller while using Storyboard connection.
----
## Background / Scenario

Storyboard connection between two view controllers are done automatically by operating system. Still we want to pass in different values to the next view controller according to different code logic.

----
## Required Resources

- macOS and Xcode
- Download the [lab project file](./labs/ios-lab-navigation-segue.zip).

----

## Part 1: Instance variable `choice`

1. In the `SecondViewController.swift`, add a `choice` instance variable under class definition.
  `var choice = 0`
2. In the `viewDidLoad` method, add the following line of code that displays the label.
  `outputLabel.text = "Selected \(choice)"`
3. Copy the entire `// Mark : - Navigation` comment block.
4. Open the `ViewController.swift` file.
5. Past the entire `// Mark : - Navigation` comment block into the `ViewController` class.
6. Add a `choice` instance variable within the `ViewController` class.

----

## Part 2: Storyboard

7. Open the `Main.storyboard` file.
8. Select the default View Controller.
9. Open “Assistant Editor” if it is not enabled yet.
10. Control-drag the first choice button to the `ViewController.swift` to create an IBAction.
11. Select event to “Touch Down” and name the action `selectChoice`.
12. Control-drag the other choice buttons to the same IBAction.
13. Change the `sender: Any` in IBAction argument to `sender: UIButton`.
14. Add the following code to the `selectChoice` IBAction.
  `choice = sender.tag`
15. Uncomment the `// Mark: - Navigation` code block to enable `prepare (for segue:, sender:)` method.
16. Put the following code inside the `prepare (for segue:, sender:)`:

```swift
let viewController = segue.destination as! SecondViewController
viewController.choice = choice
```

----

## Part 3: Reflection

We need to use the `TouchDown` instead of `TouchUpInside` event for the button because we want to set the currently selected choice before the segue triggers. If we use `TouchUpInside`, the IBAction will run after the segue triggers and we cannot set the `choice` variable in time.