# 📦 دليل النشر على npm - oqool

**الإصدار:** 3.13.0
**التاريخ:** 2025-10-24

---

## ⚠️ قبل البدء

### تأكد من:
- ✅ لديك حساب npm
- ✅ بريدك الإلكتروني مفعّل
- ✅ المشروع مبني بنجاح (`npm run build`)
- ✅ جميع الاختبارات نجحت

---

## 📝 خطوات النشر

### 1. تسجيل الدخول على npm

```bash
npm login
```

**سيطلب منك:**
```
Username: oqool
Password: ******  (كلمة مرورك)
Email: moaid15@googlemail.com
```

**إذا كان لديك 2FA:**
```
Enter one-time password: ******
# سيأتي OTP على بريدك moaid15@googlemail.com
```

---

### 2. التحقق من تسجيل الدخول

```bash
npm whoami
# يجب أن يظهر: oqool
```

---

### 3. بناء المشروع

```bash
npm run build
```

**تأكد من:**
- ✅ لا توجد أخطاء
- ✅ مجلد `dist/` محدّث
- ✅ جميع الملفات مترجمة

---

### 4. التحقق من محتوى الحزمة

**معاينة الملفات التي سيتم نشرها:**
```bash
npm pack --dry-run
```

**الملفات المضمّنة:**
- ✅ `dist/` - الكود المترجم
- ✅ `bin/` - ملفات التنفيذ
- ✅ `README.md` - الدليل
- ✅ `LICENSE` - الترخيص
- ✅ `package.json` - الإعدادات

**الملفات المستثناة:**
- ❌ `src/` - الكود المصدري
- ❌ `docs/` - التوثيق
- ❌ `tests/` - الاختبارات
- ❌ `node_modules/` - المكتبات
- ❌ `.git/` - تاريخ Git

---

### 5. إنشاء حزمة محلية (اختياري)

**لاختبار الحزمة قبل النشر:**
```bash
npm pack
```

**سيُنشئ ملف:**
```
oqool-oqool-3.13.0.tgz
```

**اختبار التثبيت:**
```bash
npm install -g ./oqool-oqool-3.13.0.tgz
oqool --version
```

---

### 6. النشر

#### أ. النشر العام (Public)

```bash
npm publish --access public
```

**لماذا `--access public`؟**
- الحزم التي تبدأ بـ `@` (مثل `@oqool/oqool`) تكون خاصة افتراضياً
- `--access public` يجعلها عامة ومجانية

#### ب. معاينة ما سيتم نشره

```bash
npm publish --dry-run
```

---

### 7. التحقق من النشر

**على الموقع:**
1. اذهب إلى: https://www.npmjs.com/package/@oqool/oqool
2. تحقق من:
   - ✅ الإصدار: 3.13.0
   - ✅ الوصف صحيح
   - ✅ README يظهر بشكل صحيح

**من الطرفية:**
```bash
npm view @oqool/oqool
```

---

### 8. اختبار التثبيت

**في مجلد جديد:**
```bash
# في مجلد آخر
cd /tmp
npm install -g @oqool/oqool
oqool --version
# يجب أن يظهر: 3.13.0

oqool --help
# يجب أن يظهر قائمة الأوامر

# اختبار الاختصار
mg --version
```

---

## 🔧 إصلاح المشاكل الشائعة

### المشكلة 1: "You must be logged in"

**الحل:**
```bash
npm login
# أدخل بياناتك من جديد
```

### المشكلة 2: "Package name already exists"

**الحل:**
- الحزمة `@oqool/oqool` موجودة بالفعل
- إما:
  1. استخدم `npm version patch/minor/major` لزيادة الإصدار
  2. أو غيّر الاسم في `package.json`

### المشكلة 3: "You do not have permission"

**الحل:**
```bash
# تأكد أنك المالك
npm owner ls @oqool/oqool

# إضافة نفسك كمالك (إذا لزم)
npm owner add oqool @oqool/oqool
```

### المشكلة 4: "403 Forbidden"

**الأسباب المحتملة:**
- لست مسجل دخول
- ليس لديك صلاحيات على `@oqool` scope
- البريد الإلكتروني غير مفعّل

**الحل:**
```bash
npm logout
npm login
# أو
# تحقق من تفعيل البريد على npmjs.com
```

---

## 📈 بعد النشر

### 1. إنشاء Git Tag

```bash
git tag v3.13.0
git push origin v3.13.0
```

### 2. إنشاء GitHub Release

```bash
gh release create v3.13.0 \
  --title "oqool v3.13.0" \
  --notes "أول إصدار رسمي باسم oqool"
```

### 3. مشاركة الإصدار

```bash
# Twitter
npm install -g @oqool/oqool 🚀
أداة ذكاء اصطناعي متقدمة لتوليد وتعديل الأكواد
#oqool #AI #CodeGen

# Discord/Slack
تم نشر oqool 3.13.0! 🎉
npm install -g @oqool/oqool
```

---

## 🔄 تحديث الإصدار القادم

عند إضافة ميزات جديدة:

```bash
# زيادة الإصدار
npm version patch   # 3.13.0 → 3.13.1 (إصلاحات)
npm version minor   # 3.13.0 → 3.14.0 (ميزات جديدة)
npm version major   # 3.13.0 → 4.0.0 (تغييرات كبيرة)

# بناء
npm run build

# نشر
npm publish --access public
```

---

## 📊 معلومات الحزمة

### الحزمة:
```json
{
  "name": "@oqool/oqool",
  "version": "3.13.0",
  "description": "أداة ذكاء اصطناعي متقدمة لتوليد وتعديل الأكواد",
  "author": "Dr. Muayad",
  "license": "MIT"
}
```

### الأوامر:
```bash
oqool     # الأمر الكامل
mg            # الاختصار
```

### الحجم المتوقع:
```
~2-3 MB (مع dependencies)
~500 KB (بدون dependencies)
```

---

## ✅ قائمة التحقق النهائية

قبل `npm publish`:

- [ ] ✅ تسجيل دخول على npm (`npm whoami`)
- [ ] ✅ المشروع مبني (`npm run build`)
- [ ] ✅ لا توجد أخطاء
- [ ] ✅ `package.json` صحيح
- [ ] ✅ `README.md` محدّث
- [ ] ✅ `CHANGELOG.md` محدّث
- [ ] ✅ الإصدار صحيح (3.13.0)
- [ ] ✅ اختبار محلي (`npm link`)
- [ ] ✅ كل الأوامر تعمل
- [ ] ✅ `.npmignore` صحيح

---

## 🎯 الأوامر الكاملة

```bash
# 1. تسجيل الدخول
npm login

# 2. البناء
npm run build

# 3. معاينة
npm pack --dry-run

# 4. النشر
npm publish --access public

# 5. التحقق
npm view @oqool/oqool

# 6. التثبيت العالمي
npm install -g @oqool/oqool

# 7. الاختبار
oqool --version
mg --help
```

---

## 📞 الدعم

إذا واجهت أي مشكلة:

1. **وثائق npm:** https://docs.npmjs.com/
2. **دعم npm:** https://www.npmjs.com/support
3. **تسجيل الدخول:** https://www.npmjs.com/login
4. **إدارة الحساب:** https://www.npmjs.com/settings

---

**تاريخ الإنشاء:** 2025-10-24
**الحالة:** ✅ جاهز للنشر
**الإصدار:** 3.13.0

**حظاً موفقاً! 🚀**
