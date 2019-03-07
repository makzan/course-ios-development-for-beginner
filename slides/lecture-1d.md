# Lecture 1, Extra example

Rock-paper-scissors

---- 

# Example of Rock-paper-scissors example

<iframe src="https://player.vimeo.com/video/259699882?color=ff9933&byline=0&portrait=0" width="800" height="514" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

---- 

# Steps to build a Rock-paper-scissors

---- 

^ Preview

![](https://onionslides.com/system/media/uploads/000/000/214/original/4416-Screen_Shot_2018-03-13_at_1.43.22_AM.png)

---- 

^ Create a new Xcode project and select “Single View App” template.

![](https://onionslides.com/system/media/uploads/000/000/001/large/xcode-new-single-view-app.png)

---- 

^ In the new project, enter the application name. The identifier is usually a reverse domain.

![](https://onionslides.com/system/media/uploads/000/000/215/original/4456-xcode-new-project-detail.png)

---- 

^ On the upper-left of Xcode, we can run the project into selected simulator.

![](https://onionslides.com/system/media/uploads/000/000/216/original/4448-xcode-choose-view-controller.png)

---- 


^ Select `Main.storyboard` on the file panel on the left.

![](https://onionslides.com/system/media/uploads/000/000/217/original/4443-xcode-choose-main-storyboard.png)

---- 

^ In the UI list, find the Navigation Controller. (The UI List is either on the top of Xcode 10 or on the bottom right of Xcode 9)

![](https://onionslides.com/system/media/uploads/000/000/218/original/4444-xcode-choose-navigation-controller.png)

---- 

^ Drag Navigation Controller into the Storyboard.

![](https://onionslides.com/system/media/uploads/000/000/219/original/4454-xcode-drag-navigation-controller-to-storyboard.png)

---- 

^ Now the screen is full of view controller, we can zoom in and out to work on specific view controller interface.

![](https://onionslides.com/system/media/uploads/000/000/220/original/4466-xcode-zoom-out-storyboard.png)

---- 


^ We don’t need the table view controller on the right. We delete it.

![](https://onionslides.com/system/media/uploads/000/000/221/original/4451-xcode-delete-right-view-controller.png)

---- 

^ There is an arrow pointing to the default view controller. It is the initial view controller indicator. We can drag it to the newly created navigation controller.

![](https://onionslides.com/system/media/uploads/000/000/222/original/xcode-drag-starting-arrow.gif)

---- 

^ We can put the two view controllers together for better readability. The navigation controller is on the left and the default blank view controller is on the right.

![](https://onionslides.com/system/media/uploads/000/000/223/original/4461-xcode-reposition.png)

---- 


^ We can define the relationship of these two view controllers by control-dragging (or right-click-and-dragging) from the navigation controller to the original view controller.

![](https://onionslides.com/system/media/uploads/000/000/224/original/xcode-right-drag.gif)

---- 

^ Then we select root view as the relationship.

![](https://onionslides.com/system/media/uploads/000/000/225/original/4445-xcode-choose-root-view.png)

---- 

^ In the UI list, we find the Button element and drag 3 of them into the blank view controller.

![](https://onionslides.com/system/media/uploads/000/000/226/original/4452-xcode-drag-3-buttons.png)

---- 

^ We rename the label of button to Rock, Paper and Scissors.

![](https://onionslides.com/system/media/uploads/000/000/227/original/4460-xcode-rename-buttons.png)

---- 

^ Drag 3 more view controllers into Storyboard.

![](https://onionslides.com/system/media/uploads/000/000/228/original/4453-xcode-drag-3-view-controllers.png)

---- 

^ Control drag the button to the newly created view controller

![](https://onionslides.com/system/media/uploads/000/000/229/original/4463-xcode-right-drag-button-to-view.png)

---- 

^ Select the “Show” relationship

![](https://onionslides.com/system/media/uploads/000/000/230/original/4450-xcode-choose-show.png)

---- 
^ Repeat the steps to connect all 3 view controllers from 3 buttons.

![](https://onionslides.com/system/media/uploads/000/000/231/original/4449-xcode-connect-all-3-views.png)

---- 

^ In the UI List, drag a label to each of the newly created view controller.

![](https://onionslides.com/system/media/uploads/000/000/232/original/4455-xcode-drag-label.png)

---- 
^ Set the label to Rock, Paper, Scissors. We may also make the text bigger.

![](https://onionslides.com/system/media/uploads/000/000/233/original/4457-xcode-font-size.png)

---- 

^ We may also set background color to the view controllers.

![](https://onionslides.com/system/media/uploads/000/000/234/original/4447-xcode-bg-color.jpg)

---- 

^ Here is how it runs in the simulator.

![](https://onionslides.com/system/media/uploads/000/000/235/original/4462-xcode-result.jpg)



---- 

End of Rock-Paper-Scissors demo.