`pd.read_csv(fname: str | Path)` - read the file as [[DataFrame]]
	- `usecols: list[str]` - what columns to read from a file
	- `index_col: str | list[str]` - column to be index values
	- `parse_dates: str | list[str]` - convert column(s) values to date object
`melt()` - 

## Good practices
Remember to keep a proper data types of the columns. You can check the column data types and memory usage by using the `.info()` method on the [[DataFrame]]. Keep in mind the `category` data type and always cast the values from columns with the small amount of unique values to this kind of type.
Always keep the date values as a date objects.
Create a masks while filtering. It will make your code more readable and clear. You can join the masks as a logical operations with the `&` and `|` symbols.
Remember to copy the [[DataFrame]] in case of further analysis of original data after transformation.