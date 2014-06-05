# Vectorization

Vectorization leads a function to produce a vector of the same length, with each element resulting from applying the function to the respective element of the original vector. Recycling furl by repeating the shorter vector until it fills in the size of the larger vector will be applied if two vectors have not the same length.

	> v1 <- c(4, 6, 8, 12)
	> v2 <- c(10, 2)
	> v1 + v2 # 14 8 18 26
