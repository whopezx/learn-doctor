# Basic Concepts
### spin density
reference: [思想家公社 353 博文](http://sobereva.com/353)

For open shell molecules, the number of $\alpha$ and $\beta$ electrons are differents. This lead to electron density of $\alpha$ are different with electron density of $\beta$. To investigate distribution of single electron can define spin density
$$
spin\ density = \mathbf{n}_{\alpha}(\mathbf{r}) - \mathbf{n}_{\beta}(\mathbf{r})
$$
obvirously, if spin density great than $0$, there are more $\alpha$ electrons at $\mathbf{r}$ than $\beta$ electrons, vice versa. And for closed shell moleculars, spin density equal to zero.

### magnitic moment
reference: [wiki](https://en.wikipedia.org/wiki/Magnetic_moment)

there are three useful definition

1. The magnetic moment can be defined as a vector relating the aligning torque on the object from an externally applied magnetic field to the field vector itself. 
$$
\bm{\tau} = \bm{m} \times \bm{B}
$$
where $\bm{\tau}$ is torque acting on the dipole, $\bm{m}$ is magnetic moment, $\bm{B}$ is magnetic field.
This definition is based on how one could measure the magnetic moment of an unknown sample.

2. Magnetic moment generate by current, so the definition is
$$
\bm{m} = I\bm{a}
$$
where $\bm{m}$ is magnetic moment, $I$ is the magnitude of current, $\bm{a}$ is area vector.
This definition is based on how to generate magnetic moment.

3. For thermodynamics calculations, there is an useful definition
$$
\bm{m} 
= -\hat{\bm{x}}\frac{\partial U}{\partial B_{x}}
- \hat{\bm{y}}\frac{\partial U}{\partial B_{y}}
- \hat{\bm{z}}\frac{\partial U}{\partial B_{z}}
$$
i.e. magnetic moment is the negative gradient of energy $U$.
This definition is based on how to define it as a conjugate variable.

These three definition is equal. According to definition of energy $U = -\bm{m}\cdot B$ and definition of current $I = \int\int \bm{J}\cdot d\bm{a}\rightarrow \bm{m} = \frac{1}{2}\int\bm{r}\times\bm{J}d^3 r$ can derivative they are equal.