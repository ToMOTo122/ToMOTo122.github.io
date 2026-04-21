# 📌 Research on Physics-Informed Neural Networks (PINNs)

## 🧠 Overview
This project focuses on the application and improvement of **Physics-Informed Neural Networks (PINNs)** for solving partial differential equations (PDEs). Unlike traditional data-driven models, PINNs incorporate physical laws directly into the training process, enabling better generalization and reduced dependency on labeled data.

## 🎯 Motivation
Classical numerical methods (e.g., FEM, FDM) often require fine discretization and high computational cost, especially for high-dimensional or complex systems. PINNs offer a promising alternative by:

- Embedding governing equations into loss functions
- Reducing reliance on large datasets
- Providing continuous and differentiable solutions

## ⚙️ Methodology

### 1. Problem Formulation
We consider PDEs of the form:

\[
\mathcal{N}[u(x)] = f(x), \quad x \in \Omega
\]

where:
- \( \mathcal{N} \) is a nonlinear differential operator
- \( u(x) \) is the unknown solution
- \( \Omega \) is the domain

### 2. PINN Framework
A neural network \( u_\theta(x) \) is used to approximate the solution. The loss function consists of:

- **Physics loss**: enforcing PDE constraints
- **Boundary loss**: satisfying boundary conditions
- **Data loss (optional)**: fitting observed data

\[
\mathcal{L} = \lambda_1 \mathcal{L}_{PDE} + \lambda_2 \mathcal{L}_{BC} + \lambda_3 \mathcal{L}_{data}
\]

### 3. Key Techniques
- Automatic differentiation for computing derivatives
- Adaptive loss weighting strategy
- Sampling strategies for collocation points

## 🚀 Contributions

- 🔹 Improved convergence stability through adaptive weighting
- 🔹 Enhanced accuracy on benchmark PDE problems
- 🔹 Systematic comparison with baseline PINN implementations
- 🔹 Experimental validation on datasets such as KdV

## 📊 Experimental Results

| Dataset / PDE | Metric | Baseline | Ours |
|--------------|--------|----------|------|
| Example PDE  | MSE    | 1e-3     | **5e-4** |
| Example PDE  | Error  | 2.1%     | **1.2%** |

> Results demonstrate consistent improvements in both accuracy and convergence speed.

## 🛠️ Tech Stack

- Python
- PyTorch / TensorFlow
- NumPy, SciPy
- Matplotlib for visualization

## 📎 Paper & Resources

- 📄 Paper: *Uncertainty-Aware Physics-Informed Neural Networks*
- 🔗 Code: *(add repo link here if applicable)*
- 📌 Related work: Deep learning for scientific computing, PDE solving, and neural operators

## 🔍 Future Work

- Extending to high-dimensional PDEs
- Combining PINNs with operator learning methods (e.g., DeepONet)
- Improving training efficiency and scalability

---

## 👤 Author
**Chenwen Wang**  
Undergraduate @ Southeast University  
Research Interests: Machine Learning, Unsupervised Learning, Scientific Computing
