# مصادر المحتوى | Content sources — 1.1.0

## العربية

يتضمن التطبيق ١٠٠ آية قرآنية كاملة ومختلفة. نُقل النص العربي من حقل `arabic_text` في واجهة QuranEnc، وأُرفقت بكل آية تسع ترجمات منشورة لمعانيها مع حواشي المترجم. يوضح الجدول أدناه أسماء الجهات والمترجمين وأرقام الإصدارات المعتمدة في هذه الحزمة.

جُمعت المصادر في ٢٦ أكتوبر ٢٠٢٦. تعود بيانات النسختين البنغالية والملايوية إلى فهرس QuranEnc السابق، وطُوبقت النصوص المختارة مع قواعد البيانات المنشورة لهما. تتضمن `app/src/main/assets/content.json` بيانات المصادر وبصمات قواعد البيانات.

تقتضي إعادة النشر الاحتفاظ بنصوص الترجمة وحواشيها وبيانات نسبتها إلى المصدر. تُراجع التصحيحات والإصدارات اللاحقة لدى المصدر، وتُرسل إليه ملاحظات الأخطاء. راجع [شروط QuranEnc](https://old.quranenc.com/ar/home) و[توثيق واجهته](https://quranenc.com/ar/home/api).

يقتصر تقسيم النصوص الطويلة على طريقة العرض؛ فضم الصفحات يعيد النص الأصلي دون فقد كلمات. تُميّز صفحات الترجمة عن صفحات النص العربي، ولا يُقصد بها ترجمة كل جزء عربي على حدة. يعرض خيار «النص والمصدر» الآية والترجمة والحواشي كاملة، مع تحويل علامات التنسيق إلى نص مقروء.

يضم الأرشيف العربي عشرين ذكرًا من الإصدار السابق، مع مراجع الكتب وأرقام الأحاديث وتمييز المقتطفات. لا يشمل الأرشيف ترجمات بلغات أخرى. ضُبط نص دعاء العافية وفق رواية أبي داود ٥٠٧٤. تُحفظ العدادات القديمة وتُربط المفضلة القرآنية بالآيات الكاملة المقابلة.

خَطّا Amiri وNoto Sans Bengali مضمنان بموجب رخصة SIL Open Font License. ملفات الرخص موجودة داخل `assets/fonts`، وتتوفر نسخة ثابتة من الخط البنغالي لتوافق أفضل مع إصدارات WebView القديمة.

## English

100 distinct, complete Quran verses are included. Arabic is copied verbatim from the `arabic_text` field of QuranEnc’s documented verse API. Each verse has nine published translations of meanings; translation text and footnotes are stored verbatim, with their published wording retained. Selection by feeling is an editorial topic index, not a claim that a verse guarantees a particular emotional outcome.

| Language | Published translation | Version | Source |
|---|---|---|---|
| en | English Translation - Rowwad Translation Center | 1.0.20 | QuranEnc.com |
| ur | Urdu Translation - Muhammad Junagarhi | 1.1.3 | QuranEnc.com |
| id | Indonesian Translation - Ministry of Religious Affairs | 1.0.1 | QuranEnc.com |
| bn | Bengali Translation — Dr. Abu Bakr Muhammad Zakaria | 1.1.1 | QuranEnc.com |
| tr | Turkish Translation - Rowwad Translation Center | 1.0.4 | QuranEnc.com |
| fa | Persian Translation - Rowwad Translation Center | 1.1.3 | QuranEnc.com |
| ms | Malay Translation — Abdullah Muhammad Basmeih | 1.0.0 | QuranEnc.com |
| fr | French Translation - Rachid Maach | 1.0.3 | QuranEnc.com |
| sw | Swahili Translation - Rowad Translation Center | 1.0.5 | QuranEnc.com |

Retrieved: 2026-10-26. Bengali and Malay edition metadata comes from QuranEnc’s legacy published catalogue; the selected records were checked against their distributed databases. The source snapshot and per-database SHA-256 are retained in `app/src/main/assets/content.json`.

## Attribution and permitted redistribution

Publisher and source: **QuranEnc.com** and the translation publishers named above. Edition names, versions, descriptions, translation text and footnotes are bundled. The app contains no ads. Translation text must not be edited, expanded or abridged; corrections and future editions should be obtained from the source, and issues should be reported to the source.

Terms: https://old.quranenc.com/ar/home (الشروط والسياسات). API documentation: https://quranenc.com/ar/home/api.

The display may paginate a verse or translation at whitespace boundaries; joining its pages reproduces the original string. Translation pages are identified separately and are not presented as translations of individual Arabic page fragments. The full verse, full translation and all supplied translator notes are available in “Full text and source”. Note line-break encoding and bold markup are rendered as plain text; no source words are removed.

The 20 traditional entries from version 1.0 remain in a separate **Arabic archive**, with detailed collection/number references and excerpt labels. Translations are not included for this archive. The short wellbeing supplication has been aligned with the wording of Abu Dawud 5074. Old Quran-excerpt favorites migrate to the corresponding full verses; all old traditional counters are retained.

## Fonts

Amiri Regular: Google Fonts / Amiri project, SIL Open Font License, bundled under `assets/fonts/OFL-Amiri.txt`. Noto Sans Bengali: Google Fonts / Noto project, SIL Open Font License, bundled under `assets/fonts/OFL-NotoSansBengali.txt`. A static regular instance is supplied for older WebViews.
