# The pillars
My dear reader, welcome to the cornerstone of your programming enlightenment--or whatever semblance of it you'll achieve after wading through this chapter. Here, we dissect the four almighty pillars that hold up the shaky (very shaky) roof of the world: **Mathematics**, **Computer Networks**, **Algorithms & Data Structures** and **Operating Systems**. And yes, don't you worry, we'll tell you where blockchain fits into all this

## 1. Mathematics - The Nerdy Language of Computers
### Why Math Matters (Even If You Think It Doesn't)
Here's the thing: Math is everywhere. From the algorithms that sort your data to the cryptographic protocols securing blockchain transactions, and even your CRUD apps (actually, probably not). The very term "compute" is derived from "count", underscoring the deep-rooted connection between mathematics and computing, and some would even argue that computer science is a branch of mathematics. In fact, early computer science pioneers were essentially mathematicians, people like Alan Turing, Ada Lovelace and Donald Knuth (the goat), the grandmaster who wrote *The Art of Computer Programming*, whose work laid the mathematical foundations for algorithms and data structures, compilers, and much, much more.

### Computing -- A Less Fancy Version Of Math
At it's core, computer science is just mathematics applied to solve real-world problems. While mathematicians might argue about abstract concepts, such as infinity, computer scientists take those concepts and turn them into tangible solutions, bound to the computer's capabilities. Topics like boolean algebra, discrete math, calculus, linear algebra, probabilites & statistics are great examples of math topics that sustain the computer science world.

### When Math Meets Reality
Math is unforgiving, as it operates on universal axioms and elegent theories that don't give a single **** about the messy, unpredictable world. Translating the pristine mathematical concepts into actual code is where lies the fun and frustration, for as much as math demands precision, computers demand practicality

### Math vs Code
> "Talk is cheap. Show the Code" - Linus Torvalds

#### Simple Addition
*Mathematical Concept:* $C = A + B$

*In Code*:
```C
#include <stdio.h>

int main() {
    int A = 5;
    int B = 10;
    int C = A + B;
    printf("%d\n", C); // Prints 15
    return 0;
}
```

Simple addition maps directly to a single line of code. No surprises here, right? please agreee with me.

#### Floating-Point Precision
*Mathematical Concept:* $0.1 + 0.2 = 0.3$

*In Code*:
```C
#include <stdio.h>

int main() {
    double a = 0.1;
    double b = 0.2;
    double c = a + b;
    printf("%.20lf\n", c);  // Prints 0.30000000000000004441
    return 0;
}
```

Wtf? Well, floating point arithmetic can introduce tiny errors that can snowball into significant bugs, especially in finance applications like blockchain where
