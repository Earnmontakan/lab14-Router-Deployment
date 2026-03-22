# Lab 14: React Router & Deployment

แอปพลิเคชัน React นี้ได้รับการพัฒนาขึ้นสำหรับ Lab 14 เพื่อสาธิตการใช้งาน **React Router v6** และ **React Context API** รวมถึงการตั้งค่าสำหรับการ Deploy บน Vercel.

## 🎯 วัตถุประสงค์
- **React Router Navigation**: การกำหนดเส้นทาง (Routes) สำหรับหน้าต่างๆ ในแอป
- **Dynamic Routing (`useParams`)**: การสร้างหน้ารายละเอียดสินค้าที่ดึงข้อมูลตาม ID จาก URL 
- **Programmatic Navigation (`useNavigate`)**: การสร้างปุ่มย้อนกลับหรือเปลี่ยนหน้าด้วยโค้ด
- **Global State (`useContext`)**: การสร้าง Shopping Cart เพื่อแชร์ข้อมูลสินค้าและตะกร้าระหว่างหน้าต่างๆ
- **Deployment**: การตั้งค่า `vercel.json` เพื่อรองรับ Client-side Routing ของ React บน Vercel

## 📂 โครงสร้างโปรเจค

- `src/pages/Home.jsx`: หน้าหลักของเว็บไซต์
- `src/pages/About.jsx`: หน้าเกี่ยวกับเรา
- `src/pages/Products.jsx`: หน้ารวมสินค้า
- `src/pages/ProductDetail.jsx`: หน้ารายละเอียดสินค้า (ใช้ Dynamic Route `/products/:id`)
- `src/pages/Cart.jsx`: หน้าตะกร้าสินค้า
- `src/pages/NotFound.jsx`: หน้าแจ้งเตือนเมื่อไม่พบ URL ที่ระบุ (404 Page)
- `src/components/Navbar.jsx`: เมนูนำทางด้านบน (ใช้ `NavLink` เพื่อทำ Active State และแสดงจำนวนของในตะกร้า)
- `src/contexts/CartContext.jsx`: ตัวจัดการ Context สำหรับตะกร้าสินค้า

## 🚀 วิธีการรันโปรเจค

1. **ติดตั้ง Dependencies**:
   ```bash
   npm install
   ```

2. **เริ่มต้น Development Server**:
   ```bash
   npm run dev
   ```

3. **การ Build สำหรับใช้งานจริง (Production)**:
   ```bash
   npm run build
   ```

## 🛠 ฟีเจอร์หลัก
- **Navigation Navbar**: กดเปลี่ยนหน้าโดยที่เว็บไม่ต้องโหลดใหม่ 
- **Product Listing & Detail**: สามารถกดดูรายละเอียดสินค้าแต่ละชิ้นและดึงข้อมูลตามที่เลือกได้
- **Shopping Cart**: ระบบเพิ่มสินค้าลงตะกร้า (ป้องกันการเพิ่มซ้ำ) พร้อมหน้าสรุปยอดสินค้าทั้งหมด 

---
*จัดทำขึ้นสำหรับการเรียนรู้ React Router และ State Management*
