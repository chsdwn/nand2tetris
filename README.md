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

### De Morgan Laws

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
