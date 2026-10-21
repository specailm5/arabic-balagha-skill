# مهارة البلاغة والصورة
### (Arabic Balagha & Imagery Skill)

**Arabic rhetoric skill for AI agents** — analyzes and crafts simile, metaphor, metonymy, and rhetorical figures; diagnoses affectation, hyperbole, contradiction, and obscurity: `العلم كالنور` ← `العلم مصباح في زاوية معتمة`, `الموت يأخذ الناس` ← `الموت ينصب شباكه`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (المعاني والبيان والبديع والنماذج): [specailm5.github.io/arabic-balagha-skill](https://specailm5.github.io/arabic-balagha-skill/)**

> مهارة برمجية ولغوية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لتحليل الصورة البلاغية وصناعتها ونقدها، استناداً إلى **«جواهر البلاغة»** للسيد أحمد الهاشمي، و**«البلاغة الواضحة»** لعلي الجارم ومصطفى أمين، و**«أسرار البلاغة»** لعبد القاهر الجرجاني.

---

## 🎬 عرض توضيحي (Demo)

| قبل ❌ | بعد ✅ | التوجيه |
| :--- | :--- | :--- |
| «العلم كالنور» | «العلم مصباح في زاوية معتمة: لا يغيّر الغرفة، لكنه يمنعك من العثور على الباب» | تجديد الصورة المبتذلة |
| «الموت يأخذ الناس» | «الموت ينصب شباكه في الطرق التي لا نراها» | استعارة مكنية حسية |
| «كثير الرماد» | «كثير الرماد: لا يخبو ناره، ولا يخلو بيته من ضيف» | توضيح وسائط الكناية |
| «سيفه يقطع الجبال» | «سيفه يقطع ما تعجز عنه الجبال» | غلو ← مبالغة ممكنة |
| «كان كالليل في ضيائه» | «كان كالليل في سكونه، وكالنهار في ضيائه» | رفع التناقض |

---

## 📖 ما هي المهارة؟

**البلاغة** ليست قائمة مصطلحات تُحفظ، بل **مطابقة الكلام لمقتضى الحال**، ثم صورة تخدم المعنى. وكثير من النصوص «مزخرفة بلا أثر»: فيها تشبيه مبتذل، أو استعارة مقلوبة، أو كناية غامضة، أو سجع يقدّم اللفظ على المعنى.

تُمكِّنُ هذه المهارةُ الوكيلَ الذكيَّ من:

1. **تحليل الصورة:** النوع، الأركان، وجه الشبه، الوظيفة.
2. **صناعة الصورة:** من المعنى إلى المرساة الحسية إلى الصورة.
3. **نقد الصورة:** التكلف، الغلو، التناقض، فساد التأويل، التعقيد.
4. **البدائل:** ثلاث درجات: آمنة، متوسطة، جريئة.
5. **التمييز بين العلوم:** المعاني، البيان، البديع.

**القواعد الأربع:**
> **المعنى أولاً. مقتضى الحال. وجه شبه واحد. لا زينة بلا أثر.**

---

## 📂 بنية المهارة ومكوناتها

```
arabic-balagha-skill/
│
├── skills/arabic-balagha-skill/          # المهارة (تركيب Agent Skills القياسي)
│   ├── SKILL.md                          # الدليل الأساسي: التحليل والصناعة والنقد
│   ├── references/                       # المراجع التفصيلية
│   │   ├── maani.md                      # الخبر والإنشاء، التقديم، الحذف، القصر
│   │   ├── bayan.md                      # التشبيه، الاستعارة، الكناية، المجاز
│   │   ├── badii.md                      # الطباق، المقابلة، الجناس، السجع
│   │   ├── imagery_workshop.md           # ورشة الصورة
│   │   └── critique.md                   # نقد الصورة
│   └── examples/                         # دراسات الحالة والنماذج
│       ├── before_after_images.md        # نماذج قبل/بعد
│       └── analysis_examples.md          # تحليلات جاهزة
│
├── docs/                                 # الموقع المرجعي (GitHub Pages)
│
├── .agents/skills/arabic-balagha-skill/  # مسار Codex و Antigravity
│
└── .claude/skills/arabic-balagha-skill/  # مسار Claude Code
```

---

## 🚀 طرق التثبيت والاستخدام (Installation Guide)

تُثبَّتُ المهارةُ إما في مشروعٍ بعينه (**محلياً**)، وإما **عامةً (Global)** لتعمل في كافة المشاريع.

---

### أولاً: التثبيت بأمر واحد عبر `npx` (الطريقة الأسرع — موصى به)

```bash
npx skills add specailm5/arabic-balagha-skill -g -y
```

ولاختيار بيئات بعينها أو التثبيت داخل مشروع محدد:

```bash
npx skills add specailm5/arabic-balagha-skill -a claude-code -a codex
npx skills add specailm5/arabic-balagha-skill --skill arabic-balagha-skill -g -y
```

---

### ثانياً: التثبيت العام لبيئة Claude Code و Codex و Antigravity (يدوياً)

#### لنظام Windows (PowerShell):

```powershell
# مصدر المهارة داخل المستودع
$src = "skills\arabic-balagha-skill"

# 1. تثبيت لبيئة Claude Code
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-balagha-skill\"

# 2. تثبيت لبيئة Codex و Agent Skills العامة
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-balagha-skill\"

# 3. تثبيت لبيئة Google Antigravity / Gemini
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-balagha-skill\"
```

#### لنظام macOS / Linux (Bash):

```bash
src=skills/arabic-balagha-skill

# 1. لبيئة Claude Code
mkdir -p ~/.claude/skills/arabic-balagha-skill
cp -r "$src/." ~/.claude/skills/arabic-balagha-skill/

# 2. لبيئة Codex و Agent Harness
mkdir -p ~/.agents/skills/arabic-balagha-skill
cp -r "$src/." ~/.agents/skills/arabic-balagha-skill/

# 3. لبيئة Antigravity / Gemini
mkdir -p ~/.gemini/config/skills/arabic-balagha-skill
cp -r "$src/." ~/.gemini/config/skills/arabic-balagha-skill/
```

---

### ثالثاً: التثبيت المحلي داخل مشروع محدد (VS Code Workspace Harness)

إذا أردت حصر المهارة داخل مستودع أو مجلد عمل واحد في VS Code:

```powershell
# داخل مجلد مشروعك الحالي:
New-Item -ItemType Directory -Force -Path ".agents\skills\arabic-balagha-skill"
Copy-Item -Recurse -Force "path\to\skills\arabic-balagha-skill\*" ".agents\skills\arabic-balagha-skill\"
```

بمجرد فتح المشروع في **VS Code** أو تشغيل `Claude Code` / `Codex`، يكتشفُ الوكيلُ المهارةَ ويقرؤها من تلقاء نفسه عند صياغة أي نص باللغة العربية.

---

### رابعاً: الاستخدام اليدوي (Direct System Prompt / Custom Instructions)

إذا كنت تستخدم واجهات الويب (مثل ChatGPT أو Claude أو Gemini) مباشرة دون بيئة برمجية:

* افتح ملف [`skills/arabic-balagha-skill/SKILL.md`](skills/arabic-balagha-skill/SKILL.md) وانسخ محتواه وضعه في خانة **التعليمات المخصصة (Custom Instructions)** أو **System Prompt**.

---

## ⚡ كيف تعمل المهارة؟

### خمسة أسئلة قبل التحليل

| السؤال | لماذا؟ |
| :--- | :--- |
| **ما نوع النص؟** | شعر/نثر/خطبة/مقال/إعلان |
| **ما المطلوب؟** | تحليل/صياغة/تصحيح/مقارنة |
| **ما مستوى القارئ؟** | عمق المصطلح |
| **ما النبرة؟** | فخمة/رصينة/حديثة |
| **هل هناك قيد؟** | وزن/سجع/مصطلح/حساسية |

### العلوم الثلاثة

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

## 📚 المراجع والاعتماد

* **«جواهر البلاغة في المعاني والبيان والبديع»** — السيد أحمد الهاشمي — المكتبة العصرية:
  <https://archive.org/details/ar114rhet18>
* **«البلاغة الواضحة»** — علي الجارم ومصطفى أمين — دار المعارف:
  <https://archive.org/details/20210827_20210827_2340>
* **«أسرار البلاغة»** — عبد القاهر الجرجاني:
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

## 📜 الترخيص (License)

هذه المهارة مفتوحة المصدر ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم البلاغة العربية.
