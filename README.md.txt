# 🩺 Diabetes AI Predictor (Accuracy 92.02%)

ระบบพยากรณ์ความเสี่ยงโรคเบาหวานอัจฉริยะ พัฒนาด้วย Python และ Machine Learning โดยใช้ข้อมูลสุขภาพกว่า 100,000 ชุดข้อมูล เพื่อช่วยคัดกรองความเสี่ยงเบื้องต้นอย่างมีประสิทธิภาพ

## 🚀 Live Demo
https://diabetes-ndzgfk8lzrwddvgn4yzhqd.streamlit.app/

## 🧪 ข้อมูลทางเทคนิค (Model Insights)
โปรเจกต์นี้ผ่านกระบวนการ Data Science แบบครบวงจร:
- **Dataset:** วิเคราะห์ข้อมูลจากกลุ่มตัวอย่าง 100,000 ราย
- **Feature Selection:** ทำการลดจำนวนตัวแปรจาก 13+ ตัว เหลือเพียง 8 ตัวแปร "หัวกะทิ" (เช่น HbA1c, Glucose, BMI) โดยที่ความแม่นยำไม่ลดลง (Less is More)
- **Winning Model:** Gradient Boosting Classifier
- **Performance:** - Accuracy: **92.02%**
  - F1-Score: **0.9209**

## 💡 จุดเด่นของแอปพลิเคชัน
- **Dual Mode Support:**
  - 🟢 **Standard Mode:** สำหรับบุคคลทั่วไป ใช้เพียงข้อมูลทางกายภาพและพฤติกรรม
  - 🔵 **Advanced Mode:** สำหรับผู้ที่มีผลตรวจสุขภาพ (Lab) ให้ความแม่นยำระดับสูงสุด
- **Version Compatibility:** มีการใช้เทคนิค *Monkey Patching* เพื่อรองรับการทำงานของโมเดลข้ามเวอร์ชันของ Library (Scikit-learn)
- **Data Validation:** ระบบตรวจสอบความสมเหตุสมผลของข้อมูลก่อนประมวลผล (ป้องกันการกรอกค่าที่ผิดปกติ)

## 🛠️ เครื่องมือที่ใช้ (Tech Stack)
- **Language:** Python 3.13
- **Framework:** Streamlit (UI)
- **ML Libraries:** Scikit-learn, Pandas, Numpy, Joblib
- **Visualization:** Matplotlib, Seaborn

## 📦 วิธีการติดตั้งและรันในเครื่อง (Local Setup)
1. Clone repository นี้ลงเครื่อง
2. ติดตั้ง Library ที่จำเป็น:
   ```bash
   pip install -r requirements.txt