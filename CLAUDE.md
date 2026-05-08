# หอพักลุงฟุ้ง — Project Brief

## โปรเจคนี้คืออะไร
เว็บไซต์สำหรับหอพักลุงฟุ้ง — หอพักนักศึกษา 14 ห้อง ของ Nueng (Sutiwat Kumnerdwum)

## เว็บไซต์ออนไลน์ที่
https://nuengmvth.github.io/lung-fung-dorm/

## ไฟล์หลัก
- `index.html` — ไฟล์เดียว รวม HTML + CSS + JavaScript ทั้งหมด

## ข้อมูลสำคัญ
- **LINE OA**: `@2009932183` — ลิงก์: `https://line.me/R/ti/p/@2009932183`
- **ห้องทั้งหมด**: 14 ห้อง (ห้องพัดลม + ห้องแอร์)
- **เจ้าของ**: ลุงฟุ้ง (Nueng จัดการเอง)

## หน้าที่มีในเว็บ
1. หน้าหลัก (home)
2. ห้องว่าง (available) — grid 14 ห้อง พร้อม status badge
3. ห้องพัก & ราคา (rooms)
4. ข่าวสาร & บิล (news) — ค่าน้ำ ค่าไฟ ค่าห้อง
5. นัดชม (booking) — form → เปิด LINE OA พร้อมข้อความ
6. แจ้งซ่อม (maint) — form → เปิด LINE OA พร้อมข้อความ
7. ติดต่อ (contact)

## สิ่งที่ทำเสร็จแล้ว
- [x] UI ครบทุกหน้า
- [x] Grid ห้อง 14 ห้อง พร้อม lightbox รูปภาพ
- [x] LINE OA floating button
- [x] Form นัดชม + แจ้งซ่อม → ส่งข้อมูลผ่าน LINE OA อัตโนมัติ
- [x] Responsive mobile

## สิ่งที่ยังไม่ได้ทำ (Next Steps)
- [ ] เพิ่มรูปห้องจริง (ตอนนี้ใช้ emoji placeholder)
- [ ] เชื่อม Google Sheets สำหรับจัดการข้อมูลห้อง (config พร้อมแล้ว ใช้ `useSheets: false`)
- [ ] อัปเดตสถานะห้อง (ว่าง/ไม่ว่าง) ให้ตรงกับความเป็นจริง

## วิธี deploy
Push ขึ้น GitHub → เว็บอัปเดตอัตโนมัติใน 1-2 นาที
```cmd
git add index.html
git commit -m "อธิบายการเปลี่ยนแปลง"
git push
```

## Google Sheets (เปิดเมื่อพร้อม)
ใน `index.html` หา `SHEETS_CONFIG` แล้วเปลี่ยน:
- `useSheets: false` → `true`
- ใส่ Google Sheets ID ที่ต้องการ
