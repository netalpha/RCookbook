# Lists

Lists consist of an ordered collection of other objects known as their components. The components do not need to be of the same type, mode and length. The components of a list are always numbered and may also have a name attached to them.

	> my.lst <- list(stud.id = 34455, stud.name="John", stud.marks=c(14.3, 12, 15, 19))
	> my.lst
	$stud.id
	[1] 34455
	$stud.name
	[1] "John"
	$stud.marks
	[1] 14.3 12.0 15.0 19.0

### Subset

	> my.lst[[1]]
	[1] 34455
	> mode(my.lst[[1]])
	[1] "numeric"
	> my.lst[1]
	$stud.id
	[1] 34455
	> mode(my.lst[1])
	[1] "list"
	> my.lst$stud.id
	[1] 34455
	> names(my.lst)
	[1] "stud.id" "stud.name" "stud.marks"

### Extension

	> my.lst$parents.names <- c("Ana", "Mike")
	> my.lst
	$stud.id
	[1] 34455
	$stud.name
	[1] "John"
	$stud.marks
	[1] 14.3 12.0 15.0 19.0
	$parent.names
	[1] "Ana" "Mike"

### The number of components

	> length(my.lst)
	[1] 4

### Removal

	> my.lst <- my.lst[-5]

### Concatenate

	> other <- list(age=19, sex="male")
	> lst <- c(my.lst, other)
	> lst
	$stud.id
	[1] 34455
	$stud.name
	[1] "John"
	$stud.marks
	[1] 14.3 12.0 15.0 19.0
	$parent.names
	[1] "Ana" "Mike"
	$age
	[1] 19
	$sex
	[1] "male"

### unlist

	> unlist(my.lst)
	stud.id     stud.name    stud.marks1  stud.marks2  stud.marks3
	"34455"        "John"       "14.3"     "12"          "15"
	stud.marks4  parents.names1  parents.names2
	"19"            "Ana"            "Mike"
