# navigate-between-views-by-selecting-an-item-in-a-horizontal-listView-in-.net-maui

This example demonstrates how to navigate across views by selecting an item from the horizontal listview in .NET MAUI ListView (SfListView).

## Sample

```xaml
<listView:SfListView
                x:Name="list"
                Grid.Row="2"
                ItemSize="70"
                ItemSpacing="0,0,5,0"
                ItemTapped="list_ItemTapped"
                ItemsSource="{Binding Items}"
                Orientation="Horizontal"
                SelectionBackground="#d3d3d3"
                SelectionMode="Single">

    <listView:SfListView.ItemTemplate>
        <DataTemplate x:Name="ItemTemplate">
            <ViewCell>
                <ViewCell.View>
                    <Grid x:Name="grid" RowSpacing="5">
                        <Image
                            HeightRequest="50"
                            HorizontalOptions="Center"
                            Source="{Binding ContactImage}"
                            VerticalOptions="Center" />
                    </Grid>
                </ViewCell.View>
            </ViewCell>
        </DataTemplate>
    </listView:SfListView.ItemTemplate>
</listView:SfListView>
```

```c#
private void list_ItemTapped(object sender, Syncfusion.Maui.ListView.ItemTappedEventArgs e)
{
    GridView.BindingContext = e.DataItem;
}
```

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
