## Task 3

The goal is to compute the following integral:
$$ I\left( x, \Sigma_1, \Sigma_2 \right) =
    \int \mathcal{N}\left( x - y\ |\ \Sigma_1 \right) \mathcal{N}\left(y\ |\ \Sigma_2\right) d^ky, $$

where

$$ \mathcal{N}\left( x\ |\ \Sigma \right) =
    (2\pi)^{-\frac k2} \det \left(\Sigma\right)^{-\frac 12} \exp{\left( -\frac 12 x^T \Sigma^{-1}x \right)}. $$

The probabilistic interpretation of this integral is the probability density of distribution
of the sum of two random variables, namely $ x = x_1 + x_2 $, where $x_i \sim \mathcal{N} (x_i\ |\ \Sigma_i) $.

For a 1-dimensional case, the result would be simply $\mathcal{N}\left(x\ |\ \Sigma_x \right) $,
where $\Sigma_x = \Sigma_1 + \Sigma_2 $. We may assume that this result stays true for a k-dimensional
multivariate distribution.

For a formal proof, consider how the integral can be reduced to a standard integral:
$$ \int \exp{\left( -\frac{1}{2} x^TAx + B^Tx \right)} d^kx = \sqrt{\frac{(2\pi)^k}{\det A}} \cdot e^{\frac{1}{2} B^TA^{-1}B} $$

Let $\det\Sigma_{1,2} = \Delta_{1,2}$.

$$ I = (2\pi)^{-k} \left( \Sigma_1 \Sigma_2 \right)^{-\frac{1}{2}} \int
        e^{ -\frac{1}{2} x^T\Sigma_1^{-1} x } \cdot 
        e^{  \frac{1}{2} y^T \left( \Sigma_1^{-1} - \Sigma_2^{-1} \right) y }\
    d^ky = $$
$$ (2\pi)^{-k} \left( \Delta_1 \Delta_2 \right)^{-\frac{1}{2}} \cdot
    \int \exp{\left\{ -\frac 12 \left(
        x^T\Sigma_1^{-1}x - y^T\Sigma_1^{-1}x - x^T\Sigma_1^{-1}y + y^T\Sigma_1^{-1}y + y^T\Sigma_2^{-1}y
    \right)\right\}} d^ky
$$