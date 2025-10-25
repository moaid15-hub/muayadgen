# 🚀 دليل البدء السريع - oqool المحلي

## ⚠️ **مهم: لتجنب الخلط مع النسخة القديمة**

هناك نسختان من oqool على جهازك:

### 1️⃣ **النسخة القديمة (عالمية)**
```bash
oqool          # النسخة القديمة - تحتاج oqool.net
/usr/local/bin/oqool
```

### 2️⃣ **النسخة الجديدة (محلية مع Claude)**
```bash
cd /media/amir/Boot/aliai/oqool-code
./mg-claude        # النسخة الجديدة - مع Claude API مباشرة ✅
```

---

## ✅ **الاستخدام الصحيح:**

```bash
# انتقل للمجلد
cd /media/amir/Boot/aliai/oqool-code

# استخدم mg-claude (النسخة الجديدة)
./mg-claude "اصنع ملف test.js"
```

---

## 🎯 **أمثلة:**

### مثال 1: ملف JavaScript
```bash
cd /media/amir/Boot/aliai/oqool-code
./mg-claude "اصنع ملف calculator.js لآلة حاسبة بسيطة"
```

### مثال 2: Express API
```bash
./mg-claude "اصنع Express API مع endpoint للمستخدمين"
```

### مثال 3: صفحة HTML
```bash
./mg-claude "اصنع صفحة login كاملة مع CSS"
```

---

## 🔧 **إزالة النسخة القديمة (اختياري):**

إذا أردت حذف النسخة القديمة:

```bash
npm uninstall -g @oqool/oqool
```

---

## 📝 **ملخص الأوامر:**

| الأمر | النسخة | يعمل مع |
|-------|---------|----------|
| `oqool` | قديمة | oqool.net backend |
| `./mg-claude` | **جديدة ✅** | **Claude API مباشرة** |
| `node mg-local.js` | **جديدة ✅** | **Claude API مباشرة** |

---

## 🎉 **جاهز للاستخدام:**

```bash
cd /media/amir/Boot/aliai/oqool-code
./mg-claude "مرحبا"
```

---

**💡 نصيحة:** استخدم `mg-claude` دائماً للنسخة الجديدة مع Claude API!
