# load-checkbox-in-each-nodes-with-unbound-mode-in-.net-maui-treeview
This repository demonstrates how to display checkboxes in each node of the .NET MAUI TreeView (SfTreeView) control using unbound mode data population. It provides a sample implementation that shows how to define nodes directly in XAML, enable recursive checkbox selection, and bind checkbox states for interactive hierarchical selection.

## Sample

### XAML

```xaml
<ContentPage.Content>
        <treeview:SfTreeView x:Name="treeView" 
                             CheckBoxMode="Recursive"
                             SelectionMode="None">

            <treeview:SfTreeView.Nodes>
                <treeviewengine:TreeViewNode Content="North America" IsExpanded="True">
                    <treeviewengine:TreeViewNode.ChildNodes>
                        <treeviewengine:TreeViewNode Content="United States of America"/>
                        <treeviewengine:TreeViewNode Content="Cuba"/>
                        <treeviewengine:TreeViewNode Content="Mexico" IsChecked="True"/>
                    </treeviewengine:TreeViewNode.ChildNodes>
                </treeviewengine:TreeViewNode>
                <treeviewengine:TreeViewNode Content="Africa" IsExpanded="True">
                    <treeviewengine:TreeViewNode.ChildNodes>
                        <treeviewengine:TreeViewNode Content="Nigeria" IsChecked="True"/>
                        <treeviewengine:TreeViewNode Content="Egypt"/>
                        <treeviewengine:TreeViewNode Content="South Africa"/>
                    </treeviewengine:TreeViewNode.ChildNodes>
                </treeviewengine:TreeViewNode>
            </treeview:SfTreeView.Nodes>

        <treeview:SfTreeView.ItemTemplate>
            <DataTemplate>
                <Grid Padding="5">
                    <checkbox:SfCheckBox Text="{Binding Content}" IsChecked="{Binding IsChecked, Mode=TwoWay}"/>
                </Grid>
            </DataTemplate>
        </treeview:SfTreeView.ItemTemplate>
    </treeview:SfTreeView>

</ContentPage.Content>
```

## Requirements to run the demo

To run the demo, refer to [System Requirements for .NET MAUI](https://help.syncfusion.com/maui/system-requirements).

Make sure that you have the compatible versions of [Visual Studio 2022](https://visualstudio.microsoft.com/downloads/ ) with the Dot NET MAUI workload and [.NET Core SDK 7.0](https://dotnet.microsoft.com/en-us/download/dotnet/7.0) or later version in your machine before starting to work on this project.

## Troubleshooting:
### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion® has no liability for any damage or consequence that may arise from using or viewing the samples. The samples are for demonstrative purposes. If you choose to use or access the samples, you agree to not hold Syncfusion® liable, in any form, for any damage related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion®'s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion®'s samples. 
