`.barplot(x: str, y: str, data: [[DataFrame]])`
	- `estimator: function`  - function to estimate the category.
`.countplot(x: str, data: [[DataFrame]])` - count the number of occurrences.
`.boxplot(x: str, y: str, data: [[DataFrame]])` - coincidence between variables.
	- `hue: str`  - split the data by the other categorical column.
`.violinplot(x: str, y: str, data: [[DataFrame]])`- extended box plot.
	- `hue: str`  - split the data by the other categorical column.
	- `split: bool`
`.stripplot(x: str, y: str, data: [[DataFrame]])` - scatter plot for data.
	 - `jitter: bool` - add noise to see the points clearly
	 - `hue: str` - split the data by the other categorical column.
	 - `split: bool`
`.swarmplot(x: str, y: str, data: [[DataFrame]])` - combination of strip and violin plots.
`.factorplot(x: str, y: str, data: [[DataFrame]], kind: str)` - generator for plots.
	- `kind` - what kind of plot to plot.