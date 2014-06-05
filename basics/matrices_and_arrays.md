# Matrices and Arrays

Arrays store data elements in several dimensions; matrices are a specical case of arrays with two single dimensions. Arrays and matrices are nothing more than vectors with a particular attribute that is the _dimension_.

	> m <- c(45, 23, 66 , 77, 33 ,44, 56, 12 , 78, 23)
	> dim(m) < c(2, 5)
	> m
	     [,1]  [,2]  [,3]  [,4]  [,5]
	[1,]   45   66    33    56     78
	[2,]   23   77    44    12     23
	> m <- matrix(c(45, 23, 66 , 77, 33 ,44, 56, 12 , 78, 23), 2, 5)
	# fill the column first
	> m < - matrix(c(45, 23, 66 , 77, 33 ,44, 56, 12 , 78, 23), 2, 5, byrow = T)
		     [,1]  [,2]  [,3]  [,4]  [,5]
	[1,]   45   23    66    77     33
	[2,]   44   56    12    78     23

### Subset

	> m[2, 3]
	[1] 12
	> m[-2, 1]
	[1] 45
	> m[1, -c(3, 5)]
	[1] 45 23 77
	> m[1,]
	[1] 45 23 66 77 33
	> m[, 4]
	[1] 77 78
	> m[1, , drop=F]
		     [,1]  [,2]  [,3]  [,4]  [,5]
	[1,]   45   23    66    77     33

### Joining two vector or matrices

	> m <- matrix(c(45, 23, 66 , 77, 33 ,44, 56, 12 , 78, 23), 2, 5)
	> m
	     [,1]  [,2]  [,3]  [,4]  [,5]
	[1,]   45   66    33    56     78
	[2,]   23   77    44    12     23
	> cbind(c(4, 76), m[, 4])  # and rbind
	      [,1]  [,2]
	[1,]   4     56
	[2,]   76    12

### Naming the columns and rows

	> m < - matrix(c(45, 23, 66 , 77, 33 ,44, 56, 12 , 78, 23), 2, 5, byrow = T)
		     [,1]  [,2]  [,3]  [,4]  [,5]
	[1,]   45   23    66    77     33
	[2,]   44   56    12    78     23
	> colnames(m) <- c("1qrt", "2qrt", "3qrt", "4qrt", "5qrt")
	> rownames(m) <- c("store1", "store2")

### Arrays

	> a <- array(1:24, dim=c(4,3,2))
	a
	, , 1
	     [,1]  [,2]  [,3]
	[1,]  1      5     9
	[2,]  2      6     10
	[3,]  3      7     11
	[4,]  4      8     12
	, , 2
	     [,1]  [,2]  [,3]
	[1,]  13     17    21
	[2,]  14     18    22
	[3,]  15     19    23
	[4,]  16     20    24
