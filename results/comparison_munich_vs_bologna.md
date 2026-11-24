# Cross-City Comparative Evaluation: Munich vs. Bologna

| Evaluation Dimension | Munich (Bavarian Modern Grid) | Bologna (Piazza Maggiore Medieval Core) | Physical & Engineering Insight |
| :--- | :---: | :---: | :--- |
| **3D Urban Geometry** | Wide avenues, modern orthogonal blocks | Narrow medieval street canyons, porticoes, Piazza Maggiore open plaza | Deep shadowing in alleys; higher diffraction around historic stone corners. |
| **Building Material** | ITU Concrete / Glass | ITU Brick / Concrete ("Bologna la rossa") | Brick permittivity ($\epsilon_r=4.44$, $\sigma=0.01$) vs Concrete ($\epsilon_r=5.31$). |
| **Path Gain Dynamic Range** | 75.5 dB (Min: -134.9 dB, Max: -59.4 dB) | 69.3 dB (Min: -135.0 dB, Max: -65.6 dB) | Severe street canyon shadowing in Bologna accentuates the need for per-sample normalization. |
| **Multipath Ray Count (Median / Max)** | 21 / 136 rays | 36 / 158 rays | Richer multi-bounce reflection order in narrow Bologna alleys. |
| **Top-10 Angular Beams Energy** | 92.6% | 92.7% | Spatial sparsity in virtual DFT angular domain $\mathbf{H}_{\text{ang}}$. |

## Autoencoder Compression Performance (NMSE [dB])

| Model | Ratio (d) | Munich NMSE [dB] | Bologna NMSE [dB] | Delta (Bologna - Munich) |
| :--- | :---: | :---: | :---: | :---: |
| **2D-CNN** | 4× (d=32) | -13.85 dB | -10.08 dB | +3.77 dB |
| **2D-CNN** | 8× (d=16) | -9.25 dB | -8.33 dB | +0.92 dB |
| **2D-CNN** | 16× (d=8) | -7.11 dB | -6.45 dB | +0.66 dB |
| **MLP** | 4× (d=32) | -9.87 dB | -8.87 dB | +1.00 dB |
| **MLP** | 8× (d=16) | -9.03 dB | -7.37 dB | +1.66 dB |
| **MLP** | 16× (d=8) | -6.71 dB | -5.36 dB | +1.35 dB |
| **Linear PCA** | 4× (d=32) | -7.07 dB | -5.67 dB | +1.41 dB |
| **Linear PCA** | 8× (d=16) | -3.79 dB | -3.21 dB | +0.58 dB |
| **Linear PCA** | 16× (d=8) | -2.09 dB | -1.98 dB | +0.12 dB |
