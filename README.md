# ลอยกระทงออนไลน์ 🪷

เลือกกระทง เขียนคำอธิษฐาน แตะน้ำเพื่อเลือกจุดลอย แล้วกด "ลอยเลย" — ทุกคนที่เปิดเว็บพร้อมกันจะเห็นกระทงของกันและกัน และเห็นจำนวนคนออนไลน์

## 1) ขึ้น GitHub Pages
1. สร้าง repo ใหม่ แล้วอัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้
2. Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save
3. เปิด `https://<username>.github.io/<repo>/`

(ถ้ายังไม่ตั้งค่า Firebase จะเป็นโหมดทดลอง เห็นเฉพาะกระทงจำลอง)

## 2) เปิดให้ทุกคนลอยร่วมกัน (Firebase ฟรี)
GitHub Pages เป็นเว็บ static จึงต้องใช้ฐานข้อมูล realtime ภายนอก:
1. https://console.firebase.google.com → Add project
2. Build → **Realtime Database** → Create database (เลือก asia-southeast1)
3. แท็บ **Rules** → วางเนื้อหาจาก `database.rules.json` → Publish
4. Project settings → Your apps → เพิ่ม Web app → คัดลอก `firebaseConfig` ไปใส่ใน `config.js`
5. commit แล้วรอ Pages อัปเดต

กระทงแต่ละอันลอยนาน 150 วินาที แล้วค่อยๆ หายไป (ปรับที่ `LIFE` ใน index.html)
