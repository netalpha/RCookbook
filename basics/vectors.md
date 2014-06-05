# Vectors

Vectors are used to store a set of elements of the same atomic data type, including:

- character,
- logical,
- numbers,
- complex numbers.

Each vector has a _mode_ and _length_.

	> v <- 4
	# a vector containing a single element
	>v <- c(4,7,23.5,76.2, 80)
	>length(v)
	[1] 5
	> mode(v)
	[1] "numeric"

## Missing value

All elements of a vector must belong to the same mode. A special value called _NA_ may be contained to represent a missing value.

	> u <- c(T, F, NA, TRUE)

## Empty vector

	> x <- vector()
	> x[3] <- 45 # NA, NA, 45
	> length(x) # 3
	> x[10] # NA
	> x[5] <- 4 # NA, NA, 45, NA, 4
