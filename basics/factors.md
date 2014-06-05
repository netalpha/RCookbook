# Factors

Factors provide an easy and compact form of handling categorical (nominal) data. Factors have _levels_ that are the possible values they can take.

	> g <- c("f", "m", "f", "m")
	> g
	[1] "f" "m" "f" "m"
	> g <- factor(g)
	> g
	[1] f m f m
	Levels: f m

	> other.g <- factor(c("m", "m", "m"), levels=c("f", "m"))
	> other.g
	[1] m m m
	Levels: f m

### Table

One of the many things to do with factor is to count the occurance of each possible values.

	> table(g)
	g
	f m
	2 2
	> table(other.g)
	other.g
	f m
	0 3

### Cross-tabulate

	> g <- factor(c("f", "m", "f", "m"))
	> a <- factor(c('adult', 'juvenile', 'adult', 'juvenile'))
	> table(a, g)
			g
	a         f m
	adult    2 0
	juvenile 0 2

### Marginal

	> t <- table(a, g)
	> margin.table(t, 1) # "1" represents the first dimension
	a
	  adult juvenile
	    2     2
	> margin.table(t, 2)
	g
	f m
	2 2

### Relative frequencies

	> prop.table(t, 1)
	        g
	a          f    m
	 adult    1     0
	 juvenile 0     1
	> prop.table(t, 2)
	a          f    m
	 adult    1     0
	 juvenile 0     1
	> prop.table(t)
	a            f    m
	 adult   0.5   0
	 juvenile 0   0.5
