# 🚀 دليل البدء السريع - Oqool Code

## في 5 دقائق فقط!

### الخطوة 1: التنصيب ⚡

```bash
npm install -g @oqool/code
```

### الخطوة 2: احصل على API Key 🔑

1. اذهب إلى [oqool.net](https://oqool.net)
2. سجل حساب جديد (مجاني!)
3. اذهب إلى **الإعدادات** → **API Keys**
4. انسخ مفتاحك: `oqool_xxxxxxxxxxxxx`

### الخطوة 3: سجل دخول 🔐

```bash
oqool-code login oqool_your_api_key_here
```

**النتيجة:**
```
✅ تم تسجيل الدخول بنجاح!

البريد: your@email.com
الباقة: Free Plan
الرسائل المتبقية اليوم: 10

ابدأ الآن: oqool-code "اصنع API بسيط"
```

### الخطوة 4: جرب! 🎉

#### مثال بسيط:

```bash
cd ~/my-project
oqool-code "اصنع ملف hello.js يطبع Hello World"
```

**ستحصل على:**
```javascript
// hello.js
console.log('Hello World! 🌍');
```

#### مثال متوسط:

```bash
oqool-code "اصنع Express API بسيط مع endpoint واحد"
```

**ستحصل على:**
```javascript
// server.js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.json({ message: 'مرحباً من Oqool Code!' });
});

app.listen(3000, () => {
  console.log('Server running on port 3000');
});
```

#### مثال متقدم:

```bash
oqool-code "اصنع React component للـ Todo list مع TypeScript"
```

---

## 🎯 استخدامات شائعة

### للبرمجة السريعة:
```bash
oqool-code "اصنع دالة JavaScript لحساب المتوسط"
```

### لبناء المشاريع:
```bash
oqool-code "اصنع Next.js app مع home page و about page"
```

### للتعلم:
```bash
oqool-code "اشرح واكتب مثال عن Promises في JavaScript"
```

---

## 💬 المحادثة التفاعلية

للتطوير التدريجي:

```bash
oqool-code chat
```

```
أنت: اصنع API بسيط
🤖: [ينشئ الكود]

أنت: أضف authentication
🤖: [يضيف المصادقة]

أنت: اكتب اختبارات
🤖: [يكتب الاختبارات]

أنت: exit
```

---

## 📊 تحقق من حسابك

```bash
oqool-code status
```

```
📊 معلومات الحساب:
──────────────────────────────────────────────────
API Key: oqool_abc...xyz
البريد: your@email.com
الباقة: 💎 Medium Plan
آخر مزامنة: 2025-01-15
──────────────────────────────────────────────────
```

---

## ⚙️ خيارات إضافية

### حدد ملفات للسياق:
```bash
oqool-code "عدل هذا" --files server.js routes.js
```

### اختر مزود AI:
```bash
oqool-code "..." --provider claude    # للتحليل العميق
oqool-code "..." --provider deepseek  # للبرمجة السريعة
oqool-code "..." --provider openai    # متوازن
```

### عرض بنية المشروع:
```bash
oqool-code structure
```

---

## 🆘 مشاكل شائعة

### "API Key غير صحيح"
- تأكد من نسخ المفتاح كاملاً
- لا تترك مسافات في البداية أو النهاية

### "لا توجد ملفات للكتابة"
- كن أكثر وضوحاً في الطلب
- استخدم `chat` mode للتوضيح

### "انتهت الرسائل اليومية"
- ترقية الباقة من [oqool.net](https://oqool.net)
- انتظر حتى الغد (يتجدد يومياً)

---

## 🎓 تعلم المزيد

- 📖 [الوثائق الكاملة](README.md)
- 💡 [أمثلة متقدمة](examples/USAGE_EXAMPLES.md)
- 📹 [فيديوهات تعليمية](https://youtube.com/@oqoolai)
- 💬 [انضم للمجتمع](https://discord.gg/oqool)

---

## 🚀 ابدأ الآن!

```bash
oqool-code "اصنع شيئاً رائعاً!"
```

**Happy Coding! 🎉**
