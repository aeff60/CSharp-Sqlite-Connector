# การเชื่อมต่อฐานข้อมูล SQLite ด้วย Microsoft.Data.Sqlite

โค้ดนี้เป็นตัวอย่างการเชื่อมต่อฐานข้อมูล SQLite ด้วย Microsoft.Data.Sqlite และสร้างตาราง MyTable ถ้ายังไม่มี โดยใช้ภาษา C#

## วิธีการใช้งาน

1. เพิ่ม NuGet Package ชื่อ Microsoft.Data.Sqlite เข้าไปในโปรเจ็กต์ C#
2. นำโค้ดด้านบนไปวางในคลาสหรือไฟล์ที่ต้องการใช้งาน
3. เรียกใช้เมธอด `InitializeDatabase()` เพื่อสร้างตาราง MyTable ในฐานข้อมูล SQLite ที่มีชื่อว่า sqliteSample.db

## การปรับแต่ง

- เปลี่ยนชื่อฐานข้อมูลหรือชื่อตารางได้โดยแก้ไขค่าตัวแปร `Filename` และ `MyTable` ในโค้ด
- เพิ่มหรือปรับเปลี่ยนฟิลด์ในตาราง MyTable โดยเพิ่มหรือแก้ไขคำสั่ง SQL ใน `tableCommand`

## ข้อจำกัด

- โค้ดนี้ยังไม่ได้รองรับการจัดการ error handling อย่างเหมาะสม
- เมธอด `InitializeDatabase()` เป็น async แต่ไม่มีการ await ใดๆ ทำให้ไม่สามารถจับ error ได้ด้วยวิธีการทั่วไป
