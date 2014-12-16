---
title: Calendar Getting Started
page_title: Calendar Getting Started
position: 3
slug: calendar-getting-started
---

# Getting Started #
This example will guide you through the steps needed to add a basic RadCalendar control in your application.

## Add References to Telerik UI for Xamarin.Forms ##
First you have to create a new Xamarin.Forms project. You can see how in the [Getting Started Example]({% slug getting-started %} "Getting Started with Telerik UI foe Xamarin.Forms"). Then you have to add reference to the following assemblies:

* **Portable** (if you have created Xamarin.Forms Portable App)
	- Telerik.XamarinForms.Input.dll
	- Telerik.XamarinForms.Common.dll
* **Android**

	- Telerik.Xamarin.Android.Input.dll
	- Telerik.Xamarin.Android.Common.dll
	- Telerik.Xamarin.Android.Primitives.dll
	- Telerik.XamarinForms.Chart.dll
	- Telerik.XamarinForms.ChartRenderer.Android.dll
	- Telerik.XamarinForms.Common.dll
* **iOS**

	- Telerik.Xamarin.iOS.dll
	- Telerik.XamarinForms.Input.dll
	- Telerik.XamarinForms.ChartRenderer.iOS.dll
	- Telerik.XamarinForms.Common.dll
* **WinPhone**
	
	- Telerik.Windows.Controls.Input.dll
	- Telerik.Windows.Controls.Primitives.dll
	- Telerik.Windows.Core.dll
	- Telerik.XamarinForms.Input.dll
	- Telerik.XamarinForms.ChartRenderer.WinPhone.dll
	- Telerik.XamarinForms.Common.dll

![Add Calendar References](calendar-getting-started-references.png)

You will have to add the following code to these project files:

* **Android**: MainActivity.cs
  
		[assembly: Xamarin.Forms.ExportRenderer(typeof(Telerik.XamarinForms.Input.RadCalendar), typeof(Telerik.XamarinForms.InputRenderer.Android.CalendarRenderer))]
	
	You also have to add the following code in the `OnCreate(Bundle bundle)` before the `Forms.Init(this, bundle)` call:

		CalendarCustomResourcesAndroid.Instance.Load();

* **iOS**: AppDelegate.cs

		[assembly: Xamarin.Forms.ExportRenderer(typeof(Telerik.XamarinForms.Input.RadCalendar), typeof(Telerik.XamarinForms.InputRenderer.iOS.CalendarRenderer))]

	You also have to create the following instances in the `FinishedLaunching()` method before the `Forms.Init()` call:

		new Telerik.XamarinForms.InputRenderer.iOS.CalendarRenderer();
		CalendarCustomResourcesIOS.Instance.Load();



* **WinPhone**: MainPage.xaml.cs
    
		[assembly: Xamarin.Forms.ExportRenderer(typeof(Telerik.XamarinForms.Input.RadCalendar), typeof(Telerik.XamarinForms.InputRenderer.WinPhone.CalendarRenderer))]

	You also have to create the following instances in the `MainPage()` constructor before the `Forms.Init()` call:

		CalendarCustomResourcesWP.Instance.Load();

##Add Calendar Control to Your Project##

1. Add new Xamarin.Forms page to your Portable/Shared project:
	* **Visual Studio**: right click on the project > `Add` > `New Item...` > choose `Forms Xaml Page`
	* **Xamarin Studio**: right click on the project > `Add` > `New File` > choose `Forms ContentPage Xaml`

1. Modify the GetMainPage() method in the App.xaml.cs file to set the newly created page as a front page of the application:

		public class App
		{
			public static Page GetMainPage()
			{
				return new MainPage();
			}
		}

1. Edit the MainPage.xaml file to add a RadCalendar control:

	    <telerikInput:RadCalendar/>
where:  

		 xmlns:telerikInput="clr-namespace:Telerik.XamarinForms.Input;assembly=Telerik.XamarinForms.Input"
Alternatively, you can add the calendar in code behind:

		public partial class MainPage
	    {
	        public MainPage()
	        {
	            InitializeComponent();
	            
				this.Content = new RadCalendar();
	        }
		}

Here is the result:  
![Basic RadCalendar Example](calendar-getting-started-example.png "Basic RadCalendar")