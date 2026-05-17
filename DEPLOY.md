# คู่มือ Deploy ขึ้น Vercel

## ขั้นตอนที่ 1: ติดตั้ง Git (ถ้ายังไม่มี)
ดาวน์โหลดที่: https://git-scm.com/download/win

## ขั้นตอนที่ 2: สร้าง GitHub Repository

1. ไปที่ https://github.com/new
2. ตั้งชื่อ: `thrcc-queue-system`
3. เลือก **Public**
4. กด **Create repository**

## ขั้นตอนที่ 3: Push โค้ดขึ้น GitHub

เปิด PowerShell ใน folder `queue-system (1)` แล้วรันคำสั่ง:

```powershell
git init
git add index.html vercel.json README.md
git commit -m "Initial: THRCC Queue System with localStorage history"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/thrcc-queue-system.git
git push -u origin main
```

> แก้ `YOUR_USERNAME` เป็น GitHub username ของคุณ

## ขั้นตอนที่ 4: Deploy บน Vercel

1. ไปที่ https://vercel.com
2. ล็อกอินด้วย GitHub
3. กด **"Add New Project"**
4. เลือก repository `thrcc-queue-system`
5. กด **Deploy**
6. รอ ~30 วินาที → ได้ URL เช่น `thrcc-queue-system.vercel.app`

## ขั้นตอนที่ 5: เสร็จแล้ว! 🎉

ระบบจะพร้อมใช้งานที่ URL ที่ Vercel ให้มา  
ทุกครั้งที่ push code ใหม่ → Vercel จะ deploy อัตโนมัติ

---

## ข้อมูลเกี่ยวกับประวัติ (localStorage)

- ข้อมูลเก็บอยู่ใน **browser** ของแต่ละเครื่อง
- ถ้าต้องการแชร์ข้อมูลระหว่างอุปกรณ์ ต้องใช้ database (Firebase/Supabase)
- ส่งออกเป็น CSV ได้เพื่อเก็บข้อมูล
