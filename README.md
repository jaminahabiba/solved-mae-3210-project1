Download Link: https://assignmentchef.com/product/solved-mae-3210-project1
<br>
<ol>

 <li>Linear algebraic equations can arise in the solution of differential equations.For example, the following <em>heat equation </em>describes the equilibrium temperature <em>T </em>= <em>T</em>(<em>x</em>)(<sup>o</sup>C) at a point <em>x </em>(in meters m) along a long thin rod,</li>

</ol>

<em>,                                              </em>(1)

where <em>T<sub>a </sub></em>= 10<sup>o</sup>C denotes the temperature of the surrounding air, and <em>h</em><sup>0 </sup>= 0<em>.</em>03(m<sup>−2</sup>) is a heat transfer coefficient. Assume that the rod is 10 meters long (i.e. 0 ≤ <em>x </em>≤ 10) and has boundary conditions imposed at its ends given by <em>T</em>(0) = 20<sup>o</sup>C and <em>T</em>(10) = 100<sup>o</sup>C.

<ul>

 <li>Using standard ODE methods, which you do not need to repeat here, thegeneral form of an analytic solution to (1) can be derived as</li>

</ul>

<em>T</em>(<em>x</em>) = <em>A </em>+ <em>Be<sup>λx </sup></em>+ <em>Ce</em><sup>−<em>λx</em></sup><em>,                                       </em>(2)

where <em>A</em>, <em>B</em>, <em>C</em>, and <em>λ </em>are constants. Plug the solution of type (2) into both sides of equation (1). This should give you an equation that must be satisfied for all values of <em>x</em>, for 0 ≤ <em>x </em>≤ 10, for some fixed constants <em>A</em>, <em>B</em>, <em>C</em>, and <em>λ</em>. Analyze this conclusion to determine what the values of <em>A </em>and <em>λ </em>must be.

<ul>

 <li>Next, impose the boundary conditions <em>T</em>(0) = 20<sup>o</sup>C and <em>T</em>(10) = 100<sup>o</sup>C to derive a system of 2 linear algebraic equations for <em>B </em>and <em>C</em>. Provide the system of two equations you have derived.</li>

 <li>Use one of the numerical algorithms you developed for homework 3 (Gausselimination <em>or </em>LU decomposition) to solve the algebraic system you derived in question 2(b) above, and obtain an <em>analytic solution </em>to (1) of the form (2). By <em>analytic solution </em>we mean an explicit solution to equation (1) which is valid for each <em>x </em>in the interval [0<em>,</em>10].</li>

 <li>Next we will discuss how to obtain a <em>numerical solution </em>to (1). That is, we will seek to obtain an approximate solution to (1) which describes the value of <em>T </em>at 9 intermediate points inside the interval [0<em>,</em>10]. More precisely, the equation (1) can be transformed into a linear algebraic system for the temperature at 9 interior points <em>T</em><sub>1 </sub>= <em>T</em>(1), <em>T</em><sub>2 </sub>= <em>T</em>(2), <em>T</em><sub>3 </sub>= <em>T</em>(3), <em>T</em><sub>4 </sub>= <em>T</em>(4), <em>T</em><sub>5 </sub>= <em>T</em>(5), <em>T</em><sub>6 </sub>= <em>T</em>(6), <em>T</em><sub>7 </sub>= <em>T</em>(7), <em>T</em><sub>8 </sub>= <em>T</em>(8), <em>T</em><sub>9 </sub>= <em>T</em>(9), by using the following finite difference approximation for the second derivative at the <em>i</em><sup>th </sup>interior point,</li>

</ul>

<em>,                                    </em>(3)

where 1 ≤ <em>i </em>≤ 9, <em>T</em><sub>0 </sub>= <em>T</em>(0) = 20<sup>o</sup>C, <em>T</em><sub>1</sub>0 = <em>T</em>(10) = 100<sup>o</sup>C, and ∆<em>x </em>is the equal spacing between consecutive interior points (i.e. with 9 equally spaced interior points inside [0<em>,</em>10] it holds that ∆<em>x </em>= 1). Use (3) to rewrite (1) as a system of 9 linear algebraic equations for the unknowns

<em>T</em><sub>1</sub><em>,T</em><sub>2</sub><em>,T</em><sub>3</sub><em>,T</em><sub>4</sub><em>,T</em><sub>5</sub><em>,T</em><sub>6</sub><em>,T</em><sub>7</sub><em>,T</em><sub>8</sub><em>, </em>and <em>T</em><sub>9</sub>. Provide the system of 9 equations you have derived.

<ul>

 <li>Use one of the numerical algorithms you developed for homework 3 (Gausselimination <em>or </em>LU decomposition) to solve the system derived in question 1(d) above. Validate your numerical solution by comparison to the analytic solution that you obtained in 1(c) through depicting the two solutions on plots over the interval 0 ≤ <em>x </em>≤ 10.</li>

 <li>Write a function that takes as input the number of interior nodes <em>n </em>desired for your numerical solution (i.e. <em>n </em>= 9 in 1(d) above), and outputs the numerical solution to (1) in the form of the interior node values <em>T</em><sub>1 </sub>= <em>T</em>(∆<em>x</em>), <em>T</em><sub>2 </sub>= <em>T</em>(2∆<em>x</em>)<em>,…</em>, <em>T<sub>n </sub></em>= <em>T</em>(<em>n</em>∆<em>x</em>).</li>

 <li>Produce and submit 4 plots that compare your analytic solution to (1) derived in question 2(b) to the numerical solution generated in question 2(f) for <em>n </em>= 1, <em>n </em>= 4, <em>n </em>= 9, and <em>n </em>= 19, respectively.</li>

</ul>

<ol start="2">

 <li>Develop an algorithm that uses the golden section search to locate the minimum of a given function. Rather than using the iterative stopping criteria we have previously implemented, design the algorithm to begin by determining the number of iterations <em>n </em>required to achieve a desired absolute error |<em>E<sub>a</sub></em>| (not a percentage), where the value for |<em>E<sub>a</sub></em>| is input by the user. You may gain insight by comparing this approach to a discussion regarding the bisection method on page 132 of the textbook. Test your algorithm by applying it to find the minimum of with initial guesses <em>x<sub>l </sub></em>= 1 and <em>x<sub>u </sub></em>= 5 and desired absolute error |<em>E<sub>a</sub></em>| = 0<em>.</em></li>

 <li>Given <em>f</em>(<em>x,y</em>) = 2<em>xy </em>+ 2<em>y </em>− 1<em>.</em>5<em>x</em><sup>2 </sup>− 2<em>y</em><sup>2</sup>,

  <ul>

   <li>Start with an initial guess of (<em>x</em><sub>0</sub><em>,y</em><sub>0</sub>) = (1<em>,</em>1) and determine (by hand is fine) two iterations of the steepest ascent method to maximize <em>f</em>(<em>x,y</em>).</li>

   <li>What point is the steepest ascent method converging towards? Justifyyour answer without computing any more iterations.</li>

  </ul></li>

</ol>