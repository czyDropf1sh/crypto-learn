For a Non-native English speakers,section 1.1 is a little bit boring,so let's start with mathmatical part

###  Section 1.2. Divisibility and Greatest Common Divisors
 **1.6.** Let $a, b, c \in \mathbb{Z}$. Use the definition of divisibility to directly prove the following properties of divisibility. (This is Proposition 1.4.)

(a) If $a \mid b$ and $b \mid c$, then $a \mid c$.

(b) If $a\mid b$ and $b \mid a$, then $a = \pm b $.

(c) If \( a \mid b \) and \( a \mid c \), then \( a \mid (b + c) \) and \( a \mid (b - c) \).

For (a),if \(a \mid b\) so there exist a integer \(t \) that \(at = b\),samely,there is a integer \(g\) that \(bg=c\),so \(c=bg=atg\),both \(t,g\) are integer,so \(a\mid c\).

For (b),by \( a \mid b \) there is an integer \(k\) with \(b=ak\). By \( b \mid a \) there is an integer \(l\) that \(a=bl\).
Substitude \(b=ak\) into \(a=bl\) to get \(a=akl\) .
Hence \(a(kl-1)=0\).   If \(a=0\) then \(b=ak=0\) ,\(a=\pm b\).
If \(a \ne 0\) , then for \(a(kl-1)=0\) we can devide it by \(a\) then \(kl-1=0\),so \(kl=1\) ,since \(k,l\) are integer,so \((k,l)=(1,1)\) or \((k,l)=(-1,-1)\) ,so \(b=ak=-a\) or \(b=ak=a\).

For (c), we have \(b=ak\) and \(c=al\) for some integers \(k,l\),so 

\(b\pm c=a(k\pm l)\),
Both of \((b + c) \) and \((b - c) \) are divisible by \(a\),since \(k,l\) are integer.
 **1.7.** Use a calculator and the method described in Remark 1.9 to compute the
 following quotients and remainders.
 I 'd like to use a piece of python code to solve this excercise and excercise 1.8.
```python
dividend = int(input())
divisor = int(input())
quotient, remainder=divmod(dividend,divisor)
print(f"  {dividend} ÷ {divisor} = {quotient} ... {remainder}")
```
 **1.9.**Use the Euclidean algorithm to compute the following greatest common divisors.
 Let's implement this algo by our hand.
 ```python
 def gcd_euclid(a,b):
    a, b = abs(a), abs(b)
    while b != 0:
        a, b = b, a%b
    return a
x = int(input())
y = int(input())
print(gcd_euclid(x,y))
 ```
