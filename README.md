# 📱 مُذكِّر الدواء — الحصول على APK

## ⚡ الطريقة الأسهل: GitHub Actions (مجاناً، بدون تثبيت أي شيء)

### الخطوة 1 — إنشاء حساب GitHub
👉 https://github.com/signup (مجاني)

### الخطوة 2 — إنشاء repository جديد
1. اضغط **New repository**
2. اسمه: `followupdose`
3. اجعله **Public**
4. اضغط **Create repository**

### الخطوة 3 — رفع الملفات
**الطريقة السهلة (بدون Git):**
1. افتح الـ repository الجديد
2. اضغط **Add file → Upload files**
3. اسحب وأسقط **كل محتويات** مجلد `FollowUpDose-Build`
4. اضغط **Commit changes**

### الخطوة 4 — GitHub يبني APK تلقائياً!
1. اضغط على تبويب **Actions**
2. هتشوف workflow اسمه **Build APK** شغّال
3. استنى 3-5 دقائق
4. لما يخلص، اضغط على الـ workflow
5. تحت **Artifacts** → حمّل **FollowUpDose-APK**
6. أو اضغط **Releases** وحمّل `app-debug.apk` مباشرة

### الخطوة 5 — ثبّت على تلفونك
1. انقل `app-debug.apk` للتلفون
2. افتح الملف
3. لو ظهرت رسالة "Unknown source" → اضغط **Settings → Allow**
4. اضغط **Install** ✅

---

## هيكل الملفات

```
FollowUpDose-Build/
├── .github/
│   └── workflows/
│       └── build.yml      ← GitHub Actions
├── web/
│   ├── index.html          ← التطبيق الرئيسي
│   ├── sw.js
│   ├── manifest.json
│   └── icons/
├── package.json
└── capacitor.config.json
```

---

## مميزات النسخة Android

| الميزة | PWA | Android APK |
|--------|-----|-------------|
| منبه لما التطبيق مفتوح | ✅ | ✅ |
| منبه لما التلفون مقفول الشاشة | ⚠️ | ✅ |
| منبه لما التطبيق مغلق تماماً | ❌ | ✅ |
| إشعار خارجي | ⚠️ | ✅ |
| يكسر الصمت (Silent mode) | ❌ | ✅ |
| يشتغل بدون نت | ✅ | ✅ |
