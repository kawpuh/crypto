# Zk-SNARK Study Guide
## Links
### Main
- https://vitalik.ca/general/2021/01/26/snarks.html
- https://vitalik.ca/general/2017/02/01/zk_snarks.html
### Vitalik Prereq
- https://blog.cloudflare.com/a-relatively-easy-to-understand-primer-on-elliptic-curve-cryptography/
- https://medium.com/@VitalikButerin/exploring-elliptic-curve-pairings-c73c1864e627
- https://vitalik.ca/general/2017/01/14/exploring_ecp.html
- https://medium.com/@VitalikButerin/quadratic-arithmetic-programs-from-zero-to-hero-f6d558cea649
- https://vitalik.ca/general/2016/12/10/qap.html

## Notes
### Elliptic Curve Cryptography
https://en.wikipedia.org/wiki/Elliptic-curve_cryptography#Theory

https://blog.cloudflare.com/a-relatively-easy-to-understand-primer-on-elliptic-curve-cryptography/

#### Setup
We define a curve

$$ y^{2}=x^{3}+ax+b $$

over a [finite field](https://en.wikipedia.org/wiki/Finite_field) (specifically one of integers mod $p$ where $p$ is prime) along with an addition operation as described [here](https://en.wikipedia.org/wiki/Elliptic_curve#The_group_law). This addition operation is used to create our point multiplication operation which is the one-way function used in ecc and described in greater detail [here](https://en.wikipedia.org/wiki/Elliptic_curve_point_multiplication).
#### Cryptographic Scheme
If we multiply an initial point by $n$ to get a final point, there is no more efficient way to recover $n$ than by repeated addition. This is known as the elliptic curve discrete logarithm problem (ECDLP).
