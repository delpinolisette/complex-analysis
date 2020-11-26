# Problem 1
Find the images of :

(A) $[-1,1]\times[0,\pi]$ under the map $f(z)=e^z$

(B) $|z|=R$ under the map $f(z) = \frac{1}{z-R}$

(C) {$z \in \mathbb{C}$}



### Solution

(A) First, decompose the map $w = f(z) = e^z$ into two real functions, so $w = u(x,y)+iv(x,y)$ where $u,v \in \mathbb{R}$ 

Then $$w = u+iv = e^{z} = e^{x+iy} = e^xe^{iy} = e^x(cosy+isiny) = e^xcosy + ie^xsiny$$ by Eueler's formula. 
So the real part of $w$, $$u(x,y)=e^xcosy$$
The imaginary part of $w$, $$v(x,y)=e^xsiny$$
Since the rectangle looks like this:

(B) Notice $$|z| = R \Rightarrow |x+iy|=R \Rightarrow \sqrt{x^2 + y^2} = R$$ Then we get that $$x = \sqrt{R^2-y^2}$$ $$y = \sqrt{R^2-x^2}$$
and the map is then $$f(z) = \frac{1}{z-R} = \frac{1}{x+iy-R} = \frac{1}{\sqrt{R^2-y^2} +i\sqrt{R^2-x^2}-R}$$
