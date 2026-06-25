# Thai SMS Scam Detection using Machine Learning

ระบบตรวจจับและจำแนกข้อความ SMS หลอกลวงภาษาไทย โดยการทำ Feature Engineering เพื่อจับพิรุธข้อความ Scam และเปรียบเทียบประสิทธิภาพของโมเดล Machine Learning 4 รูปแบบ

>  **Important Note:** เนื่องจาก Dataset และ Model Artifact ไม่ได้ถูกจัดเก็บไว้ใน Repository นี้ **ตัวโค้ดใน Colab Notebook จึงถูกบันทึกผลการรัน (Execution Outputs), กราฟ และตัวเลขประสิทธิภาพของโมเดลทั้งหมดไว้แล้วอย่างสมบูรณ์** สามารถเปิดดูเพื่อตรวจสอบ Logic การวิเคราะห์และผลลัพธ์ได้ทันทีครับ

---

## My Role & Responsibilities
ในโปรเจกต์นี้เป็นส่วนหนึ่งในชั้นเรียน ซึ่งผมใน notebook นี้มีแค่ส่วนที่ผมรับผิดชอบ ซึ่งผมทำในส่วน End-to-End ML Pipeline ทั้งหมด:
- **Data Preprocessing & Feature Engineering:** พัฒนาระบบตัดคำภาษาไทย (PyThaiNLP) คลีนข้อความ และสกัดฟีเจอร์เฉพาะกลุ่มข้อความหลอกลวง เช่น ลิงก์ย่อ (Short URLs), จำนวนเงิน, รหัส USSD และกลุ่มคำเร่งด่วน/คำสแกมเฉพาะ
- **Model Training & Evaluation:** พัฒนาและเปรียบเทียบโมเดล 4 รูปแบบ (Logistic Regression, Naive Bayes, Random Forest, และ Neural Network) บนอัตราส่วน Train:Test ที่หลากหลาย
- **Model Interpretability:** สร้างระบบวิเคราะห์เหตุผลเบื้องหลังคำทำนาย (Reasoning System) เพื่อแจกแจงออกมาเป็นเปอร์เซ็นต์ความเสี่ยง[cite: 1]

---

## Key Results & Insights
จากการทดลองเปรียบเทียบ โมเดล **Random Forest (Train/Test Split 80:20)** ให้ผลลัพธ์ที่ดีที่สุดในการตรวจจับข้อความสแกม:[cite: 1]

*   **Accuracy:** 93.94%[cite: 1]
*   **Scam F1-Score:** 0.9444[cite: 1]

*(สามารถเปิดดูตารางเปรียบเทียบของโมเดลอื่น ๆ, Confusion Matrix และระบบ Predict อธิบายเหตุผล ได้ในไฟล์ Notebook ข้อมูลทั้งหมดถูกเซฟ Output ไว้เรียบร้อยครับ)*[cite: 1]

---

## Tech Stack
- **Language:** Python
- **Libraries:** PyThaiNLP, Scikit-learn, Keras/TensorFlow, Pandas, NumPy[cite: 1]
