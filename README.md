# Ground State Energy Estimation using Variational Monte Carlo  

This project uses **Variational Monte Carlo (VMC)** with the **Metropolis algorithm** to estimate the ground-state energy of:  

- **Quantum Harmonic Oscillator**  
- **Hydrogen Atom**  

The variational parameter **α** is optimized to minimize the expectation value of the Hamiltonian, providing an approximation of the ground-state energy.
## Features  
- Uses **Metropolis algorithm** for Monte Carlo sampling  
- Computes **ground-state energy** for both systems  
- Optimizes **variational parameter α**  
- **Plots**:  
  - Energy vs. α  
  - Histogram of sampled positions  
- Outputs **table of α, energy, and variance**  
## How to Run  

### **Option 1: Jupyter Notebook**  
1. Download the `.ipynb` file.  
2. Open Jupyter Notebook.  
3. Run the cells in order.  

### **Option 2: Google Colab**  
1. Open [Google Colab](https://colab.research.google.com/).  
2. Click **"File" → "Upload Notebook"**.  
3. Select the `.ipynb` file.  
4. Run the cells.  
## Dependencies  
Ensure you have the following Python libraries installed:  
- NumPy  
- Matplotlib  

To install missing libraries, run:  
```bash
pip install numpy matplotlib

---

#### **5. Methodology**  
```markdown
## Methodology  

### **1. Harmonic Oscillator**  
- **Trial Wavefunction:**  
  - `ψ(x) ∝ exp(-α² x² / 2)`  

- **Energy Estimation:**  
  - `E(α) = α² + x² (1 - α⁴)`  

- **Metropolis Algorithm:**  
  - Samples position space using **ψ(x)²**  
  - Uses **random walk** with step size  

- **Variational Monte Carlo (VMC):**  
  - Runs Monte Carlo sampling  
  - Computes **mean energy** & **variance**  

---

### **2. Hydrogen Atom**  
- **Trial Wavefunction:**  
  - `ψ(r) ∝ α r exp(-α r)`  

- **Energy Estimation:**  
  - `E(α) = E(α) = (-α / 2) * (α - 2 / r) - 1 / r^1.1  

- **Metropolis Algorithm:**  
  - Samples **radial position space** using **ψ(r)²**  
  - Uses **random walk in 3D space**  

- **Variational Monte Carlo (VMC):**  
  - Computes **mean energy** & **variance**  
## Example Output  
### **Table of Variational Parameter, Energy, and Variance**  
#### *Harmonic Oscillator:*  
| α  | Energy  | Variance  |
|----|---------|----------|
| 0.5  | 2.0775  | 6.4109  |
| 0.6  | 1.5679  | 2.9694  |
| 0.7  | 1.2571  | 1.1671  |
| 0.8  | 1.0967  | 0.4237  |
| 0.9  | 1.0230  | 0.0889  |
| 1.0  | 1.0000  | 0.0000  |
| 1.1  | 1.0160  | 0.0752  |
| 1.2  | 1.0677  | 0.2753  |
| 1.3  | 1.1429  | 0.6115  |
| 1.4  | 1.2315  | 1.0516  |
| 1.5  | 1.3563  | 1.6077  |

---

### **Hydrogen Atom**
| α  | Energy  | Variance  |
|----|---------|----------|
| 0.5  | -0.3528  | 0.0970  |
| 0.6  | -0.4134  | 0.1803  |
| 0.7  | -0.4514  | 0.1877  |
| 0.8  | -0.4857  | 0.0826  |
| 0.9  | -0.5145  | 0.0837  |
| 1.0  | -0.5347  | 0.2319  |
| 1.1  | -0.5414  | 0.0695  |
| 1.2  | -0.5413  | 0.0615  |
| 1.3  | -0.5327  | 0.0671  |
| 1.4  | -0.5106  | 0.0534  |
| 1.5  | -0.4846  | 0.1240  |




#### *Hydrogen Atom:*  




## Notes  
- Results depend on **step size** and **sampling iterations**.  
- The optimal α is found by minimizing the energy**.  
- Hydrogen simulation runs in **3D**, while Harmonic Oscillator is **1D**.  






 

