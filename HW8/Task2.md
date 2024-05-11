## Task 2

Let $x_1$ and $x_2$ be normal random variables, $x_1 \sim \left( 0, \sigma_2 \right)$ and
$x_2 \sim \left( 0, \sigma_2 \right) $.

Find the distribution function of $y = x_1 + x_2$

$$ \rho_y(y) = \int_{\mathbb{R}} \rho_{x_1}(x) \cdot \rho_{x_2}(y - x) dx =
    \frac{1}{2\pi\sigma_1\sigma_2} \int_{\mathbb{R}} e^{-\frac{x^2}{2\sigma_1^2}} 
        e^{\frac{-\left(y - x\right)^2}{2\sigma_2^2}} dx = $$

$$ \frac{1}{2\pi\sigma_1\sigma_2}\int_{-\infty}^{+\infty}
    \exp{\left(-\frac
        {\left( \sigma_1^2 + \sigma_2^2 \right)x^2 - 2\sigma_1^2xy + \sigma_1^2y}
        {2\sigma_1^2\sigma_2^2} \right)} dx = $$

$$ \frac{1}{2\pi\sigma_1\sigma_2}\int_{-\infty}^{+\infty}
    \exp{\left(-\frac
        {x^2 - \frac{2\sigma_1^2}{\sigma_1^2 + \sigma_2^2}xy
            + \frac{\sigma_1^4}{\left( \sigma_1^2 + \sigma_2^2 \right)^2}y^2
            - \frac{\sigma_1^4}{\left( \sigma_1^2 + \sigma_2^2 \right)^2}y^2
            + \frac{\sigma_1^2}{\sigma_1^2 + \sigma_2^2}y^2}
        {2\frac{\sigma_1^2 \sigma_2^2}{\sigma_1^2 + \sigma_2^2}} \right) dx} = $$

$$ \frac{1}{2\pi\sigma_1\sigma_2}\int_{-\infty}^{+\infty}
    \exp{\left( -\frac
        {\left( x - \frac{\sigma_1^2}{\sigma_1^2 + \sigma_2^2} y\right)^2
            - \frac{\sigma_1^4}{\left( \sigma_1^2 + \sigma_2^2 \right)^2}y^2
            + \frac{\sigma_1^2}{\sigma_1^2 + \sigma_2^2}y^2}
        {2\frac{\sigma_1^2 \sigma_2^2}{\sigma_1^2 + \sigma_2^2}} \right)} dx  = $$

$$ \frac{\sqrt{2\pi}\sigma_1\sigma_2}{2\pi\sigma_1\sigma_2\sqrt{\sigma_1^2 + \sigma_2^2}}
    \exp{\left( -\frac
        {-\sigma_1^4 + \sigma_1^2\left(\sigma_1^2 + \sigma_2^2\right)}
        {2\sigma_1^2\sigma_2^2\left(\sigma_1^2 + \sigma_2^2 \right)} y^2 \right)} = 

\frac{1}{\sqrt{2\pi\left(\sigma_1^2 + \sigma_2^2\right)}}
    \exp{\left( -\frac{y^2}{2\left(\sigma_1^2 + \sigma_2^2\right)} \right)}. $$


The result: $y \sim \left(0, \sqrt{\sigma_1^2 + \sigma_2^2} \right)$.
