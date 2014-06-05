# Sequences

### Generating Sequences

	> x <- 1:1000
	> 5:0
	[1] 5 4 3 2 1

### Real numbers

	> seq(-4, 1, 0.5)
	[1] -4.0 -3.5 -3.0 -2.5 -2 -1.5 -1 -0.5 0.0 0.5 1.0
	> seq(from=1, to=5, length=4)
	[1] 1.000000 2.333333 3.666667 5.0000000
	> seq(length=10, to=-2, by=0.2)
	[1] -2.0 -1.8 -1.6 -1.4 -1.2 -1.0 -0.8 -0.6 -0.4 -0.2

### Repeat with patterns

	> rep(5, 10)
	[1] 5 5 5 5 5 5 5 5 5 5
	> rep(1:2, 3)
	[1] 1 2 1 2 1 2
	> rep(1:2, each=3)
	[1] 1 1 1 2 2 2

### Repeat involving factors

The function gl() can be used to generate sequences involving factors. The syntax of the funtion is gl(k,n), where k is the number of levels of the factor, and n is the number of repetitions of each level.

	> gl(3, 5)
	[1] 1 1 1 1 1 2 2 2 2 2 3 3 3 3 3
	Levels: 1 2 3
	> gl(2, 5, labels=c("female", "male"))
	[1] female female female female female male male male male male
	Levels: female male

### Random sequences

The functions have the generic structure _rfunc(n, par1, par2, ..._, where _func_ is the name of the probability distribution, _n_ is the number of data to generate, and _par1, par2,..._ are the values of some parameters of the density function that may be required.

	> rnorm(10)
	# Ten random generated numbers from a normal distribution with zero mean and unit standard deviation.
	> rnorm(4, mean=10, sd=3)
