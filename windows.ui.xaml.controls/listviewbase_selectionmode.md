---
-api-id: P:Windows.UI.Xaml.Controls.ListViewBase.SelectionMode
-api-type: winrt property
---

<!-- Property syntax
public Windows.UI.Xaml.Controls.ListViewSelectionMode SelectionMode { get;  set; }
-->

# Windows.UI.Xaml.Controls.ListViewBase.SelectionMode

## -description
Gets or sets the selection behavior for a [ListViewBase](listviewbase.md) instance.

## -xaml-syntax
```xaml
<listViewBase SelectionMode="listViewSelectionModeMemberName" />
```


## -xaml-values
<dl><dt>listViewSelectionModeMemberName</dt><dd>listViewSelectionModeMemberNameA named constant of the ListViewSelectionMode enumeration; for example, Extended.</dd>
</dl>
## -property-value
One of the [ListViewSelectionMode](listviewselectionmode.md) enumeration values. The default is **Single** selection.

## -remarks
By default, a user can select a single item in a view. You can set the [SelectionMode](listviewbase_selectionmode.md) property to a [ListViewSelectionMode](listviewselectionmode.md) enumeration value to enable multi-selection or to disable selection. Here are the selection mode values.<table>
   <tr><td>[None](listviewselectionmode.md)</td><td>Item selection is disabled.</td></tr>
   <tr><td>[Single](listviewselectionmode.md)</td><td>With no modifier keys:

<ul><li>A user can select a single item using the space bar, mouse click, or touch tap.</li><li>A user can deselect an item using a downward swipe gesture.</li></ul>While pressing Ctrl:

<ul><li>A user can deselect the item by using the space bar, mouse click, or touch tap.</li><li>Using the arrow keys, a user can move focus independently of selection.</li></ul></td></tr>
   <tr><td>[Multiple](listviewselectionmode.md)</td><td>With no modifier keys:

<ul><li>A user can select multiple items using the space bar, mouse click, or touch tap to toggle selection on the focused item.</li><li>Using the arrow keys, a user can move focus independently of selection.</li></ul></td></tr>
   <tr><td>[Extended](listviewselectionmode.md)</td><td>With no modifier keys:

<ul><li>The behavior is the same as [Single](listviewselectionmode.md) selection.</li></ul>While pressing Ctrl:

<ul><li>A user can select multiple items using the space bar, mouse click, or touch tap to toggle selection on the focused item.</li><li>Using the arrow keys, a user can move focus independently of selection.</li></ul>While pressing Shift:

<ul><li>A user can select multiple contiguous items by clicking or tapping the first item in the selection and then the last item in the selection.</li><li>Using the arrow keys, a user can create a contiguous selection starting with the item selected when Shift is pressed.</li></ul></td></tr>
</table>

> [!NOTE]
> Touch interactions are enabled only when [IsSwipeEnabled](listviewbase_isswipeenabled.md) is **true**.

If [SelectionMode](listviewbase_selectionmode.md) is [None](listviewselectionmode.md), and [CanDragItems](listviewbase_candragitems.md) and [CanReorderItems](listviewbase_canreorderitems.md) are **false**, you should set [IsSwipeEnabled](listviewbase_isswipeenabled.md) to **false** to improve app performance. See the [IsSwipeEnabled](listviewbase_isswipeenabled.md) property for more info.

When [SelectionMode](listviewbase_selectionmode.md) is **Single**, use the [Selector.SelectedItem](../windows.ui.xaml.controls.primitives/selector_selecteditem.md) property to get the item that's selected. When [SelectionMode](listviewbase_selectionmode.md) is **Multiple** or **Extended**, use the [SelectedItems](listviewbase_selecteditems.md) property to get the items that are selected.

When item selection is disabled, you can make items respond to a user click like a button instead of being selected. To do this, set [SelectionMode](listviewbase_selectionmode.md) to [None](listviewselectionmode.md), the [IsItemClickEnabled](listviewbase_isitemclickenabled.md) property to **true**, and handle the [ItemClick](listviewbase_itemclick.md) event.

For more info and examples, see [How to change the interaction mode](http://msdn.microsoft.com/library/7591268b-3835-4a48-a4ba-b2e6c9db73e6).

## -examples

## -see-also
[SelectedItems](listviewbase_selecteditems.md), [Selector.SelectedItem](../windows.ui.xaml.controls.primitives/selector_selecteditem.md), [Selector.SelectedIndex](../windows.ui.xaml.controls.primitives/selector_selectedindex.md), [Selector.SelectionChanged](../windows.ui.xaml.controls.primitives/selector_selectionchanged.md), [How to change the interaction mode](http://msdn.microsoft.com/library/7591268b-3835-4a48-a4ba-b2e6c9db73e6)