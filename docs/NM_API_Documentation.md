# Non-Linear Solver



```c
# include  "myNM.h"
```



## newtonRaphson()

Finds the solution of a non-linear equation with the given range.‌

```C
 void newtonraphson()
```

**Parameters**

- vector type m



------





# Linear Solver



## gaussElim()

solves for vector **x** from  Ax=b,  a linear system problem  

```c
void	gaussElim(Matrix _A, Matrix _B, Matrix* _U, Matrix* _B_out);
```

#### **Parameters**

- **A**:  Matrix **A** in structure Matrix form.  Should be (nxn) square.

- **B**:  vector  **b** in structure Matrix form.  Should be (nx1) 

  

  

## solveLinear()

solves for vector **x** from  Ax=b,  a linear system problem  

```c
extern Matrix solveLinear(Matrix _A, Matrix _b, char* _method)
```

#### **Parameters**

- **A**:  Matrix **A** in structure Matrix form.  Should be (nxn) square.

- **b**:  vector  **b** in structure Matrix form.  Should be (nx1) 

- **method:  character type,** 

  - **'lu' :** LU decomposition
  - **'gauss':** Gauss elimination

  

#### Examples

exit: Ctrl+↩

```C
double A_array[] = { 1, 3, -2, 4,		2, -3, 3, -1,		-1, 7, -4, 2,		-1, 7, -4, 2 };
double b_array[] = { -11,		6,		-9,		15 };

Matrix matA = arr2Mat(A_array, M, N);
Matrix vecb = arr2Mat(b_array, M, 1);

Matrix x_lu = solveLinear(matA, vecb, "LU");
Matrix invA_gj = inv(matA, "gj");
Matrix invA_lu = inv(matA, "LU");
```



------

# Vector/Matrix Operation

### Matrix Addition 

```c
extern	Matrix	addMat(Matrix _A, Matrix _B);
```

### Matrix Subtraction 

### Matrix Multiplication

### Dot Product

### Vector Norm

