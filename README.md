[this is not ready yet]

# The functional equation for $L$-functions of hyperelliptic curves
## Data of the examples for our paper (arXiv:1504.00508), to appear

#### Structure of the file set

The folder 'main examples' contains the 7 curves we discussed in our paper. 

For each curve we provide 
1. an uncompressed text file readable by any computer or browser
2. a compressed .sobj file, to be opened in Sage

The files are named as follows.

c<genus>_<badprime>_<...>_<badprime>.sage



#### How to use the files

Each of the files has the following structure.

The file is a Sage dictionary, with the following keys:
0: genus, 1: g(x), 2: h(x), 3: conductor, 4: bad primes, 5:bad factors, 6: bound M, 7: root number or sign, 8: L-series up to M




######suggested use:

sage: c=load('c7_227_1227_1609.sobj')
OR
sage: c=load('c7_227_1227_1609.sage')

sage: c[0]
5
sage: c[2]
-3*x^3 + x^2 + 3*x + 1 
