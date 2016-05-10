## The functional equation for $L$-functions of hyperelliptic curves
### Data of the examples for our paper (arXiv:1504.00508), to appear

#### Structure of the file set

The folder  [ /main_examples](./main_examples) contains the 8 curves we discussed in our paper. 

For each curve we provide 

1. an uncompressed .sage text file readable by any computer or browser
 
2. a compressed .sobj file, to be opened in Sage

The files are named after the prime decomposition of the conductor $N$:
```
c<bad_prime_power>_<...>_<bad_prime_power>.sage
```
e.g.
```
c4_27_121_37.sage
```
where 
```
N = 2^2 * 3^3 * 11^2 * 37.
```

The folder [ /further_examples](./further_examples) contains another 14 curves with further interesting examples not discussed in the paper.


#### How to use the files

Each of the files has the following structure.

The file is a Sage dictionary with the following keys:
```
0: genus, 1: g(x), 2: h(x), 3: conductor, 4: bad primes, 
5: bad factors, 6: bound M, 7: root number or sign, 8: L-series up to M
```



######Suggested use:
```python
sage: c = load('c4_27_121_37.sobj')
sage: c[0]
3
sage: c[1]
x^7 + x^6 + 2*x^5 + 2*x^4 + 2*x^3 - 1
sage: c[2]
-x^3 + x^2 + x + 2
sage: c[3]         
483516
sage: c[3].factor()
2^2 * 3^3 * 11^2 * 37
sage: c[4]
[2, 3, 11, 37]
sage: c[5]
[-2*x^4 + x^3 + x^2 - x + 1,
 -x^3 - x^2 + x + 1,
 11*x^4 + 18*x^3 + 4*x^2 - 2*x + 1,
 -1369*x^5 + 1221*x^4 + 134*x^3 + 10*x^2 + 3*x + 1]
sage: c[5][1]
-x^3 - x^2 + x + 1
sage: c[6]
15133
sage: c[7]
1
sage: c[8][0:40]
[1,  1, -1,  0,  4, -1, -4, -2,  2,  4,
 2,  0, -8, -4, -4, -1,  6,  2,  6,  0,
 4,  2, -2,  2,  5, -8, -2,  0,  6, -4,
 0,  3, -2,  6,-16,  0, -3,  6,  8, -8]
```
If you are familiar with the construction of $L$-series, note the second, third, 11th, and 37th term. They are the negatives of the linear terms in the corresponding bad factors.


