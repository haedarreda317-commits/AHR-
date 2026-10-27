# مشروع AHR للهاتف

هذا مشروع بداية يحزم واجهة AHR الحالية داخل تطبيق Android/iOS باستخدام Capacitor. ليس ملف APK جاهزاً بعد؛ يجب بناء النسخة النهائية على كمبيوتر.

## المتطلبات
- Node.js إصدار LTS
- Android Studio لبناء Android
- لبناء iPhone/iOS: جهاز Mac مع Xcode (أو خدمة بناء سحابية متوافقة)

## إعداد Android
1. فك ضغط الملف.
2. افتح الطرفية داخل مجلد `AHR_mobile_project`.
3. نفّذ:
   ```bash
   npm install
   npx cap add android
   npx cap sync android
   npx cap open android
   ```
4. في Android Studio جرّب التطبيق على هاتف موصول أو محاكي.
5. لإخراج ملف قابل للتثبيت، استخدم Build > Build Bundle(s) / APK(s) > Build APK(s). للنشر على Google Play غالباً تحتاج Android App Bundle (AAB).

## إعداد iPhone
على جهاز Mac فقط، نفّذ:
```bash
npm install
npx cap add ios
npx cap sync ios
npx cap open ios
```
ثم افتح المشروع في Xcode وشغّله على جهاز أو محاكي. النشر يتطلب إعدادات توقيع Apple المناسبة.

## ملاحظات مهمة
- هذه الحزمة تنقل واجهة الويب الحالية إلى مشروع هاتف؛ لا تعني أن كل الميزات الأصلية أصبحت جاهزة تلقائياً.
- إشعارات الخلفية، مزامنة الحسابات، تسجيل الدخول الآمن، وعرض المهمة على شاشة القفل تحتاج تطويراً واختباراً إضافيين، وقد تتطلب إضافات Capacitor وخدمة خلفية.
- تسجيل الاسم والمهام في النسخة الحالية محلي، وليس حساباً سحابياً آمناً.
