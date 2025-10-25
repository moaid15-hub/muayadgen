# 🔧 دليل نظام Patch المتقدم

## 📖 المقدمة

نظام **Patch** الجديد في Oqool Code يسمح لك بتعديل ملفات الكود **بدقة عالية** بدلاً من إعادة كتابة الملف كاملاً.

### ✅ المزايا:

- ⚡ **أسرع**: تعديل أسطر محددة فقط
- 🎯 **أدق**: تغيير جزء محدد من الكود
- 🛡️ **أأمن**: لا يخرب بقية الكود
- 👁️ **معاينة**: شوف التعديلات قبل التطبيق

---

## 🚀 الاستخدام السريع

### الأمر الأساسي:

\`\`\`bash
oqool-code patch "الطلب هنا" --files file.js
\`\`\`

### مع معاينة:

\`\`\`bash
oqool-code patch "الطلب هنا" --files file.js --preview
\`\`\`

---

## 📝 أمثلة عملية

### مثال 1: تعديل سطر واحد

**الطلب:**
\`\`\`bash
oqool-code patch "غير السطر 4 ليستخدم template literals" --files test-file.js
\`\`\`

**رد AI المتوقع:**
\`\`\`
PATCH: test-file.js
LINE: 4
REPLACE:
\`\`\`js
  console.log(\`Hello \${name}\`);
\`\`\`
\`\`\`

**النتيجة:**
- السطر 4 تم استبداله بالكود الجديد
- باقي الملف لم يتغير

---

### مثال 2: حذف وإضافة

**الطلب:**
\`\`\`bash
oqool-code patch "احذف دالة calculate واستبدلها بدالة multiply" --files test-file.js
\`\`\`

**رد AI المتوقع:**
\`\`\`
PATCH: test-file.js
LINE: 8
REMOVE: 3
ADD:
\`\`\`js
function multiply(a, b) {
  return a * b;
}
\`\`\`
\`\`\`

**النتيجة:**
- حذف 3 أسطر بدءاً من السطر 8
- إضافة دالة multiply الجديدة

---

### مثال 3: إضافة كود جديد

**الطلب:**
\`\`\`bash
oqool-code patch "أضف دالة farewell بعد دالة greet" --files test-file.js
\`\`\`

**رد AI المتوقع:**
\`\`\`
PATCH: test-file.js
LINE: 6
ADD:
\`\`\`js

function farewell(name) {
  console.log(\`Goodbye \${name}\`);
}
\`\`\`
\`\`\`

**النتيجة:**
- إضافة دالة جديدة في السطر 6
- باقي الملف يتحرك للأسفل

---

## 🔍 صيغة PATCH للـ AI

عند استخدام الأمر \`patch\`, الـ AI يجب أن يرد بهذه الصيغة:

### 1. استبدال سطر (REPLACE):

\`\`\`
PATCH: path/to/file.js
LINE: 10
REPLACE:
\`\`\`js
const newCode = "updated";
\`\`\`
\`\`\`

### 2. حذف وإضافة (REMOVE + ADD):

\`\`\`
PATCH: path/to/file.js
LINE: 45
REMOVE: 2
ADD:
\`\`\`js
const result = await db.query(...);
console.log(result);
\`\`\`
\`\`\`

### 3. إضافة فقط (ADD):

\`\`\`
PATCH: path/to/file.js
LINE: 20
ADD:
\`\`\`js
// تعليق جديد
const newVariable = 123;
\`\`\`
\`\`\`

### 4. حذف فقط (REMOVE):

\`\`\`
PATCH: path/to/file.js
LINE: 15
REMOVE: 3
\`\`\`

---

## ⚙️ الخيارات المتاحة

| الخيار | الوصف | مثال |
|--------|-------|------|
| \`--files <paths...>\` | الملفات المراد تعديلها | \`--files src/api.js src/db.js\` |
| \`--preview\` أو \`-p\` | معاينة قبل التطبيق | \`--preview\` |

---

## 🎯 أمثلة متقدمة

### مثال 4: تعديلات متعددة في ملف واحد

**الطلب:**
\`\`\`bash
oqool-code patch "حدث دالة greet وأضف error handling لدالة calculate" --files test-file.js
\`\`\`

**رد AI:**
\`\`\`
PATCH: test-file.js
LINE: 4
REPLACE:
\`\`\`js
  console.log(\`مرحباً \${name}!\`);
\`\`\`

PATCH: test-file.js
LINE: 8
REMOVE: 3
ADD:
\`\`\`js
function calculate(a, b) {
  if (typeof a !== 'number' || typeof b !== 'number') {
    throw new Error('يجب أن تكون المدخلات أرقام');
  }
  return a + b;
}
\`\`\`
\`\`\`

**النتيجة:**
- تعديلان منفصلان في نفس الملف
- كل تعديل مستقل عن الآخر

---

### مثال 5: تعديلات على عدة ملفات

**الطلب:**
\`\`\`bash
oqool-code patch "أضف 'use strict' في أول كل ملف" --files src/api.js src/db.js src/utils.js
\`\`\`

**رد AI:**
\`\`\`
PATCH: src/api.js
LINE: 1
ADD:
\`\`\`js
'use strict';

\`\`\`

PATCH: src/db.js
LINE: 1
ADD:
\`\`\`js
'use strict';

\`\`\`

PATCH: src/utils.js
LINE: 1
ADD:
\`\`\`js
'use strict';

\`\`\`
\`\`\`

---

## 🛡️ ميزة المعاينة (Preview)

قبل تطبيق أي تعديل، يمكنك معاينته:

\`\`\`bash
oqool-code patch "التعديل" --files file.js --preview
\`\`\`

**المخرجات:**
\`\`\`
📋 معاينة الـ patch على test-file.js:
────────────────────────────────────────────────────────────
  1: // test-file.js
  2: // ملف تجريبي لاختبار نظام Patch
  3:
- 4:   console.log('Hello ' + name);
+ 4:   console.log(\`Hello \${name}\`);
  5: }
  6:
  7: function calculate(a, b) {
────────────────────────────────────────────────────────────

هل تريد تطبيق هذه التعديلات? (Y/n)
\`\`\`

---

## 📊 مقارنة: Patch vs Generate

### استخدم \`generate\`:
- ✅ إنشاء ملفات جديدة
- ✅ كتابة كود كامل من الصفر
- ✅ مشاريع جديدة

### استخدم \`patch\`:
- ✅ تعديل كود موجود
- ✅ تغييرات دقيقة ومحددة
- ✅ إصلاح أخطاء
- ✅ تحسينات صغيرة
- ✅ إضافة features لكود موجود

---

## 💡 نصائح للاستخدام الأمثل

### 1. كن محدداً في الطلب:

❌ **سيء:**
\`\`\`bash
oqool-code patch "حسن الكود" --files app.js
\`\`\`

✅ **جيد:**
\`\`\`bash
oqool-code patch "غير دالة fetchData لتستخدم async/await بدلاً من then" --files app.js
\`\`\`

---

### 2. استخدم المعاينة دائماً لتعديلات مهمة:

\`\`\`bash
oqool-code patch "احذف كل console.log" --files src/api.js --preview
\`\`\`

---

### 3. عدّل ملف واحد في كل مرة للتعديلات الكبيرة:

\`\`\`bash
oqool-code patch "أعد كتابة دالة authenticate" --files src/auth.js
\`\`\`

---

## 🔧 API للمطورين

إذا كنت تريد استخدام النظام برمجياً:

\`\`\`typescript
import { createFileManager, PatchOperation } from '@oqool/code';

const fileManager = createFileManager();

// تطبيق patch واحد
await fileManager.applyPatch('src/api.js', {
  line: 45,
  remove: 2,
  add: 'const result = await db.query();'
});

// تطبيق عدة patches
await fileManager.applyPatches('src/api.js', [
  { line: 10, replace: 'const updated = true;' },
  { line: 20, remove: 1 },
  { line: 30, add: 'console.log("New code");' }
]);

// معاينة patch
await fileManager.previewPatch('src/api.js', {
  line: 15,
  replace: 'const x = 100;'
});
\`\`\`

---

## ❓ استكشاف الأخطاء

### خطأ: "رقم سطر غير صحيح"

**السبب:** رقم السطر أكبر من عدد أسطر الملف

**الحل:** تحقق من عدد الأسطر:
\`\`\`bash
wc -l test-file.js
\`\`\`

---

### خطأ: "الملف غير موجود"

**السبب:** المسار خاطئ

**الحل:** تأكد من المسار:
\`\`\`bash
oqool-code structure  # اعرض بنية المشروع
\`\`\`

---

### "لم يتم العثور على تعديلات"

**السبب:** AI لم يفهم الطلب أو لم يستخدم صيغة PATCH

**الحل:**
1. اجعل الطلب أكثر وضوحاً
2. حدد رقم السطر إذا كنت تعرفه
3. استخدم \`generate\` بدلاً من \`patch\` للتغييرات الكبيرة

---

## 🎓 تمارين عملية

### تمرين 1: استبدال بسيط
غير \`var\` إلى \`const\` في السطر 12

### تمرين 2: إضافة error handling
أضف try-catch لدالة معينة

### تمرين 3: تحديث متعدد
حدث جميع دوال الـ callback لتستخدم arrow functions

---

## 📚 المراجع

- [README.md](README.md) - الوثائق الرئيسية
- [QUICKSTART.md](QUICKSTART.md) - البدء السريع
- [SETUP_REPORT.md](SETUP_REPORT.md) - تقرير الإعداد

---

**صُنع بـ ❤️ بواسطة Oqool AI Team**

للدعم: support@oqool.net
