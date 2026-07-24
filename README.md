# DevOps Take-Home Exam — Candidate Package

แพ็กเกจนี้สำหรับผู้สมัครตำแหน่ง DevOps (Lexnetix Co., Ltd.)

## เริ่มต้น

1. อ่านโจทย์ทั้งหมดใน [`DevOps_TakeHome_Exam.md`](./DevOps_TakeHome_Exam.md)
2. ใช้โครงโฟลเดอร์ใน repo นี้เป็นจุดตั้งต้น (หรือแตก `devops-starter.zip` ถ้าต้องการ zip เดิม)
3. ทำงานตามข้อ 1–4 แล้ว push ขึ้น GitHub **public** ของคุณเอง
4. ส่งลิงก์ repo มาที่ **admin@lexnetix.co.th** ภายใน 5 วัน

---

# DevOps Take-Home — Starter Repo

โฟลเดอร์นี้คือจุดตั้งต้น ให้ push ขึ้น GitHub แบบ public แล้วทำงานต่อจากตรงนี้

## สิ่งที่ต้องแก้ก่อนส่ง

ไฟล์นี้ต้องถูกเขียนทับด้วย README ของคุณเอง โดยอย่างน้อยต้องมี

- สภาพแวดล้อมที่ใช้ (เวอร์ชัน minikube, kubectl, Docker, Jenkins)
- วิธีติดตั้งและรันตั้งแต่ศูนย์จนระบบทำงาน คนอ่านต้องทำตามได้โดยไม่ต้องถามคุณ
- วิธีติดตั้ง Jenkins ที่คุณใช้ plugin ที่ต้องลง และวิธีสร้าง job
- วิธี import `grafana/dashboard.json` กลับเข้า Grafana
- ค่า config หรือ credential ที่ต้องใส่เอง ใส่ตรงไหน (ใช้ค่าปลอมในไฟล์ตัวอย่างเท่านั้น)
- สรุปว่าทำข้อไหนบ้าง ข้อไหนไม่ได้ทำ

## โครงสร้าง

```
app/                 ซอร์สโค้ดแอปพลิเคชัน (ข้อ 1)
k8s/                 manifest (ข้อ 1)
Jenkinsfile          pipeline (ข้อ 2)
jenkins/             วิธีติดตั้ง Jenkins และไฟล์ประกอบ (ข้อ 2)
grafana/             dashboard.json และ config (ข้อ 3)
troubleshooting/     broken-stack.yaml ที่ให้มา และ fixed-stack.yaml ที่คุณแก้ (ข้อ 4)
docs/                คำตอบแต่ละข้อ
docs/images/         ภาพประกอบ
NOTES.md             ข้อจำกัด สิ่งที่ทำไม่ทัน เหตุผลของการตัดสินใจ
```

## ข้อควรระวัง

repo เป็น public ห้าม commit password, token, key หรือ kubeconfig จริง
ตรวจก่อน push ทุกครั้ง
