🩺 Diabetes AI Predictor (ระบบวิเคราะห์ความเสี่ยงเบาหวานอัจฉริยะ)

ระบบคัดกรองความเสี่ยงโรคเบาหวานเบื้องต้นที่ใช้พลังของ Machine Learning ในการวิเคราะห์ข้อมูลสุขภาพกว่า 100,000 ชุดข้อมูล เพื่อให้ผลลัพธ์ที่รวดเร็วและแม่นยำสูงสุดถึง 85.52% ## 🔗 Live Demo
สามารถเข้าใช้งานแอปพลิเคชันได้ที่: https://diabetes-ndzgfk8lzrwddvgn4yzhqd.streamlit.app/

🌟 จุดเด่นของโปรเจค (Project Highlights)

โปรเจคนี้ไม่ได้เป็นเพียงแค่โมเดลทำนายผล แต่ผ่านการออกแบบโดยคำนึงถึง User Experience (UX) และ Medical Context อย่างลึกซึ้ง:

🟢 Dual-Mode Flexibility:

Standard Mode: สำหรับบุคคลทั่วไป ใช้เพียงข้อมูลพื้นฐาน (อายุ, BMI, การออกกำลังกาย)

Advanced Mode: สำหรับผู้ที่มีผลตรวจ Lab (HbA1c, Glucose, LDL) ให้ความแม่นยำระดับ Clinical Grade

🧠 Intelligent Model Selection:

ใช้ Gradient Boosting Classifier สำหรับโหมดมาตรฐาน เพื่อรีดประสิทธิภาพค่า Recall ให้สูงที่สุด

ใช้ SVM (Calibrated) สำหรับโหมดเชิงลึก เพื่อความเสถียรในการแยกแยะข้อมูลทางการแพทย์

⚖️ Risk Score Normalization: ระบบปรับสเกลเปอร์เซ็นต์ความเสี่ยงให้สมจริง (1-99%) เพื่อลดความคลาดเคลื่อนทางสถิติและช่วยให้ผู้ใช้เข้าใจสถานะสุขภาพได้ง่ายขึ้น

🛠️ Technical Robustness: มีการทำ Monkey Patching เพื่อแก้ปัญหาความเข้ากันได้ของเวอร์ชัน Library (Scikit-learn) มั่นใจได้ว่าแอปจะทำงานได้เสถียรบนคลาวด์

🧪 ข้อมูลทางเทคนิค (Model & Data Science)

📊 Dataset Insight

วิเคราะห์จากกลุ่มตัวอย่างขนาดใหญ่ 100,000 ราย ผ่านกระบวนการเตรียมข้อมูล (Preprocessing) ดังนี้:

Outlier Handling: จัดการค่าผิดปกติในส่วนของ Glucose และ Blood Pressure

Feature Engineering: ลดจำนวนตัวแปรจาก 13+ ตัว เหลือเพียง 8 ตัวแปร "หัวกะทิ" (High Correlation) เช่น HbA1c และ Glucose

Standardization: ใช้ StandardScaler ภายใน Pipeline เพื่อป้องกัน Data Leakage

📈 Performance Metrics

Metric

Standard Mode (GB)

Advanced Mode (SVM)

Accuracy

61.%

85.52%

Recall (Sensitivity)

89.00%

F1-Score

0.62

0.5561

📁 โครงสร้างไฟล์ (Repository Structure)

├── app.py                # ไฟล์หลักสำหรับ Streamlit Application (UI & Logic)
├── เบาหวานมั้ยนะ.ipynb	      # Jupyter Notebook สำหรับ EDA และ Model Training
├──  standard.pkl              # โมเดล Gradient Boosting (3 Features)
├──  advanced.pkl              # โมเดล SVM (8 Features)
├── requirements.txt      # รายการ Library ที่จำเป็นต้องใช้
└── README.md             # เอกสารอธิบายโปรเจค


🚀 วิธีการติดตั้งและรันบนเครื่องของคุณ (Installation)

Clone Repository:

git clone [https://github.com/yourusername/diabetes-ai-predictor.git](https://github.com/yourusername/diabetes-ai-predictor.git)
cd diabetes-ai-predictor


สร้าง Virtual Environment (แนะนำ):

python -m venv venv
source venv/bin/activate  # สำหรับ Windows ใช้: venv\Scripts\activate


ติดตั้ง Libraries:

pip install -r requirements.txt


เริ่มการทำงาน:

streamlit run app.py หรือ python -m streamlit run app.py


🏥 ข้อจำกัดความรับผิดชอบ (Disclaimer)

แอปพลิเคชันนี้พัฒนาขึ้นเพื่อการคัดกรองความเสี่ยงเบื้องต้นเท่านั้น ผลลัพธ์ที่ได้ไม่ใช่การวินิจฉัยทางการแพทย์ โปรดปรึกษาแพทย์ผู้เชี่ยวชาญหากท่านมีความกังวลเกี่ยวกับสุขภาพ หรือมีอาการผิดปกติเกิดขึ้น

โปรเจคนี้พัฒนาขึ้นเพื่อเป็นส่วนหนึ่งของวิชา Data Science & Machine Learning Deployment