# Acrylic Toolkit Blur for UWP
Add HostBackdrop with this library to your UWP app. HostBackdrop adds blur and transparency through the window (by the specified element on XAML). If you want give a Neon look for you app, so this is the lib! This is based on the open-source UWP Community Toolkit.

# How to use?
The very first thing you need to do, is to add as a [nuget package to your project](https://www.nuget.org/packages/Mika.Toolkit.Uwp.UI.Animations/), or clone this project and add to your solution and reference it. 

After that, you need to add to your XAML these 3 lines first:
```
   xmlns:acrylic="using:Microsoft.Toolkit.Uwp.UI.Animations.Behaviors"
   xmlns:core="using:Microsoft.Xaml.Interactions.Core"   
   xmlns:interactivity="using:Microsoft.Xaml.Interactivity"
  ``` 
   
And the app body, you will call Acrylic Blur like this:
```
 <Grid Background="White" Opacity="0.55" >
            <interactivity:Interaction.Behaviors>
                <acrylic:Blur Value="1"
                        AutomaticallyStart="True" />
            </interactivity:Interaction.Behaviors>
  </Grid>    
  ```
            
You don't need to put it just on Grid's. You can put on almost every XAML element, like SlackPanel, pictures and more.    
If you are familiar with XAML and Behaviors, this will be extremally easy for you. 
Here is the full "code" on a sample app:

``` XAML
<Page
    x:Class="App3.MainPage"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:local="using:App3"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:acrylic="using:Microsoft.Toolkit.Uwp.UI.Animations.Behaviors"
    xmlns:core="using:Microsoft.Xaml.Interactions.Core"
    xmlns:interactivity="using:Microsoft.Xaml.Interactivity"
    mc:Ignorable="d">

    <Grid Background="{ThemeResource ApplicationPageBackgroundThemeBrush}">
        <Grid Background="White" Opacity="0.55" >
            <interactivity:Interaction.Behaviors>
                <acrylic:Blur Value="1"
                        AutomaticallyStart="True" />
            </interactivity:Interaction.Behaviors>
        </Grid>
    </Grid>
</Page>
```

# Requirements
You can install on Mobile and other devices, but for now, the API used on the library (CreateHostBackdrop) just works on Desktop and it needs Windows 10 version 1703 (build 15063) at least. On devices that is not Desktop, it will show a black background, as the Windows compositor doesn't support yet.

# Issues and Pull Request 
If you have any problems, you can open issues and if you want improvements, you can open Pull Requests any time.

# Contact
If you want to talk with me and other stuff, https://t.me/vitorgrs on Telegram or https://twitter.com/vitorgrs
