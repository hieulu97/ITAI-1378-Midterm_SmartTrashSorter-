# ITAI-1378-Midterm_SmartTrashSorter-

# Smart Trash Sorter

**Team Member:** Hieu Lu  
**Course:** ITAI 1378 – Computer Vision and AI  
**Project Tier:** Tier 2

---

## Tier Selection and Justification
**Tier 2:**  
This project involves model training, dataset handling, and potential real-time image classification. It goes beyond basic image recognition but remains achievable using Google Colab and open datasets. It’s practical, well-scoped, and can be implemented within the semester timeframe.

---

## Problem Statement
Improper waste sorting is a common issue in schools, cafés, and public spaces. People often throw recyclable or compostable items into the wrong bins, leading to contamination and increased disposal costs. Manual sorting is also labor-intensive and unhygienic.

---

## Solution Overview
Smart Trash Sorter uses a **camera-based computer vision model** to automatically classify waste items into **Recycle**, **Compost**, or **Trash** categories.  
Users can point the camera at an object, and the system provides a visual or on-screen indicator showing the correct bin. This can help improve recycling accuracy and reduce human sorting efforts.

---

## Technical Approach
- **Technique:** Image Classification  
- **Model:** MobileNetV3 (pre-trained and fine-tuned on waste images)  
- **Framework:** TensorFlow + TensorFlow Lite  
- **Justification:** MobileNetV3 offers high accuracy and low latency, suitable for real-time performance on Colab or embedded devices.

---

## Dataset Plan
- **Sources:**  
  - Roboflow’s *Waste Classification Dataset*  
  - Kaggle’s *TrashNet* Dataset ([https://www.kaggle.com/datasets/techsash/waste-classification-data](https://www.kaggle.com/datasets/techsash/waste-classification-data))
- **Size:** ~2,500 labeled images  
- **Labels:** Plastic, Paper, Metal, Glass, Compost, Trash  
- **Preparation Steps:**  
  - Clean and verify dataset quality  
  - Resize to 224×224 pixels  
  - Normalize pixel values  
  - Split into 80% training / 20% validation  

---

## Metrics
| Metric Type | Description | Target |
|--------------|--------------|---------|
| **Primary Metric** | Classification Accuracy | ≥ 90% |
| **Secondary Metric** | Inference Speed | ≤ 0.5 seconds per image |

---

## Week-by-Week Plan
| Week | Task | Milestone |
|------|------|------------|
| **10 (Oct 30)** | Collect and clean dataset | Dataset ready |
| **11 (Nov 6)** | Train MobileNetV3 model | Model working |
| **12 (Nov 13)** | Evaluate model and fine-tune | Accuracy ≥ 90% |
| **13 (Nov 20)** | Build Colab demo for image upload & prediction | Demo ready |
| **14 (Nov 27)** | Final testing and documentation | Submission ready |
| **15 (Dec 4)** | Present project | Presentation Day |

---

## Resources Needed
| Resource | Description |
|-----------|-------------|
| **Compute** | Google Colab GPU |
| **Frameworks** | TensorFlow, TensorFlow Lite |
| **APIs / Tools** | Roboflow (for labeling and augmentation) |
| **Estimated Cost** | $0 (free tier resources and public datasets) |

---

## Risks & Mitigation
| Risk | Probability | Mitigation Strategy |
|------|--------------|----------------------|
| Dataset imbalance | Medium | Apply augmentation (flip, rotate, brightness) |
| Low accuracy | Medium | Increase epochs or switch to ResNet-18 |
| Hardware limitations | High | Use Colab or skip embedded version |
| Poor lighting during image capture | Low | Apply brightness normalization |

---

📁 **Repository Structure**
```
SmartTrashSorter/
├── README.md
├── requirements.txt
├── notebooks/
│   └── 01_exploration.ipynb
├── data/
    └── proposal.pdf
```

---

✏️ **AI Usage Log**
| Tool | Purpose |
|------|----------|
| **Canva** | Drafted proposal slides design and structure |
| **Roboflow** | Dataset labeling and augmentation |
| **Google Colab** | Model training and testing environment |

---

✅ **Summary**
Smart Trash Sorter is a practical, environmentally meaningful project that uses deep learning to automate waste classification. It demonstrates applied computer vision skills while contributing to sustainability and efficiency.
