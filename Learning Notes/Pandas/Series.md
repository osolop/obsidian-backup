`pd.Series(data: list[any])`
	- `index: list[any]` - index values (must be the same length as data value)

## Methods
`.to_datetime()` - convert the values to a date object
	- `errors: str`  - what to do with the values we can not convert

### Values
`.sort_values()`
	- `ascending: bool` - order the [[Series]] by values
`.value_counts()` - count value occurrences
`.dropna()` - remove rows/columns with N/A values
	- `how: {‘any’, ‘all’}` - drop when any value is N/A or all values are
	- `inplace: bool` - default is False
`.fillna(value: any)` - replace all N/A occurrences with value
	- `inplace: bool` - default is False
`.astype(type: type)` - convert values of series to  specific type
`nunique()` - amount of unique values in [[Series]]
`.map(mapping: dict[str, str])` - replace the values with something else.

### Index
`.sort_index()`
	- `ascending: bool` - order the [[Series]] by index
`.set_index(index_col: str | list[str])` - create an index based on a column(s)
`.reset_index()` - add default number index to [[Series]]

### Filtering
`.is_null()`
`.not_null()`
`.between(min: any, max: any)`
`.duplicated()`
	- `keep: {‘first’, ‘last’, False}` - False value marks all the duplicates to remove

### Math operations
`.count()` - amount of values in [[Series]]
`.sum()` - sum values in [[Series]]
`.product()` - multiply values in [[Series]]
`.mean()` - mean for the values in [[Series]]
`.mul()` - multiply by a value
`.div()` - divide by a value
`.std()` - standard deviation
`.min()`
`.max()`
`.median()`
`.mode()`
`describe()` - most of the above at once

## Attributes
`.size` - the length.
`.is_unique` - validate if all the values are unique
`.values` - numpy array of values
`.index` - generator for index values
`.dtype` - type of series
`.shape` - tuple with only first value as size
`.ndim` - number of dimensions (1)
