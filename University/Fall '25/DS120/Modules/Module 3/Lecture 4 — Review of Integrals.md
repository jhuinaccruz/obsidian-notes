__Differential Calculus__: The study of change of quantities, where the differential measures the rate of change

__Integration__: Two kinds
- __Indefinite__ (with respect to x): The reverse process of differentiation, resulting in a function that when differentiated gives `f(x)`
 $$
\int f(x)dx
$$
- __Definite__ (between limits a and b):
$$
\int_a^bf(x)dx
$$
## Indefinite Integrals
__Indefinite Integrals__ (Antiderivatives): A function (F(x)) is an antiderivative when
$$
F(x). F'(x) = f(x)
$$
The collection of antiderivatives of a function f(x) is denoted by a symbol:
$$
\int f(x)dx
$$
- Common antiderivatives
$$
f(x) = a \iff \int f(x)dx = ax + C
$$
$$
f(x) = ax^n \iff \int f(x)dx = \frac{ax^{n+1}}{n+1} + C
$$
$$
f(x) = ae^{bx} \iff \int(f(x)dx) = \frac{1}{k} ae^{bx} + C
$$
$$
f(x) = a\cos(bx) \iff \int f(x)dx = \frac{1}{k}\sin(bx) + C
$$
$$
f(x) = a\sin(bx) \iff \int f(x)dx = \frac{1}{k}a\cos(bx) + C
$$
__Antiderivatives differ by a constant__:
$$
F'(x) = f(x), G'(x) = f(x) \implies F(x) = G(x) + C 
$$
where:
- F(x), G(x) are antiderivatives
- C is some constant

__Antiderivative Rules__:
- Addition:
$$
\int(f(x) + g(x))dx = \int f(x)dx + \int g(x)dx
$$
- Scalar Multiplication:
$$
\int(af(x))dx = a \int f(x)dx 
$$
## Definite Integrals
__Definite Integrals__: When f is continuous of \[a, b]
$$
\int_a^b f(x)dx = F(b) - F(a)
$$
