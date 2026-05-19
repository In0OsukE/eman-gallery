# Eman Gallery — شغل خرز يدوي 🧿

## هيكل المشروع

```
eman_gallery/
├── public/
│   ├── index.html          ← الصفحة الرئيسية للمتجر
│   ├── products.json       ← بيانات المنتجات
│   ├── admin/
│   │   └── index.html      ← لوحة التحكم
│   └── images/             ← صور المنتجات (اختياري)
└── vercel.json             ← إعدادات Vercel
```

---

## طريقة رفع المنتجات والصور

### الطريقة 1: من لوحة التحكم (الأسهل)
1. افتح `/admin` في المتجر
2. أضف منتجاتك مع صورها مباشرةً
3. اضغط **تحميل products.json**
4. ارفع الملف اللي اتحمل على GitHub وـVercel هيتحدث تلقائياً

### الطريقة 2: رفع صور منفصلة (للصور الكبيرة)
1. حط الصور في مجلد `public/images/`
2. عدّل `products.json` واكتب المسار: `"image": "/images/bag1.jpg"`
3. ارفع المجلد كله على GitHub

---

## نشر على Vercel

### أول مرة:
1. ارفع المجلد ده على **GitHub** (مجاني)
2. روح على [vercel.com](https://vercel.com) وسجل بحساب GitHub
3. اضغط **Add New Project** → اختار الـ repo
4. **Framework Preset**: Other
5. **Root Directory**: `public` (مهم!)
6. اضغط Deploy ✅

### تحديث المنتجات بعدين:
- عدّل `products.json` وـ push على GitHub → Vercel بيتحدث تلقائياً

---

## تغيير رقم الواتساب

افتح `public/index.html` وغير السطر ده:
```js
const WA = "201000000000"; // ← رقمك هنا
```

---

## ملاحظات مهمة
- الصور المرفوعة من Admin بتتحفظ كـ **Base64** في localStorage
- لما تعمل Export للـ JSON، الصور بتكون جوه الملف نفسه (مناسب للصور الصغيرة)
- للصور الكبيرة: حطها في `public/images/` وعدّل المسار في JSON
