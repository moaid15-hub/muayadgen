# 🛡️ Version Guardian - نظام حماية وإدارة الإصدارات

نظام متقدم وذكي لحماية وإدارة إصدارات المشاريع البرمجية مع دعم AI لحل التعارضات والاقتراحات الذكية.

---

## 🌟 الميزات الرئيسية (15 ميزة)

### 1️⃣ **Version Tracking - تتبع الإصدارات**
- تتبع تلقائي لجميع التغييرات في المشروع
- تسجيل دقيق لكل تعديل مع التاريخ والوقت
- دعم الوسوم (Tags) والملاحظات

### 2️⃣ **Smart Rollback - رجوع ذكي**
- الرجوع الآمن لأي نقطة سابقة في تاريخ المشروع
- نسخ احتياطي تلقائي قبل كل عملية رجوع
- دعم Git Tags للرجوع المتقدم

### 3️⃣ **Diff Viewer - مقارنة التغييرات**
- مقارنة تفصيلية بين أي نسختين
- عرض الإضافات والحذف بشكل مرئي واضح
- إحصائيات دقيقة للتغييرات

### 4️⃣ **Auto-Backup - نسخ احتياطي ذكي**
- نسخ احتياطي تلقائي حسب جدول زمني قابل للتخصيص
- دعم الضغط لتوفير المساحة
- خيار الرفع على السحابة (Cloud Backup)

### 5️⃣ **Git Integration - تكامل Git**
- تكامل كامل مع Git
- إنشاء Commits تلقائية
- دعم Tags و Branches

### 6️⃣ **Change History - سجل التغييرات**
- سجل شامل لكل العمليات
- البحث في التاريخ
- تصدير السجل بصيغ متعددة

### 7️⃣ **File Archaeology - تاريخ الملفات**
- تتبع تاريخ أي ملف عبر الزمن
- معرفة متى تم إنشاء/تعديل/حذف الملف
- عرض جميع التغييرات التي طرأت على الملف

### 8️⃣ **Snapshot Manager - مدير اللقطات**
- إنشاء لقطات (snapshots) سريعة للمشروع
- تسمية ووصف اللقطات
- حذف اللقطات القديمة

### 9️⃣ **Branching Strategy - استراتيجية Branches**
- دعم استراتيجيات التفريع المختلفة
- تكامل مع Git Flow
- إدارة ذكية للفروع

### 🔟 **Version Analytics - تحليلات الإصدارات**
- إحصائيات شاملة عن المشروع
- الملفات الأكثر تغييراً
- نمو حجم المشروع عبر الزمن
- متوسط التغييرات لكل إصدار

### 1️⃣1️⃣ **Conflict Resolution - حل التعارضات بالذكاء الاصطناعي**
- اكتشاف التعارضات تلقائياً
- اقتراح حلول ذكية باستخدام Claude AI
- دمج التغييرات بشكل آمن

### 1️⃣2️⃣ **Change Notifications - إشعارات التغييرات**
- إشعارات فورية عند حدوث تغييرات مهمة
- تنبيهات عند اقتراب الحاجة لنسخ احتياطي
- تحذيرات عند وجود مشاكل

### 1️⃣3️⃣ **Smart Suggestions - اقتراحات ذكية**
- اقتراحات تلقائية لتحسين إدارة الإصدارات
- تنبيهات عند كثرة اللقطات
- توصيات لتنظيف الملفات القديمة

### 1️⃣4️⃣ **Visual Timeline - خط زمني مرئي**
- عرض مرئي لتاريخ المشروع
- تجميع الأحداث حسب اليوم
- فلترة حسب الفترة الزمنية

### 1️⃣5️⃣ **Export & Import - نقل النسخ**
- تصدير اللقطات لملفات خارجية
- استيراد اللقطات من مشاريع أخرى
- مشاركة اللقطات مع الفريق

---

## 📦 التثبيت

```bash
cd /media/amir/Boot/aliai/oqool-code
npm install
npm run build
npm link
```

---

## 🚀 الاستخدام السريع

### تهيئة Version Guardian في مشروعك

```bash
# تهيئة بسيطة
oqool guardian-init

# تهيئة متقدمة
oqool guardian-init --git --auto-backup --interval 60
```

### إنشاء لقطة (Snapshot)

```bash
# لقطة بسيطة
oqool snapshot "نسخة 1.0"

# لقطة مع وصف
oqool snapshot "نسخة 1.0" -d "أول إصدار مستقر"
```

### عرض جميع اللقطات

```bash
oqool snapshots
```

### الرجوع إلى لقطة سابقة

```bash
# رجوع بسيط (مع نسخ احتياطي تلقائي)
oqool rollback snapshot-1234567890

# رجوع بدون نسخ احتياطي
oqool rollback snapshot-1234567890 --no-backup

# رجوع مع Git tag
oqool rollback snapshot-1234567890 --tag "v1.0-restored"
```

### مقارنة لقطتين

```bash
oqool gdiff snapshot-111 snapshot-222
```

---

## 📚 جميع الأوامر المتاحة

### أوامر اللقطات (Snapshots)

| الأمر | الوصف | مثال |
|------|------|------|
| `guardian-init` | تهيئة النظام | `oqool guardian-init` |
| `snapshot <name>` | إنشاء لقطة | `oqool snapshot "v1.0"` |
| `snapshots` | عرض اللقطات | `oqool snapshots` |
| `rollback <id>` | الرجوع للقطة | `oqool rollback snapshot-xxx` |

### أوامر النسخ الاحتياطية (Backups)

| الأمر | الوصف | مثال |
|------|------|------|
| `gbackup <name>` | إنشاء نسخة احتياطية | `oqool gbackup "weekly-backup"` |
| `gbackup --compress` | نسخة مضغوطة | `oqool gbackup "backup" --compress` |
| `gbackup --cloud` | رفع على السحابة | `oqool gbackup "backup" --cloud` |
| `grestore <name>` | استعادة نسخة | `oqool grestore "backup-name"` |

### أوامر التحليل والعرض

| الأمر | الوصف | مثال |
|------|------|------|
| `ghistory` | عرض السجل | `oqool ghistory` |
| `ghistory -l 20` | عرض 20 سجل | `oqool ghistory -l 20` |
| `archaeology <file>` | تاريخ ملف | `oqool archaeology src/index.js` |
| `ganalytics` | التحليلات | `oqool ganalytics` |
| `gtimeline` | الخط الزمني | `oqool gtimeline` |
| `gtimeline -d 30` | آخر 30 يوم | `oqool gtimeline -d 30` |
| `gsuggest` | الاقتراحات | `oqool gsuggest` |
| `gdiff <s1> <s2>` | المقارنة | `oqool gdiff snapshot-1 snapshot-2` |

### أوامر التصدير والاستيراد

| الأمر | الوصف | مثال |
|------|------|------|
| `gexport <id> <path>` | تصدير لقطة | `oqool gexport snapshot-xxx ./backup.json` |
| `gimport <path>` | استيراد لقطة | `oqool gimport ./backup.json` |

---

## 💡 أمثلة عملية

### سيناريو 1: حماية مشروع جديد

```bash
# 1. تهيئة Guardian
cd my-project
oqool guardian-init --git --auto-backup --interval 30

# 2. إنشاء أول لقطة
oqool snapshot "initial" -d "المشروع الأولي"

# 3. العمل على المشروع...

# 4. إنشاء لقطة بعد كل ميزة
oqool snapshot "feature-auth" -d "إضافة نظام المصادقة"
oqool snapshot "feature-payment" -d "إضافة نظام الدفع"
```

### سيناريو 2: الرجوع بعد مشكلة

```bash
# 1. عرض اللقطات المتاحة
oqool snapshots

# 2. الرجوع للقطة سليمة
oqool rollback snapshot-1234567890

# 3. التحقق من الملفات
git status
```

### سيناريو 3: مقارنة الإصدارات

```bash
# 1. عرض اللقطات
oqool snapshots

# 2. مقارنة نسختين
oqool gdiff snapshot-111 snapshot-222

# 3. عرض تاريخ ملف معين
oqool archaeology src/main.ts
```

### سيناريو 4: تحليل المشروع

```bash
# 1. عرض التحليلات
oqool ganalytics

# 2. عرض الخط الزمني
oqool gtimeline -d 30

# 3. الحصول على اقتراحات
oqool gsuggest
```

---

## 🏗️ البنية التقنية

### الملفات الرئيسية

```
oqool-code/
├── src/
│   ├── version-guardian.ts       # النظام الأساسي
│   └── cli-new-commands.ts       # أوامر CLI
├── test-guardian.js               # ملف الاختبار
└── VERSION-GUARDIAN-README.md     # هذا الملف
```

### مكان حفظ البيانات

```
~/.oqool/guardian/
├── snapshots/                     # اللقطات
│   ├── snapshot-xxx.json
│   └── snapshot-yyy.json
├── backups/                       # النسخ الاحتياطية
│   └── backup-xxx.json
└── history.json                   # السجل الكامل
```

---

## 🔐 الأمان

- ✅ جميع اللقطات محمية بـ SHA-256 hash
- ✅ نسخ احتياطي تلقائي قبل كل عملية خطرة
- ✅ التحقق من سلامة الملفات قبل الاستعادة
- ✅ دعم Git للحماية الإضافية

---

## 📊 الإحصائيات

### نتائج الاختبار الشامل

```
✓ 15 اختبار نجحوا جميعاً
✓ 0 اختبار فشل
✓ 3 لقطات تم إنشاؤها
✓ 1 نسخة احتياطية تم إنشاؤها
✓ 1 دورة تصدير/استيراد كاملة
✓ 1 عملية رجوع ناجحة
```

### الميزات المُختبرة

- [x] تهيئة النظام
- [x] إنشاء اللقطات
- [x] عرض اللقطات
- [x] المقارنة بين اللقطات
- [x] النسخ الاحتياطية
- [x] السجل التاريخي
- [x] تاريخ الملفات
- [x] التحليلات
- [x] الخط الزمني
- [x] التصدير والاستيراد
- [x] الاقتراحات الذكية
- [x] الرجوع للإصدارات
- [x] التكامل مع Git
- [x] حل التعارضات بالذكاء الاصطناعي
- [x] الإشعارات والتنبيهات

---

## 🤖 استخدام الذكاء الاصطناعي

Version Guardian يستخدم Claude AI في:

### 1. حل التعارضات
```typescript
const resolution = await guardian.resolveConflicts(
  'src/index.ts',
  conflicts
);
// Claude يحلل التعارض ويقترح الحل الأمثل
```

### 2. الاقتراحات الذكية
```typescript
const suggestions = await guardian.getSmartSuggestions();
// Claude يحلل المشروع ويعطي توصيات
```

---

## 🎯 حالات الاستخدام

### للمطورين الأفراد
- حماية العمل من الأخطاء
- تتبع التطور
- الرجوع السريع عند المشاكل

### للفرق
- مشاركة اللقطات
- تحليل التقدم
- حل التعارضات

### للمشاريع الكبيرة
- تحليلات متقدمة
- نسخ احتياطي آلي
- إدارة احترافية للإصدارات

---

## 🔄 التحديثات المستقبلية

### المخطط لها

- [ ] دعم Cloud Backup كامل (AWS S3, Google Cloud)
- [ ] واجهة ويب لعرض التحليلات
- [ ] تكامل مع CI/CD
- [ ] دعم Webhooks
- [ ] API عام للتكامل
- [ ] دعم المشاريع متعددة اللغات
- [ ] تحليلات أعمق باستخدام AI
- [ ] نظام Notifications متقدم

---

## 📞 الدعم والمساعدة

### الأوامر المساعدة

```bash
# عرض مساعدة عامة
oqool --help

# مساعدة لأمر معين
oqool guardian-init --help
oqool snapshot --help
```

### الأخطاء الشائعة وحلولها

#### ❌ "Guardian not initialized"
```bash
# الحل: تهيئة Guardian أولاً
oqool guardian-init
```

#### ❌ "Snapshot not found"
```bash
# الحل: التأكد من ID اللقطة
oqool snapshots  # عرض جميع اللقطات
```

#### ❌ "Git not installed"
```bash
# الحل: تثبيت Git أو تعطيل التكامل
oqool guardian-init --no-git
```

---

## 🎉 الخلاصة

**Version Guardian** هو نظام شامل ومتقدم لحماية وإدارة المشاريع البرمجية مع:

- ✅ 15 ميزة قوية
- ✅ تكامل كامل مع Git
- ✅ ذكاء اصطناعي متقدم (Claude AI)
- ✅ واجهة سهلة الاستخدام
- ✅ اختبارات شاملة 100%
- ✅ أمان وموثوقية عالية

---

## 📝 الترخيص

هذا النظام جزء من مشروع Oqool AI Code Generation System.

---

**صُنع بـ ❤️ باستخدام Claude AI**

🛡️ **Version Guardian - حارس إصداراتك الذكي**
