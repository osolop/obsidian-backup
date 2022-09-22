`.displot(values: [[Series]])`
	- `kde: bool` - sum of all normal dist. for each point.
`.jointplot(x: str, y: str, data: [[DataFrame]])` - distribution for two columns.
	- `kind: str` - for example *hex*|*reg*|*kde*.
`.pairplot()` - *joint plots* for all numerical values.
	- `hue: str` - categories column name to color the proportion of each value(bar/point).
	- `pallete: str` - coloring style.
`.rugplot(values: [[Series]])` - 
	- `kde: bool` - sum of all normal dist. for each point.