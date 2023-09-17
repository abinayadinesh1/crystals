convex set - a set that preserves linearity; any two points in the set can be connected by a line

hyperplane is just a plane in an n dimensional space. the plan has n-1 dimensions. 

parallel hyperplanes are many hyperplanes spaced evenly parall

hyperplane: have a point and a vector, find the plain passing through the point and orthogonal to the vector.
  

hyperplane = support vector machine. allows you to calculate if two points are part of different sets (take two random points (vectors) and take the dot product between your hyperplane and that n d vector)

  

  

convex cones - is just a subset of a linear space that is closed under positive scalar addition

polytopes - a shape with flat sides

bounded convex polytope - made up of convex sets

  

is every convex polygon a polytope? no, bc convex sets can be rounded

  

a hyperplane can be used to find the boundaries of a convex cone (convex hull) or polytope (outermost edges)! 

  

zonohedron - a special type of convex set

# 1.2 functionals and hyperplanes
L: V --> W
![[Screenshot 2023-09-15 at 6.59.02 PM.png]]
applying multiplication to or adding two vectors in a plane and then taking the transformation should be the same as taking the transformation and doing the same

linear operator: an operation that goes from one vector space to itself
linear functional/functional is when the vector space W you are going to is just the line

	a linear functional subdivides a vector space into a setof parallel hyperplanes
a linear transformation that goes from the space to a line divides the original space into a set of parallel hyperplanes. 

<mark style="background: #ABF7F7A6;">		but hyperplane is degined with one less dimension as the original and the linear functional take you to a 1d line :(</mark>. so how can it always be making a hyperplane?

linear functional from vector space to scalars
F (from vector space to the reals)
real number a
F^-1 (1) is the preimage of a. apply the inverse of the functional on the output and you get the input vector space. only possible if its onto and one to one. (or else you lose information)

kernal - part of the domain where the operator takes you to 0. aka nullspace. 
	**A vector v is in the kernel of a matrix A if and only if Av=0**
	KERNAL is the span of all those vectors v. 
		taking the kernel of a matrix returns the set of vectors that multiplied by the original image will return 0 

the hyperplanes foliate V: each vector in V belongs to one and only one hyperplane


the kernel of F is the set of vectors that cause the functional to be 0 ? is the set of all vectors in the domain of the functional (the vector space) that map to zero

when you take the functional of the vector space, it lands on 0 (recognizing the functional is a 1d line that passes through the origin)


convex sets, convex combinations, convex hulls
the set Q is a set of generators for the hull(Q). you can sometimes add points to Q and remove points from Q without changing the hull(Q), so it will always generate the same hull space. 

a convex cone is made by all the rays starting at the origin and going forward with some angle for infinite distance. 

## zonohedra
minkownski sum
they occur when simple colors, like the primaries of a display, come to produce new colors

there is a physical restriction that the coefficients of the linear combinations of the primaries cant exceed one
the set of all possible color combinations makes a zonohedra

minkowski sum of two subsets of a vector space is another subset, with all the sums of pairs of vectors. 

minowski sum of a set of vectors is a zonohedron


zonohedra is when all the vectors in the Minkowski sum are 3D!
-tope is a shape in arbitrary dimensions