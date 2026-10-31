# EPS Assistant DZ — طريقة بناء التطبيق (موقع واحد فقط: GitHub)

كل شيء جاهز في هذا المجلد. لا تعدّل أي ملف.

## الخطوات
1. ادخل إلى github.com وسجّل الدخول.
2. اضغط **New repository** (زر + في الأعلى) ← اكتب اسماً مثل `eps-assistant` ← اختر **Public** ← **Create repository**.
3. في الصفحة التي تظهر اضغط الرابط **uploading an existing file**.
4. افتح هذا المجلد على حاسوبك، حدّد **كل ما بداخله** (Ctrl+A) واسحبه إلى صفحة GitHub.
   - يجب أن يظهر ضمن الملفات: `lib` و`assets` و`.github` و`pubspec.yaml`.
5. انتظر انتهاء الرفع ثم اضغط **Commit changes**.
6. اضغط تبويب **Actions** ← سترى عملية اسمها **Build Android APK** تعمل (دائرة صفراء). انتظر 10 إلى 20 دقيقة.
7. عند ظهور علامة ✔ خضراء: اضغط على العملية ← انزل إلى أسفل الصفحة إلى **Artifacts** ← حمّل **EPS-Assistant-APK**.
8. فك الضغط عن الملف المحمَّل وانقل `app-release.apk` إلى هاتفك وثبّته (اسمح بالتثبيت من مصدر غير معروف).

## إن ظهرت علامة ✖ حمراء
افتح العملية، اضغط على الخطوة الحمراء، انسخ الأسطر الحمراء كاملة وأرسلها إلى Claude.

## إن لم يظهر مجلد `.github` بعد الرفع
في GitHub: **Add file ← Create new file** ← في خانة الاسم اكتب بالضبط:
`.github/workflows/build.yml`
ثم الصق فيها محتوى الملف `.github/workflows/build.yml` من هذا المجلد واضغط **Commit changes**.

## بديل (لا تحتاجه إلا إذا فضّلت Codemagic)
ارفع نفس الملفات إلى GitHub ثم اربط المستودع في Codemagic؛ الملف `codemagic.yaml` جاهز.
