---
-api-id: P:Windows.UI.Xaml.Controls.ItemsControl.ItemsSource
-api-type: winrt property
---

<!-- Property syntax
public object ItemsSource { get;  set; }
-->

# Windows.UI.Xaml.Controls.ItemsControl.ItemsSource

## -description
Gets or sets an object source used to generate the content of the [ItemsControl](itemscontrol.md).

## -xaml-syntax
```xaml
<itemsControl ItemsSource="bindingDeclaration"/>
-or-
<itemsControl ItemsSource="resourceReferenceToSource"/>
```


## -xaml-values
<dl><dt>bindingDeclaration</dt><dd>bindingDeclarationA Binding declaration using a {Binding ....} markup extension. For more information, see {Binding} markup extension.</dd>
<dt>resourceReferenceToSource</dt><dd>resourceReferenceToSourceA resource reference to an existing iterable/enumerable items source from a resources collection. The resource reference must specify the desired items source by key.</dd>
</dl>
## -property-value
The object that is used to generate the content of the [ItemsControl](itemscontrol.md). The default is null.

## -remarks
The ItemsSource property value must implement either the IIterable&lt;IInspectable&gt; or IBindableIterable interface.  For example, in a C# application, it must implement IEnumerable&lt;Object&gt; or IEnumerable.  

The ItemsControl can provide better performance if the ItemsSource property value also implements a random-access list interface:  IVector&lt;IInspectable&gt;, IVectorView&lt;IInspectable&gt;, IBindableVector, or IBindableVectorView.  In C#, this means IList&lt;Object&gt;, IReadOnlyCollection&lt;Object&gt;, or IList.

The ItemsControl can respond to changes if the ItemsSource property value also implements a change notification interface:  IObservableVector&lt;IInspectable&gt; or INotifyCollectionChanged.

## -examples

## -see-also
