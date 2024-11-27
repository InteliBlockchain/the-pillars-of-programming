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

Wtf? Well, floating point arithmetic can introduce tiny errors that can snowball into significant bugs, especially in finance applications like blockchain.

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

### Math as a tool
The key takeaway from this is that math should be a tool, not the end goal (unless you also want to be a mathematician). Embracing the power of mathematics to build better software, but never letting it overshadow the practical concerns of software development. Think like this: There is some sort of universal language that, over the course of thousands of years, has layed fundamental ideas on how to manipulate data and express logic in different ways. Now think like this: You have the power to take those ideas, take them out of the paper, put them on a computer, and extrapolate them into cool software. Some important math topics that every good software engineer should know:

#### Discrete Math
  - **Topics**: Logic, Set Theory, Combinatorics, Graph Theory, Algorithms, Number Theory, Proof Techniques, etc.
  - **Why**: It's pretty much de backbone of computer science. It deals with distinct and separate values, making it perfect for understanding how algorithms and data structures work, and lays the foundations of how logic works in general, and how you can read and understand math propositions.
  - **Applications**: Coding as a whole is pretty much discrete math in practice.
  - **Practical Considerations**: It's not that important of a topic to study by itself, since much of it is covered naturally by other topics of computer science, but it's important to be able to read math propositions, argue against them, and also make proofs of your own.
  - **Resources**: [Discrete Math and It's Applications - Kenneth H. Rosen](https://www.amazon.com/Discrete-Mathematics-Its-Applications-Seventh/dp/0073383090)
#### Linear Algebra
  - **Topics**: Vectors, Matrices, Eigenvalues, Vector Spaces, Linear Maps, etc.
  - **Why**: Linear Algebra was invented by mathematicians as a framework for working with data by transforming them in an abstract way, allowing for manipulations in data that can be represented by n-dimensions (which is the majority of real-world data).
  - **Applications**: Applications range from blockchain, quantum computing, data science, machine learning, computer graphics, video games programming, computer vision, networks, and so on.
  - **Practical Considerations**: Honestly, that's probably the most important topic on this list because of the huge amount of potention it lays. Any non trivial problem can probably be broken into the tools that linear algebra provides, hence why it's present pretty much everywhere in computation as a whole.
  - **Resources**: [Linear Algebra Done Right - Sheldon Axler](https://linear.axler.net/)
#### Probabilities and Statistics
  - **Topics**: Probability Theory, Random Variables, Distributions, Statistical Inference, etc.
  - **Why**: This topic is crucial for making sense of uncertainty and variability in data. They provide the mathematical foundations for reasoning about randomness and making data-driven decisions. They help you create models that make accurate predictions, measure the likelihood of outcomes, and test hypotheses.
  - **Applications**: Probabilities and Statistics are the foundation for machine learning and data science, I guess this says it all.
  - **Practical Considerations**: It's probably not the idea for you to become full-fledged statistician, but having a strong grasp of probability and statistical methods is a huge asset in computer science.
  - **Resources**: [Introduction to Probability - Dimitri P. Bertsekas and John N. Tsitsiklis](https://www.amazon.com/Introduction-Probability-Second-Dimitri-Bertsekas/dp/188652923X)

#### Calculus
  - **Topics**: Limits, Derivatives, Integrals, Series, Differencial Equations etc.
  - **Why**: Calculus provides tools for understanding change, motion, and the behavior of complex systems over time. It's a particularly great tool for optimizations, continuous modeling, and analysis, which are all core tasks in software development.
  - **Applications**: Calculus is key for tasks involving optimization (like finding the best parameters in a machine learning model), understanding rates of change (e.g., network latency or system load), and modeling real-world phenomena (such as physical simulations in gaming and graphics, or analyzing dynamic financial data). In blockchain, it can help optimize network performance and resource allocation.
  - **Practical Considerations**: It's not really important to become incredibly advanced in calculus. Having a firm grasp of the basics is probably all you'll ever need, which means Calculus I, II.
  - **Resources**: [Calculus - Michael Spivak](https://www.amazon.com/Calculus-Michael-Spivak/dp/0914098918)

#### Number Theory and Cryptography
  - **Topics**: Prime Numbers, Modular Arithmetic, Cryptographic Algorithms, Public-Key Cryptography, Hash Functions, etc.
  - **Why**: Number Theory forms the backbone of modern cryptography, you can now imagine how crucial this is for blockchain.
  - **Applications**: Number Theory and Cryptography are indispensable in cybersecurity, blockchain, and digital transactions. Applications range from encryption algorithms like RSA and Elliptic Curve Cryptography (ECC) to hashing functions used in blockchain to secure transaction data. Without these concepts, modern digital security—including secure internet transactions, blockchain, and data integrity—would be impossible.
  - **Practical Considerations**: Again, there is no need for you to become an expert on this topic, but understanding the basics can help you understand better cryptographic protocols.
  - **Resources**: [An Introduction to the Theory of Numbers - G.H. Hardy and E.M. Wright](https://www.amazon.com/Introduction-Theory-Numbers-G-H-Hardy/dp/0199219869), [Understanding Cryptography - Christof Paar and Jan Pelzl](https://www.amazon.com/Understanding-Cryptography-Textbook-Students-Practitioners/dp/3642041000)

## 2. Computer Networks

### What are Computer Networks?
At its core, a **computer network** is a collection of interconnected computers that can communicate with one another. It allows devices to exchange information and share resources seamlessly. Think of it as the nervous system of the digital world, where every device contributes to a global ecosystem.

### A Brief History
The concept of connecting the world began with a vision to unite people and machines, bridging gaps both geographically and socially. From ARPANET—the ancestor of today’s internet—to the social and economic phenomena we call globalization, computer networks have revolutionized communication. They’ve transformed how we share ideas, build relationships, and conduct business.

### This topic sounds very romantic: connect the world, provide information to everyone, CONNECT PEOPLE, but as a programmer. Why should I care about this?

Let’s face it: your application will likely run on some computer that needs to communicate with others, in many forms. Understanding computer networks isn't just a theoretical exercise—it directly impacts how you design, debug, and optimize your software. Here’s why it matters:

- **Connectivity**: Networks are the backbone of modern computing. Without them, distributed systems, cloud computing, and web applications wouldn’t exist.
- **Debugging**: A top-down understanding of network behavior helps troubleshoot latency issues, packet loss, or even unexpected application behavior.
- **Layered Design**: Networking follows a layered approach (like the OSI model), and understanding this helps you build efficient and secure systems.
- **Protocols**: Learning about protocols such as TCP/IP, HTTP, DNS, and even lower-level concepts like error detection, routing, and multiplexing can transform how you design communication between services.
- **Software Revolution**: Networks have sparked revolutions like CDMA in telecommunications, decentralized blockchain systems, and cloud-native applications, all of which redefine how systems are architected.
- **Security**: Secure communication channels protect sensitive data as it travels between nodes, a vital concern for modern applications.
- **Cloud Platforms**: Services like AWS, GCP, and Azure provide robust infrastructure for deploying and scaling distributed applications, those services are just classic Networks Admin's routine.

### The Fusion of Communication and Computer Networks
The fusion of communication technologies and computer networks has revolutionized modern system design, laying the groundwork for distributed systems, cloud platforms, and global connectivity. This integration enables applications to seamlessly scale across multiple devices and locations, leveraging protocols, wireless communication, and advanced networking infrastructure. Distributed systems, which rely on interconnected nodes to function as a cohesive whole, thrive in this environment, powering innovations like IoT, blockchain, and cloud-native architectures. By mastering the principles of networks and their synergy with communication technologies, developers gain the tools to build resilient, scalable, and interconnected systems that redefine the boundaries of what software can achieve in a hyper-connected world.
