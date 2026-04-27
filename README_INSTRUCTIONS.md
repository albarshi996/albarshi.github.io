# 📦 إصلاحات حرجة لموقع دورلي

هذي الحزمة فيها 5 ملفات معدّلة تحتوي على إصلاحات الأخطاء الحرجة.

---

## 📋 ما تم إصلاحه

| الملف | الإصلاح |
|-------|---------|
| `request.astro` | تصحيح "شخرة" → "إجخرة" + إضافة فئتي "تجميل ونظافة" و"مواد بناء وصيانة" |
| `services.astro` | تصحيح زر التجميل والنظافة + زر مواد البناء (يحولان للفئة الصحيحة) |
| `index.astro` | حذف وسم `</Layout>` المكرر في النهاية |
| `script.js` | إصلاح تعارض النموذج في صفحة /request (لا يحدث ضغط مزدوج بعد الآن) |
| `sitemap.xml` | حذف `.html` من كل الروابط + إضافة صفحة /pricing |

---

## 🚀 طريقة التطبيق (3 خيارات)

### الخيار 1: عبر GitHub Web (الأسهل من الهاتف) ⭐

لكل ملف من الملفات الخمسة:

1. افتح المستودع: https://github.com/albarshi996/albarshi_dl
2. اذهب للملف المطلوب (مثلاً: `src/pages/request.astro`)
3. اضغط على أيقونة القلم ✏️ (Edit)
4. **احذف كل المحتوى** (Ctrl+A ثم Delete)
5. افتح الملف الجديد من هذي الحزمة، **انسخ كل محتواه**
6. **الصقه** في GitHub
7. انزل لأسفل، اكتب رسالة commit بالعربي:
   - مثلاً: `إصلاح خطأ "شخرة" → "إجخرة" + إضافة فئات جديدة`
8. اختر **"Create a new branch"** واكتب اسم الفرع: `fix/critical-bugs`
9. اضغط **Propose changes**

كرر العملية لكل ملف لكن **في نفس الفرع `fix/critical-bugs`**.

ملاحظة المسارات داخل المستودع:
- `request.astro` → `src/pages/request.astro`
- `services.astro` → `src/pages/services.astro`
- `index.astro` → `src/pages/index.astro`
- `script.js` → `script.js` (في الجذر)
- `sitemap.xml` → `sitemap.xml` (في الجذر)

بعد رفع كل الملفات، اذهب لتبويب **Pull requests** في GitHub، ستجد زر أخضر **"Compare & pull request"**. اضغطه، راجع التعديلات (أخضر = مضاف، أحمر = محذوف)، ثم اضغط **Create pull request** ثم **Merge**.

---

### الخيار 2: عبر Git من الهاتف (Termux أو Working Copy)

```bash
# 1. نزّل المستودع (إذا ما هو موجود)
git clone https://github.com/albarshi996/albarshi_dl.git
cd albarshi_dl

# 2. أنشئ فرع جديد
git checkout -b fix/critical-bugs

# 3. انسخ ملفات الحزمة فوق الملفات القديمة (يدوياً أو cp)

# 4. ارفع التعديلات
git add .
git commit -m "إصلاحات حرجة: روابط sitemap + تصحيح فئات + حذف Layout مكرر"
git push origin fix/critical-bugs
```

بعدها GitHub سيعرض رابط لإنشاء Pull Request.

---

### الخيار 3: عبر الكمبيوتر

نفس الخيار 2 بس من الكمبيوتر.

---

## ✅ بعد الـ Merge

GitHub Pages سيعيد بناء الموقع تلقائياً خلال 1-3 دقائق.

تحقق من:
- [ ] صفحة /request: مدينة "إجخرة" ظاهرة في القائمة
- [ ] صفحة /request: فئتي "تجميل ونظافة" و"مواد بناء وصيانة" ظاهرتان
- [ ] صفحة /services: زر "اطلب منتجات تجميل" يفتح /request مع الفئة الصحيحة
- [ ] صفحة /services: زر "اطلب مواد بناء" يفتح /request مع الفئة الصحيحة
- [ ] أرسل طلب من نموذج /request → يفتح واتساب مرة واحدة فقط
- [ ] افتح https://dawerli.org.ly/sitemap.xml → الروابط بدون .html

---

## 🆘 إذا واجهت مشكلة

أرجع لي بصورة من الخطأ وسنحلها.
