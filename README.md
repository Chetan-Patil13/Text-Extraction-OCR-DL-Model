# 🚀 Drug Text Detection 💊  
**Automated Text Detection and Recognition with PaddleOCR**  

---

## 🧐 **Project Overview**  
Reading drug labels can be tricky due to:  
✅ Small text size  
✅ Poor lighting conditions  
✅ Faded or worn-out labels  

This project automates the extraction of text from drug labels using **Optical Character Recognition (OCR)**. The tool makes it easier to access critical information accurately and quickly, reducing human error and improving efficiency in both healthcare and other industries.  

This project will help in:  
✅ Improving patient safety by ensuring accurate medication information  
✅ Reducing manual effort in reading labels  
✅ Speeding up data extraction for automated systems  

---

## 🧠 **What is OCR?**  
**Optical Character Recognition (OCR)** is a technology that converts printed or handwritten text from images into machine-readable text. This allows you to:  
- Digitize physical documents  
- Make text searchable and editable  
- Automate data entry tasks  

---

## 🔎 **Why PaddleOCR?**  
PaddleOCR is an open-source OCR tool built on the PaddlePaddle deep learning framework. It's known for:  
✅ **Multi-language support** – Handles multiple languages and complex scripts  
✅ **High-speed processing** – Fast and optimized for both CPU and GPU  
✅ **Robust recognition** – Handles low-resolution and distorted text effectively  
✅ **Pre-trained models** – Ready-to-use models for real-world scenarios  

### 🔥 **Comparison with EasyOCR**  
| Feature | PaddleOCR | EasyOCR |
|---------|------------|---------|
| **Language Support** | Over 80 languages | Around 80 languages |
| **Performance** | Faster and more accurate for complex layouts | Simple and easy to set up |
| **Model Architecture** | DBNet + CRNN + CTC | CNN + LSTM |
| **Flexibility** | Highly customizable | Limited customization options |
| **Real-time Processing** | Optimized for real-time performance | Moderate real-time performance |

PaddleOCR is more suitable for handling complex layouts and low-resolution images, making it ideal for real-world applications like drug label text extraction.

---

## 🏆 **End-to-End Pipeline Summary**  
Here’s how the complete process works behind the scenes:

### 1. **Input Handling**  
- Load drug label images from the dataset  
- Preprocess the image (resize, normalize, adjust lighting)  

### 2. **Text Detection**  
- **Model:** DBNet  
- Detects the location of text in the image  
- Outputs bounding boxes around text regions  

### 3. **Text Recognition**  
- **Model:** CRNN with CTC Loss  
- Cropped text regions passed to CRNN  
- Recognizes and converts text into readable strings  

### 4. **Post-Processing**  
- Correct misaligned text  
- Remove low-confidence predictions  
- Clean and organize text output  

### 5. **Visualization**  
- Draw bounding boxes on the original image  
- Display extracted text alongside the image  

---

## 🧠 **Key Models Behind PaddleOCR**  
| Task | Model | Purpose |
|-------|-------|---------|
| **Text Detection** | DBNet (Differentiable Binarization Network) | Detects text regions at pixel level |
| **Text Recognition** | CRNN (Convolutional Recurrent Neural Network) + CTC Loss | Recognizes character sequences |
| **Angle Classification** | Lightweight CNN | Corrects rotated text |
| **Language Model** | LSTM-based | Improves accuracy for complex scripts |

---

## 🌍 **Use Cases**  
While this project focuses on drug label text extraction, similar techniques can be applied in other industries:  

### 💊 **Healthcare:**  
- Automating drug label reading  
- Pharmacy inventory automation  
- Patient safety and medication accuracy  

### 🏭 **Manufacturing:**  
- Reading serial numbers and barcodes on products  
- Automating quality checks on packaging  

### 📦 **Logistics:**  
- Scanning labels on shipping containers  
- Automating package sorting and tracking  

### 🔍 **Legal and Compliance:**  
- Extracting terms from contracts  
- Digitizing historical documents  

---

## 🏋️ **Learning Outcomes**  
Through this project, I have gained hands-on experience in:  
✅ Configuring and working with **PaddleOCR**  
✅ Understanding how **DBNet** and **CRNN** work together for detection and recognition  
✅ Preprocessing and handling real-world images  
✅ Automating text extraction for faster and more reliable results  
✅ Visualizing extracted text using bounding boxes  

---

## 🛠️ **Project Execution Steps**  
### 1. **Data Collection**  
- Collected drug label images from multiple sources  
- Ensured quality and diversity in the dataset  

### 2. **Model Setup**  
- Installed PaddleOCR and configured model parameters  
- Fine-tuned model for drug label characteristics  

### 3. **Processing and Extraction**  
- Ran the PaddleOCR pipeline for detection and recognition  
- Extracted text stored in structured format  

### 4. **Visualization**  
- Annotated the extracted text on the original image  
- Displayed confidence scores for each extracted text block  

---

## 📂 **Directory Structure**  
```
📁 Drug_Text_Detection
├── 📁 data                # Input images
├── 📁 models              # Trained models
├── 📁 scripts             # Code files
├── 📁 results             # Output images and text
└── README.md
```

---

## 🚀 **How to Run**  
1. **Clone the repository:**  
```bash
git clone https://github.com/your-repo/drug-text-detection.git
```

2. **Install dependencies:**  
```bash
pip install -r requirements.txt
```

3. **Run the script:**  
```bash
python detect_drug_text.py --input data/sample_image.jpg
```

4. **View Results:**  
- Extracted text stored in `/results`  
- Annotated image saved in `/results`  

---

## 🎯 **Future Scope**  
✔️ Improve recognition accuracy using domain-specific fine-tuning  
✔️ Add support for real-time video-based label extraction  
✔️ Build a web-based interface using Flask for wider accessibility  

---

## 🙌 **Contributions**  
Feel free to open a pull request or report issues to improve this project!  

---

## 🏆 **Acknowledgments**  
- [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)  
- Open-source community  

---

Would you like to tweak any sections or add more details? 😎
