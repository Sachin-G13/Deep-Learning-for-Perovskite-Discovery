# **Generating Novel Perovskite Structures using Deep Learning**

### **Overview**
This project applies **Variational Autoencoders (VAEs)** to generate novel **perovskite structures** for advanced materials discovery. The model is trained using crystal structure data obtained from the **Materials Project Database**, encoding high-dimensional perovskite data into a **low-dimensional latent space**. The trained model can generate new, potential perovskite materials with unique structural properties.

### **Project Workflow**
1. **Data Collection**  
   - Perovskite **CIF files** are obtained from the **Materials Project Database** using API queries.  
   - Features such as **atomic positions, atomic numbers, and statistical properties** are extracted.

2. **Data Preprocessing**  
   - Extracting **24 numerical features** from the perovskite structures.  
   - **Min-max normalization** is applied for feature scaling.  
   - Data is converted into **PyTorch tensors** for training.

3. **Variational Autoencoder (VAE) Architecture**
   - **Encoder**: Compresses input features into a **4D latent space**.  
   - **Reparameterization Trick**: Ensures smooth latent space sampling using Gaussian distributions.  
   - **Decoder**: Reconstructs crystal structures from latent representations.  
   - **Loss Function**: Uses a combination of **KL-divergence loss** and **Reconstruction loss**.

4. **Training the Model**  
   - The model is trained for **50 epochs** using a batch size of **32**.  
   - **Validation split of 20%** prevents overfitting.  
   - Loss trends are analyzed to ensure stable learning.

5. **Generating Novel Perovskite Structures**  
   - Novel perovskite structures are **sampled from the latent space**.  
   - Decoded outputs are visualized and compared with real structures.

---

### **Installation**
Ensure you have the required dependencies installed before running the code:

```bash
pip install pymatgen numpy torch matplotlib
```

You will also need an API key from the **Materials Project Database** to fetch perovskite structures.

---

### **Usage**
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/perovskite-VAE.git
   cd perovskite-VAE
   ```

2. Define your **API key** in the script:
   ```python
   API_KEY = "your_api_key_here"
   ```

---

### **Results**
- Encoded and decoded perovskite samples are **visualized** to compare structural similarity.
- **Loss plots** confirm model convergence and generalization.

---

### **Contributors**
- **Thejas Kasilingam**, IIT Kanpur  
- **Sachin Gaikwad**, IIT (BHU) Varanasi  

For any queries, feel free to reach out or open an issue!
