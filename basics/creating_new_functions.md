# Creating New Functions

To check the existence of a function, it is sufficient to type its name at the prompt:

	> se
	Error: Object 'se' not found
	> se <- function(x) {
	+ v <- var(x)
	+ n <- length(x)
	+ return(sqrt(v/n))
	+ }
