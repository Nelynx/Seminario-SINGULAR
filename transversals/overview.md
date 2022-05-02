**Note:**
See _Transversal: A Maple Package For Singularity Theory_ for details.
Since there is an upper bound for the determinacy degree of a G-finite map in terms of its G-codimension, there could be an optional argument to set the maximum degree.

## Input
`f\colon F^n \to F^p` (map)
`G` (group)

## Step 1
For the given jet `f`, jet-space degree `k` and tangent space `G`, calculate `Gf` in `J^k(n,p)`.
The space `J^k(n,p)` is identified with `F[x_1,\dots,x_n]^p/(x_1,\dots,x_n)^{k+1}`, the space of `p`-tuples of polynomials in `n` indeterminates over `F` truncated to degree `k`.

### The space Lf
_(`_j` denotes fixing terms of degree `\leq j`)_

- `G=R_j`: `\mf{m}^{j+1} tf(\theta_n)`
- `G=L_j`: `\mf{m}^{j+1} \omega f(\theta_p)`
- `G=C_j`: `\mf{m}_n^{j+1} f^*\mf{m}_p \theta_n^p`

Computations are done manually: since each one of these modules is given in the form `\mf{m}^{j+1} T`, we fix an upper bound `k` for the degree and compute elements of `\mf{m}^{l}T` until we "run out" of elements of degree `\leq k`.

## Step 2
Since `Gf` is a module over `J^k(n,p)`, it can be identified with a matrix with entries in `J^k(n,p)`
Reduce `Gf` to echelon form using Gaussian elimination.
The resulting matrix gives a canonical basis for `Gf`.

### Computing the echelon form on Singular
Gaussian elimination can be computed via `groebner` (on global ordering) or `std` (local ordering).
The matrix must be coded as an ideal or a module.
While these commands admit matrices, results differ, and _A Singular Introduction to Commutative Algebra_ does this casting.
However, the matrix is sparse, and alternative reduction methods are suggested, so computational costs should be measured down the line.
