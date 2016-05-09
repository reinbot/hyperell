## The functional equation for $L$-functions of hyperelliptic curves
### Data of the examples for our paper (arXiv:1504.00508), to appear

#### Structure of the file set

The folder  [ /main_examples](./main_examples) contains the 7 curves we discussed in our paper. 

For each curve we provide 

1. an uncompressed text file readable by any computer or browser
 
2. a compressed .sobj file, to be opened in Sage

The files are named after the prime decomposition of the conductor $N$:
```
c<bad_prime_power>_<...>_<bad_prime_power>.sage
```
e.g.
```
c9_343_31_53.sage
```
where 
```
N = 3^2 * 7^4 * 31 * 53.
```

The folder [ /further_examples](./further_examples) contains another 14 curves with further interesting examples not discussed in the paper.


#### How to use the files

Each of the files has the following structure.

The file is a Sage dictionary, with the following keys:
```
0: genus, 1: g(x), 2: h(x), 3: conductor, 4: bad primes, 
5: bad factors, 6: bound M, 7: root number or sign, 8: L-series up to M
```



######Suggested use:
```python
sage: c=load('c7_227_1227_1609.sobj')
sage: # OR
sage: c=load('c7_227_1227_1609.sage')
sage: c[0]
5
sage: c[1]
x^11 + 3*x^4 + 2*x^3 - 3*x^2 - 2*x
sage: c[2]
-3*x^3 + x^2 + 3*x + 1
sage: c[3]
3264907177
sage: c[3].factor()
7 * 227 * 1277 * 1609
sage: c[4]
[7, 227, 1227, 1609]
sage: c[5]
[-2401*x^9 + 2401*x^8 + 588*x^7 - 588*x^6 - 134*x^5 + 134*x^4 + 12*x^3 - 12*x^2 - x + 1,
 200*x^3 + 213*x^2 + 14*x + 1,
 -35*x^2 - 34*x + 1,
 -26*x^2 - 25*x + 1]
sage: c[5][3]
-26*x^2 - 25*x + 1
sage: c[6]
1112661
sage: c[7]
1
sage: c[8][0:10]
[1, -1, 0, 1, 2, 0, 1, 1, -2, -2]
```
