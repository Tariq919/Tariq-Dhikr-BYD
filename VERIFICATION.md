# الفحوصات وحدود التوافق | Verification — 1.1.0

## العربية

اجتاز المشروع ١٣ نتيجة اختبار باستخدام Node.js، شملت المحتوى والترجمات وملصقات الواجهة بعشر لغات ونقل المفضلة والعدادات وتقسيم النصوص دون فقد. واختُبرت وظائف التأكيد والإلغاء والرجوع والإعدادات والوضع الليلي واختيار الشعور في بيئة DOM. لا تحل هذه الاختبارات محل فحص التطبيق على شاشة فعلية.

طُوبقت نصوص الآيات المائة مع سجلات QuranEnc، وطُوبقت الترجمات التسعمائة وحواشيها مع قواعد البيانات المنشورة. كما فُحص توافق JavaScript مع ES5 وتغطية الخطوط للحروف المستخدمة.

بُني ملف APK باستخدام أدوات Android SDK 35 وECJ وD8 بحد أدنى API 23، ثم ضُبطت محاذاته ووُقّع بمفتاح الإصدار السابق. فُحص التوقيع ومعرّف الحزمة ورقم الإصدار، وطُوبقت ملفات الواجهة والمحتوى والخطوط داخل APK مع ملفات المشروع. تظهر بصمة شهادة التوقيع في القسم الإنجليزي أدناه.

لم يُختبر الإصدار على شاشة BYD فعلية أو محاكي أندرويد، ولم يُنجز فحص Gradle وAndroid Lint كامل في بيئة البناء هذه. يتطلب التحقق من سلوك زر الرجوع والتخطيط واللمس والتقسيم الفعلي للنصوص وشاشة التوقف تجربة على الجهاز المستهدف. مشروع Gradle وملف سير العمل مرفقان بالمصدر؛ وجودهما داخل ملف ZIP لا يشغّل الفحوصات آليًا في مستودع التوزيع.

الترجمات التسع تخص الآيات القرآنية المائة. يبقى أرشيف الأذكار السابقة بالعربية. قوائم المشاعر فهرسة موضوعية للآيات، ولا تعِد بأثر نفسي محدد. لم تُجرَ مراجعة لغوية من متحدث أصلي لكل لغة في الواجهة، ولا يُنسب إلى التطبيق اعتماد شرعي مستقل.

لا تتضمن الحزمة العامة مفاتيح توقيع أو كلمات مرور. ولا يطلب التطبيق صلاحيات الإنترنت أو أنظمة المركبة، ولا يتضمن تحليلات استخدام.

## English

## Completed checks

- 13 Node test results pass: 12 core/content/localization/migration/ES5 tests plus the portable UI behavior test file.
- Content checks cover exactly 100 distinct complete Quran references, all nine translations per verse, every localized label in ten languages, mood coverage and filtering, favorites migration (including both verses of the former two-verse favorite), per-dhikr reset/cancel behavior, invalid saved state, navigation and lossless long-text pagination.
- UI behavior was exercised in a DOM harness with no NodeList.forEach: optional feeling selection, settings-first Back, confirm/cancel/back-out reset, one-counter persistence, each language/direction, translation attribution, night mode and screensaver isolation. These are DOM tests, not real-device or pixel-layout tests.
- All runtime JavaScript parses as ES5. The CSS uses flexbox and static fallbacks without CSS custom-property or NodeList iteration requirements. Arabic and Bengali fonts are embedded, with coverage checks for the selected Quran and Bengali translation characters.
- The 100 Arabic verse strings were compared to the QuranEnc API source records. All 900 translation/footnote pairs were compared to the distributed source databases. Stored texts are unchanged; translator note bold markers and encoded line breaks are rendered as plain text only.
- Android resources and Java were compiled with Android SDK 35 tools, ECJ and D8 at minimum API 23. APK was aligned and signed with the existing release key; APK signatures and package/version metadata were checked with apksigner and aapt2.
- The signed APK’s packaged UI/content/font files are compared byte-for-byte with this source tree before publication.
- Same release certificate as v1.0.0: SHA-256 `02db3c3a26f05a37515655ea1c9ad79e69044db79b66942f5ab29ae5dbb08b7a`. The preferences filename, key and package ID are unchanged. Old counters are retained by the migration tests.

## Limits

- Not tested on a physical BYD head unit or Android emulator. Native Back routing, touch ergonomics, actual text pagination, firmware-specific install restrictions, WebView rendering and DreamService availability still require target-device testing. DOM tests do not certify those behaviors.
- No full Gradle/Android-lint run was completed in this environment. The source archive includes the Gradle Wrapper and a CI workflow for those checks; a workflow inside the archive does not run automatically in the distribution repository.
- Quran topic/feeling associations are an editorial index, and does not promise a psychological outcome. Published translations are attributed to their publishers; no independent scholarly certification of the app or native-speaker review of every UI label is claimed.
- The traditional Arabic archive has detailed references and excerpt labels but does not include sourced translations. The nine-language translation guarantee applies to the 100 Quran verses.
- No signing key, password, network/vehicle permission or analytics is included in the public source or APK.
