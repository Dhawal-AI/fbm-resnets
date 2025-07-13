# FBMResNet: Scaling and Stabilizing Deep Residual Networks with Fractional Brownian Motion

This project explores the theoretical and empirical behavior of deep residual networks (ResNets) initialized using fractional Brownian motion (fBm). Inspired by the work of Marion et al. (2022), we study how correlated weight structures and correction terms can improve stability and expressivity in the large-depth regime.

---

## 📚 Background

Standard ResNets often suffer from vanishing or exploding behavior as depth increases. Marion et al. show that:
- **i.i.d. weight initialization** requires scaling by \(1/\sqrt{L}\) to prevent collapse.
- **fBm-inspired correlated weights** offer a structured alternative, but become unstable for Hurst index \( H < 0.5 \) without correction.

To address this, we implement:
- fBm-based initialization across varying \( H \in (0,1) \),
- A mathematical **correction term** for \( H < 0.5 \),
- An optional **outer bias** term to improve generalization.

---

## 🧠 Features

- ✅ Scalar case analysis with full Taylor expansion of \(\log(1 + w)\)
- ✅ Validation of scaling regimes through simulations
- ✅ Replication of diffeomorphism approximation (2D & 3D) from the Fermanian et al. paper
- ✅ Custom FBMResNet model with correction term and bias
- ✅ Full CIFAR-10 classification experiments
- ✅ Heatmap sweeps over \( (H, \text{scaling}) \)


