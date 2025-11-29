Quantum Harmonic Oscillator — Numerical Solver (Python)

This project numerically solves the time-independent Schrödinger equation for the 1D quantum harmonic oscillator using a finite-difference Hamiltonian and diagonalization via scipy.linalg.eigh.
It computes and plots the lowest energy eigenstates and their corresponding wavefunctions.


Physics Background

The quantum harmonic oscillator is governed by:
$$ \hat{H}\psi(x) = E\psi(x) $$

with Hamiltonian:
$$ \hat{H} = -\frac{\hbar^2}{2m} \frac{d^2}{dx^2} + \frac{1}{2} m\Omega^2 x^2 $$

Energy eigenvalues (analytic solution):
$$ E_n = \hbar\Omega \left(n + \frac{1}{2}\right) $$
This project numerically reconstructs these eigenvalues and eigenstates by converting the Hamiltonian into a matrix form and solving the matrix eigenvalue problem.

Numerical Method:
1.	Create a spatial domain { -x_max to x_main} with N grid points.
2.	Approximate the second derivative with a finite difference tridiagonal matrix.
3.	Construct:
  •	Kinetic energy matrix KE
	•	Potential energy matrix PE
	•	Hamiltonian H = KE + PE
4.	Diagonalize H to obtain:
	•	Eigenvalues (energy levels)
	•	Eigenvectors (wavefunctions)
5.	Normalize each wavefunction.
6.	Plot the lowest few eigenstates.

  Output

The script produces a plot of:
	•	Ground state wavefunction ψ₀
	•	First excited state ψ₁
	•	Second excited state ψ₂
	•	Third excited state ψ₃

All plotted over the spatial coordinate x.

These show the characteristic node structure:
	•	ψ₀ has 0 nodes
	•	ψ₁ has 1 node
	•	ψ₂ has 2 nodes
	•	ψ₃ has 3 nodes

matching the analytic solution.

Dependencies:
install all required libraries:
pip install numpy scipy matplotlib

How to run:
python3 main.py

License:
This project is licensed under the MIT license.

Author
Sapun Sunar.
