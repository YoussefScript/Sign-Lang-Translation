# Hand Gesture Recognition System
# نظام التعرف على إشارات اليد

---

<img width="1586" height="786" alt="image" src="https://github.com/user-attachments/assets/d21eb633-04c0-421a-b009-9421757b06e7" />
<img width="1607" height="869" alt="image" src="https://github.com/user-attachments/assets/d1aef4da-1428-4395-a11c-d7ee6ada5897" />



## English Version

### Project Overview
This project is a **Hand Gesture Recognition System** that detects both **static (image-based) gestures** and **dynamic (video-based) gestures** in real-time using a webcam.  
It can be used for:  
- Device control  
- Interactive applications and games  
- Accessibility tools for special needs users  
- VR/AR interfaces  

---

### Features
- Detects **static hand gestures** using **TFLite KeyPointClassifier**  
- Detects **dynamic gestures (motions)** using an **LSTM model** trained on 30-frame sequences  
- Uses **MediaPipe Hands** to extract 21 landmarks per hand  
- Displays recognized gesture on screen in real-time  
- Auto-record gesture videos with **K key**  
- Auto-label videos using **number keys (0–9)**  
- Dynamic gestures have priority over static gestures in display  

---

### How to Use
1. Open **app.py** or the provided **EXE**  
2. Camera will open and start detecting gestures  
3. Controls:
   - `ESC` → exit camera  
   - `K` → record a 3-second gesture video  
   - `0–9` → select gesture label before recording  
4. Recorded videos are saved in `video_records/<gesture_name>/`  
5. Static gestures are predicted in real-time per frame  
6. Dynamic gestures are predicted using the last 30 frames  

---

### Training Dynamic Gestures
1. Save gesture videos in folders under `video_records/`  
2. Open **video_gesture_training.ipynb**  
3. Run all cells to train the **LSTM model**  
4. The trained model is saved as `video_gesture_lstm.h5`  

---

### Requirements
- Python 3.10 (if running app.py directly)  
- Libraries:
PyQt5==5.15.9
opencv-python==4.8.1.78
numpy==1.23.5
tensorflow==2.12.0
mediapipe==0.10.9
scikit-learn==1.2.2
pyttsx3==2.90
Pillow==9.5.0

markdown
Copy code
- Or run the provided **EXE**, which does **not require Python**  

---

### Notes
- EXE works on **Windows** without Python  
- The system combines **static and dynamic gestures** for real-time detection  
- Dynamic gestures require sequences of 30 frames for accurate prediction  
- CSV file can be used to add or modify gesture labels  

---

## النسخة العربية

### نظرة عامة على المشروع
هذا المشروع هو **نظام التعرف على إشارات اليد** ويكتشف كل من **الإشارات الثابتة (بالصور)** و **الإشارات المتحركة (من الفيديو)** بشكل لحظي باستخدام الكاميرا.  
يمكن استخدامه في:  
- التحكم بالأجهزة  
- التطبيقات التفاعلية والألعاب  
- أدوات مساعدة لذوي الاحتياجات الخاصة  
- واجهات الواقع الافتراضي والمعزز  

---

### المميزات
- التعرف على **الإشارات الثابتة** باستخدام **TFLite KeyPointClassifier**  
- التعرف على **الإشارات المتحركة** باستخدام نموذج **LSTM** مدرب على تسلسل 30 إطار  
- استخراج 21 نقطة لكل يد باستخدام **MediaPipe Hands**  
- عرض الإشارة المكتشفة على الشاشة بشكل لحظي  
- تسجيل فيديوهات الإشارات تلقائيًا باستخدام زر **K**  
- اختيار تسمية الإشارة تلقائيًا باستخدام **أزرار الأرقام 0–9**  
- الإشارات المتحركة لها أولوية على الثابتة عند العرض  

---

### طريقة الاستخدام
1. افتح **app.py** أو ملف **EXE** المرفق  
2. ستفتح الكاميرا وتبدأ في التعرف على الإشارات  
3. التحكم:
 - `ESC` → لإغلاق الكاميرا  
 - `K` → لبدء تسجيل فيديو الإشارة (3 ثواني)  
 - `0–9` → لاختيار اسم الإشارة قبل التسجيل  
4. يتم حفظ الفيديوهات في `video_records/<gesture_name>/`  
5. التعرف على الإشارات الثابتة يتم لكل إطار  
6. التعرف على الإشارات المتحركة يتم باستخدام آخر 30 إطار  

---

### تدريب الإشارات المتحركة
1. احفظ الفيديوهات في مجلدات تحت `video_records/`  
2. افتح ملف **video_gesture_training.ipynb**  
3. شغل جميع الخلايا لتدريب نموذج **LSTM**  
4. سيتم حفظ النموذج باسم `video_gesture_lstm.h5`  

---

### المتطلبات
- Python 3.10 (إذا تم تشغيل app.py مباشرة)  
- المكتبات:
PyQt5==5.15.9
opencv-python==4.8.1.78
numpy==1.23.5
tensorflow==2.12.0
mediapipe==0.10.9
scikit-learn==1.2.2
pyttsx3==2.90
Pillow==9.5.0

yaml
Copy code
- أو تشغيل **EXE** مباشرة بدون الحاجة لتثبيت Python  

---

### ملاحظات هامة
- EXE يعمل على **Windows** بدون Python  
- يجمع النظام بين التعرف على الإشارات **الثابتة والمتغيرة** في الوقت الفعلي  
- الإشارات المتحركة تحتاج لتسلسل من 30 إطار للحصول على دقة عالية  
- يمكن تعديل أو إضافة تسميات الإشارات باستخدام CSV  

---

**جميع الحقوق محفوظة 2026 | برمجة يوسف عماد كامل**  
**All rights reserved 2026 | Developed by Youssef Emad Kamel**
