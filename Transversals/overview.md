**Note:**
See _Transversal: A Maple Package For Singularity Theory_ for details.
Since there is an upper bound for the determinacy degree of a G-finite map in terms of its G-codimension, there could be an optional argument to set the maximum degree.

## Input
`f\colon F^n \to F^p` (map)
`L` (group)

## Step 1
For the given jet `f`, jet-space degree `k` and tangent space `L`, calculate `Lf` in `J^k(n,p)`.
Procedures for constructing `Lf` depending on `L` will be given in future commits.

The space `J^k(n,p)` is identified with `F[x_1,\dots,x_n]^p/(x_1,\dots,x_n)^{k+1}`, the space of `p`-tuples of polynomials in `n` indeterminates over `F` truncated to degree `k`.

## Step 2
Since `Lf` is a module over `J^k(n,p)`, it can be identified with a matrix with entries in `J^k(n,p)`
Reduce `Lf` to echelon form using Gaussian elimination.
The resulting matrix gives a canonical basis for `Lf`.

### Computing the echelon form on Singular
Gaussian elimination can be computed via `groebner` (on global ordering) or `std` (local ordering).
The matrix must be coded as an ideal or a module.
While these commands admit matrices, results differ, and _A Singular Introduction to Commutative Algebra_ does this casting.
However, the matrix is sparse, and alternative reduction methods are suggested, so computational costs should be measured down the line.

## Step 3
A basis `C` for the complement space is computed via adding monomials.

## Step 4
