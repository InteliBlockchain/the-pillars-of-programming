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

#### Matrix multiplication
*Mathematical Concept:* $C = A \times B$

*In Code*:
```C
// C program to multiply two matrices
#include <stdio.h>
#include <stdlib.h>

// matrix dimensions so that we dont have to pass them as
// parametersmat1[R1][C1] and mat2[R2][C2]
#define R1 2 // number of rows in Matrix-1
#define C1 2 // number of columns in Matrix-1
#define R2 2 // number of rows in Matrix-2
#define C2 3 // number of columns in Matrix-2

void multiplyMatrix(int m1[][C1], int m2[][C2])
{
	int result[R1][C2];

	printf("Resultant Matrix is:\n");

	for (int i = 0; i < R1; i++) {
		for (int j = 0; j < C2; j++) {
			result[i][j] = 0;

			for (int k = 0; k < R2; k++) {
				result[i][j] += m1[i][k] * m2[k][j];
			}

			printf("%d\t", result[i][j]);
		}

		printf("\n");
	}
}

// Driver code
int main()
{
	// R1 = 4, C1 = 4 and R2 = 4, C2 = 4 (Update these
	// values in MACROs)
	int m1[R1][C1] = { { 1, 1 }, { 2, 2 } };

	int m2[R2][C2] = { { 1, 1, 1 }, { 2, 2, 2 } };

	// if coloumn of m1 not equal to rows of m2
	if (C1 != R2) {
		printf("The number of columns in Matrix-1 must be "
			"equal to the number of rows in "
			"Matrix-2\n");
		printf("Please update MACROs value according to "
			"your array dimension in "
			"#define section\n");

		exit(EXIT_FAILURE);
	}

	// Function call
	multiplyMatrix(m1, m2);

	return 0;
}
```

Well, as you can see, in math, we can just say that $A$ and $B$ are both matrices, write a little multiplication symbol and boom, done. We don't have to write any sort of detailed explanation as to how we should multiply anything, just declare it and we gucci boyz. Well in code, if you're not using something like [NumPy](https://numpy.org/), you're probably in for some pain in the ass. This is a great example where understanding math is a lot more simple than code.
