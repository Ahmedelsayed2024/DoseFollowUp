# 📱 FollowUpDose — مُذكِّر الدواء v2.0

## ✨ المميزات الجديدة في v2.0

| الميزة | التفاصيل |
|--------|---------|
| 🚀 **Onboarding** | شاشة إعداد أولي جميلة عند أول تشغيل |
| 📊 **إحصائيات Canvas** | دائرة الالتزام + رسم بياني يومي + تقويم الأيام |
| 💉 **تطعيمات تفاعلية** | تتبع اللقاحات + مواعيد حسب تاريخ الميلاد |
| 🧮 **حاسبة الجرعات** | 7 أدوية شائعة محسوبة حسب وزن الطفل (بالمل) |
| 📷 **صورة الدواء** | إضافة صورة لكل دواء |
| 🔔 **أصوات مخصصة** | 6 أصوات تنبيه مختلفة + تحكم في الصوت |
| 📤 **مشاركة الملف** | إرسال قائمة الأدوية + التطعيمات للطبيب |

## 🏗️ بناء APK عبر GitHub Actions

### الخطوة 1: إنشاء Repository
1. افتح [github.com/new](https://github.com/new)
2. الاسم: `followupdose` | Public ✓
3. اضغط **Create repository**

### الخطوة 2: رفع الملفات
1. اضغط **Add file → Upload files**
2. ارفع **كل محتويات هذا المجلد** (بما فيها `.github`)
3. اضغط **Commit changes**

### الخطوة 3: انتظر البناء (3-5 دقائق)
1. اضغط تبويب **Actions**
2. انتظر ✅ Build APK
3. اضغط على الـ workflow ← **Artifacts** → حمّل `FollowUpDose-APK`
4. أو اضغط **Releases** وحمّل `app-debug.apk`

### الخطوة 4: تثبيت على الهاتف
```
1. انقل app-debug.apk للهاتف
2. الإعدادات ← الأمان ← مصادر غير معروفة ← السماح
3. افتح الملف ← تثبيت ✅
```

## 📁 هيكل المشروع
```
FollowUpDose-Build/
├── .github/workflows/build.yml   ← GitHub Actions (يبني APK تلقائياً)
├── web/
│   ├── index.html                ← التطبيق الكامل (151KB)
│   ├── manifest.json             ← PWA manifest
│   ├── sw.js                     ← Service Worker
│   └── icons/                   ← أيقونات 8 أحجام
├── android/                     ← مشروع Android Gradle
│   └── app/src/main/...
├── package.json                  ← Capacitor dependencies
├── capacitor.config.json         ← إعدادات Capacitor
└── README.md
```

## ⚡ مقارنة PWA vs APK

| الميزة | PWA | APK |
|--------|-----|-----|
| منبه والتطبيق مفتوح | ✅ | ✅ |
| منبه والشاشة مقفولة | ⚠️ | ✅ |
| منبه والتطبيق مغلق تماماً | ❌ | ✅ |
| يكسر وضع الصمت | ❌ | ✅ |
| يشتغل بدون نت | ✅ | ✅ |
