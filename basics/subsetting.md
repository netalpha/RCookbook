# Subsetting

	> x <- c(0, -3, 4, -1, 45, 90, -5)
	> x>0
	[1] F F T F T T F
	> x[x>0]
	[1] 4 45 90
	> x[x <= -2 | x > 5]
	[1] -3 45 90 -5
	> x[x > 40 & x < 100]
	[1] 45 90
	> x[c(4, 6)]
	[1] -1 90
	> x[1:3]
	[1] 0 -3 4

### Exclusion

	> x[-1]
	[1] -3 4 -1 45 90 -5
	> x[-(1:3)]
	[1] -1 45 90 -5

### Named vectors

	> pH <- c(4.5, 7)
	> names(pH) < c("area", "mud")
	> pH
	area mud
	4.5 7
	> pH <- c(area = 4.5, mud = 7)
	> pH["mud"]
	mud
	7

### All zeros

	> x[] <- 0

