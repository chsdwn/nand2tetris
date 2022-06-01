# [From Nand To Tetris](https://www.nand2tetris.org/)

# CAUTION: Arrays is indexed from right to left: `a=01, a[0]=1, b[1]=0`

## Boolean Identities

### Commutative Laws

- (x AND y) = (y AND x)
- (x OR y) = (y OR x)

### Associative Laws

- (x AND (y AND z)) = ((x AND y) AND z)
- (x OR (y OR z)) = ((x OR y) OR z)

### Distributive Laws

- (x AND (y OR z)) = (x AND y) OR (x AND z)
- (x OR (y AND z)) = (x OR y) AND (x OR z)

### De Morgan Laws

- NOT(x AND y) = NOT(x) OR NOT(y)
- NOT(x OR y) = NOT(x) AND NOT(y)

## Boolean Algebra

- NOT(NOT(x) AND NOT(x OR y)) = ?

1. NOT(NOT(x) AND (NOT(x) AND NOT(y)))
1. NOT(NOT(x) AND NOT(x)) AND NOT(y))
1. NOT(NOT(x) AND NOT(y))
1. NOT(NOT(x)) OR NOT(NOT(y))
1. x OR y

## Boolean Expression

| x   | y   | out |                                  |
| --- | --- | --- | -------------------------------- |
| 0   | 0   | 0   |
| 0   | 1   | 1   | NOT(x) AND y                     |
| 1   | 0   | 1   | x AND NOT(y)                     |
| 1   | 1   | 0   |
|     |     |     | (NOT(x) AND y) OR (x AND NOT(y)) |

## Boolean Arithmetic

### 2's Complement: 2^n-x

| Digit | Num     |
| ----- | ------- |
| 0000  | 0       |
| 0001  | 1       |
| 0010  | 2       |
| 0011  | 3       |
| 0100  | 4       |
| 0101  | 5       |
| 0110  | 6       |
| 0111  | 7       |
| 1000  | -8 (8)  |
| 1001  | -7 (9)  |
| 1010  | -6 (10) |
| 1011  | -5 (11) |
| 1100  | -4 (12) |
| 1101  | -3 (13) |
| 1110  | -2 (14) |
| 1111  | -1 (15) |

#### -2 + -3 = ?

- 14 + 13 = 11
- 1110 + 1101 = [1]1011(-5)

### Computing -x

- in=x, out=-x
- 2^n-x = 1 + (2^n-1) - x

#### in=4, out=-4 ?

- 1111 - 0100 = 1011
- 1011 + 1 = 1100(-4)
