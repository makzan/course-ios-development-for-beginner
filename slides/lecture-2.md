# Lecture 2—Connecting Interface and Swift Source Code

In this lecture, we use implement code on the interface. 

---- 

- Connecting storyboard and view controller classes
- Using UILabel and UIButton
- Learning IBOutlet and IBAction

---- 

# Connecting interface and view controller

---- 
In Storyboard, we can drag many view controller interface into the storyboard file. How Xcode knows which source code to match each interface? 

---- 

This is done via assigning the ViewController reference (cmd+option+3) in the View Controller interface.

---- 

![](view-controller-reference.png)

^ On the third tab on right panel, it defines the custom class for the selected interface element.

---- 

![](view-controller.png)

^ If we select the left yellow icon on top of the interface, we select the `View Controller`.

---- 

![](interface-sidebar.png)

^ It is also selectable via the interface sidebar.
---- 
^Then, we can assign view controller class on the third tab.

![](custom-class.png)

---- 

## View Controller Naming

---- 

We create new swift file for each view controller. Normally, we name them such as `HomeViewController`, `LoginViewController`.

^ Note that we usually use the type as suffix when naming in Swift.
---- 

# IBOutlet and IBAction
---- 
There are 2 important concepts when we refer the interface elements in code. They are **IBOutlet** and **IBAction**.

---- 
- **IBOutlet** is for referencing element as variables in code. 
- **IBAction** is for registering events as methods in code. Most of them are tap event for buttons.

---- 
 
# Connecting IBOutlet and IBAction

---- 
^ We can connect IBOutlet reference or IBAction method between interface and Swift code in Xcode.

1. Turn on the Assistant Editor.
2. On the left, we should see the Storyboard.
3. On the right, we should see the corresponding view controller source code.

---- 
If the source code on the right side doesn’t match the interface, we may check the upper navigation bar on the assistant editor.
---- 
![](navigation-tab.png)
---- 
## Naming rule for IBOutlet and IBAction
---- 
The naming rule follows the same rule of variable naming.

1. No space between words.
2. First character is always letter. No number on first character.
3. First character is lower case.
4. Other words begins with upper case.

^ Naming rule

---- 
## Renaming IBOutlet and IBAction
---- 
Be careful when we need to rename the IBOutlet or IBAction. The name is referenced in both Storyboard file and the swift code. It is very easy to forget to change both name.

^ Renaming IBOutlet and IBAction

---- 

^ Renaming IBOutlet and IBAction

If we only change one name in code and forget to change the storyboard, we will have app crash when it executes.
---- 
^ The correct way to rename IBOutlet and IBAction:

1. Delete the references in Interface Builder
2. Rename in swift source code
3. Use the + sign next to the variable or method and drag it to the target view on the interface. (From right to left)
