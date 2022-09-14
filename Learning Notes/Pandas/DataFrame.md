`.squeeze("columns")` - create a [[Series]] from [[DataFrame]]

## Methods
`.info()` - general information about the [[DataFrame]] like size, data types and memory usage
`get_dtype_counts()` - summary count of data types
`.sort_values(by: str | list[str])` - sort values in [[DataFrame]] by column(s)
	- `inplace: bool` - default is False
`.dropna()` - remove rows/columns with N/A values
	- `how: {‘any’, ‘all’}` - drop when any value is N/A or all values are
	- `inplace: bool` - default is False
	- `subset: list[str]` - what columns to validate
`.fillna(value: any)` - replace all N/A occurrences with value
	- `inplace: bool` - default is False
`.drop_duplicates()` - remove the duplicates
	- `subset: list[str]` - columns which take a part in filtering
	- `keep: {‘first’, ‘last’, False}` - False value remove all the duplicates
`.rename()` - rename the index/column names
	- `columns: dict[str, str]`
	- `index: dict[str, str]` 
`.sample()`
	- `n: int` - the size of a sample
	- `axis: {0, 1} | {indexes, columns}` - what to sample
`.nsmallest()/.nlargest()`
	- `n: int` - the amount of items
	- `columns: str | list[str]` - columns to sort by
`.apply()`
`.applymap()`
`.copy` - create a copy of [[DataFrame]] object to not change the original instance.

### Index
`.set_index(str | list[str])`
	- `inplace: bool` - default is False
`.sort_index()` - sort rows in [[DataFrame]] by index
	- `ascending: bool` - order the [[Series]] by index
`.index.names` - list of indexes
`.get_level_values(int | str)` - get index values by position or name
`.index.set_names(str | list[str])` - rename the indexes
`.transpose()` - swap the indexes and columns
`.swaplevel()` - revert the index levels
`.pivot(columns: str | list[str])` - create a columns based on columns values
	- `index: str: list[str]` - create index if not exists
	- `values: str | list[str]` - values to show
`.stack()` - create index from column values
	- `level: int | str | list[int] | list[str]` - default -`1` (last level)
`.unstack()` - create columns from index values
	- `level: int | str | list[int] | list[str]` - default -`1` (last level)
`pivot_table(values, index, columns)` - that's complicated. It creates a indexes based on *`index`* argument, create columns based on *`columns`* values and perform a math operation from *`aggfunc`* on *`values`*

### Filtering
`.loc[]` - filter the [[DataFrame]] by index values.
`.iloc[]` - filter the [[DataFrame]] by index position.
`.where()` - do not remove the items from [[DataFrame]], but set all the False row values to N/A.
`.query(query: str)` - string query is way faster than a normal filtering.

### Groups
`.groupby(column: str: list[str])` - create collection of [[DataFrame]] grouped by argument settings
	- `sort`
	- `axis`
`.get_group(name: str)` - [[DataFrame]] object for particular group


### Join, Merge, Concatenate
`pd.concat(dataframe_objects: list[pd.DataFrame])` - build a new [[DataFrame]] object with [[DataFrame]]s build one on another
	- `ignore_index: bool` - create a new index, default is False
	- `keys: list[str]` - list of values for a multi index
`.join(other: pd.DataFrame, on: str)` - join one [[DataFrame]] to another based on a column
	- `how: {left, right, outer, inner}` - how to handle the operation
	- `suffixes: list[str]` - suffix indicator for columns with the same names
`.merge(right: pd.DataFrame, on; str)` - merge the [[DataFrame]] objects based on specific keys
	- `how: {left, right, outer, inner}` - how to handle the operation
	- `left_on: str` - left column to merge on
	- `right_on: str` - right column to merge on
	- `right_index: bool` - merge on right index
	- `left_index: bool` - merge on left index
	- `suffixes: list[str]` - suffix indicator for columns with the same names
	- `indicator: bool` - add the column with information from what [DataFrame] the data coming from

![[1 9eH1_7VbTZPZd9jBiGIyNA.png]]

## Attributes
`.index` - indexes as iterator object
`.values` - list of values
`.shape` - tuple with (rows count, column number)
`.dtypes` - series of column and data type values
`.columns` - list of columns
`.axes` - index and columns values at once