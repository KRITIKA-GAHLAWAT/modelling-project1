
Rational Fractal Spline - Modeling Project
Overview
This project explores Rational Fractal Splines, a modern technique in fractal interpolation used for scientific data approximation. Unlike classical interpolation methods, fractal interpolation functions (FIFs) provide enhanced flexibility by incorporating scaling factors and shape parameters. This makes them highly adaptable for preserving shape properties such as monotonicity, positivity, and convexity in interpolated data.

Features
Fractal Interpolation Functions (FIFs): Uses iterated function systems (IFS) with rational cubic polynomials.
Shape Preservation: Ensures monotonicity, positivity, and convexity in the interpolated curve.
Automated Parameter Selection: Develops an optimized approach to compute scaling factors and shape parameters.
Applications: Useful in modeling real-world shapes such as mountain ranges, cloud profiles, and natural landscapes.
Mathematical Formulation
Given a dataset {(xi, fi)} with xi in ascending order, the interpolation function Fi(x, f) is defined using rational cubic polynomials:

𝐹
𝑖
(
𝑥
,
𝑓
)
=
𝛼
𝑖
𝑓
+
𝑝
𝑖
(
𝑥
)
𝑞
𝑖
(
𝑥
)
Fi(x,f)=αif+ 
qi(x)
pi(x)
​
 
where pi(x) and qi(x) are cubic polynomials ensuring shape preservation.

Derivative Conditions:
Boundary derivatives di are computed to maintain smooth transitions between interpolated segments.

𝑑
𝑖
=
∆
𝑖
ℎ
𝑖
−
1
+
∆
𝑖
−
1
ℎ
𝑖
ℎ
𝑖
+
ℎ
𝑖
−
1
,
where
∆
𝑖
=
𝑓
𝑖
+
1
−
𝑓
𝑖
𝑥
𝑖
+
1
−
𝑥
𝑖
di= 
hi+hi−1
∆ihi−1+∆i−1hi
​
 ,where∆i= 
xi+1−xi
fi+1−fi
​
 
Monotonicity-Preserving Conditions:
To ensure monotonicity, scaling factors αi and shape parameters vi, wi are chosen using:

𝛼
𝑖
∈
[
0
,
\mui
]
where
\mui
=
min
⁡
(
𝑎
𝑖
𝑑
𝑖
𝑑
1
,
𝑎
𝑖
𝑑
𝑖
+
1
𝑑
𝑛
,
𝑓
𝑖
+
1
−
𝑓
𝑖
𝑓
𝑛
−
𝑓
1
)
αi∈[0,\mui]where\mui=min( 
d1
aidi
​
 , 
dn
aidi+1
​
 , 
fn−f1
fi+1−fi
​
 )
Approach
Trial and Error: Manually tuning scaling and shape parameters.
Automated Method: A systematic approach to optimize parameter selection for shape preservation.
Conclusion
This project demonstrates how rational cubic FIFs can enhance interpolation by preserving critical shape properties. By defining mathematical conditions and optimizing parameters, FIFs provide a powerful tool for accurate data modeling.

