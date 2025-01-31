# Modifications and Additions to Ekera-Gartner Repository

For a comprehensive understanding of the general structure and functionality of the code, please refer to the original README provided by Ekerå and Gärtner. This README highlights only the modifications and additions made to the repository.

## Modified Files

### 1. `simulator_noisy-r.sage`
The following modification has been introduced:
- **`sample_error_model(R, m1, p, eta, verbose)`**:
  - Implements an advanced error model for simulating noise in quantum samples.
  - Samples can be corrupted either additively or replaced entirely with noise, based on a probability `p` and an error type parameter `eta`.
  - This addition provides greater flexibility in modeling real-world quantum noise and its impact on lattice-based postprocessing.

### 2. `factoring_error_model.sage`
A new function has been added:
- **`lattice_postprocessing(vectors, R, d, gamma, alpha, verbose)`**:
  - Implements a lattice-based postprocessing algorithm to select a subset of generated samples.
  - This function follows a structured procedure to refine noisy vectors and optimize the selection for further computations.

## Additional Script

### `Test_noise_selection.sage`
This script extends the functionality of the original `factoring.md` script. The following features have been added:
- **Large Number Factorization**:
  - Generates a large composite number \( N = p \cdot q \), where \( p \) and \( q \) are primes, and performs factorization using lattice-based methods.

- **Noise Analysis**:
  - Studies the impact of corrupted samples on the success rate of factorization by varying the corruption probability (`p`).

- **Comparison of Postprocessing Techniques**:
  - Compares the efficiency of the classical lattice postprocessing method with Ragavan's procedure for sample selection.

## Summary of Updates
These modifications introduce:
1. Advanced error modeling for simulating quantum noise.
2. Enhanced lattice postprocessing for refining sample selection.
3. Tools for analyzing the impact of noise on factorization performance and comparing different postprocessing strategies.

These updates provide a more robust framework for experimenting with and analyzing quantum algorithms in noisy environments.

