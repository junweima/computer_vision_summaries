# [MRF](https://en.wikipedia.org/wiki/Markov_random_field)

# Boltzman distribution (aka Gibbs distribution)
* The only distribution that satisfies the Markov blanket property

# MRF energy minimization
* The common model gives the energy as unary term + pairwise term
* turns out that minimization of that engery is equivalent to solving a max flow/min cut problem

# cases
* binary MRF
	* can always be solved in polynomial time using mincut
* multi-label MRF
	* can be solved in polynomial time if submularity is satisfied

# Tricks
* use local information to turn multi-lavel to binary MRF
* alpha-beta swap
	* basically use current region and rest of the picture as binary MRF
* alpha expansion (most effective)
	* compare certain region and other region for all combinations


