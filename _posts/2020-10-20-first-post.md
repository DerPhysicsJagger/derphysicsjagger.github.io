---
layout: post
title: Euler's Disk
tags: first markdown example
categories: demo
---



**a** Choose $O$ of coordinate system is placed at the center of the disk. Consider in the rotating frame of reference with vertical angular velocity $\Omega_0$.

In this frame, there is only the rotating part $$\omega_x \hat{\vec{x}}$$ in order to fix the contact point. 

From the non-slipping condition we would have that
$$
    \Omega_0 a \cos \alpha_0 = - \omega_x a \Rightarrow \omega_x = -\Omega_0 \cos \alpha_0.
$$

Back to the laboratory frame, we will have the total angular velocity
$$
        \boldsymbol{\omega}_{tot} &= \Vec{\Omega}_0 + \boldsymbol{\omega}_x\\
        &=\Omega_0 (\sin \alpha_0 \hat{\Vec{z}} + \cos \alpha_0 \hat{\vec{x}}) - \Omega_0 \cos \alpha_0 \hat{\Vec{x}}\\
        &=\Omega_0 \sin \alpha_0 \hat{\vec{z}}.
$$

which lies on the plane of the disk and go through the contact point.

From the Euler's equation of precession, we have
$$
    \frac{d\vec{L}}{dt}  &= \vec{\Omega}_0 \times \vec{L}\\
    &=\vec{\Omega}_0 \times \frac{1}{4} ma^2 \Omega_0 \sin \alpha_0 \hat{\vec{z}}\\
    mg a \cos \alpha_0 &= \frac{1}{4} ma^2 \Omega_0^2 \sin \alpha_0 \cos \alpha_0\\
\Rightarrow \Omega_0 &= \boxed{2 \sqrt{\frac{g}{a \sin \alpha_0}}}.
$$

**b** The total energy of the disk is given by 
$$
        E &= m g a \sin \alpha_0 + \frac{1}{2} \frac{1}{4} m a^2 \omega_{tot}^2\\
        &=  m g a \sin \alpha_0 + \frac{1}{8} ma^2 \Omega^2_0 \sin^2 \alpha_0\\
        & = \boxed{\frac{3}{2} mg a \sin \alpha_0}.
$$

**c** When the contact point of the disk passes a bump, the lost energy is $$ \Delta E = M g h $$ in an interval of time $$\displaystyle \Delta t = \frac{\delta}{v_p}$$, in which $$v_p = \Omega a \cos \alpha$$ is the velocity of the contact point.

Consequently, we have the equation
$$
     \frac{dE}{dt}& = \frac{d}{dt} \left(\frac{3}{2} Mg a \sin \alpha \right) = - \frac{Mgh}{\cfrac{\delta}{\Omega a \cos \alpha}}\\
    \frac{3}{2} Mg a \cos \alpha \dot{\alpha} &= - \frac{Mgh}{\delta} \Omega a \cos \alpha.
$$

$$
         \Rightarrow \boxed{\dot{\alpha} =-\frac{4}{3} \frac{h}{\delta } \sqrt{\frac{g}{a \sin \alpha}} \approx - \frac{4 h}{3 \delta} \sqrt{\frac{g}{a}} \alpha^{-1/2}}. 
$$

Note that $$\sin \alpha \approx \alpha$$ when $$0<\alpha \ll 1$$.



**d** Integrate the above differential equation, we can solve for $\alpha (t)$
$$
       \int_{\alpha_0}^{\alpha(t)} \alpha^{1/2} d\alpha&= -\frac{4h}{3\delta}\sqrt{\frac{g}{a}} \int_{t_0}^{t} dt\\
       \frac{2}{3} \left(\alpha(t)^{3/2} - \alpha_0^{3/2} \right)& = -\frac{4h}{3\delta}\sqrt{\frac{g}{a}} (t-t_0)\\
       \Rightarrow \alpha(t)&=\alpha_0 \left[ 1 - \frac{2h}{\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{2/3}.
$$

where $$t_0$$ is the initial moment of time.

Consequently, we can express $$\Omega(t)$$, which is given by
$$
        \Omega(t) &= 2 \sqrt{\frac{g}{a \sin \alpha(t)}} \approx \boxed{2 \sqrt{\frac{g}{a \alpha_0}} \left[ 1 - \frac{2h}{\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}}\\
        & = \Omega_0 \left[ 1 - \frac{2h}{\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}.
$$

Easily see that $$\Omega(t)$$ approaches infinity while $$\alpha(t)$$ approaches zero. The time for the disk to completely settle down on the horizontal surface is $$\displaystyle \tau = t_0+ \frac{\delta \alpha_0^{3/2}}{2h} \sqrt{\frac{a}{g}}$$.


**e** Two consecutive collisions with two bumps will produce a single wavelength of sound. That means
$$
 f = \frac{\Omega a \cos \alpha}{\delta} \approx \Omega \frac{a}{\delta} =  \frac{2}{\delta} \sqrt{\frac{ga}{ \alpha_0}}\left[ 1 - \frac{2h}{\delta \alpha_0^{3/2}} \sqrt{\frac{g}{a}} (t-t_0) \right]^{-1/3}
$$

Interval of time for the frequency of the sound the disk makes
against the surface to reach the maximum audible frequency $$f_0$$ is given by
$$
    \boxed{\tau_0 = \frac{\delta \alpha_0^{3/2}}{2 h } \sqrt{\frac{a}{g}} \left[ 1 - \left( \frac{2}{\delta f_0}\sqrt{\frac{ga}{\alpha_0}}\right)^3 \right]}.
$$
