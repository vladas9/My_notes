---
Date: 2024-04-11
tags:
  - Math
---
### Reduction of Order
The reduction of order method is a technique used to find a second linearly independent solution to a second-order linear differential equation when one solution is already known. This method is particularly useful when solving homogeneous differential equations of the form:

$\Large a(t)y'' + b(t)y' + c(t)y = 0$

where $a(t)$, $b(t)$, and $c(t)$ are continuous functions of $t$.
#### Method:

1. **Given Solution**: Suppose we have one solution of the form $y_1(t)$

2. **Assume Second Solution**: We assume a second solution of the form $y_2(t) = v(t)y_1(t)$, where $v(t)$ is a function to be determined.
   
3. **Substitute into the Differential Equation**: Substitute $y_2(t)$ into the original differential equation, replacing $y$ with $v(t)y_1(t)$.
  
4. **Simplify**: Simplify the resulting equation by differentiation and substitution, obtaining a first-order differential equation involving only $v(t)$.
  
5. **Solve for $v(t)$**: Solve the simplified equation for $v(t)$.
  
6. **Integrate**: Integrate $v(t)$ to find $y_2(t)$.
  
7. **Form the General Solution**: Combine $y_1(t)$ and $y_2(t)$ to form the general solution of the original differential equation.

>[!example]
>$2t^2y'' +ty'-3y=0$
>I know that y = $t^{-1}$ is a solution
>Look for 2nd solution in the form
>$\quad y_2=v(t)y_1=v(t)t^{-1}$
>Now we can substitute it in the initial equation
> $\quad 2t^2(y_2'') + t(y_2')-3y = 0$
> And we obtain
>$\quad 2tv'' - 3v' =0$ 
>Let $w = v'$ =>
>$\quad 2tx'-3w = 0$ - Linear equation
>$\quad w = Ct^{3/2} = v'$
>$\quad v(t) = \int Ct^{3/2}dt = C\frac{2}{5}t^{5/2}+k$
>The easiest solution is
>$\quad C = \frac{5}{2}$ and $k=0$ => $v(t) = t^{5/2}$
>$\quad y_1 = \frac{1}{t}$ and    $y_2=t^{3/2}$
>And finally
>$\quad y(t) = C_1\frac{1}{t} + C_2t^{3/2}$

