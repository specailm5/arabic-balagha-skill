# مهارة البلاغة والصورة
### (Arabic Balagha & Imagery Skill)

**Arabic rhetoric skill for AI agents** — analyzes and crafts simile, metaphor, metonymy, and rhetorical figures; diagnoses affectation, hyperbole, contradiction, and obscurity; produces three levels of alternatives; and refuses to decorate a corrupt meaning. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي: [specailm5.github.io/arabic-balagha-skill](https://specailm5.github.io/arabic-balagha-skill/)**

> مهارة برمجية لتحليل الصورة البلاغية وصناعتها ونقدها، مبنية على **«جواهر البلاغة»** للسيد أحمد الهاشمي، و**«البلاغة الواضحة»** لعلي الجارم ومصطفى أمين، و**«أسرار البلاغة»** لعبد القاهر الجرجاني.

---

## 📖 ما هي المهارة؟

أربع وظائف:

1. **تحليل الصورة:** النوع، الأركان، وجه الشبه، الوظيفة.
2. **صناعة الصورة:** من المعنى إلى المرساة الحسية إلى الصورة.
3. **نقد الصورة:** التكلف، الغلو، التناقض، فساد التأويل، التعقيد.
4. **البدائل:** آمنة/متوسطة/جريئة، مع الحفاظ على المعنى.

**القواعد الأربع:**
> **المعنى أولاً. مقتضى الحال. وجه شبه واحد. لا زينة بلا أثر.**

---

## 📂 بنية المهارة

```
arabic-balagha-skill/
│
├── skills/arabic-balagha-skill/
│   ├── SKILL.md
│   ├── references/
│   │   ├── maani.md              # الخبر والإنشاء، التقديم، الحذف، القصر
│   │   ├── bayan.md              # التشبيه، الاستعارة، الكناية، المجاز
│   │   ├── badii.md              # الطباق، المقابلة، الجناس، السجع
│   │   ├── imagery_workshop.md   # ورشة الصورة
│   │   └── critique.md           # نقد الصورة
│   └── examples/
│       ├── before_after_images.md
│       └── analysis_examples.md
│
├── docs/
├── .agents/skills/arabic-balagha-skill/
└── .claude/skills/arabic-balagha-skill/
```

---

## 🚀 التثبيت

```bash
npx skills add specailm5/arabic-balagha-skill -g -y
```

أو لبيئات محددة:

```bash
npx skills add specailm5/arabic-balagha-skill -a claude-code -a codex
```

### يدوياً (Windows)

```powershell
$src = "skills\arabic-balagha-skill"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-balagha-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-balagha-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-balagha-skill\"
```

---

## ⚡ كيف تعمل؟

### خمسة أسئلة

| السؤال | لماذا؟ |
| :--- | :--- |
| **ما نوع النص؟** | شعر/نثر/خطبة/مقال/إعلان |
| **ما المطلوب؟** | تحليل/صياغة/تصحيح/مقارنة |
| **ما مستوى القارئ؟** | عمق المصطلح |
| **ما النبرة؟** | فخمة/رصينة/حديثة |
| **هل هناك قيد؟** | وزن/سجع/مصطلح/حساسية |

### الأنواع الثلاثة

| العلم | موضوعه | أمثلة |
| :--- | :--- | :--- |
| **المعاني** | مطابقة الكلام للمقام | الخبر/الإنشاء، التقديم، الحذف، القصر |
| **البيان** | إبراز المعنى بصور | التشبيه، الاستعارة، الكناية، المجاز |
| **البديع** | تحسين الكلام بعد مطابقته | الطباق، المقابلة، الجناس، السجع |

### ثلاث درجات للبديل

| الدرجة | مثال |
| :--- | :--- |
| **آمنة** | «الوقت يمضي كالماء» |
| **متوسطة** | «الوقت نهر لا يعود إلى منابعه» |
| **جريئة** | «الوقت حبل يُسحب من بين أصابعنا» |

### ما يفسد البلاغة

| العيب | العلاج |
| :--- | :--- |
| تكلف | احذف المحسن |
| غلو | اجعل المبالغة ممكنة |
| تناقض | وحّد وجه الشبه |
| فساد تأويل | اترك الظاهر |
| استعارة مقلوبة | أعد الأصل |
| تعقيد | أعد الترتيب |
| ابتذال | جدّد المرساة |

---

## 📚 المصادر

1. **«جواهر البلاغة في المعاني والبيان والبديع»** — السيد أحمد الهاشمي:
   <https://archive.org/details/ar114rhet18>
2. **«البلاغة الواضحة»** — علي الجارم ومصطفى أمين — دار المعارف:
   <https://archive.org/details/20210827_20210827_2340>
3. **«أسرار البلاغة»** — عبد القاهر الجرجاني:
   <https://archive.org/details/Asrar_Albalagha>

> **إقرار بالفضل:** هذه المهارة صياغة تعليمية مستقلة لمبادئ هذه الكتب، مع نقل قواعد وأمثلة بإسنادها إلى أبوابها. ولا يتضمّن المستودع نسخاً كاملة من الكتب، ولا يُغني عن الرجوع إلى الأصل.

---

## ⚠️ حدود المسؤولية

- المهارة **لتحليل الصورة وصناعتها ونقدها**، لا لتدريس البلاغة كاملاً.
- لا تُحسّن صورة فاسدة المعنى.
- بعض المسائل خلافية؛ يُذكر الخلاف ولا يُجزم.
- المستخدم مسؤول عن مراجعة النص النهائي.
- لا تُستخدم المهارة للإسفاف أو التجريح أو التحريض.

---

## 📜 الترخيص

هذه المهارة مفتوحة المصدر ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم البلاغة العربية.
