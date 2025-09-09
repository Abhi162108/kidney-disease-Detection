# Kidney Disease Detection

Our kidney disease detection system utilizes a fine-tuned **InceptionResNetV2 model** for comprehensive renal imaging analysis.

#### 🎯 Detection Categories
- **Kidney Cysts** - Fluid-filled sacs detection
- **Kidney Stones** - Mineral deposit identification
- **Kidney Tumors** - Benign and malignant growth detection
- **Normal Kidney** - Healthy tissue classification

#### 🔧 Technical Specifications
- **Base Architecture:** InceptionResNetV2
- **Input Resolution:** 244×244 pixels
- **Training Dataset:** Comprehensive kidney imaging dataset
- **Classification Output:** 4 categories with confidence scores

---
## 📈 Model Performance

| Model | Accuracy | 
|-------|----------|
| Kidney Disease Detection | 99.52% | 


---

### Model Training Pipeline

```mermaid
graph LR
    A[Raw Medical Images] --> B[Data Augmentation]
    B --> B1[Rotation]
    B --> B2[Scaling]
    B --> B3[Flipping]
    B --> B4[Brightness/Contrast]
    
    B1 --> C[Training Split]
    B2 --> C
    B3 --> C
    B4 --> C
    
    C --> D[80% Training]
    C --> E[10% Validation]
    C --> F[10% Testing]
    
    D --> G[Model Training]
    E --> G
    
    G --> H[Adam Optimizer]
    G --> I[Learning Rate Scheduling]
    G --> J[Regularization]
    
    J --> J1[Dropout]
    J --> J2[Batch Normalization]
    J --> J3[Early Stopping]
    
    H --> K[Model Evaluation]
    I --> K
    J1 --> K
    J2 --> K
    J3 --> K
    
    F --> K
    K --> L[Performance Metrics]
    L --> M[K-fold Cross Validation]
    M --> N[Final Model]
    
    style A fill:#0366d6,stroke:#0366d6,stroke-width:2px,color:#fff
    style G fill:#28a745,stroke:#28a745,stroke-width:2px,color:#fff
    style K fill:#fd7e14,stroke:#fd7e14,stroke-width:2px,color:#fff
    style N fill:#6f42c1,stroke:#6f42c1,stroke-width:2px,color:#fff
```

---
