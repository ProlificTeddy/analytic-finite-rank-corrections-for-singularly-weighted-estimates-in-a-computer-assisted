# Analytic Finite-Rank Corrections for Singularly Weighted Estimates

[![Paper](https://img.shields.io/badge/Paper-arXiv%3A2607.15256v1-B31B1B.svg)](https://arxiv.org/pdf/2607.15256v1)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This repository provides a Python implementation of the methods described in the paper **"Analytic finite-rank corrections for singularly weighted estimates in a computer-assisted proof of 3D Euler singularity"** by Jiajie Chen and Thomas Y. Hou. The implementation focuses on the analytic low-rank correction method for enforcing vanishing conditions in singularly weighted energy estimates, as well as its application to the stability analysis of approximate solutions to the 3D Euler equations.

---

## 📜 Paper Overview

The paper addresses a critical challenge in computer-assisted proofs of singularity formation in fluid equations, particularly the 3D Euler equations. These proofs often rely on weighted energy estimates with singular weights near the singularity. However, such estimates require exact local vanishing conditions, which are not automatically preserved by the governing equations or numerical approximations.

To overcome this, the authors propose an **analytic finite-rank correction method** that:
1. **Numerically constructs approximate profiles** with coefficients, rigorous bounds, and low-order defect modes in a global basis representation.
2. **Enforces vanishing conditions analytically** using low-rank corrections derived from Taylor expansions of relevant quantities.

This approach ensures that the required vanishing conditions are satisfied, enabling robust stability analysis for singular solutions of nonlocal partial differential equations (PDEs).

### Key Contributions
- **Singularly Weighted Estimates**: A review of the role of singular weights and vanishing conditions in stability arguments for the 3D Euler equations.
- **Finite-Rank Correction Principle**: A simplified formulation of the analytic correction method using Taylor expansions.
- **Broader Applicability**: Discussion of the method's potential for other nonlocal PDEs and computer-assisted proofs.

---

## 🚀 How It Works

The implementation in this repository focuses on the core computational aspects of the paper, including the following components:

1. **Weighted Energy Norms**:
   - Implements singularly weighted norms that are critical for stability analysis near the singularity.
   - Computes the weighted energy of perturbations around numerically constructed profiles.

2. **Finite-Rank Corrections**:
   - Derives low-rank corrections to enforce vanishing conditions using Taylor expansions.
   - Ensures that the residual error in approximate solutions is minimized.

3. **Numerical Approximation**:
   - Constructs approximate space-time solutions and stream functions in a global basis.
   - Calculates coefficients and defect modes for stability analysis.

4. **Validation**:
   - Verifies the corrected profiles against the theoretical vanishing conditions.
   - Demonstrates the effectiveness of the corrections in reducing residual errors.

---

## 🛠️ Usage Instructions

### Prerequisites

- Python 3.8 or higher
- Required Python packages (install via `requirements.txt`):
  ```
  numpy
  scipy
  matplotlib
  sympy
  ```

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/finite-rank-corrections.git
   cd finite-rank-corrections
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Implementation

The main script for the implementation is `implementation.py`. To execute the script, run:
```bash
python implementation.py
```

### Script Overview

The script performs the following steps:
1. **Setup**:
   - Defines the singular weights and basis functions.
   - Initializes the numerical approximation of the profile.
2. **Finite-Rank Correction**:
   - Computes Taylor expansions for the correction terms.
   - Applies corrections to enforce vanishing conditions.
3. **Validation**:
   - Evaluates the corrected profile against the required conditions.
   - Plots the residual error before and after correction.

### Example Output

After running the script, you should see:
- **Plots**: Visualizations of the residual error and corrected profiles.
- **Logs**: Numerical values of the residual error and validation metrics.

---

## 📂 Repository Structure

```
finite-rank-corrections/
│
├── implementation.py       # Main Python script implementing the method
├── requirements.txt        # Required Python packages
├── LICENSE                 # License file
├── README.md               # Project documentation
└── examples/               # Example configurations and test cases
    ├── example1.py
    └── example2.py
```

---

## 📖 References

1. Jiajie Chen, Thomas Y. Hou. *Analytic finite-rank corrections for singularly weighted estimates in a computer-assisted proof of 3D Euler singularity*. [arXiv:2607.15256v1](https://arxiv.org/pdf/2607.15256v1).
2. ChenHou2023a, ChenHou2023b. Referenced works in the paper for the development of the analytic correction method.

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improving the implementation or extending its functionality, feel free to open an issue or submit a pull request.

---

## 📬 Contact

For questions or feedback, please contact the repository maintainer at [your.email@example.com].