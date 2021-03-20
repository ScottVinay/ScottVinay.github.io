---
layout: post
title:  "The mathematically best way to clean a water bottle"
date:   2020-05-05 12:33:47 +0100
last_modified_at: 2020-05-05
categories: general
sidebar: true
text: true
---

Who says they never use calculus in real life, eh?

<figure>
<img src="/assets/images/posts/clean_bottle/bottle.jpg" />
</figure>

Ok, so this is just a cool little application of calculus directed towards solving a very practical problem.

Suppose you have a water bottle that you drink out of every day. One night, you decide to fill it with whisky before heading out on the town. The next day, you want to drink water from it again, but even the slightest taste of whisky sends your head reeling. So you partially fill the bottle with water, give it a shake, and pour it out.

The question is this: how far up the bottle should you fill it before shaking it?

<figure>
<img src="/assets/images/posts/clean_bottle/waterbottle.png"/>
<figcaption></figcaption>
</figure>

Any residue at the top of the bottle will be dislodged by the water striking it.  The residue is held to the bottle by chemical bonds of some fixed energy. We  therefore want to maximise the kinetic energy of the water that strikes the top of the bottle. This is a function of both the mass of water ($ m_w $) and its velocity on impact ($v$). If you fill it up only a little bit, then $ m_w $ will be very small. However, if we fill it up almost all the way, then the water will not have very far in which to accelerate before stopping, so $v$ will be small. Clearly we need something in between.

Before we do this calculation, try to get an estimate of the answer. Grab a bottle and fill it up different amounts, say, by 1/4, by 1/3, by 1/2, by 2/3, etc, and give it a shake. See which one _feels_ like it is cleaning the bottle best. I've found that people's intuition on this question is right more often than not.

<br>

## Initial calculation

However, this is not the whole story. When the water collides with the top of the bottle, not all of its kinetic energy goes into breaking the chemical bonds in the residue. Much of it is transferred to the bottle and remains as kinetic energy. The actual energy available to break the bonds, $\Delta E$, is equal to the difference of the kinetic energy before the water collides with the bottle, $E_0$, and the kinetic energy of the water and bottle combined after the collision, $E_1$.

The before-energy is what we have already seen: $E_0 = m_w v_0^2 / 2$ (where $v_0$) is the velocity we calculated above of the water immediately before collision. The after-energy is then given by $E_1 = (m_w+m_b) v_1^2 / 2$, where $m_b$ is the mass of the bottle itself, and $v_1$ is the velocity of the water and bottle after the collision.

To find $v_1$, we can note that the momentum of the system before the collision, $p_0$, must equal the momentum after the collision, $p_1$. Since $p_0 = m_w v_0$ and $p_1 = (m_w + m_b) v_1$, we can say that

$v_1 = \frac{m_w}{m_w+m_b} v_0$.

Substituting this into our equation for $E_1$ we get 

$\Delta E = E_0 - E_1 = \frac{1}{2}v_0^2m\left( 1-\frac{m_w}{m_w+m_b} \right)$.

Plugging in our expressions for $v_0$ and $m_w$ in terms of x we get

$\Delta E = \rho a x (L - x) \frac{\bar{m}}{x+\bar{m}}$,

where $\bar{m} = m/\rho$ (with dimensions of length). Differentiating by x gets

$\frac{\partial \Delta E}{\partial x} = - \rho a \bar{m} \left(3 x^2 + 2 x \bar{m} - L \bar{m}\right)$.

<br>

## Results

We can solve the previous equation and find the value of x at which it equals zero to give the final optimal height to which we should fill our water bottle:

$x_\text{best} = \left(\sqrt{4\bar{m}^2 + 12 L \bar{m}}-2\bar{m}\right)/6$.

This is shown below for various values of $\bar{m}$ at L = 23.8 cm.

<figure>
<img src="/assets/images/posts/clean_bottle/graph.png"/>
</figure>

We can look at a specific example to get an estimate for $\bar{m}$. The 375 ml water bottle here has a height of 23.8 cm and a mass of 275 g. Recall that $\rho$ is the linear density of water, so we get it by taking the mass of 375 ml of water (375 g), and divide it by the height of the bottle. This gives a value of $\bar{m}$ of 0.1745, which gives an optimal value of x = 0.31 L.

Note that this is likely an under-estimate. After collision between the water and the bottle, the two do not move freely, they are resisted by the motion of your arm. This increases the effective mass of the bottle. The best way to clean a bottle is to fill it up more than a third of the way, but always less than a half before giving it a shake.  