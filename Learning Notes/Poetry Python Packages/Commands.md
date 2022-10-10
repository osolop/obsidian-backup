#### Basics
`poetry init` - to create a configuration file for the project.
`poetry install` - to create virtual environment and generate *poetry.lock* file.
`poetry add ${module}` - insert additional dependency to configuration file.
	`--dev | -D` - flag to add the development dependency.
`poetry remove ${module}` - remove the dependency.
`poetry shell` - run the virtual environment. You can do it also by referencing to an *activate* like with regular *venv*.
`poetry show` - all installed dependencies.
	`--tree`  - 
	`--outdated` - dependencies that could be updated.
`poetry update` - update the dependencies.
	`${module}` - to update a specific package.

##### Additional package management (groups)
`poetry add ${module} --group ${dependency_group_name}` - add package to a particular group. *Same with remove*.
`poetry install` 
	`--with ${dependency_group_name(s)}` -  install the optional dependencies group(s). Comma separated values.
	`--without ${dependency_group_name(s)}` -  don't install the dependencies group(s). Comma separated values.
	`--only ${dependency_group_name}` - install specific group only. To install the default set use *main*.

##### The *lock* file
`poetry lock --no-update` - update the file after manually added dependencies to configuration file.