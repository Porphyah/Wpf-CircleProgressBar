# Wpf-CircleProgressBar
A Circle Progress Bar based on Data Binding, you can use it in your WPF project.

How to use it?

①Import these two files to your wpf project.

②Pay attention to change the two code positions below:
  -CircleProgressBar.xaml line:3
    xmlns:local="clr-namespace:YourNamespace"
  Change [YourNamespace] to your project namespace.
  
  -CircleProgressConverter.cs line:11
    namespace YourNamespace
  Change [YourNamespace] to your project namespace.
  
③Now open App.xaml to add:
  <Application.Resources>
    <ResourceDictionary>
      <ResourceDictionary.MergedDictionaries>
         <ResourceDictionary Source="CircleProgressBar.xaml"/>
      </ResourceDictionary.MergedDictionaries>
    </ResourceDictionary>
  </Application.Resources>
 Notice: If you import the file into a folder inside the project, you should add the folder path into the ResourceDictionary Source.
 
 ④When you add a progress bar in your xaml file, just code Style="{StaticResource CircleProgressBarStyle}" in the ProgressBar Section.
  All the properties are used like the default progress bar, 
  and there's one thing more: the property Tag represents the thickness of the progress ring.
  
 Example:
  <ProgressBar Style="{StaticResource CircleProgressBarStyle}" Value="50" Tag="10" 
               HorizontalAlignment="Center" Height="100" Width="100" VerticalAlignment="Center"/>
               
 Wish you enjoy!
