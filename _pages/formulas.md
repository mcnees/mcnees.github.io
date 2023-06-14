---
permalink: /formulas/
title: "Conventions, Definitions, Identities, and Formulas"
<!-- layout: splash -->
classes: wide
---

<!-- # Conventions, Definitions, Identities, and Formulas -->
_Last Modified: July 12, 2022_

A collection of results that are useful enough for me to keep them all in one place. [Let me know][Mail-me] if you find typos or mistakes.


Several people have contacted me to say that they used some of these results in published papers. That's great! If you use this reference for something that ends up in a publication, please consider including a citation with my name, the page title, and the url. [Here's how to do it in REVTeX][REVTeX-code] (thanks, [Tim Wiser][Tim-tweet]), and here's [BibTeX code][BibTeX-code]. 

Watch out for MathJax that hasn't compiled! Porting this over from pure html to markdown has been a real pain. LaTeX sitting in an html element uses a single slash, but outside an element an extra slash is needed.
 {: .notice--danger}

<!-- {% include toc title="Table of Contents" %} -->

### Table of Contents

- [Curvature Tensors](#curvature-tensors)
- [Differential Forms](#differential-forms)
- [Lie Derivatives](#lie-derivatives)
- [Euler Densities](#euler-densities)
- [Hypersurface Formed by a Spacelike Vector](#hypersurface-formed-by-a-spacelike-vector)
- [Sign Conventions for the Action](#sign-conventions-for-the-action)
- [Hamiltonian Formulation for Evolution Along a Spatial Direction](#hamiltonian-formulation-for-evolution-along-a-spatial-direction)
- [Weyl Transformations](#weyl-transformations)
- [Small Variations of the Metric](#small-variations-of-the-metric)
- [The ADM Decomposition](#the-adm-decomposition)
- [Converting to ADM Variables](#converting-to-adm-variables)

<!-- End TOC  -->

### Curvature Tensors

Consider a \\(d+1\\) dimensional spacetime \\((\mathcal{M}, g)\\) and a covariant derivative \\(\nabla\\) compatible with the metric \\(g\\).

<ul>
	<li> Christoffel Symbols 
    \begin{equation}
    	\Gamma^{\lambda}_{\,\mu\nu} = \frac{1}{2} g^{\lambda \rho}\left(\partial_{\mu} g_{\rho \nu}
        + \partial_{\nu} g_{\mu \rho} - \partial_{\rho} g_{\mu \nu}\right)
 	\end{equation}

    </li>	    
	<li> Riemann Tensor  
    \begin{equation}
    	R^{\lambda}{}_{\mu\sigma\nu} = \partial_{\sigma} \Gamma^{\lambda}_{\, \mu\nu}  -
		\partial_{\nu} \Gamma^{\lambda}_{\, \mu\sigma} +
		\Gamma^{\kappa}_{\,\mu\nu} \Gamma^{\lambda}_{\, \kappa \sigma} -
		\Gamma^{\kappa}_{\,\mu\sigma} \Gamma^{\lambda}_{\, \kappa \nu}
	\end{equation}
	</li>
	<li> Ricci Tensor
    \begin{equation}
	    R_{\mu\nu} = \delta^{\sigma}{}_{\lambda} R^{\lambda}{}_{\mu \sigma \nu}
	\end{equation}
	</li>
	<li> Schouten Tensor
    \begin{equation}
		S_{\mu\nu} = \frac{1}{d-1} \, \left(R_{\mu\nu} - \frac{1}{2\,d}\,g_{\mu\nu} R \right)
	\end{equation}
    \begin{equation}
       \nabla^{\nu} S_{\mu\nu} = \nabla_{\mu} S^{\nu}_{\,\, \nu} 
	\end{equation}
	</li>
	<li> Weyl Tensor
    \begin{equation}
		C^{\lambda}{}_{\mu \sigma \nu} = R^{\lambda}{}_{\mu \sigma \nu} +
   g^{\lambda}{}_{\nu} \, S_{\mu \sigma} - g^{\lambda}{}_{\sigma} \, S_{\mu\nu}
   + g_{\mu\sigma} \, S^{\lambda}{}_{\nu} -  g_{\mu\nu} \, S^{\lambda}{}_{\sigma}
	\end{equation}
	</li>
	<li> Commutators of Covariant Derivatives
    \begin{equation}
		\left[ \nabla_{\mu}, \nabla_{\nu} \right] A_{\lambda} = R_{\lambda \sigma \mu \nu} A^{\sigma}
	\end{equation}
    \begin{equation}
		\left[ \nabla_{\mu}, \nabla_{\nu} \right] A^{\lambda} = R^{\lambda}{}_{\sigma \mu \nu}
		 A^{\sigma} 
	\end{equation}
	</li>
	<li> Bianchi Identities
    \begin{equation}
		\nabla_{\kappa} R_{\lambda \mu \sigma \nu} - \nabla_{\lambda} R_{\kappa \mu \sigma \nu}
		+ \nabla_{\mu} R_{\kappa \lambda \sigma \nu} = 0 
	\end{equation}
    \begin{equation}
  		\nabla^{\nu} R_{\lambda \mu \sigma \nu} = \nabla_{\mu} R_{\lambda \sigma} -
  		\nabla_{\lambda} R_{\mu\sigma}  
	\end{equation}
    \begin{equation}
		\nabla^{\nu} R_{\mu\nu} = \frac{1}{2} \, \nabla_{\mu} R 
	\end{equation}
	</li>
	<li> Bianchi Identities for the Weyl Tensor
	\begin{align}	
		\nabla^{\nu} C_{\lambda \mu \sigma \nu}  = & \, (d-2) \, \left( \nabla_{\mu} S_{\lambda \sigma}
		- \nabla_{\lambda} S_{\mu \sigma} \right)
	\end{align}
	\begin{align}	
	  \nabla^{\lambda} \nabla^{\sigma} C_{\lambda \mu \sigma \nu}  =  \frac{d-2}{d-1} 
     & \,\left[ \, \nabla^{2} R_{\mu\nu} - \frac{1}{2d} \, g_{\mu\nu} \nabla^{2} R -
    \frac{d-1}{2d} \, \nabla_{\mu} \nabla_{\nu} R \right. \\ \nonumber
     & \,\, - \left. \left(\frac{d+1}{d-1}\right) \,
    R_{\mu}{}^{\lambda} R_{\nu \lambda} 
    +  C_{\lambda \mu \sigma \nu} R^{\lambda \sigma} + \frac{(d+1)}{d(d-1)} \,
    R \, R_{\mu\nu} \right. \\ \nonumber
    & \,\, \left. + \frac{1}{d-1} \, g_{\mu\nu} \left(R^{\lambda\sigma} R_{\lambda \sigma}
     - \frac{1}{d} \, R^2 \right) \, \right]
	\end{align}
	</li>
</ul> 

### Differential Forms
<ul>
	<li>p-Form Components
	\begin{align}
		{\bf A}_{(p)} = \frac{1}{p!}\,A_{\mu_1 \ldots \mu_p}\,dx^{\mu_1} \land \ldots \land dx^{\mu_p}
	\end{align}
	</li>
	
	<li>Exterior Derivative
	\begin{align}
		\Big(d{\bf A}_{(p)}\Big)_{\mu_1 \ldots \mu_{p+1}} = (p+1)\,\partial_{\,[\,\mu_1} A_{\mu_2 \ldots \mu_{p+1}\,]\,}
	\end{align}
	\begin{align}
		B_{\,[\, \mu_1 \ldots \mu_n ]\,} \defeq \frac{1}{n!}\,\Big(\,B_{\mu_1 \ldots \mu_n} + \textrm{permutations}\,\Big)
	\end{align}
	</li>
	
	<li>Hodge-Star
	\begin{align}
		\Big( \star {\bf A}_{(p)}\Big)_{\mu_1 \ldots \mu_{d+1-p}} = \frac{1}{p!}\,\epsilon_{\mu_1 \ldots \mu_{d+1-p}}{}^{\nu_1 \ldots 		\nu_p}\,A_{\nu_1 \ldots \nu_p}
	\end{align}
	\begin{align}
		\star \,\star = \big(-1 \,\big)^{p\,(d+1-p)+1}
	\end{align}	
	</li>

	<li>Wedge Product
	\begin{align}
		\Big( {\bf A}_{(p)} \land {\bf B}_{(q)} \Big)_{\mu_1 \ldots \mu_{p+q}} = \frac{(p+q)!}{p!\,q!}\,A_{\,[\,\mu_1 \ldots \mu_p} 		\, B_{\mu_{p+1} \ldots \mu_{p+q} \,]}
	\end{align}
	</li>	
</ul>


### Lie Derivatives
Let \\(T\\) be a rank \\((n,m)\\) tensor and \\(\xi\\) be a vector. The Lie derivative of \\(T\\) along \\(\xi\\) is also a rank \\((n,m)\\) tensor, with components

	$$ \begin{align} \nonumber
		\pounds_{\xi} \,T^{\mu_{1}\ldots\mu_{n}}{}_{\nu_{1}\ldots\nu_{m}} = & \,\, \xi^{\lambda}\partial_{\lambda}\,T^{\mu_{1}\ldots\mu_{n}}{}_{\nu_{1}\ldots\nu_{m}} \\
		&\,\, - \,T^{\lambda\mu_{2}\ldots\mu_{n}}{}_{\nu_{1}\ldots\nu_{m}}\,\partial_{\lambda}\xi^{\mu_{1}} - \ldots - \,T^{\mu_{1}\ldots\mu_{n-1}\lambda}{}_{\nu_{1}\ldots\nu_{m}}\,\partial_{\lambda}\xi^{\mu_{n}} \\ \nonumber
		&\,\, + \,T^{\mu_{1}\ldots\mu_{n}}{}_{\lambda\nu_{2}\ldots\nu_{m}}\,\partial_{\nu_{1}} \xi^{\lambda} + \ldots + \,T^{\mu_{1}\ldots\mu_{n}}{}_{\nu_{1}\ldots\nu_{m-1}\lambda}\,\partial_{\nu_{m}}\xi^{\lambda}
	\end{align} $$
	
Any derivative operator can be used here.



### Euler Densities
Let \\(\MM\\) be a manifold (with no boundary!) and dimension \\(d+1=2n\\) an even number. Our normalization gives \\(\chi(S^{2n})=2\\).

<ul>

<li> Curvature Two-Form
	\begin{equation}
		{\bf R}^{a}_{\dub b} = \frac{1}{2} \, R^{a}_{\dub b \, c\,d} \,{\bf e}^c \land {\bf e}^d
	\end{equation}
</li>

<li>Euler Density
	\begin{equation}
		{\bf e}_{_{2n}} = \frac{1}{(4\pi)^n \, \Gamma(n+1)}\,\eps_{a_{_1} \ldots a_{_{2n}}}
		{\bf R}^{a_{_1} a_{_2}}\land \ldots \land{\bf R}^{a_{_{2n-1}} a_{_{2n}}}
	\end{equation}
	\begin{equation*}
		\EE_{2n} = \frac{1}{(8\pi)^n\,\Gamma(n+1)} \, \eps_{\mu_{_1} \ldots \mu_{_{2n}}} \,
		\eps_{\nu_{_1} \ldots \nu_{_{2n}}} \, R^{\mu_{_1}\mu_{_2}\nu_{_1}\nu_{_2}} \ldots
		R^{\mu_{_{2n-1}}\mu_{_{2n}}\nu_{_{2n-1}}\nu_{_{2n}}}
	\end{equation*}
</li>

<li>Euler Number
	\begin{align}
		\chi(\MM) & \, = \int_{\MM} \nts d^{2n}x \,\sqrt{g} \, \EE_{2n} \\ \nonumber
            & \, = \int_{\MM} \nts  {\bf e}_{_{2n}}
	\end{align}
</li>

<li>Examples
	\begin{align}
		\EE_{2} & \, = \frac{1}{8\pi} \, \eps_{\mu\nu} \eps_{\lambda\rho} \, R^{\mu\nu\lambda\rho} \\ \nonumber
		& \, = \frac{1}{4\pi}\,R \\
		\EE_{4} & \, = \frac{1}{128 \pi^2} \, \eps_{\mu\nu\lambda\rho} \, \eps_{\alpha\beta\gamma\delta}
		\, R^{\mu\nu\alpha\beta} \, R^{\lambda\rho\gamma\delta} \\ \nonumber
		& \, = \frac{1}{32 \pi^2} \, \left(R^{\mu\nu\lambda\rho} R_{\mu\nu\lambda\rho}
        - 4 \, R^{\mu\nu} R_{\mu\nu} + R^2 \right) \\ \nonumber
		& \, = \frac{1}{32 \pi^2} \, C^{\mu\nu\lambda\rho} C_{\mu\nu\lambda\rho} - \frac{1}{8\pi^2} \,
        \left(\frac{d-2}{d-1}\right)\,\left(R^{\mu\nu} R_{\mu\nu} - \frac{d+1}{4\,d} \, R^2
         \right) \\ \nonumber
		 & 
	\end{align}

</li>
</ul>

###  Hypersurface Formed by a Spacelike Vector

Let \\(\Sigma \subset \MM\\) be a \\(d\\) dimensional hypersurface whose embedding is described locally by an outward-pointing, unit normal vector \\(n^{\mu}\\). The vector \\(n^{\mu}\\) is assumed to be spacelike: \\(n^{\mu} n_{\mu} = 1\\). (Properties of hypersurfaces formed by a timelike vector are described in the section on the ADM decomposition.) Indices are lowered and raised using \\(g_{\mu\nu}\\) and \\(g^{\mu\nu}\\), and
symmetrization of indices is implied when appropriate.

<ul>
<li>First Fundamental Form / Induced Metric on \(\Sigma\)
	\begin{equation}
	    h_{\mu\nu} = g_{\mu\nu} - n_{\mu} n_{\nu}
	\end{equation}
</li>

<li>Projection onto \(\Sigma\)
	\begin{equation}
	    \bot \,T^{\mu \,\ldots}{}_{\nu \, \ldots} = h^{\mu}{}_{\lambda} \ldots
	    h^{\sigma}{}_{\nu} \ldots T^{\lambda \, \ldots}{}_{\sigma \, \ldots}
	\end{equation}
</li>

<li>Second Fundamental Form / Extrinsic Curvature of \(\Sigma\)
	\begin{gather}
	    K_{\mu\nu} = \bot (\nabla_{\mu} n_{\nu} ) = h_{\mu}{}^{\lambda} h_{\nu}{}^{\sigma}\,
	    \nabla_{\lambda} n_{\sigma}  = \frac{1}{2} \, \pounds_{n} h_{\mu\nu}
	\end{gather}
</li>

<li>Trace of Extrinsic Curvature
	\begin{equation}
	    K = \nabla_{\mu} n^{\mu}
	\end{equation}
</li>

<li>&ldquo;Acceleration&rdquo; Vector
	\begin{equation}
	    a^{\mu} = n^{\nu} \nabla_{\nu} n^{\mu}
	\end{equation}
</li>

<li>Surface-Forming Normal Vectors
	\begin{equation}\label{SFNV}
	    n_{\mu} = \frac{1}{\sqrt{g^{\nu\lambda} \, \partial_{\nu} \alpha \partial_{\lambda} \alpha}} \,
	    \partial_{\mu} \alpha \quad \Rightarrow \quad \bot \nabla_{[\,\mu} n_{\nu\,]} = 0
	\end{equation}
</li>

<li>Covariant Derivative on \(\Sigma\) compatible with \(h_{\mu\nu}\)
	\begin{equation}
	 \DD_{\mu} T^{\alpha \, \ldots}{}_{\beta \, \ldots} = \bot \, \nabla_{\mu} T^{\alpha \, \ldots}{}_{\beta \, \ldots} \quad \forall \quad T = \bot\,T
	\end{equation}
</li>

<li>Intrinsic Curvature of \((\Sigma,h)\)
	\begin{equation}
	  \left[ \DD_{\mu}, \DD_{\nu} \right] A^{\lambda} = \RR^{\lambda}{}_{\sigma \mu \nu} A^{\sigma} \quad
	    \forall \quad A^{\lambda} = \bot \, A^{\lambda} %= h^{\lambda}{}_{\sigma} \, A^{\sigma}
	\end{equation}
</li>

<li>Gauss-Codazzi
\begin{align}
    \bot R_{\lambda \mu \sigma \nu} \, = & \dub \RR_{\lambda \mu \sigma \nu} - K_{\lambda \sigma}
    K_{\mu \nu} + K_{\mu \sigma} K_{\nu \lambda} \\ 
    \bot \left( R_{\lambda \mu \sigma \nu} \,n^{\lambda} \right) \, = & \dub \DD_{\nu} K_{\mu\sigma} -
    \DD_{\sigma} K_{\mu\nu} \\ 
    \bot \left(R_{\lambda \mu \sigma \nu} \,n^{\lambda}  n^{\sigma}\right) \, = & \, - \pounds_{n} \, K_{\mu\nu} + K_{\mu}{}^{\lambda} \, K_{\lambda \nu} + \DD_{\mu} a_{\nu} - a_{\mu} a_{\nu}
\end{align}
</li>

<li>Projections of the Ricci tensor
	\begin{align}
	 \bot \left( R_{\mu\nu} \right) \, = & \,\, \RR_{\mu\nu} + \DD_{\mu} a_{\nu} - a_{\mu} a_{\nu} -
	 \pounds_{n} \, K_{\mu\nu} - K \, K_{\mu\nu} + 2 K_{\mu}{}^{\lambda} \, K_{\nu \, \lambda} \\ 
	 \bot \left( R_{\mu\nu} \,n^{\mu}  \right) \, =  & \,\, \DD^{\mu} K_{\mu\nu} - \DD_{\nu} K \vphantom{\Big|}
	 \\ 
	 R_{\mu\nu} n^{\mu} n^{\nu} \, = & - \pounds_{n} \, K - K^{\mu\nu} \, K_{\mu\nu} + \DD_{\mu} a^{\mu}
	 -a_{\mu} a^{\mu}
	\end{align}
</li>

<li>Decomposition of the Ricci scalar
	\begin{align}
	 R \, = & \dub \RR - K^2 - K^{\mu\nu}\,K_{\mu\nu} - 2\,\pounds_{n} \, K + 2 \, \DD_{\mu} a^{\mu} - 2 \,
	 a_{\mu} a^{\mu}
	\end{align}
</li>

<li>Lie Derivatives along \(n^{\mu}\)
	\begin{gather}
	  \pounds_{n} K_{\mu\nu} \, = \, n^{\lambda} \nabla_{\lambda} K_{\mu\nu} +
	  K_{\lambda \nu} \nabla_{\mu} n^{\lambda} + K_{\mu \lambda} \nabla_{\nu} n^{\lambda} \\ 
	  \bot \left( \pounds_{n} \, \FF^{\mu \,\ldots}{}_{\nu \, \ldots}\right) \, = \,  \pounds_{n} \, \FF^{\mu \,\ldots}{}_{\nu \,
	  \ldots} \quad \forall \quad \bot \FF = \FF
	\end{gather}
</li>

</ul>


### Sign Conventions for the Action

These conventions follow Weinberg (after accounting for his definition of the Riemann tensor, which has a minus sign relative to our definition). They are appropriate when using Lorentzian signature \\((-,+,\ldots,+)\\). The \\(d+1\\)-dimensional Newton's constant is \\(2\kappa^{2} = 16 \pi G_{d+1}\\). The boundary \\((\dM,h)\\) is formed by a spacelike unit vector \\(n^{\mu}\\), as in the previous section, and the sign on the boundary term follows from our definition of the extrinsic curvature.

<ul>
<li>Gravitational Action
\begin{align}
    I_G = & \dub \frac{1}{2\,\kappa^2} \int_{\MM} \nts d^{d+1}x \sqrt{g} \left( R - 2 \,\Lambda
     \right) + \frac{1}{\kappa^2} \int_{\dM} \nts d^{d} x \sqrt{h} \, K <!-- \\
     = & \dub \frac{1}{2\,\kappa^2} \int_{\MM} \nts d^{d+1}x \sqrt{g} \left( \RR + K^2
    - K^{\mu\nu}\, K_{\mu\nu} - 2 \,\Lambda \right) -->
\end{align}
</li>

<li>Gauge Field Coupled to Particle
\begin{align}
    I_{Maxwell} + I_{Matter} = & \dub -\frac{1}{4} \int_{\MM} \nts d^{d+1}x \sqrt{g} \,F^{\mu\nu} F_{\mu\nu} \\
            & \dub - \sum_{n} m_{n}  \int dp \, \sqrt{ -g_{\mu\nu}(x_{n}(p))\,\frac{dx_{n}{}^{\mu}(p)}{dp}
                \frac{dx_{n}{}^{\nu}(p)}{dp} } \\
            & \dub + \sum_{n} e_{n}  \int dp \, \frac{dx_{n}{}^{\mu}(p)}{dp}\,A_{\mu}(x_{n}(p))
\end{align}
</li>

<li>Gravity Minimally Coupled to a Scalar Field
\begin{align}
    I_G + I_{scalar} = & \dub \int_{\MM} \nts d^{d+1}x \sqrt{g} \left[ \frac{1}{2\,\kappa^2} \left( R - 2 \,\Lambda \right)
     - \frac{1}{2} \nabla_{\mu} \varphi \, \nabla^{\mu} \varphi - V(\varphi)  \right] 
\end{align}
</li>

<li>Gravity Minimally Coupled to a Gauge Field
\begin{align}
    I_G + I_{Maxwell} = & \dub \int_{\MM} \nts d^{d+1}x \sqrt{g} \left[ \frac{1}{2\,\kappa^2} \left( R - 2 \,\Lambda \right)
     - \frac{1}{4} F^{\mu\nu} F_{\mu\nu} \right] 
\end{align}
</li>

<li>Stress Tensor
\begin{gather}
	T^{\mu\nu} \defeq \frac{2}{\sqrt{g}}\,\frac{\delta I}{\delta g_{\mu\nu}} = - g^{\mu\lambda} g^{\nu\rho} \frac{2}{\sqrt{g}}\,\frac{\delta I}{\delta g^{\lambda\rho}}
\end{gather}
</li>
</ul>

### Hamiltonian Formulation for Evolution Along a Spatial Direction

The canonical variables are the metric \\(h_{\mu\nu}\\) on \\(\Sigma\\) and its conjugate momentum \\(\pi^{\mu\nu}\\), which is defined with respect to evolution along the spacelike direction \\(n^{\mu}\\) normal to \\(\Sigma\\). Even though the evolution is along a spacelike direction we will use the same terminology as for timelike evolution: &ldquo;Hamiltonian&rdquo;, &ldquo;momentum constraint&rdquo;, etc.

<ul>
<li>Bulk Lagrangian Density
	\begin{gather}
	    \Lag_{\MM} = \frac{1}{2\,\kappa^2} \left( K^2 - K^{\mu\nu} \, K_{\mu\nu}
	        + \RR - 2\,\Lambda \right)
	\end{gather}
</li>	

<li>Momentum Conjugate to \(h_{\mu\nu}\)
	\begin{equation}
	    \pi^{\mu\nu} = \frac{\partial \Lag_{\MM}}{\partial \left( \pounds_{n}
	    h_{\mu\nu} \right)} = \frac{1}{2\,\kappa^2} \left(h^{\mu\nu}\,K - K^{\mu\nu} \right)
	\end{equation}
	\begin{equation}
	    \pi = \pi^{\mu}{}_{\mu} = \frac{d-1}{2\,\kappa^2} K
	\end{equation}</li>

<li>Momentum Constraint
	\begin{gather}
	    \HH_{\mu} = \frac{1}{\kappa^2} \bot \left(n^{\nu} G_{\mu\nu} \right) =  2\,\DD^{\nu} \pi_{\mu\nu} = 0
	\end{gather}
</li>

<li>Hamiltonian Constraint
	\begin{gather}
	   \HH = - \frac{1}{\kappa^2} n^{\mu} n^{\nu} G_{\mu\nu} =  2 \, \kappa^2 \left(\pi^{\mu\nu} \, \pi_{\mu\nu}
	    - \frac{1}{d-1} \, \pi^2 \right) + \frac{1}{2\,\kappa^2} \left( \RR - 2 \, \Lambda \right) = 0
	\end{gather}
</li>
</ul>

### Weyl Transformations

The dimension of spacetime is \\(d+1\\). Indices are raised and lowered using the metric \\(g_{\mu\nu}\\) and its inverse \\(g^{\mu\nu}\\). 

<ul>
<li>Metric
	\begin{gather}
	    \hg_{\mu\nu} = e^{\,2\,\sigma} \, g_{\mu\nu}
	\end{gather}
</li>

<li>Christoffel
	\begin{gather}
	 \hat{\Gamma}^{\,\lambda}_{\,\mu\nu} = \Gamma^{\lambda}_{\,\mu\nu} + \Theta^{\lambda}_{\,\mu\nu}
	 \\ 
	 \Theta^{\lambda}_{\,\mu\nu} = \delta^{\lambda}{}_{\mu} \nabla_{\nu} \sigma
	    + \delta^{\lambda}{}_{\nu} \nabla_{\mu} \sigma
	    - g_{\mu\nu} \nabla^{\lambda} \sigma
	\end{gather}
</li>

<li>Riemann Tensor
	\begin{align}
	 \hat{R}^{\,\lambda}{}_{\mu\rho\nu} = & \dub R^{\lambda}{}_{\mu\rho\nu}
	 + \delta^{\lambda}{}_{\nu} \, \nabla_{\mu} \nabla_{\rho} \sigma
	 - \delta^{\lambda}{}_{\rho} \, \nabla_{\mu} \nabla_{\nu} \sigma
	 + g_{\mu\rho} \, \nabla_{\nu} \nabla^{\lambda} \sigma - g_{\mu\nu} \, \nabla_{\rho} \nabla^{\lambda} \sigma \\ \nonumber
	& \dub + \delta^{\lambda}{}_{\rho} \, \nabla_{\mu} \sigma \, \nabla_{\nu} \sigma
	 - \delta^{\lambda}{}_{\nu} \, \nabla_{\mu} \sigma \, \nabla_{\rho} \sigma
	 + g_{\mu\nu}\,\nabla_{\rho} \sigma \, \nabla^{\lambda} \sigma
	 - g_{\mu\rho}\,\nabla_{\nu} \sigma \, \nabla^{\lambda} \sigma \\ \nonumber
	 & \dub + \left( g_{\mu\rho} \, \delta^{\lambda}{}_{\nu} - g_{\mu\nu} \, \delta^{\lambda}{}_{\rho}
	  \right)  \nabla^{\alpha} \sigma \, \nabla_{\alpha} \sigma
	\end{align}
</li>

<li>Ricci Tensor
	\begin{align}
	 \hat{R}_{\mu\nu} = & \dub R_{\mu\nu} - g_{\mu\nu} \, \nabla^{2} \sigma - (d-1)\,\nabla_{\mu}
	    \nabla_{\nu} \sigma + (d-1) \, \nabla_{\mu} \sigma \, \nabla_{\nu} \sigma \\ \nonumber
	     & \dub - (d-1) \, g_{\mu\nu} \nabla^{\lambda} \sigma \, \nabla_{\lambda} \sigma
	\end{align}
</li>

<li>Ricci Scalar
	\begin{align}
	 \hat{R} = e^{-2\,\sigma} \left( R -2\,d\,\nabla^{2} \sigma - d\,(d-1)\,\nabla^{\mu} \sigma \,
	     \nabla_{\mu} \sigma \right)
	\end{align}
</li>

<li>Schouten Tensor
	\begin{align}
	 \hat{S}_{\mu\nu} = & \dub S_{\mu\nu} - \nabla_{\mu} \nabla_{\nu} \sigma
	    + \nabla_{\mu} \sigma \, \nabla_{\nu} \sigma - \frac{1}{2} \, g_{\mu\nu} \nabla^{\lambda} \sigma \, \nabla_{\lambda} \sigma
	\end{align}
</li>

<li>Weyl Tensor
	\begin{gather}
	    \hat{C}^{\,\lambda}{}_{\mu \rho \nu} = C^{\lambda}_{\dub \mu \rho \nu}
	\end{gather}
</li>

<li>Normal Vector
	\begin{gather}
	    \widehat{n}^{\mu} = e^{-\sigma} \, n^{\mu} \quad \quad \widehat{n}_{\mu} = e^{\,\sigma} \, n_{\mu}
	\end{gather}
</li>

<li>Extrinsic Curvature
	\begin{gather}
	  \hat{K}_{\mu\nu} = e^{\,\sigma} \left( K_{\mu\nu} + h_{\mu\nu} \, n^{\lambda}
	    \nabla_{\lambda} \sigma \right) \\
	  \hat{K} = e^{-\sigma} \left( K + d \, n^{\lambda} \nabla_{\lambda} \sigma \right)
	\end{gather}
</li>

</ul>


### Small Variations of the Metric

Consider a small perturbation to the metric of the form \\(g_{\mu\nu} \to g_{\mu\nu} +
\dg_{\mu\nu}\\). All indices are raised and lowered using the unperturbed metric \\(g_{\mu\nu}\\) and
its inverse. All quantities are expressed in terms of the perturbation to the metric, and never in terms of the perturbation to the inverse metric. As in the previous sections, \\(\nabla_{\mu}\\) is the covariant derivative compatible with the metric \\(g_{\mu\nu}\\), and \\(\DD_{\mu}\\) is the covariant derivative along a hypersurface \\(\Sigma \subset \MM \\) (formed by the spacelike vector \\(n^{\mu}\\)) compatible with \\(h_{\mu\nu}\\).

<ul>

<li>Inverse Metric
	\begin{equation}
	   g^{\mu\nu} \to g^{\mu\nu} - g^{\mu\alpha}\,g^{\nu\beta} \,\dg_{\alpha\beta} +
	   g^{\mu\alpha}\,g^{\nu\beta}\,g^{\lambda\rho}\,\dg_{\alpha\lambda}\,\dg_{\beta\rho}
	    + \ldots
	\end{equation}
</li>

<li>Square Root of Determinant of Metric
	\begin{equation}
	  \sqrt{g} \to \sqrt{g} \, \left( 1 + \frac{1}{2}\,g^{\mu\nu} \dg_{\mu\nu} +  \left( \frac{1}{8}\,g^{\alpha\beta} g^{\mu\nu} - \frac{1}{4}\,g^{\mu\alpha} g^{\nu\beta} \right)\,\dg_{\alpha\beta} \dg_{\mu\nu} +  \ldots \right)
	\end{equation}
</li>

<li>Variational Operator
	\begin{gather}
	   \delta (g_{\mu\nu}) = \dg_{\mu\nu} \quad \quad \delta^{\,2} (g_{\mu\nu}) = \delta (\dg_{\mu\nu}) = 0 \\ 
	   \delta(g^{\mu\nu}) = - g^{\mu\alpha}\,g^{\nu\beta} \,\dg_{\alpha\beta} \\
	   \delta^{\,2} (g^{\mu\nu}) = \delta \left( -g^{\mu\lambda} \, g^{\nu\rho} \, \dg_{\lambda \rho}\right)
	    = 2 \,  g^{\mu\alpha}\,g^{\nu\beta}\,g^{\lambda\rho}\,\dg_{\alpha\lambda}\,\dg_{\beta\rho} \\ 
	   \FF(g+\dg) = \FF(g) + \delta \FF(g) + \frac{1}{2} \delta^{\,2} \FF(g) + \ldots
	    + \frac{1}{n!} \delta^{\,n} \FF(g) + \ldots
	\end{gather}
</li>

<li>Christoffel 
	\begin{gather}
	   \delta \,\Gamma^{\lambda}{}_{\mu \nu} = \frac{1}{2} g^{\lambda \rho} 
	     \left( \nabla_{\mu} \,\dg_{\rho \nu} + \nabla_{\nu} \,\dg_{\mu\rho} - \nabla_{\rho} \,\dg_{\mu\nu}
	     \right) \\ 
	   \delta^{\,2} \Gamma^{\lambda}{}_{\mu \nu} = - g^{\lambda \alpha}\,g^{\rho \beta}\,\dg_{\alpha\beta}
	     \left( \nabla_{\mu} \,\dg_{\rho \nu} + \nabla_{\nu} \,\dg_{\mu\rho} - \nabla_{\rho} \,\dg_{\mu\nu}
	     \right) \\ 
	   \delta^{\,n} \Gamma^{\lambda}{}_{\mu \nu} = \frac{n}{2} \delta^{\,n-1}\left(g^{\lambda \rho} \right) \,
	    \left( \nabla_{\mu} \,\dg_{\rho \nu} + \nabla_{\nu} \,\dg_{\mu\rho} - \nabla_{\rho} \,\dg_{\mu\nu}
	     \right)
	\end{gather}
</li>

<li>Riemann Tensor
	\begin{gather}
	   \delta R^{\lambda}{}_{\mu \sigma \nu} = \nabla_{\sigma} \delta \Gamma^{\lambda}{}_{\mu\nu}
	    - \nabla_{\nu} \delta \Gamma^{\lambda}{}_{\mu\sigma}
	\end{gather}
</li>

<li>Ricci Tensor
\begin{align}
  \delta R_{\mu\nu} = & \dub \nabla_{\lambda} \delta \Gamma^{\lambda}{}_{\mu\nu}
    - \nabla_{\nu} \delta \Gamma^{\lambda}{}_{\mu\lambda} \\
    = & \dub \frac{1}{2} \left( \nabla^{\lambda}  \nabla_{\mu} \dg_{\lambda \nu}
    + \nabla^{\lambda}  \nabla_{\nu} \dg_{\mu \lambda} - g^{\lambda \rho} \nabla_{\mu} \nabla_{\nu}
    \dg_{\lambda \rho} - \nabla^{2} \dg_{\mu\nu} \right)
\end{align}
</li>

<li>Ricci Scalar
	\begin{align}
	  \delta R = - R^{\mu\nu} \dg_{\mu\nu} + \nabla^{\mu} \left( \nabla^{\nu} \dg_{\mu\nu} -
	    g^{\lambda \rho} \nabla_{\mu} \dg_{\lambda \rho} \right)
	\end{align}
</li>

<li>Spacelike, Surface Forming Unit Vector
	\begin{gather}
	   \delta n_{\mu} = \frac{1}{2} n_{\mu} n^{\nu} n^{\lambda} \dg_{\nu\lambda}
	        = \frac{1}{2} \dg_{\mu\nu} n^{\nu} + c_{\mu}
	\end{gather}
	\begin{gather}
	    c_{\mu} = \frac{1}{2} n_{\mu} n^{\nu} n^{\lambda} \dg_{\nu\lambda} - \frac{1}{2} \dg_{\mu\nu} n^{\nu}
	    = -\frac{1}{2} h_{\mu}{}^{\lambda} \dg_{\lambda \nu} n^{\nu}
	\end{gather}
</li>

<li>Extrinsic Curvatures
	\begin{align}
	   \delta K_{\mu\nu} = & \dub \frac{1}{2} n^{\alpha} n^{\beta} \dg_{\alpha \beta} K_{\mu\nu}
	     + \dg_{\lambda \rho} n^{\rho} \left(n_{\mu} K^{\lambda}{}_{\nu}
	     + n_{\nu} K_{\mu}{}^{\lambda} \right) \\ \nonumber
	    & \dub - \frac{1}{2} h_{\mu}{}^{\lambda} h_{\nu}{}^{\rho} n^{\alpha}
	    \left(\nabla_{\lambda} \dg_{\alpha \rho} + \nabla_{\rho} \dg_{\lambda \alpha} -
	    \nabla_{\alpha} \dg_{\lambda \rho} \right)
	\end{align}
	\begin{gather}
	  \delta \, K = - \frac{1}{2} K^{\mu\nu} \dg_{\mu\nu} - \frac{1}{2} n^{\mu}
	    \left(\nabla^{\nu} \dg_{\mu\nu} - g^{\nu\lambda} \nabla_{\mu} \dg_{\nu \lambda} \right) + \DD_{\mu} c^{\mu}
	\end{gather}
</li>


</ul>



### The ADM Decomposition

The conventions and notation in this section (and the next) differ from the preceding sections. In this section we consider a \\(d\\)-dimensional spacetime with metric \\(h\\) and metric-compatible covariant derivative \\({}^{d}\nabla\\).

We start by identifying a scalar field \\(t\\) whose isosurfaces \\(\Sigma_t\\) are normal to the timelike unit vector given by
\begin{gather}
	u_{a} = - \alpha \, \partial_{a} t ~,
\end{gather}
where the lapse function \\(\alpha\\) is
\begin{gather} \label{Lapse}
	\alpha \defeq \frac{1}{\sqrt{-h^{ab}\,\partial_a t \, \partial_b t}} ~.
\end{gather}
An observer whose worldline is tangent to \\(u_{a}\\) experiences an acceleration given by the vector
\begin{gather}
	a_{b} = u^{c} \cdot {}^{d}\nabla_{c} u_{b} ~,
\end{gather} 
which is orthogonal to \\(u_{a}\\). The (spatial) metric on the \\(d-1\\) dimensional surface \\(\Sigma_t\\) is given by
\begin{gather}
	\sigma_{ab} = h_{ab} + u_a u_b ~.
\end{gather}
The intrinsic Ricci tensor built from this metric is denoted by \\(\RR_{ab}\\), and its Ricci scalar is \\(\RR\\). The covariant derivative on \\(\Sigma_t\\) is defined in terms of the \\(d\\) dimensional covariant derivative as
\begin{gather}
	D_{a} V_{b} \defeq \sigma_{a}{}^{c} \sigma_{b}{}^{e} \big({}^{d}\nabla_{c} V_{e} \big) \quad \text{for any} \quad V_{b} = \sigma_{b}{}^{c} V_{c} ~. 
\end{gather}
The extrinsic curvature of \\(\Sigma_t\\) embedded in the ambient \\(d\\) dimensional spacetime is
\begin{gather}\label{tExtrinsic}
	\theta_{ab} \defeq - \sigma_{a}{}^{c} \sigma_{b}{}^{d} \big( {}^{d}\nabla_{c} u_{d} \big) = - {}^{d}\nabla_{a} u_{b} - u_{a} a_{b} = - \frac{1}{2}\,\pounds_{u} \sigma_{ab} ~.
\end{gather}
This definition has an overall minus sign compared to the extrinsic curvature in section <a href="#Hypersurface">4</a>, where we considered surfaces normal to a spacelike vector.


Now we consider a &lsquo;time flow&rsquo; vector field \\(t^{a}\\), which satisfies the condition
\begin{gather}
	t^{a} \, \partial_{a} t = 1 ~. 
\end{gather}
The vector \\(t^{a}\\) can be decomposed into parts normal and along \\(\Sigma_t\\) as
\begin{gather}
	t^{a} = \alpha \, u^{a} + \beta^{a} ~,
\end{gather}

where \\(\alpha\\) is the lapse function \eqref{Lapse}  and \\(\beta^{a} \defeq \,\sigma^{a}{}_{b}\, t^{b}\\) is the shift vector. An important result in the derivations that follow relates the Lie derivative of a scalar or spatial tensor (one that is orthogonal to \\(u^{a}\\) in all of its indices) along the time flow vector field, to Lie derivatives along \\(u^{a}\\) and \\(\beta^{a}\\). Let \\(S\\) be a scalar. Then

\begin{gather}
	\pounds_{t} S = \pounds_{\alpha \, u} S + \pounds_{\beta} S = \alpha \,\pounds_{u} S + \pounds_{\beta} S ~.
\end{gather}    

Rearranging this expression then gives	
\begin{gather}
	\pounds_{u} S = \frac{1}{\alpha}\, \big(\pounds_{t} S - \pounds_{\beta} S \big) ~.
\end{gather}
Similarly, for a spatial tensor with all lower indices we have
\begin{gather}
	\pounds_{t} W_{a\ldots} = \alpha \,\pounds_{u} W_{a\ldots} + \pounds_{\beta} W_{a\ldots} ~. 
\end{gather} 
This is not the case when the tensor has any of its indices raised. In a moment, these identities will allow us to express certain Lie derivatives along \\(u^{a}\\) in terms of regular time derivatives and Lie derivatives along the shift vector \\(\beta^{a}\\). 


 Next, we construct the coordinate system that we will use for the decomposition of the equations of motion. The adapted coordinates \\((t,x^i)\\) are defined by
\begin{gather}
	\partial_{t} x^{a} \defeq t^{a} ~.
\end{gather}
The \\(x^i\\) are coordinates along the \\(d-1\\) dimensional hypersurface \\(\Sigma_t\\). If we define
\begin{gather}
	P_{i}{}^{a} \defeq \frac{\partial x^{a}}{\partial x^{i}} ~,
\end{gather}
then it follows from the definition of the coordinates that \\(P_{i}{}^{a} \partial_{a} t = 0\\) and we can use \\(P_{i}{}^{a}\\) to project tensors onto \\(\Sigma_t\\). For example, in the adapted coordinates the spatial metric, extrinsic curvature, and acceleration and shift vectors are
\begin{gather}
	\sigma_{ij} = P_{i}{}^{a} P_{j}{}^{b} \sigma_{ab} \\
	\theta_{ij} = P_{i}{}^{a} P_{j}{}^{b} \theta_{ab} \\
	a_{j} =  P_{j}{}^{b} a_{b} \\
	\beta_{i} =  P_{i}{}^{a} \beta_{a} = P_{i}{}^{a} t_{a}~.
\end{gather}
The line element in the adapted coordinates takes a familiar form:

$$
\begin{align}
	h_{ab} dx^a dx^b = & \,\, h_{ab} \bigg(\frac{\partial x^a}{\partial t}\,dt + \frac{\partial x^a}{\partial x^i}\,dx^i\bigg)
	\bigg( \frac{\partial x^b}{\partial t}\,dt + \frac{\partial x^b}{\partial x^j}\,dx^j \bigg) \\
	 = & \,\, h_{ab} \bigg( t^{a} dt + P_{i}{}^{a} dx^i \bigg) \bigg(t^{b} dt + P_{j}{}^{b} dx^j \bigg) \\
	 = & \,\, t^{a} t_{a} dt^2 + 2 t_{a} dt P_{i}{}^{a} dx^i + h_{ab} P_{i}{}^{a} P_{j}{}^{b} dx^i dx^j \\
	 = & \,\, \big( - \alpha^{2} + \beta^i \beta_i \big) dt^2 + 2 \beta_i dt dx^i + \sigma_{ij} dx^i dx^j \\ \label{ADMds}
	\Rightarrow h_{ab} dx^a dx^b = & \,\, -\alpha^2 dt^2 + \sigma_{ij} \big(dx^i + \beta^i dt \big) \big(dx^j + \beta^j dt \big) ~.
\end{align} 
$$

Thus, in the adapted coordinate system we can express the components of the spacetime metric \\(h_{ab}\\) and its inverse \\(h^{ab}\\) as 

$$
\begin{gather}
	h_{ab} = \left( \begin{array}{c|c}
	-\alpha^{2} + \beta^i \beta_i & \hspace{1em} \sigma_{ij} \beta^{j} \hspace{1em} \\ \hline
	\sigma_{ij} \beta^{j} & \sigma_{ij}  \end{array} \right) \\ \label{ADMInverseMetric}
	h^{ab} = \left( \begin{array}{c|c}
	\hspace{1em} -\frac{1}{\alpha^{2}}  \hspace{1em} & \frac{1}{\alpha^2} \, \beta^{i}  \\ \hline
	 \frac{1}{\alpha^2} \, \beta^{i}  & \sigma^{ij} -  \frac{1}{\alpha^2} \, \beta^{i} \beta^{j}  \end{array} \right) \\
	\det(h_{ab}) = -\alpha^{2} \det(\sigma_{ij}) \vphantom{\Big|}
\end{gather}
$$

Obtaining the components of the inverse is a short algebraic calculation. Note that the spatial indices \\(i,j,\ldots\\) in the adapted coordinates are lowered and raised using the spatial metric \\(\sigma_{ij}\\) and its inverse \\(\sigma^{ij}\\).	


In adapted coordinates there are several results concerning the projections of Lie derivatives of scalars and tensors which will be important in what follows. The first, which is trivial, is that the Lie derivative of a scalar \\(S\\) along the time-flow vector \\(t^a\\) is just the regular time-derivative
\begin{gather}
	\pounds_{t} S = t^{a} \partial_{a} S = \frac{\partial x^{a}}{\partial t}\,\frac{\partial S}{\partial x^{a}} = \partial_{t} S ~.
\end{gather}
Next, we consider the projector \\(P_{i}{}^{a}\\) applied to the Lie derivative along \\(t^{a}\\) of a general vector \\(W_{a}\\), which gives
\begin{gather}
	P_{i}{}^{a} \pounds_{t} W_{a} = \partial_{t} W_{a} \quad \forall \quad W_{a} ~. 
\end{gather}
The important point is that this applies not just to spatial vectors but to <i>any</i> vector \\(W_{a}\\), as a consequence of the result
\begin{gather}
	P_{i}{}^{a} \pounds_{t} u_{a} = 0 ~. 
\end{gather}
Finally, we can show that the Lie derivative along \\(t^{a}\\) of any contravariant spatial vector satisfies

$$
\begin{gather}
	P^{i}{}_{a} \pounds_{t} V^{a}  = \partial_{t} V^{i} \quad \forall \quad V^{i} = P^{i}{}_{a} V^{a} ~.
\end{gather}
$$

This follows from a lengthier calculation than what is required for the first two results. 	


Given these results, we can express various geometric quantities and their projections normal to and along \\(\Sigma_t\\) in terms of quantities intrinsic to \\(\Sigma_t\\) and simple time derivatives. First, the extrinsic curvature is

$$
\begin{align}
	\theta_{ij} = & \,\, - \frac{1}{2}\, P_{i}{}^{a} P_{j}{}^{b} \pounds_{u} \sigma_{ab} \\
		    = & \,\, - \frac{1}{2}\, P_{i}{}^{a} P_{j}{}^{b} \bigg(\frac{1}{\alpha}\,\big( \pounds_{t} \sigma_{ab} - 
			\pounds_{\beta} \sigma_{ab} \big)\bigg) \\
	\Rightarrow \, \theta_{ij} = & \,\, - \frac{1}{2 \alpha} \, \bigg(\partial_{t} \sigma_{ij} - \big( D_{i} \beta_{j} + D_{j} \beta_{i} \big) \bigg) ~.
\end{align}
$$

Since \\(\theta_{ab}\\) is a spatial tensor, projections of its Lie derivative along \\(u^{a}\\) can be expressed in a similar manner
\begin{gather}
	P_{i}{}^{a} P_{j}{}^{b} \pounds_{u} \theta_{ab} = \frac{1}{\alpha}\,\big(\partial_t \theta_{ij} - \pounds_{\beta} \theta_{ij} \big) ~.
\end{gather}
Now we present the Gauss-Codazzi and related equations in adapted coordinates:

$$
\begin{align}
	P_{i}{}^{a} P_{j}{}^{b} \big( {}^{d}R_{ab}\big)  = & \,\, \RR_{ij} + \theta \,\theta_{ij} - 2 \theta_{i}{}^{k} \theta_{jk} - \frac{1}{\alpha}\,\big( \partial_t \theta_{ij} - \pounds_{\beta} \theta_{ij} \big) - \frac{1}{\alpha} \, D_i D_j \alpha \\
	P_{i}{}^{a}\big( {}^{d}R_{ab} u^{b} \big) = & \,\, D_{i} \theta - D^{j} \theta_{ij} \\
	{}^{d}R_{ab} u^a u^b = & \,\, \frac{1}{\alpha}\,\big(\partial_t \theta - \beta^{i}\partial_i \theta \big) - \theta^{ij} \theta_{ij} + \frac{1}{\alpha} \, D_i D^i \alpha \\
	{}^{d}R = & \,\, \RR + \theta^{2} + \theta^{ij} \theta_{ij} - \frac{2}{\alpha}\,\big(\partial_t \theta - \beta^i \partial_i \theta \big) - \frac{2}{\alpha}\,D_i D^i \alpha ~.
\end{align}
$$

These allow us to write out the various projections of the Einstein equations \\(G_{ab} = \kappa^{2} T_{ab}\\).

<ul>
 <li> Hamiltonian Constraint
\begin{gather}
	\RR + \theta^{2} - \theta^{ij}\,\theta_{ij} = 2\kappa^{2}\,\rho \\
	\rho \defeq T_{ab} u^{a} u^{b}
\end{gather}
</li>	
<li> Momentum Constraint
\begin{gather}
	D^{j}\theta_{ij} - D_{i}\theta = \kappa^{2} j_{i} \\
	j_{i} \defeq - P_{i}{}^{a}(T_{ab} u^{b})
\end{gather}
</li>
<li>ADM Evolution Equations
\begin{align}
	\RR_{ij} - \frac{1}{2} \sigma_{ij} \RR - \frac{1}{\alpha}\left(\partial_{t} \theta_{ij} - \frac{1}{2} \sigma_{ij} \partial_{t} \theta \right) + \frac{1}{\alpha} \left(\pounds_{\beta} \theta_{ij} - \frac{1}{2} \sigma_{ij} \pounds_{\beta} \theta \right) & \\ \nonumber
	+ \,\theta\,\theta_{ij} -2 \theta_{i}{}^{k} \theta_{jk} -\frac{1}{2}\sigma_{ij}\left(\theta^{2} + \theta^{kl} \theta_{kl} \right) - \frac{1}{\alpha} \left(D_i D_j \alpha - \sigma_{ij} D^{k} D_{k} \alpha \right) & \\ \nonumber
	 = \kappa^{2} P_{i}{}^{a} P_{j}{}^{b} T_{ab} &
\end{align}
Or, if we use the trace of this equation to rewrite \(\RR\) and define the spatial stress tensor as \(\SS_{ij} \defeq P_{i}{}^{a} P_{j}{}^{b} T_{ab}\), this can be written as
\begin{align}
	\partial_{t} \theta_{ij} = & \,\,\pounds_{\beta} \theta_{ij} + \alpha \left(\RR + \theta \, \theta_{ij} - 2 \,\theta_{i}{}^{k} \theta_{jk} \right) - D_{i} D_{j} \alpha \\ \nonumber
	& \, - \kappa^{2}\,\alpha\,\left(\SS_{ij} - \frac{1}{d-2} \sigma_{ij} \SS^{k}{}_{k}\right) - \kappa^{2}\,\frac{1}{d-2} \sigma_{ij} \alpha \,\rho 
\end{align}
</li>
</ul>


	
### Converting to ADM Variables

The line element is often presented in the form
\begin{gather}
	h_{ab} dx^a dx^b = h_{tt} dt^2 + 2 h_{ti} dt dx^i + h_{ij} dx^i dx^j ~.
\end{gather}
We would like to relate the components of the metric to the ADM variables: the lapse function \\(\alpha\\), the shift vector \\(\beta_i\\), and the spatial metric \\(\sigma_{ij}\\). This is a straightforward exercise in linear algebra. Comparing with \eqref{ADMds}, we first note that
\begin{gather}
	\sigma_{ij} = h_{ij} ~.
\end{gather}
The inverse spatial metric, \\(\sigma^{ij}\\), is literally the inverse of \\(h_{ij}\\), which is not in general the same thing as \\(h^{ij}\\). See, for instance, equation \eqref{ADMInverseMetric}.
\begin{gather}
	\sigma^{ij} = (\sigma_{ij})^{-1} = (h_{ij})^{-1} \neq h^{ij} ~. 
\end{gather}
For the shift vector we have
\begin{gather}
	h_{ti} = \sigma_{ij} \beta^{j} \quad \rightarrow \quad \sigma^{ik} h_{tk} = \sigma^{ik} \sigma_{kl} \beta^{l} = \beta^{i} \\
	\Rightarrow \beta^i = \sigma^{ij} h_{tj} ~.
\end{gather}
Finally, for the lapse we obtain
\begin{gather}
	\alpha^{2} = \sigma^{ij} h_{ti} h_{tj} - h_{tt} ~.
\end{gather}	






[Mail-me]: mailto:rmcnees@luc.edu?subject=Your notes were useful!
[REVTeX-code]: https://gist.github.com/mcnees/6f28060a3fd61f9d5054b3b792fa804a
[Tim-tweet]: https://twitter.com/tdwiser/status/1170830257458417667
[BibTeX-code]: https://gist.github.com/mcnees/9f4958838766157c5abbe3da4b6ea163