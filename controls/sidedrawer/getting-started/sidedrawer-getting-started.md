---
title: Getting Started
page_title: Getting Started
position: 0
slug: sidedrawer-getting-started
---

# Getting Started

This example will guide you through the steps needed to add a basic **RadSideDrawer** control in your application.

>Before you proceed, please, take a look at these articles and follow the instructions to setup your app:

>- [Setup on Windows]({%slug getting-started-windows%})
>- [Setup on Mac]({%slug getting-started-mac%})

## Example

If your app is setup, you are ready to add a **RadSideDrawer** control.

You can proceed with defining the component. The DrawerContent represents the hidden view (in it you could place navigational UI, any common setting, etc), while the MainContent hosts the main View of your app.

<snippet id='sidedrawer-gettingstarted-xaml'/>
<snippet id='sidedrawer-gettingstarted-csharp'/>

You also have to add the following namespace:

<snippet id='xmlns-telerikprimitives'/>
<snippet id='ns-telerikprimitives'/>



Finally, set the drawer as content of your page.

Here is the result when you set `IsOpen="True"`:
 
![SideDrawer example](../images/sidedrawer-gettingstarted.png)

>important **SDK Browser** and **QSF** applications contain different examples that show RadSideDrawer's main features. You can find the applications in the **Examples** and **QSF** folders of your local **Telerik UI for Xamarin** installation.

## See Also

- [Project Wizard]({% slug project-wizard %})
- [Getting Started on Windows]({% slug getting-started-windows %})
- [Getting Started on Mac]({% slug getting-started-mac %})
