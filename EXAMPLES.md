# 💡 أمثلة استخدام MuayadGen v4.0

## 🎯 أمثلة سريعة

### 1. قراءة وتحليل
```bash
# قراءة package.json
muayad "اقرأ package.json واعرض اسم المشروع"

# تحليل ملف JavaScript
muayad "اقرأ src/index.js وأعطني ملخص عن الدوال الموجودة"

# فحص ملف تكوين
muayad "افحص .env واعرض المتغيرات الموجودة"
```

---

### 2. إنشاء ملفات جديدة
```bash
# ملف JavaScript بسيط
muayad "اصنع ملف hello.js يطبع Hello World"

# Express Server
muayad "اصنع Express server على البورت 3000 مع route للصفحة الرئيسية"

# React Component
muayad "اصنع مكون React اسمه UserCard يعرض اسم المستخدم وصورته"

# API endpoints
muayad "اصنع ملف routes/api.js مع CRUD endpoints للمنتجات"

# Database Schema
muayad "اصنع schema Mongoose للمستخدمين مع الاسم والإيميل والباسورد"
```

---

### 3. تعديل ملفات موجودة
```bash
# إضافة دالة جديدة
muayad "عدّل utils.js وأضف دالة formatDate لتنسيق التواريخ"

# إضافة middleware
muayad "عدّل app.js وأضف middleware للـ logging"

# إصلاح خطأ
muayad "في auth.js - الـ JWT verification ما يشتغل، أصلحه"

# تحسين كود
muayad "حسّن performance الدالة processData في data.js"

# إضافة error handling
muayad "أضف try-catch لجميع الدوال async في api.js"
```

---

### 4. تنفيذ أوامر
```bash
# تثبيت packages
muayad "ثبّت express و dotenv و mongoose"

# تشغيل اختبارات
muayad "شغّل npm test واعرض النتائج"

# بناء المشروع
muayad "شغّل npm run build وتحقق من النجاح"

# Git operations
muayad "اعمل commit للتغييرات الأخيرة برسالة واضحة"

# مسح ملفات
muayad "امسح جميع ملفات .log من المشروع"
```

---

### 5. تحليل المشاريع
```bash
# البنية العامة
muayad "حلل بنية المشروع واعطني ملخص"

# البحث عن دوال
muayad "ابحث عن جميع الدوال التي تستخدم async/await"

# فحص التبعيات
muayad "اعرض جميع الـ dependencies وقل أيها قديم"

# فحص الأخطاء
muayad "فتش عن أي console.log أو console.error وأزلهم"
```

---

### 6. مشاريع كاملة
```bash
# API كامل
muayad "اصنع REST API كامل لإدارة المهام (tasks) مع Express و MongoDB"

# صفحة ويب
muayad "اصنع صفحة HTML لتسجيل الدخول مع validation و CSS جميل"

# CRUD System
muayad "اصنع نظام CRUD كامل للمستخدمين مع الواجهة والـ backend"

# Testing Suite
muayad "اصنع ملفات Jest لاختبار جميع الـ API endpoints"
```

---

### 7. حل مشاكل معقدة
```bash
# CORS Issues
muayad "عندي مشكلة CORS بين Frontend و Backend، أصلحها"

# Memory Leaks
muayad "في server.js - عندي memory leak، جده وأصلحه"

# Performance
muayad "الـ database queries بطيئة جداً، حسّنها"

# Security
muayad "فتش عن ثغرات أمنية في authentication system"
```

---

### 8. توثيق وتنظيف
```bash
# إضافة تعليقات
muayad "أضف JSDoc comments لجميع الدوال في utils.js"

# إنشاء README
muayad "اصنع README.md احترافي للمشروع"

# تنسيق الكود
muayad "نظّف الكود في app.js وأزل الأجزاء غير المستخدمة"

# إنشاء .gitignore
muayad "اصنع .gitignore مناسب لمشروع Node.js"
```

---

### 9. سيناريوهات متقدمة
```bash
# Migration
muayad "حوّل هذا المشروع من CommonJS إلى ES Modules"

# Refactoring
muayad "أعد هيكلة المشروع لاستخدام MVC pattern"

# Upgrade
muayad "حدّث جميع dependencies لآخر إصدار آمن"

# Testing & Fixing
muayad "شغّل npm test، وإذا فشل أي test، أصلحه"
```

---

### 10. العمل التفاعلي
```bash
# ادخل الوضع التفاعلي
muayad

# ثم:
> اقرأ package.json
> الآن أضف dependency جديد lodash
> ثم ثبّته
> وأنشئ ملف utils.js يستخدمه
> اختبره
```

---

## 🎨 نصائح للحصول على أفضل نتائج

### ✅ جيد - أوامر واضحة:
```bash
muayad "اصنع Express API مع 4 endpoints للمنتجات"
muayad "عدّل auth.js وأضف bcrypt للباسوورد"
muayad "ابحث عن جميع TODO comments في المشروع"
```

### ❌ غير واضح - أوامر مبهمة:
```bash
muayad "اصنع API"
muayad "عدّل الملف"
muayad "ابحث"
```

---

## 🚀 مثال تطبيقي كامل

### المهمة: بناء Blog API

```bash
# الخطوة 1: إنشاء Server
muayad "اصنع Express server مع setup أساسي"

# الخطوة 2: Database Schema
muayad "اصنع Mongoose schema للمقالات مع (title, content, author, date)"

# الخطوة 3: Routes
muayad "اصنع routes للمقالات (GET all, GET one, POST, PUT, DELETE)"

# الخطوة 4: Middleware
muayad "أضف middleware للـ authentication باستخدام JWT"

# الخطوة 5: Error Handling
muayad "أضف error handling middleware في app.js"

# الخطوة 6: Testing
muayad "اصنع Jest tests لجميع الـ endpoints"

# الخطوة 7: Documentation
muayad "اصنع README.md يشرح كيفية تشغيل المشروع"
```

**كل هذا ببضع أوامر! 🎉**

---

## 📊 حالات استخدام حقيقية

### للمبتدئين:
- ✅ تعلم الـ syntax بسرعة
- ✅ إنشاء مشاريع تعليمية
- ✅ فهم الـ best practices

### للمطورين:
- ✅ تسريع التطوير
- ✅ إصلاح الأخطاء بسرعة
- ✅ refactoring ذكي

### للشركات:
- ✅ توليد boilerplate code
- ✅ توحيد أسلوب الكود
- ✅ توثيق تلقائي

---

**صُنع بـ ❤️ بواسطة Dr. Muayad**
