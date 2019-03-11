# Lecture 3—AutoLayout Basic

CM420-03-2019-C

---- 

# Layout approach in iOS

- Table view (e.g. Settings app)
- Table view with custom cell (e.g. [CTMBuddy](https://itunes.apple.com/us/app/ctm-buddy/id489789348?mt=8) app)
- Collection view (e.g. Photos)
- Scroll view (What Scroll view and Collection view are based on)
- Stack views and nested Stack views
- Any nested UIViews

---- 

# Views within its container

Any views with subview, we can control the sub-view layout with **AutoLayout**

---- 

# AutoLayout

It is all about **Constraints** that controls the position and dimensions.

---- 

# Constraint Fulfilment Requirement

**One and only one** variable from one edge to another edge.

---- 

# Tips

- Group views before applying auto-layout
- Place views in almost correct position before applying auto-layout
- Stick to one device size before applying auto-layout
- Remove all constraints and start over if it is too messy to fix