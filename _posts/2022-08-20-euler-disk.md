---
layout: post
title: "Euler's Disk"
author: "Zinc"
tags: first markdown example
categories: gallery
---

 <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  TeX: { equationNumbers: { autoNumber: "AMS" } }
});
</script>

## **Euler's Disk**


### **Introduction**

**Euler's Disk**, invented between 1987 and 1990 by Joseph Bendik, is a trademark for a scientific educational toy. It is used to illustrate and study the dynamic system of a spinning and rolling disk on a flat or curved surface. It has been the subject of several scientific papers. Joseph Bendik first noted the interesting motion of the spinning disk while working at Hughes Aircraft (Carlsbad Research Center) after spinning a heavy polishing chuck on his desk at lunch one day. The apparatus is a dramatic visualization of energy exchanges in three different, tightly coupled processes. As the disk gradually decreases its azimuthal rotation, there is also a decrease in amplitude and increase in the frequency of the disk's axial precession. The evolution of the disk's axial precession is easily visualized in a slow motion video by looking at the side of the disk following a single point marked on the disk. The evolution of the rotation of the disk is easily visualized in slow motion by looking at the top of the disk following an arrow drawn on the disk representing its radius. As the disk releases the initial energy given by the user and approaches a halt, its rotation about the vertical axis slows, while its contact point oscillation increases. Lit from above, its contact point and nearby lower edge in shadow, the disk appears to levitate before halting. Bendik named the toy after mathematician Leonhard Euler.

### **Problem**

A thin, uniform disk of mass $m$ and radius $a$ is initially set at an angle $\alpha_0$ to the horizontal, on a frictionless surface. It is given an initial angular velocity $\Omega_0$ with respect to a vertical axis passing through its center.


**a,** Determine $\Omega_0$ for the steady state case, where $\dot{\alpha} = \ddot{\alpha} = \dot{\Omega} = 0$.

**b,** Write an expression for the total energy of the disk.

The disk is then moved onto a special surface with small bumps of height $h$ spread over it – each bump is separated by $\delta$. As the disk climbs over a bump and falls back down, its impact is absorbed by the surface, causing a net energy loss in the system. The disk is set in motion with the same initial conditions as before
but with $\alpha_0 \ll 1$.

**c,** Assuming that this is the only source of energy loss, write a differential equation for $\dot{\alpha}$ in first order to $\alpha$.

**d,** Hence, write an approximate expression for $\Omega$ as a function of time.

**e,** Using this model, determine the time it takes for the frequency of the sound the disk makes against the surface to reach the maximum audible frequency $f_0$.

### **Solution**

**a,** Choose $O$ of coordinate system is placed at the center of the disk. Consider in the rotating frame of reference with vertical angular velocity $\Omega_0$.

<p align="center">
  <img width="300"  src="/images/gallery/eulerdisk/eulerdisk.png">
</p>

In this frame, there is only the rotating part $\omega_x \hat{\boldsymbol{x}}$ in order to fix the contact point. 

From the non-slipping condition we would have that
\begin{equation}
    \Omega_0 a \cos \alpha_0 = - \omega_x a \Rightarrow \omega_x = -\Omega_0 \cos \alpha_0. 
\end{equation}

Back to the laboratory frame, we will have the total angular velocity

$$
\begin{align}
        \boldsymbol{\omega}_{tot} &= \boldsymbol{\Omega}_0 + \boldsymbol{\omega}_x\\
        &=\Omega_0 (\sin \alpha_0 \hat{\boldsymbol{z}} + \cos \alpha_0 \hat{\boldsymbol{x}}) - \Omega_0 \cos \alpha_0 \hat{\boldsymbol{x}}\\
        &=\Omega_0 \sin \alpha_0 \hat{\boldsymbol{z}}.
\end{align}
$$
 
which lies on the plane of the disk and go through the contact point. As a result, the angular momentum of the disk is therefore $\boldsymbol{L} = I_z \boldsymbol{\omega}_{tot} = \frac{1}{4} m a^2 \Omega_0 \sin \alpha_0 \hat{\boldsymbol{z}}$.

From the Euler's equation of precession, we have

$$
\begin{align}
    \frac{d\boldsymbol{L}}{dt}  &= \boldsymbol{\Omega}_0 \times \boldsymbol{L}\\
    &=\boldsymbol{\Omega}_0 \times \frac{1}{4} ma^2 \Omega_0 \sin \alpha_0 \hat{\boldsymbol{z}}\\
    mg a \cos \alpha_0 &= \frac{1}{4} ma^2 \Omega_0^2 \sin \alpha_0 \cos \alpha_0\\
\Rightarrow \Omega_0 &= \boxed{2 \sqrt{\frac{g}{a \sin \alpha_0}}}.
\end{align}
$$

**b,** The total energy of the disk is given by 

$$
\begin{align}
        E &= m g a \sin \alpha_0 + \frac{1}{2} \frac{1}{4} m a^2 \omega_{tot}^2\\
        &=  m g a \sin \alpha_0 + \frac{1}{8} ma^2 \Omega^2_0 \sin^2 \alpha_0\\
        & = \boxed{\frac{3}{2} mg a \sin \alpha_0}.
\end{align}
$$

**c,** When the contact point of the disk passes a bump, the lost energy is $\Delta E = m g h $ in an interval of time $\displaystyle \Delta t = \frac{\delta}{v_p}$, in which $v_p = \Omega a \cos \alpha$ is the velocity of the contact point.

When the disk is falling down horizontally, we must take account the motion of the center of mass. 

The velocity of the COM is therefore

$$
\begin{align*}
     v_{COM} = \frac{d}{dt} (a \sin \alpha) = a\cos \alpha \frac{d\alpha}{dt} \approx a \dot{\alpha}.
\end{align*}
$$


Hence, we have the energy of the falling disk
$$
\begin{align*}
     E &= \frac{1}{2} m v^2_{COM} + \frac{3}{2} mga \sin \alpha\\
     &\approx \frac{1}{2} m a^2 \dot{\alpha}^2 + \frac{3}{2} mga \alpha.
\end{align*}
$$

Consequently, we have the equation 

$$
\begin{align*}
     \frac{dE}{dt}& = \frac{d}{dt} \left(\frac{1}{2} m a^2 \dot{\alpha}^2 +\frac{3}{2} m g a \alpha \right) = - \frac{mgh}{\cfrac{\delta}{\Omega a \cos \alpha}}\\
    \frac{3}{2} mg a  \dot{\alpha} + ma^2 \dot{\alpha} \ddot{\alpha}&= - \frac{mgh}{\delta} \Omega a \cos \alpha.
\end{align*}
$$


Assuming the disk spends most of its time falling down from a bump, we can approximate its COM’s acceleration to be $a \dot{\alpha} \approx g$. Fully simplifying the equation above, we get:

$$
\begin{align}
         \Rightarrow \boxed{\dot{\alpha} =-\frac{4}{5} \frac{h}{\delta } \sqrt{\frac{g}{a \sin \alpha}} \approx - \frac{4 h}{5 \delta} \sqrt{\frac{g}{a}} \alpha^{-1/2}}. 
         \label{eq:test1}
\end{align}
$$

Note that $\sin \alpha \approx \alpha$ when $0<\alpha \ll 1$. 


**d,** Integrate the above differential equation, we can solve for $\alpha (t)$

$$
\begin{align}
       \int_{\alpha_0}^{\alpha(t)} \alpha^{1/2} d\alpha&= -\frac{4h}{5\delta}\sqrt{\frac{g}{a}} \int_{t_0}^{t} dt\\
       \frac{2}{3} \left(\alpha(t)^{3/2} - \alpha_0^{3/2} \right)& = -\frac{4h}{5\delta}\sqrt{\frac{g}{a}} (t-t_0)\\
       \Rightarrow \alpha(t)&=\alpha_0 \left[ 1 - \frac{6h}{5\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{2/3}.
\end{align}
$$

where $t_0$ is the initial moment of time.

Consequently, we can express $\Omega(t)$, which is given by

$$
\begin{align}
        \Omega(t) &= 2 \sqrt{\frac{g}{a \sin \alpha(t)}} \approx \boxed{2 \sqrt{\frac{g}{a \alpha_0}} \left[ 1 - \frac{6h}{5\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}}\\
        & = \Omega_0 \left[ 1 - \frac{6h}{5\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}.
\end{align}
$$

Easily see that $\Omega(t)$ approaches infinity while $\alpha(t)$ approaches zero. The time for the disk to completely settle down on the horizontal surface is $\displaystyle \tau = t_0+ \frac{5\delta \alpha_0^{3/2}}{6h} \sqrt{\frac{a}{g}}$.


**e,** Two consecutive collisions with two bumps will produce a single wavelength of sound. That means

\begin{equation}
 f = \frac{\Omega a \cos \alpha}{\delta} \approx \Omega \frac{a}{\delta} =  \frac{2}{\delta} \sqrt{\frac{ga}{ \alpha_0}}\left[ 1 - \frac{6h}{5\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}.
\end{equation}

Interval of time for the frequency of the sound the disk makes
against the surface to reach the maximum audible frequency $f_0$ is given by


\begin{equation}
    \boxed{\tau_0 = \frac{5\delta \alpha_0^{3/2}}{6 h } \sqrt{\frac{a}{g}} \left[ 1 - \left( \frac{2}{\delta f_0}\sqrt{\frac{ga}{\alpha_0}}\right)^3 \right]}.
\end{equation}




