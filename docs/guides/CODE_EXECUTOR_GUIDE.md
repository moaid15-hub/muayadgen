# 🏃 دليل تنفيذ الكود (Code Executor)

## 📖 المقدمة

نظام **Code Executor** في Oqool Code يتيح لك:
- ▶️ **تشغيل الأكواد** مباشرة (JavaScript, TypeScript, Python)
- 🛡️ **Sandbox Mode** لتشغيل آمن
- 🔧 **Auto-fix** للأخطاء باستخدام AI
- ⏱️ **Timeout Protection** لمنع التشغيل اللانهائي
- 📊 **تحليل الأخطاء** والإصلاح الذكي

---

## 🚀 الاستخدام السريع

### 1️⃣ تشغيل ملف كود

```bash
oqool-code run <file>
```

**مثال:**
```bash
oqool-code run src/app.js
```

---

### 2️⃣ تشغيل مع خيارات

```bash
# مع Sandbox
oqool-code run src/app.js --sandbox

# مع Timeout مخصص (بالميلي ثانية)
oqool-code run src/app.js --timeout 10000

# مع معاملات
oqool-code run src/script.js --args arg1 arg2 arg3
```

---

### 3️⃣ إصلاح خطأ تلقائياً

```bash
oqool-code fix <file> --auto-apply
```

**مثال:**
```bash
oqool-code fix src/api.js --auto-apply
```

**بدون تطبيق (معاينة فقط):**
```bash
oqool-code fix src/api.js
```

---

### 4️⃣ تشغيل وإصلاح تلقائي

```bash
oqool-code run-fix <file>
```

**مثال:**
```bash
oqool-code run-fix src/app.js
```

هذا الأمر:
1. ✅ يشغل الكود
2. ❌ إذا فشل → يحلل الخطأ
3. 🔧 يصلحه تلقائياً
4. ✅ يشغله مرة أخرى

---

## 📝 اللغات المدعومة

| اللغة | الامتداد | المُفسر المستخدم |
|-------|----------|------------------|
| JavaScript | `.js`, `.mjs` | `node` |
| TypeScript | `.ts` | `npx ts-node` |
| Python | `.py` | `python3` |

---

## 🛡️ وضع Sandbox

Sandbox يوفر بيئة تشغيل معزولة:

```bash
oqool-code run script.js --sandbox
```

**ماذا يحدث في Sandbox؟**
- 🔒 تعيين `NODE_ENV=sandbox`
- 🔒 بيئة معزولة عن النظام
- 🔒 مثالي لتشغيل أكواد غير موثوقة

---

## ⏱️ Timeout Protection

تحديد وقت أقصى للتشغيل:

```bash
# توقف بعد 10 ثواني
oqool-code run longScript.js --timeout 10000
```

**الافتراضي:** 5000ms (5 ثواني)

إذا تجاوز الكود هذا الوقت:
```
❌ تجاوز الوقت المحدد (10000ms)
```

---

## 🔧 نظام Auto-fix

### كيف يعمل؟

1. **تشغيل الكود** → فشل
2. **تحليل الخطأ**:
   - نوع الخطأ (Syntax, Runtime, etc.)
   - رقم السطر
   - Stack trace
3. **إرسال للـ AI**:
   - محتوى الملف
   - الخطأ
   - تحليل AST
4. **استخراج الحل**:
   - PATCH operations
   - أو Full file rewrite
5. **تطبيق التعديلات**
6. **اختبار الحل**
7. **إعادة المحاولة** (حتى 3 مرات)

---

## 📊 أنواع الأخطاء المدعومة

### 1. **Syntax Errors**

```javascript
// خطأ: قوس مفقود
function test() {
  console.log('Hello'
// ← قوس )  مفقود
```

**Auto-fix يكتشف:**
```
❌ SyntaxError: Unexpected end of input
💡 الخطأ في السطر: 3
```

---

### 2. **Runtime Errors**

```javascript
// خطأ: متغير غير معرف
function greet() {
  console.log(userName);  // ← userName غير معرف
}
greet();
```

**Auto-fix يكتشف:**
```
❌ ReferenceError: userName is not defined
💡 الخطأ في السطر: 3
```

---

### 3. **Type Errors**

```javascript
// خطأ: استدعاء دالة غير موجودة
const obj = { name: 'Test' };
obj.getName();  // ← getName غير موجودة
```

**Auto-fix يكتشف:**
```
❌ TypeError: obj.getName is not a function
💡 الخطأ في السطر: 2
```

---

## 🎯 أمثلة عملية

### مثال 1: تشغيل بسيط

**الملف: hello.js**
```javascript
console.log('Hello, World!');
```

**الأمر:**
```bash
oqool-code run hello.js
```

**النتيجة:**
```
📤 المخرجات:
────────────────────────────────────────────────────────────
Hello, World!
────────────────────────────────────────────────────────────
✔ نجح التنفيذ! (45ms)
```

---

### مثال 2: تشغيل مع معاملات

**الملف: greet.js**
```javascript
const name = process.argv[2] || 'Guest';
console.log(`Hello, ${name}!`);
```

**الأمر:**
```bash
oqool-code run greet.js --args Ahmed
```

**النتيجة:**
```
📤 المخرجات:
────────────────────────────────────────────────────────────
Hello, Ahmed!
────────────────────────────────────────────────────────────
✔ نجح التنفيذ! (52ms)
```

---

### مثال 3: خطأ وإصلاح تلقائي

**الملف: buggy.js**
```javascript
function add(a, b) {
  return a + b;
}

console.log(add(5, notDefined));  // ← خطأ
```

**الأمر:**
```bash
oqool-code run-fix buggy.js
```

**النتيجة:**
```
🚀 تشغيل buggy.js...

❌ فشل التنفيذ!

⚠️  الخطأ:
ReferenceError: notDefined is not defined

🔧 محاولة إصلاح الخطأ في buggy.js...

📍 محاولة 1 من 3...

🤖 جاري تحليل الخطأ وإيجاد الحل...

✅ تم إيجاد الحل!

📝 الشرح:
المتغير notDefined غير معرف. يبدو أنه خطأ في الكتابة...

📝 تطبيق 1 patch(es)...

✅ تم تطبيق التعديلات

🧪 اختبار الحل...

✅ نجح الإصلاح! الكود يعمل الآن بشكل صحيح

📤 المخرجات النهائية:
────────────────────────────────────────────────────────────
13
────────────────────────────────────────────────────────────
```

---

### مثال 4: Sandbox Mode

**الملف: risky.js**
```javascript
// كود قد يكون خطر
console.log('Running in:', process.env.NODE_ENV);
console.log('Safe execution!');
```

**الأمر:**
```bash
oqool-code run risky.js --sandbox
```

**النتيجة:**
```
📤 المخرجات:
────────────────────────────────────────────────────────────
Running in: sandbox
Safe execution!
────────────────────────────────────────────────────────────
✔ نجح التنفيذ! (68ms)
```

---

### مثال 5: Timeout Protection

**الملف: infinite.js**
```javascript
// حلقة لا نهائية
while (true) {
  console.log('Running...');
}
```

**الأمر:**
```bash
oqool-code run infinite.js --timeout 2000
```

**النتيجة:**
```
❌ الخطأ:
────────────────────────────────────────────────────────────
تجاوز الوقت المحدد (2000ms)
────────────────────────────────────────────────────────────

💡 جرب: oqool-code fix infinite.js --auto-apply
```

---

## ⚙️ الخيارات المتاحة

### أمر `run`

| الخيار | الوصف | القيمة الافتراضية |
|--------|-------|-------------------|
| `-t, --timeout <ms>` | وقت انتهاء التنفيذ | 5000 |
| `--sandbox` | تشغيل في وضع sandbox | false |
| `--args <args...>` | معاملات للبرنامج | [] |

---

### أمر `fix`

| الخيار | الوصف | القيمة الافتراضية |
|--------|-------|-------------------|
| `-m, --max-attempts <n>` | عدد محاولات الإصلاح | 3 |
| `--auto-apply` | تطبيق التعديلات تلقائياً | false |

---

### أمر `run-fix`

| الخيار | الوصف | القيمة الافتراضية |
|--------|-------|-------------------|
| `-t, --timeout <ms>` | وقت انتهاء التنفيذ | 5000 |
| `-m, --max-attempts <n>` | عدد محاولات الإصلاح | 3 |
| `--no-auto-apply` | عدم التطبيق التلقائي | false |

---

## 🔧 API للمطورين

```typescript
import { createCodeExecutor } from '@oqool/code';

const executor = createCodeExecutor();

// 1. تشغيل الكود
const result = await executor.executeCode({
  file: 'src/app.js',
  env: 'sandbox',
  timeout: 5000,
  args: ['arg1', 'arg2']
});

if (result.success) {
  console.log('Output:', result.output);
  console.log('Runtime:', result.runtime, 'ms');
} else {
  console.error('Error:', result.error);
  console.error('Type:', result.errorType);
  console.error('Line:', result.errorLine);
}

// 2. إصلاح خطأ
const fixResult = await executor.fixError({
  file: 'src/app.js',
  error: result.error,
  errorType: result.errorType,
  maxAttempts: 3,
  autoApply: true
});

if (fixResult.fixed) {
  console.log('Fixed!');
}

// 3. تشغيل وإصلاح تلقائي
const finalResult = await executor.runAndFix('src/app.js', {
  timeout: 5000,
  autoApply: true,
  maxAttempts: 3
});
```

---

## 📊 ExecutionResult Interface

```typescript
interface ExecutionResult {
  success: boolean;          // نجح التنفيذ؟
  output?: string;           // المخرجات
  error?: string;            // رسالة الخطأ
  exitCode?: number;         // كود الخروج
  runtime?: number;          // وقت التنفيذ (ms)
  errorType?: 'syntax' | 'runtime' | 'timeout' | 'other';
  errorLine?: number;        // رقم السطر
  errorStack?: string;       // Stack trace
}
```

---

## 📊 FixResult Interface

```typescript
interface FixResult {
  success: boolean;          // نجحت العملية؟
  fixed: boolean;            // تم الإصلاح؟
  message: string;           // رسالة الحالة
  attempts: number;          // عدد المحاولات
  patches?: any[];           // التعديلات المطبقة
}
```

---

## 💡 نصائح

### 1. استخدم Sandbox للأكواد غير الموثوقة

```bash
# ✅ آمن
oqool-code run untrusted-script.js --sandbox

# ⚠️ خطر
oqool-code run untrusted-script.js
```

---

### 2. حدد Timeout مناسب

```bash
# للأكواد السريعة
oqool-code run quick.js --timeout 1000

# للأكواد الثقيلة
oqool-code run heavy.js --timeout 30000
```

---

### 3. استخدم run-fix للإنتاجية

بدلاً من:
```bash
oqool-code run app.js
# فشل
oqool-code fix app.js --auto-apply
oqool-code run app.js
```

استخدم:
```bash
oqool-code run-fix app.js
```

---

### 4. معاينة قبل التطبيق

```bash
# معاينة الحل
oqool-code fix app.js

# إذا كان الحل صحيح، طبقه
oqool-code fix app.js --auto-apply
```

---

## 🎓 حالات الاستخدام

### 1. **اختبار سريع**

```bash
# اختبر كود سريع
oqool-code run test.js
```

---

### 2. **التطوير**

```bash
# شغل وأصلح تلقائياً أثناء التطوير
oqool-code run-fix src/app.js
```

---

### 3. **CI/CD**

```bash
# اختبر الأكواد في CI
oqool-code run tests/*.js --timeout 10000
```

---

### 4. **تشغيل Scripts**

```bash
# شغل script مع معاملات
oqool-code run scripts/build.js --args production
```

---

## 🔗 التكامل مع الميزات الأخرى

### مع AST Analyzer

```bash
# حلل الكود قبل التشغيل
oqool-code analyze src/app.js

# ثم شغله
oqool-code run src/app.js
```

---

### مع Patch System

```bash
# عدل الكود
oqool-code patch "حسن أداء الدالة" --files src/app.js

# ثم شغله
oqool-code run src/app.js
```

---

## ⚠️ متطلبات

### لـ TypeScript:

```bash
npm install -g ts-node
```

### لـ Python:

```bash
# تأكد من تثبيت Python 3
python3 --version
```

---

## 🐛 استكشاف الأخطاء

### خطأ: ts-node غير مثبت

```bash
npm install -g ts-node
```

---

### خطأ: python3 غير موجود

```bash
# على Ubuntu/Debian
sudo apt install python3

# على macOS
brew install python3
```

---

### خطأ: الملف غير موجود

تأكد من المسار:
```bash
# ✅ صحيح
oqool-code run src/app.js

# ❌ خطأ
oqool-code run app.js  # إذا كان في src/
```

---

## 📚 المراجع

- [README.md](README.md)
- [PATCH_GUIDE.md](PATCH_GUIDE.md)
- [AST_ANALYZER_GUIDE.md](AST_ANALYZER_GUIDE.md)
- [code-executor.ts](src/code-executor.ts)

---

**صُنع بـ ❤️ بواسطة Oqool AI Team**
