# Elliptic-curve-point-multiplication
Elliptic curve scalar multiplication is the operation of successively adding a point along an elliptic curve to itself repeatedly.
It is used in elliptic curve cryptography (ECC) as a means of producing a one-way function. 
The literature presents this operation as scalar multiplication, as written in Hessian form of an elliptic curve.
A widespread name for this operation is also elliptic curve point multiplication, but this can convey the wrong impression of being
a multiplication between two points.

Basics
Given a curve, E, defined along some equation in a finite field (such as E: y2 = x3 + ax + b), point multiplication is defined as the repeated addition of a point along that curve. Denote as nP = P + P + P + … + P for some scalar (integer) n and a point P = (x, y) that lies on the curve, E. This type of curve is known as a Weierstrass curve.

The security of modern ECC depends on the intractability of determining n from Q = nP given known values of Q and P if n is large (known as the elliptic curve discrete logarithm problem by analogy to other cryptographic systems). This is because the addition of two points on an elliptic curve (or the addition of one point to itself) yields a third point on the elliptic curve whose location has no immediately obvious relationship to the locations of the first two, and repeating this many times over yields a point nP that may be essentially anywhere. Intuitively, this is not dissimilar to the fact that if you had a point P on a circle, adding 42.57 degrees to its angle may still be a point "not too far" from P, but adding 1000 or 1001 times 42.57 degrees will yield a point that may be anywhere on the circle. Reverting this process, i.e., given Q=nP and P and determining n can therefore only be done by trying out all possible n—an effort that is computationally intractable if n is large.

