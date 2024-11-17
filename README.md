
## **MNIST Dataset Analysis**
This notebook is based on the course **INFO6105 @ NEU**.  
[Link to Colab Notebook](https://colab.research.google.com/drive/151YaTirqRd32BMCqB83Pc94aFFVk1-x3?usp=sharing)

---

### **Key Objectives**
1. **Understand the MNIST dataset**: A classic dataset for handwritten digit classification.
2. Perform various experiments to improve model performance and prevent overfitting.

---

### **Steps and Attempts**
#### **1. Split the Data**
- **Objective**: Divide the dataset into **training** and **validation** sets.
- **Why**: This allows us to evaluate the model's performance on unseen data during training.

---

#### **2. Monitor Metrics**
- Tracked **accuracy** and **loss** on both the training and validation sets during training.
- **Benefits**:
  - Helps identify if the model is learning effectively.
  - Reveals potential overfitting or underfitting trends.

---

#### **3. Early Stopping Callback**
- Added an **early stopping** mechanism to prevent overfitting.
- **How It Works**:
  - Stops training when the validation performance stops improving for a defined number of epochs.
- **Why It's Important**:
  - Saves computational resources.
  - Improves model generalization.

---

### **Batch Size Comparison**
#### **Smaller Batches**
- **Advantages**:
  - Faster weight updates.
  - Introduces more gradient noise, which can help escape local minima.
- **Disadvantages**:
  - Longer training time (more updates required).

#### **Larger Batches**
- **Advantages**:
  - Faster training per step.
  - Smoother gradients, leading to more stable optimization.
- **Disadvantages**:
  - Higher memory requirements.
  - May lead to weaker generalization (model overfits the training set).

---

### **Summary**
The experiments in this notebook highlight:
- The importance of monitoring metrics and applying **early stopping**.
- The trade-offs between batch sizes, where smaller batches may generalize better but require more updates, while larger batches are computationally efficient but may overfit.
