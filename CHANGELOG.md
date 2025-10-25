# Changelog

جميع التغييرات المهمة في المشروع موثقة في هذا الملف.

## [3.13.0] - 2025-10-24

### 🎉 إعادة التسمية الرسمية

#### تغييرات رئيسية
- 🔄 **إعادة التسمية**: من `@oqool/code` إلى `@oqool/oqool`
- 🆕 **أوامر جديدة**: `oqool` و `mg` (اختصار)
- 📦 **تنظيم المشروع**: هيكل منظم احترافي مع مجلدات `docs/` و `tests/`
- 📝 **توثيق محسّن**: ملف `STRUCTURE.md` شامل

#### أضيف
- 🥇 **AI Code Completion** - نظام إكمال الكود الذكي (780+ سطر)
  - توليد اقتراحات متعددة مع مستويات ثقة
  - توليد دوال ودوال كاملة من تعليقات
  - اقتراح تحسينات للكود
  - دعم 7 لغات برمجة

- 🥈 **Database Integration** - تكامل قواعد البيانات (850+ سطر)
  - دعم 7 قواعد بيانات (PostgreSQL, MySQL, MongoDB, SQLite, Redis, MariaDB, MSSQL)
  - دعم 4 ORMs (Prisma, TypeORM, Sequelize, Mongoose)
  - توليد Schema من لغة طبيعية
  - نظام Migrations كامل
  - Query Builder بالذكاء الاصطناعي

- 🥉 **API Testing** - اختبار API المتقدم (750+ سطر)
  - Test Suite Management
  - Load Testing مع إحصائيات مفصلة
  - دعم OpenAPI/Swagger
  - تقارير HTML/JSON

#### أوامر جديدة (11 أمر)
**AI Code Completion:**
- `complete <prompt>` - إكمال كود ذكي
- `complete-function <comment>` - توليد دالة
- `improve <file>` - اقتراح تحسينات

**Database Integration:**
- `db-init <type>` - تهيئة قاعدة بيانات
- `db-schema <description>` - توليد Schema
- `db-migration <name>` - إنشاء Migration
- `db-query <description>` - توليد Query

**API Testing:**
- `api-test-create <name>` - إنشاء Test Suite
- `api-load-test <url>` - Load Testing
- `api-from-openapi <spec>` - توليد من OpenAPI

#### تحسينات البنية
- 📁 **docs/guides/** - 8 أدلة استخدام منظمة
- 📁 **docs/reports/** - 9 تقارير تطوير
- 📁 **tests/** - مشاريع اختبار ومجلدات منظمة
- 📄 **STRUCTURE.md** - دليل شامل لبنية المشروع

#### إحصائيات
- ✅ **31 ملف TypeScript** في src/
- ✅ **~20,000 سطر** كود
- ✅ **100+ أمر CLI**
- ✅ **30 نظام متكامل**
- ✅ **7 لغات برمجة** مدعومة
- ✅ **7 قواعد بيانات** مدعومة

---

## [1.0.0] - 2025-01-XX

### ✨ الإصدار الأول

#### أضيف
- 🎮 واجهة CLI كاملة مع أوامر شاملة
- 🔐 نظام مصادقة آمن مع API Keys
- 🤖 دعم متعدد لمزودات AI (OpenAI, Claude, DeepSeek)
- 📁 نظام إدارة ملفات ذكي
- 💬 وضع محادثة تفاعلية
- 🎨 واجهة طرفية ملونة وجميلة
- 🌍 دعم كامل للغة العربية
- 📊 عرض بنية المشروع
- 🔍 فهم سياق المشروع تلقائياً
- ⚙️ خيارات متقدمة للتحكم

#### الأوامر المتاحة
- `login` - تسجيل الدخول
- `logout` - تسجيل الخروج
- `status` - حالة الحساب
- `generate` - توليد كود
- `chat` - محادثة تفاعلية
- `structure` - عرض بنية المشروع

#### الميزات التقنية
- TypeScript للأمان والتطوير
- معالجة أخطاء شاملة
- Spinner animations
- تنسيق ملون للردود
- دعم .gitignore و .oqoolignore
- استخراج تلقائي للملفات من ردود AI

---

## الإصدارات القادمة

### [1.1.0] - قريباً
- [ ] دعم Git integration
- [ ] أوامر undo/redo
- [ ] حفظ تاريخ المحادثات
- [ ] دعم المزيد من اللغات البرمجية

### [1.2.0] - في الخطة
- [ ] واجهة TUI تفاعلية
- [ ] دعم الصور والملفات الثنائية
- [ ] تكامل مع IDEs
- [ ] Plugins system

---

التنسيق يتبع [Keep a Changelog](https://keepachangelog.com/)
الإصدارات تتبع [Semantic Versioning](https://semver.org/)
