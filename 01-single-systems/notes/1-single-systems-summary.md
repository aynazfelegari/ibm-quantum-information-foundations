# Lesson 1 Summary: Single Systems

## What is it?
This lesson covers the fundamental differences between classical information (bits) and quantum information (qubits) for a single system.

## Key Concepts

**1. Classical vs. Quantum State**
*   A **classical bit** is deterministic: it is either $0$ or $1$. Even if we use probabilities (like a 30% chance of 0 and 70% chance of 1), the underlying reality is definitely one or the other; we are just ignorant of which one.
*   A **quantum qubit** exists in a state represented by a vector (a `Statevector` in Qiskit). It can be in a superposition, mathematically written as $\alpha|0\rangle + \beta|1\rangle$.

**2. Measurement (The Born Rule)**
When we measure a quantum state, it "collapses" to a classical state. The probability of measuring $|0\rangle$ or $|1\rangle$ is given by the absolute square of its amplitude (e.g., $|\alpha|^2$ or $|\beta|^2$). 
*   **Rule:** The sum of the probabilities must equal $1$. This means the state vector must have a length (Euclidean norm) of exactly 1.

**3. Unitary Operators**
Because quantum states must always maintain a length of 1, the only operations we can apply to them (without measuring) are **Unitary operations**. 
*   Geometrically, these are rotations or reflections. 
*   In code, Qiskit uses the `Operator` class (matrices) or built-in gate functions (like `X`, `Y`, `Z`, `H`) to evolve the state.

## What confused me initially
*The distinction between classical probability (just not knowing the state) and quantum superposition (the state actually existing as a combination of both) takes time to wrap my head around. Phase (like the minus sign in the $|-\rangle$ state) has no classical equivalent.*

## Further Questions for Later
*   How do these state vectors scale when we add more qubits? (Looking forward to Lesson 2!)