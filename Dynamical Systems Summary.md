## Summary of Dynamical Systems Discussion

### Dynamical Systems
- **Open Dynamical System**: Systems influenced by external factors, lacking a complete world model.
- **Closed Dynamical System**: Models the complete dynamics internally, emphasized in Historical Consistent Neural Networks (HCNNs).

### Historical Consistent Neural Networks (HCNNs)
- Uses entire history as one training example without external inputs.
- Involves single learnable matrix A; avoids need for multiple matrices.
- **Architectural Teacher Forcing (ATF)**: Error-propagation technique that ensures consistent learning with one matrix, enhancing future predictions.

### Abridged HCNNs
- Limited memory length, at least double the forecast horizon.
- Utilizes Architectural Teacher Forcing for improved learning.

### Architectural Teacher Forcing
- Similar to ECNN, propagates errors from previous to future states, crucial for HCNN learning.
