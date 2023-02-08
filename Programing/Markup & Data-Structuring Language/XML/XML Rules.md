### Must have a ROOT Parent

``` XML
<name>
	<child>...</child>
</name>
```

### Must have PROLOUGE

``` XML
<?xml version="1.0" encoding="UTF-8"?>
```

### Must have CLOSING Tag

``` XML
<food></food>

<good/>
```


### References

\> = \&gt;
< = \&lt;
& = &amp;
' = &apos;
" = &quot;

### Attributes VS Elements

Data is stored: ELEMENTS

Data about data(metadata): ATTRIBUTES


### NameSpaces

``` XML
<root>
	<h:table xmlns:h="html">
		<h:tr>
			<h:td></h:td>
		</h:tr>
	</h:table>

	<f:table>
</root>
```