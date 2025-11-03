# 🧠 Deutsch Algorithm – Qiskit 2.x Implementation

This notebook demonstrates **Deutsch’s Algorithm** using **Qiskit 2.x**, compatible with the latest (2024–2025) versions.  
It determines whether a given single-bit function `f(x)` is **constant** or **balanced** using only one quantum query.

---

## 📘 Files

- **Qiskit_Deutsch.ipynb** – Main Jupyter Notebook implementing the Deutsch Algorithm.

---

## ⚙️ Requirements

Install the latest Qiskit environment:

```bash
pip install qiskit qiskit-aer
```

Run the notebook:
```bash
jupyter notebook Qiskit_Deutsch.ipynb
```

---

## ▶️ Usage

1. Open the notebook and locate:
   ```python
   function_type = 'balanced_1'
   ```
2. Change this variable to test other function types:
   - `'constant_0'`
   - `'constant_1'`
   - `'balanced_0'`
   - `'balanced_1'`
3. Run all cells and observe:
   - The circuit diagram  
   - Simulation output  
   - The conclusion (CONSTANT or BALANCED)

---

## 📊 Example Output

| Function Type | Measurement | Result     |
|----------------|-------------|-------------|
| constant_0     | `0`         | CONSTANT    |
| constant_1     | `0`         | CONSTANT    |
| balanced_0     | `1`         | BALANCED    |
| balanced_1     | `1`         | BALANCED    |

---

## 🧩 Concepts Demonstrated

- Quantum Superposition  
- Interference and Phase Cancellation  
- Oracle Function Construction  
- Quantum Speed-Up (1 query vs 2 classical queries)

---

## 🎯 Student Programming Tasks

Try the following tasks to deepen your understanding:

1. **Custom Oracle Design**  
   Modify the oracle to implement a new function `f(x) = x XOR 1`.  
   Verify whether it is detected as constant or balanced.

2. **Bloch Sphere Visualization**  
   After applying Hadamard and after the oracle, visualize states using:
   ```python
   from qiskit.visualization import plot_bloch_multivector
   plot_bloch_multivector(Statevector(qc))
   ```

3. **Deutsch–Jozsa Extension**  
   Extend this notebook to handle 2-qubit input functions and observe how the algorithm scales.

4. **Noise Impact**  
   Run the same circuit on `AerSimulator(noise_model=noise_model)` and analyze how quantum noise affects the final measurement.

5. **Compare Classical vs Quantum Queries**  
   Implement a classical function evaluator and compare the number of queries needed to classify the function type.
