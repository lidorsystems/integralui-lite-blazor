# IntegralUI Lite for Blazor, v24.1 

IntegralUI Lite for Blazor is a FREE UI library of advanced, customizable and high performance components for Blazor .NET. 

<b>Note</b> FREE for commercial use.

![IntegralUI Lite for Blazor 24.1](https://www.lidorsystems.com/products/integralui/blazor/lite/integralui-lite-blazor-24.1.png)

<b>Note</b> This library is a lite version of the full product package: <a href="https://www.lidorsystems.com/products/integralui/blazor/">IntegralUI for Blazor</a>. Some of the more advanced component features are excluded in this version.

Here is a brief overview of what is included:

## Components

[Button](https://www.lidorsystems.com/products/integralui/blazor/samples/button/overview) - Represents a button

[ButtonGroup](https://www.lidorsystems.com/products/integralui/blazor/samples/buttongroup/overview) - Manages actions of multiple buttons arranged in group

[Card](https://www.lidorsystems.com/products/integralui/blazor/samples/card/overview) - A flip card with two sides

[CheckBox](https://www.lidorsystems.com/products/integralui/blazor/samples/checkbox/overview) - Represents a check box

[DropDown]() - Shows other components in a dropdown window

[List](https://www.lidorsystems.com/products/integralui/blazor/samples/list/overview) - Displays a simple list of items with content in custom layouts

[PopOver](https://www.lidorsystems.com/products/integralui/blazor/samples/popover/overview) - Displays custom HTML content over specified element

[RadioButton](https://www.lidorsystems.com/products/integralui/blazor/samples/radiobutton/overview) - Represents a radio button

[Select](https://www.lidorsystems.com/products/integralui/blazor/samples/select/overview) - Allows you to select an item from a dropdown list

[Tooltip](https://www.lidorsystems.com/products/integralui/blazor/samples/tooltip/overview) - Adds a tooltip to an element

[TreeList](https://www.lidorsystems.com/products/integralui/blazor/samples/treelist/overview) - Allows you to navigate through tree hierarchy showing only one list at a time


## Dependencies

IntegralUI Lite for Blazor is built with .NET 8.0 framework.


## DEMO

[Online QuickStart App](https://www.lidorsystems.com/products/integralui/blazor/samples/) - An online demo of each component included


## Installation


```bash
npm install https://github.com/lidorsystems/integralui-lite-blazor.git
```

or directly from NPM

```bash
npm i integralui-lite-blazor
```

Library files are located in /bin folder of product's installation directory.

1. Copy/Paste the NuGet package from /bin folder to a referencing folder (the folder from where you are referencing external or vendor libraries) in your project. The /resources folder is optional.
2. Install the NuGet package for IntegralUI Lite library from a local folder.
3. Open your project
4. From Solution Explorer right-click on Dependencies option and select "Manage NuGet Packages..."
5. In top-right corner click on Tools icon to create new package source
6. Create a new package source by licking on + tool button
7. Under Name field enter IntegralUI Lite and under Source field click on browse button to select your referencing folder and click Update button and press OK
8. The referencing folder should contain the NuGet package for IntegralUI Lite library, the one copied from /bin folder (see first line above)
9. In NuGet package manager select the IntegralUI Lite package source from the dropdown list (from top-right corner)
10. Select the Browse tab to see all available IntegraUI versions
11. Install the latest version
12. Close the NuGet package manager

Now you can use all components available in IntegralUI Lite library. There are few namespaces that you can import:

IntegralUI.Lite.Components<br/>
IntegralUI.Lite.Events<br/>
IntegralUI.Lite.Interfaces<br/>
IntegralUI.Lite.Services<br/>

All components are located under IntegralUI.Lite.Components namespace.


### How to Use IntegralUI components in Blazor Apps

At first, you need to install the IntegralUI Lite for Blazor library on your side and add a reference to a component you want to use (see above steps).

In case of IntegralUI List component, you need to do the following:

1. Open a Blazor page in your project
2. Add code line that will import the IntegralUI Lite components
3. Place the List component using the IntegralUIList tag
4. Specify the generic TItem type that you will use as a data model
5. Set the Items property to connect the List to your data source
6. (optional) Define the template that will be used to create the content for items using the ItemTemplate
7. (optional) Add custom HTML elements or other Blazor components inside the template
8. (optional) Add other features like sorting, filtering etc. require corresponding property or event to be set
9. (optional) Create a reference to the component using the @ref attribute, to call public methods

For example:

```
@page "/"

<IntegralUIList @ref=listRef Id="list-sample" TItem="CustomItem"
    Items="@items"
    MouseWheelSpeed="IntegralUISpeedMode.VerySlow"
    Size="@ctrlSize">
    <ItemTemplate>
        <span>@context.Item?.Text</span>
    </ItemTemplate>
</IntegralUIList>

@code {
    // Get a reference to the IntegralUI TreeView component to call public methods
    private IntegralUIList<CustomItem>? listRef;

    // Data model
    public class CustomItem
    {
        public string? Id { get; set; }
        public string? Genre { get; set; }
        public double Rating { get; set; }
        public bool Selected { get; set; } = false;
        public string? Text { get; set; }
        public int Year { get; set; }
    }

    // Define the component size
    public IntegralUISize ctrlSize = new() { Width = 350, Height = 300 };

    // Add items to the List component
    public List<CustomItem> items = new()
    {
        new CustomItem { Id = "1", Genre = "Sci-Fi", Text = "Star Trek", Year = 2009, Rating = 8 },
        new CustomItem { Id = "2", Genre = "Adventure", Text = "Cast Away", Year = 2000, Rating = 7 },
        new CustomItem { Id = "3", Genre = "Action", Text = "Gladiator", Year = 2000, Rating = 8 },

        // . . .
    };
}
```


## QuickStart App

There is a demo application with source code that contains samples for each component included in the IntegralUI Lite for Blazor product package. It can help you to get started quickly with learning about the components and write tests immediatelly. 

The Quick Start project is available under /quickstart folder in product installation directory.


## License Information

You are FREE to use this product to develop Internet and Intranet web sites, web applications and other products, with no-charge.

This project has been released under the IntegralUI Lite for Blazor License, and may not be used except in compliance with the License.
A copy of the License should have been installed in the product's root installation directory or it can be found here: [License Agreement](https://www.lidorsystems.com/products/integralui/blazor/lite/integralui-lite-blazor-license-agreement.pdf).

This SOFTWARE is provided "AS IS", WITHOUT WARRANTY OF ANY KIND, either express or implied. See the License for the specific language governing rights and limitations under the License.