# BetterTrade 2026 — Persona Ranking Display

หน้าจอ 1920×1080 แสดงอันดับตัวตนนักลงทุน (12 persona) ว่าลูกค้าในงานได้ตัวตนไหนมากที่สุด

## ใช้งาน
- เปิด `index.html` ผ่าน web server (เช่น GitHub Pages, Vercel หรือ `npx serve`) — จะย่อขยายให้พอดีทุกขนาดจอ
- กด **F** เพื่อเต็มจอ
- `?demo=1` — โหมดทดสอบ ตัวเลขสุ่มเพิ่มทุก 3 วินาที (ดูแอนิเมชันสลับอันดับ)

## ข้อมูล
แก้ตัวเลขใน `ranking-data.json` — หน้าจออ่านไฟล์ใหม่ทุก 10 วินาที

```json
{ "updatedAt": "2026-10-29T15:00:00+07:00",
  "counts": { "steadyhand": 102, "diamondhand": 73, "...": 0 } }
```

คีย์ตัวตน: `guardian` `harvester` `steadyhand` `diamondhand` `analyst` `planner` `explorer` `sage` `maverick` `waverider` `contrarian` `collector`

ถ้าเปิดไฟล์ตรงๆ (file://) จะอ่าน JSON ไม่ได้ และจะแสดงตัวเลขตัวอย่างที่ฝังไว้ในหน้าแทน
