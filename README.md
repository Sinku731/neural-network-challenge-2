# neural-network-challenge-2

# Neural Network Challenge 2: HR Attrition & Department Prediction

## 📚 Background

This project builds a branched neural network to support HR decision-making by:
- Predicting employee attrition (whether an employee will leave).
- Recommending a more suitable department for current employees.

By leveraging deep learning, we aim to uncover hidden patterns in employee data that inform both retention and placement strategies.

---

## ⚙️ Technologies Used

- Python  
- Pandas / NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Google Colab  

---

## 🧪 Preprocessing Steps

1. **Imported & inspected data** using pandas.  
2. **Selected target columns**: `Attrition`, `Department`.  
3. **Chose 10 features** for input (X), excluding target columns.  
4. **Split data** into training and testing sets.  
5. **Encoded categorical features** with OneHotEncoder.  
6. **Scaled numeric data** using `StandardScaler`.  
7. **Prepared target labels** with one-hot encoding for both outputs.  

---

## 🧠 Neural Network Architecture

- **Input Layer**: Accepts 15 numeric features.  
- **Shared Hidden Layers**:  
  - Dense(128) → Dense(64) → Dense(32)  
- **Branch 1 (Department)**:  
  - Dense(16) → Dense(3, activation='softmax')  
- **Branch 2 (Attrition)**:  
  - Dense(16) → Dense(2, activation='softmax')  
- **Model Type**: Functional API with dual-output structure.  

---

## 📊 Performance Metrics

| Metric              | Training  | Validation | Test      |
|---------------------|-----------|------------|-----------|
| **Total Loss**      | 0.0108    | 4.7126     | 4.1778    |
| **Department Acc.** | 1.0000    | 0.5656     | 0.7908    |
| **Attrition Acc.**  | 1.0000    | 0.7738     | 0.5870    |

---

## 📝 Summary Questions

**1. Is accuracy the best metric to use?**  
Not always—accuracy may mislead if class imbalance exists. It may overestimate performance by favoring majority classes. F1-score or recall can offer a better picture in such cases.

**2. What activation functions did you use and why?**  
I used `softmax` for both outputs since they are classification problems. Softmax converts logits into class probabilities. It’s ideal for multi-class and binary categorical targets.

**3. How can the model be improved?**  
Use class balancing to handle skewed labels. Apply dropout or regularization to reduce overfitting. Tune hyperparameters or try more complex architectures for better performance.

---

## ✅ Requirements Checklist

### Preprocessing
- [x] Imported & explored data  
- [x] Created `y_df` with target columns  
- [x] Selected 10 feature columns for `X_df`  
- [x] Verified data types  
- [x] Split into train/test sets  
- [x] Encoded and scaled `X` data  
- [x] One-hot encoded `y` targets  

### Model
- [x] Found input feature count  
- [x] Created input layer  
- [x] Built shared hidden layers  
- [x] Built department branch  
- [x] Built attrition branch  
- [x] Compiled, trained, and evaluated model  

### Summary
- [x] Answered all questions  
- [x] Demonstrated understanding  


