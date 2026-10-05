# Online Shoppers Purchasing Intention — Interactive Data Visualization

## โครงสร้าง Repository

```text
.
├── data/
│   ├── raw/
│   │   └── online_.csv
│   └── cleaned/
│       └── online_cleaned.csv
├── web/
│   └── d3/
│       ├── index.html
│       ├── script.js
│       └── style.css
└── README.md
```

## Dataset
Source: UCI Machine Learning Repository — Online Shoppers Purchasing Intention Dataset  
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

ข้อมูลต้นฉบับมี 12,330 sessions และ 18 attributes โดย `Revenue` เป็นตัวแปรเป้าหมายว่าการเข้าชมครั้งนั้นจบด้วยการซื้อหรือไม่

## Data Cleaning
- ตรวจสอบ missing values: ไม่พบ missing values
- ตรวจสอบ duplicate rows: พบ 125 แถว
- ลบ duplicate rows จำนวน 125 แถว
- ข้อมูลหลังทำความสะอาด: 12,205 แถว × 18 คอลัมน์
- ไม่ลบคอลัมน์ที่มีความหมายต่อการวิเคราะห์ออกโดยไม่มีเหตุผล

## Visualization
Dashboard ใช้ D3.js และมีกราฟ 4 รูปแบบ:
1. Bar Chart — การซื้อแยกตาม VisitorType
2. Line Chart — อัตราการซื้อรายเดือน
3. Scatter Plot — PageValues กับ ProductRelated_Duration
4. Histogram — การกระจายของ ExitRates

## Interactivity
- Filter: Month
- Filter: VisitorType
- Filter: Revenue
- Tooltip เมื่อ hover
- ปุ่ม Reset Filter
- KPI อัปเดตตามตัวกรอง

## วิธีเปิดเว็บไซต์
แนะนำให้เปิดด้วย VS Code + Live Server หรือ deploy โฟลเดอร์นี้ผ่าน GitHub Pages เพราะ browser อาจบล็อกการโหลด CSV หากเปิด `index.html` ด้วย `file://`

## GitHub Pages
เมื่ออัปโหลด repository แล้ว:
1. Settings → Pages
2. เลือก Deploy from a branch
3. เลือก branch `main`
4. เลือกโฟลเดอร์ที่ใช้เผยแพร่ตามโครงสร้าง repository ของอาจารย์

## AI Disclosure
โปรเจกต์นี้ใช้ AI ช่วยในการออกแบบโครงสร้าง dashboard, เขียน/อธิบาย HTML, CSS และ JavaScript และช่วยตรวจสอบแนวทาง data cleaning นักศึกษาต้องตรวจสอบและสามารถอธิบายโค้ดและผลวิเคราะห์ได้ด้วยตนเอง
