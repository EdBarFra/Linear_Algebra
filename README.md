This is a test to GitHub Desktop and to Atom Editor.

from sympy import *
init_printing(use_unicode=True)

Matrix([[1, -1], [3, 4], [0, 2]])     # list of lists (rows)

Matrix([1,2,3])                       # Column vector (list of elements)

M = Matrix([[1, 2, 3], [3, 2, 1]])
N = Matrix([0, 1, 1])
M*N                                   # Matrix multiplication

# Matrices are mutable.If you need an immutable version of Matrix, use ImmutableMatrix.

M.shape
M.row(0)
M.col(-1)
M.col_del(0)
M
M.row_del(1)
M
M = M.row_insert(1, Matrix([[0, 4]]))
M
M = M.col_insert(0, Matrix([1, -2]))
M

M = Matrix([[1, 3], [-2, 3]])
N = Matrix([[0, 3], [0, 7]])
M + N
M * N
3 * M
M**2
M**-1
(M**-1) * M
M * M**-1
# N**-1
M.T       # transpose

eye(3)
zeros(2,3)
ones(3,2)
diag(1, 2, 3)
diag(-1, ones(2, 2), Matrix([5, 7, 5]))

M = Matrix([[1, 0, 1], [2, -1, 3], [4, 3, 2]])
M
M.det()

M = Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]])
M
M.rref()               # the second is a tuple of indices of the pivot columns

M = Matrix([[1, 2, 3, 0, 0], [4, 10, 0, 0, 1]])
M
M.nullspace()

M = Matrix([[1, 1, 2], [2 ,1 , 3], [3 , 1, 4]])
M
M.columnspace()

M = Matrix([[3, -2,  4, -2], [5,  3, -3, -2], [5, -2,  2, -2], [5, -2, -3,  3]])
M
M.eigenvals()
M.eigenvects()

P, D = M.diagonalize()
P
D
P*D*P**-1 == M

lamda = symbols('lamda')
p = M.charpoly(lamda)
factor(p.as_expr())

##               Zero Testing  (a estudar)
