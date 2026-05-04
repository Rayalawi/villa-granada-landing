# فيلا غرناطة - Landing Page

صفحة هبوط عربية احترافية لعرض فيلا للبيع في حي غرناطة، الرياض. جاهزة لإطلاق حملة Google Ads.

---

## ملفات المشروع

```
villa-granada-landing/
├── index.html          ← الصفحة الرئيسية
├── privacy.html        ← سياسة الخصوصية (مطلوبة لـ Google Ads)
├── terms.html          ← الشروط والأحكام (مطلوبة لـ Google Ads)
├── styles.css          ← التصميم
└── images/             ← صور الفيلا (placeholders حالياً - استبدلها بالصور الحقيقية)
```

---

## ✅ ما يجب تعديله قبل النشر

افتح `index.html` و`privacy.html` و`terms.html` و`styles.css` وابحث/استبدل:

| المتغير | الموقع | غيّره إلى |
|---|---|---|
| `+966500000000` | جميع الملفات | رقم جوالك الحقيقي |
| `info@example.com` | privacy/terms/footer | بريدك الحقيقي |
| `REPLACE_WITH_YOUR_ID` | index.html (action="..."/) | معرّف نموذج Formspree |

### استبدال الصور
الصور الحالية في مجلد `images/` هي placeholders SVG. استبدلها بصور JPG حقيقية بنفس الأسماء:
- `exterior.jpg` (الواجهة الخارجية)
- `majlis.jpg` (المجلس)
- `kitchen.jpg` (المطبخ)
- `master-bedroom.jpg` (غرفة النوم الرئيسية)
- `living-room.jpg` (صالة الجلوس)
- `pool.jpg` (المسبح)
- `stairs.jpg` (الدرج)
- `hall.jpg` (الصالة)

ثم في `index.html` و`styles.css`، استبدل `.svg` بـ `.jpg`.

---

## 🚀 خطوات النشر السريع

### الخيار 1: Netlify (الأسهل والأسرع - مجاني)
1. اذهب إلى [netlify.com](https://www.netlify.com) وأنشئ حساب
2. اسحب وأفلت مجلد `villa-granada-landing` كاملاً في صفحة Sites
3. ستحصل على رابط فوراً (مثل `villa-granada.netlify.app`)
4. (اختياري) اربط دومين خاص

### الخيار 2: Vercel
1. ارفع المجلد إلى GitHub
2. اربطه بـ [vercel.com](https://vercel.com)

### الخيار 3: استضافة عادية
ارفع الملفات عبر FTP إلى أي استضافة تدعم HTML.

---

## 📝 نموذج الاستلام (Formspree)

1. سجّل في [formspree.io](https://formspree.io) (مجاني - 50 رسالة/شهر)
2. أنشئ نموذج جديد، انسخ الـ ID
3. في `index.html` استبدل `REPLACE_WITH_YOUR_ID` بالـ ID

البديل: استخدم Google Forms أو Typeform أو خدمة CRM مثل HubSpot.

---

## 📊 إعداد Google Ads

### قبل بدء الحملة
- [x] صفحة هبوط بمحتوى عربي واضح ✅ (جاهز)
- [x] سياسة خصوصية ✅ (جاهز - privacy.html)
- [x] شروط وأحكام ✅ (جاهز - terms.html)
- [x] معلومات تواصل واضحة ✅
- [x] CTAs واضحة (اتصل، واتساب، نموذج) ✅
- [x] Schema.org markup للعقار ✅
- [ ] الموقع منشور على دومين https
- [ ] Google Tag (gtag.js) مضاف للتتبع
- [ ] حساب Google Ads
- [ ] طريقة دفع
- [ ] تحقق من رقم الجوال للإعلان (verification)

### إضافة Google Tag وتتبع التحويلات
أضف هذا قبل `</head>` في `index.html` بعد إنشاء حساب Google Ads:

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=AW-XXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'AW-XXXXXXX');
</script>
```

ولتتبع نقرات الاتصال والواتساب، أضف `onclick` events بعد الإعداد.

### الكلمات المفتاحية المقترحة
- فيلا للبيع الرياض
- فيلا للبيع حي غرناطة
- عقارات الرياض
- فلل للبيع شمال الرياض
- فيلا فاخرة الرياض
- بيع فيلا حي غرناطة

### إعلان نصي مقترح (Google Ads)
**العنوان 1:** فيلا فاخرة للبيع - حي غرناطة
**العنوان 2:** 750م² · تشطيب راقي · 5.27 مليون
**العنوان 3:** اتصل الآن واحجز معاينتك
**الوصف 1:** فيلا دورين بمساحة بناء 620م² في موقع مميز بحي غرناطة. ملحقين + مسبح + شقة جانبية.
**الوصف 2:** قريبة من المدارس والأسواق. تشطيب جيد. مناسبة للسكن والاستثمار. السعر قابل للتفاوض.

---

## ⚙️ معاينة محلية

بسبب قيود sandbox على مجلد Downloads في macOS، قد لا يعمل خادم المعاينة الداخلي.
**للمعاينة:**
- افتح `index.html` مباشرة في المتصفح (double-click)، أو
- شغّل من Terminal:
  ```bash
  cd /Users/mac/Downloads/villa-granada-landing
  python3 -m http.server 8000
  ```
  ثم افتح: http://localhost:8000

---

## 🎯 ما التالي بعد النشر

1. **اربط Google Search Console** للمراقبة المجانية
2. **أضف Google Analytics 4** للتتبع
3. **أضف Meta Pixel** إذا أردت إعلانات Facebook/Instagram أيضاً
4. **اختبر الصفحة على الجوال** قبل البدء بالإعلان (>70% من الترافيك جوال)
5. **أنشئ نسخة فيديو قصيرة (15-30 ثانية)** من الفيلا لإعلانات YouTube/Reels
6. **حضّر بدائل** للصور والعناوين لاختبار A/B

---

أُعدّت الصفحة لتكون متوافقة مع متطلبات Google Ads (سياسة خصوصية واضحة، شروط، تواصل، محتوى أصلي عربي، تجربة استخدام جيدة، توافق جوال).
