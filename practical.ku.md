# پرسیارە کردەییەکان — ئامادەکاری بۆ مۆک و میدتێرم

> **لە مۆک و میدتێرمدا 4 پرسیاری کردەیی هەیە، هەر یەکەی 2 نمرە.** لە هەر
> یەکێکیاندا کارێکی بچووک لەسەر لاپتۆپەکەت دەکەیت، دەبینیت چی ڕوودەدات، و ئەو
> وەڵامە هەڵدەبژێریت کە لەگەڵیدا یەک دەگرێتەوە.

> ⚠️ **ئەم نموونانە وەک خۆیان نایەنەوە.** بەڵام هەموو پرسیارە کردەییەکان
> **تەنها بەم پێنج شێوازە** دێن، و ڕێک بە هەمان ڕێگا دەکرێن. تەنها
> وردەکارییەکان دەگۆڕێن.

> **هەموو کارەکان تەنها سەیرکردنن:** هیچ فایلێک ناگۆڕیت و هیچ شتێک پاشەکەوت
> ناکرێت.

> 💻 **تەنها لەسەر لاپتۆپ** — بە مۆبایل ناکرێن.

> 🔒 **لە ڕۆژی تاقیکردنەوەدا لاپەڕەی ڕێنماییەکان داخراوە.** ئەم لاپەڕەیە
> پێشوەختە بخوێنەوە، و پێنج شێوازەکە لە ماڵەوە بکە.

## پێداویستییەکان

- **لاپتۆپ و بارگەکەی.** ئەگەر شحنی لاپتۆپەکەت زوو دادەبەزێت، تەقسیمی
  کارەبایی بهێنە و نزیک پلاکی کارەبایی دابنیشە.
- **پرۆگرامەکان:** VS Code و Python و Chrome لەسەر لاپتۆپەکە — هەمان ئەوانەی
  هەنگاوی 1.
- **هەژماری زانکۆ:** Chrome ی سەر لاپتۆپەکە دەبێت بە ئیمەیڵی `@epu.edu.iq`
  چووبێتە ژوورەوە، چونکە فۆڕمەکە تەنها هەژماری زانکۆ وەردەگرێت. ئەگەر Google
  هەژمارێکی تر پیشان دا، **Switch account** بکە.
- **ئینتەرنێتی خۆت** بۆ لاپتۆپەکە، بۆ نموونە Hotspot ی مۆبایلەکەت، و باڵانسی
  بەس. مۆبایلەکە تەنها بۆ ئینتەرنێتە، نەک بۆ وەڵامدانەوە.
- **کۆپی تاقیکردنەوە:** فایلی `student-system-exam-step9.zip`، کە پێشوەختە لەم
  لینکەوە دابەزێنراوە: [لینکی دابەزاندنی کۆپی تاقیکردنەوە](https://drive.google.com/file/d/1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ/view?usp=drive_link)

## جارێک لە ماڵەوە، پێش مۆک

**1.** فایلی zip ـەکە لەم لینکەوە دابەزێنە:
[لینکی دابەزاندنی کۆپی تاقیکردنەوە](https://drive.google.com/file/d/1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ/view?usp=drive_link). لە لاپەڕەی Drive دوگمەی **Download**
دابگرە، کە لە سەرەوەی لای ڕاستە. ئەگەر Google داوای چوونەژوورەوەی کرد، بە
هەژماری زانکۆ بچۆرە ژوورەوە. پاشان کلیکی ڕاست لەسەر فایلەکە بکە ←
**Extract All** ← **Extract**. لە ناو فۆڵدەرە نوێیەکەدا فۆڵدەری
`student-system-exam` هەیە — ئەوە پڕۆژەکەیە.

**2.** لە VS Code: **File → Open Folder** ← فۆڵدەری `student-system-exam`
هەڵبژێرە.

**3.** مێنیوی **Terminal → New Terminal** بکەرەوە. کۆتایی دێڕی تێرمیناڵەکە
دەبێت `student-system-exam` بێت.

**4.** هەموو سێرڤەرێکی تر بوەستێنە: ئەگەر پڕۆژەکەی خۆت کار دەکات، لە
تێرمیناڵەکەی خۆیدا `Ctrl + C` دابگرە، یان پەنجەرەی VS Code ـەکەی دابخە. ئەگەر
دوو سێرڤەر هەبن هیچ هەڵەیەک دەرناکەوێت، بەڵام Chrome لاپەڕەی سێرڤەرە کۆنەکە
پیشان دەدات.

**5.** لە **تێرمیناڵی یەکەم** سێرڤەرەکە هەڵبکە، و ئیتر ئەم تێرمیناڵە دامەخە:

```bash
python app.py
```

```out
Server running at http://localhost:8000
Press Ctrl + C to stop.
```

**6.** **تێرمیناڵی دووەم** بکەرەوە، بە دوگمەی **+** لە سەرەوەی پانێڵی
تێرمیناڵ. فەرمانەکانی پرسیارەکان لێرەدا دەنووسیت، چونکە یەکەمیان سەرقاڵی
سێرڤەرەکەیە.

**7.** لە Chrome ئەم ناونیشانە بکەرەوە:

```
http://localhost:8000
```

دەبێت **ڕێک دوو قوتابی** ببینیت: **Sara Ali** و **Ahmad Karim**. ئەگەر ناوی تر
دەبینیت، سێرڤەری پڕۆژەکەی خۆت وەڵام دەداتەوە: هەنگاوی 4 دووبارە بکەرەوە.

**8.** پێنج شێوازەکەی خوارەوە و نموونەکانیان یەک یەک بکە. ئەمە ڕاهێنانەکەتە
بۆ مۆک و میدتێرم.

## لە ڕۆژی تاقیکردنەوەدا

> 🔒 لاپەڕەی ڕێنماییەکان داخراوە، بۆیە ئەمانە پێشوەختە بزانە.

**1.** لاپتۆپەکە بە بارگەوە. ئینتەرنێتەکەت هەڵبکە، و Chrome بە هەژماری زانکۆ.

**2.** لە VS Code فۆڵدەری `student-system-exam` بکەرەوە، و هەموو سێرڤەرێکی تر
بوەستێنە.

**3.** لە تێرمیناڵی یەکەم `python app.py` بنووسە. تێرمیناڵی دووەم بە **+**
بکەرەوە، بۆ فەرمانەکان.

**4.** لە Chrome دوو تاب بکەرەوە: یەکێکیان `http://localhost:8000`، کە دەبێت
Sara Ali و Ahmad Karim پیشان بدات، و ئەوی تریان فۆڕمی تاقیکردنەوەکە.

**5.** هەموو وەڵامێک لەسەر لاپتۆپ بدەرەوە. لە فۆڕمەکەدا ڕیزبەندیی وەڵامەکان
جیاوازە لە نموونەکانی ئێرە، بۆیە بە نووسینەکەیان هەڵیان بژێرە، نەک بە
پیتەکەیان.

**6.** کاتی داخستن لە سەرەوەی فۆڕمەکە نووسراوە: پێش ئەوە **Submit** دابگرە.

## ئەگەر کێشەیەک هات

| ئەوەی دەیبینیت | چی بکەیت |
|---|---|
| لە Chrome: `This site can’t be reached`، یان `ERR_CONNECTION_REFUSED` | سێرڤەرەکە کار ناکات. لە تێرمیناڵی یەکەم `python app.py` بنووسە. |
| لە `localhost:8000` ناوی تر جگە لە Sara Ali و Ahmad Karim | سێرڤەری پڕۆژەکەی خۆت وەڵام دەداتەوە. بیوەستێنە، بە `Ctrl + C` یان بە داخستنی پەنجەرەکەی، پاشان `F5`. |
| لە تێرمیناڵ: `can't open file ... app.py`، یان `No module named 'database'` | تێرمیناڵەکە لە فۆڵدەری `student-system-exam` دا نییە. فۆڵدەرەکە لە VS Code بکەرەوە و تێرمیناڵێکی نوێ بکەرەوە. |
| هەر شتێکی تر تێکچوو، یان فایلێک بە هەڵە گۆڕا | فۆڵدەرەکە بسڕەوە و zip ـەکە دووبارە Extract بکە. هەموو شتێک وەک سەرەتا دەگەڕێتەوە. |

## کارە بنەڕەتییەکان

- **کۆپیکردنی فەرمان:** لە فۆڕمەکەدا سێ جار بە خێرایی کلیک لەسەر فەرمانەکە
  بکە تا هەمووی هەڵبژێردرێت، و `Ctrl + C` دابگرە. پاشان لە تێرمیناڵی دووەمدا
  `Ctrl + V`، و لە کۆتاییدا `Enter`.
- **خوێندنەوەی هەڵە:** ئەگەر نووسینێکی سوور دەرکەوت کە بە `Traceback` دەست
  پێ دەکات، تەنها **دوایین دێڕ** ـەکەی بخوێنەوە. هۆی هەڵەکە لەوێ نووسراوە.
- **کردنەوەی ناونیشان:** لە شریتی ناونیشانی Chrome بینووسە یان Paste ی بکە،
  پاشان `Enter`.
- **ئامرازی Inspect:** کلیکی ڕاست ڕێک لەسەر ئەو بەشەی لاپەڕەکە بکە کە
  پرسیارەکە ناوی دەبات — لەسەر تاچپاد بە دوو پەنجە لێبدە — پاشان **Inspect**.
  بەشی **Styles** ڕێسا CSS ـەکانی ئەو بەشە پیشان دەدات.
- **نوێکردنەوەی لاپەڕە:** `F5`.

## پێنج شێوازەکە

بۆ هەر شێوازێک: چی دەپرسرێت، چی دەکەیت، و دوو نموونە بە وەڵامەکانیانەوە. نموونەکان لەسەر کۆپی تاقیکردنەوەکە ڕەن کراون، بۆیە ئەگەر خۆت بیانکەیت، ڕێک هەمان ئەنجام دەبینیت. پرسیار و بژاردە و وەڵامەکان بە ئینگلیزین، وەک لە تاقیکردنەوەدا دێن؛ ڕوونکردنەوەکان بە کوردین.

### شێوازی 1 — پرسین لە داتابەیس

**چی دەپرسرێت:** پرسیارەکە فەرمانێکی ئامادەی `python -c` ت پێ دەدات کە شتێک لە داتابەیسەکە دەخوێنێتەوە، و دەپرسێت چی دەنووسێت. ئەمە هەمان ڕێگای بەشەکانی 4.7 و 7.2.1 و 8.1.1 ی ڕێنماییەکەیە.

**چی دەکەیت:**

- فەرمانەکە لە پرسیارەکەوە کۆپی بکە.
- لە تێرمیناڵی دووەمدا Paste ی بکە و `Enter` دابگرە.
- ئەو دێڕەی دەینووسێت بخوێنەوە، و هەمان شت لە وەڵامەکاندا هەڵبژێرە.

<!-- en -->
**Example 1.** How many columns does the `students` table have? Run this command:

```bash
python -c "import database; print(len(database.get_connection().execute('PRAGMA table_info(students)').fetchall()))"
```

- Option A: `6`
- Option B: `7`
- Option C: `8`
- Option D: `9`
<!-- /en -->

**ئەوەی دەیبینیت:**

```out
8
```

> <!-- en -->
> **Answer:** Option C — `8`
> <!-- /en -->
> 
> فەرمانەکە `8` دەنووسێت: هەمان هەشت ستوونەکەی بەشی 4.4، لە `id` ـەوە تا `created_at`.

<!-- en -->
**Example 2.** Which department is the student whose `id` is 2 in? Run this command:

```bash
python -c "import database; print(database.get_student(2)['department'])"
```

- Option A: `MIS`
- Option B: `Accounting`
- Option C: `Management Information Systems`
- Option D: `Statistics`
<!-- /en -->

**ئەوەی دەیبینیت:**

```out
Accounting
```

> <!-- en -->
> **Answer:** Option B — `Accounting`
> <!-- /en -->
> 
> فەرمانەکە `Accounting` دەنووسێت. قوتابیی ژمارە 2 ـی خشتەکە Sara Ali ـیە، کە لە بەشی 7.2 دا بە بەشی `Accounting` زیاد کرا.

### شێوازی 2 — خوێندنەوەی دوایین دێڕی هەڵە

**چی دەپرسرێت:** پرسیارەکە فەرمانێکت پێ دەدات کە بە ئەنقەست هەڵەی تێدایە، و دەپرسێت هەڵەکە چی دەڵێت. ئەمە ئەوەیە کە بەشی 7.2 ی ڕێنماییەکە فێری دەکات: نووسینێکی سوور کە بە `Traceback` دەست پێ دەکات، و دوایین دێڕەکەی دەخوێنیتەوە.

**چی دەکەیت:**

- فەرمانەکە کۆپی بکە و لە تێرمیناڵی دووەمدا ڕەنی بکە.
- نووسینێکی سوور دەردەکەوێت. تەنها دوایین دێڕەکەی بخوێنەوە.
- ئەو وەڵامە هەڵبژێرە کە هەمان دوایین دێڕە.

<!-- en -->
**Example 1.** Run this command. What does the last line of the error say?

```bash
python -c "import database; print(database.get_connection().execute('SELECT * FROM student').fetchall())"
```

- Option A: `sqlite3.OperationalError: no such table: student`
- Option B: `sqlite3.OperationalError: no such column: student`
- Option C: `sqlite3.IntegrityError: UNIQUE constraint failed: students.student_id`
- Option D: `[]`
<!-- /en -->

**ئەوەی دەیبینیت:**

```out
sqlite3.OperationalError: no such table: student
```

> <!-- en -->
> **Answer:** Option A — `sqlite3.OperationalError: no such table: student`
> <!-- /en -->
> 
> ناوی خشتەکە `students` ـە، بە `s` ـەوە. فەرمانەکە `student` ی نووسیوە، بۆیە SQLite دەڵێت خشتەیەکی وا نییە.

<!-- en -->
**Example 2.** Run this command. What does the last line of the error say?

```bash
python -c "import database; print(database.get_student(5)['full_name'])"
```

- Option A: `TypeError: 'NoneType' object is not subscriptable`
- Option B: `IndexError: list index out of range`
- Option C: `KeyError: 'full_name'`
- Option D: `None`
<!-- /en -->

**ئەوەی دەیبینیت:**

```out
TypeError: 'NoneType' object is not subscriptable
```

> <!-- en -->
> **Answer:** Option A — `TypeError: 'NoneType' object is not subscriptable`
> <!-- /en -->
> 
> هیچ قوتابییەک `id` ی 5 نییە، بۆیە `get_student(5)` شتی `None` دەگەڕێنێتەوە، و `None['full_name']` ئەم هەڵەیە دەدات.

### شێوازی 3 — کردنەوەی ناونیشانێک

**چی دەپرسرێت:** پرسیارەکە ناونیشانێکت پێ دەدات، و دەپرسێت لاپەڕەکە چی پیشان دەدات. ئەمە ئەوەیە کە بەشەکانی 6.7 و 9.8 ی ڕێنماییەکە دەیکەن.

**چی دەکەیت:**

- دڵنیابە سێرڤەرەکە کار دەکات.
- ناونیشانەکە لە شریتی ناونیشانی Chrome دابنێ و `Enter` دابگرە.
- سەیری لاپەڕەکە بکە: سەردێڕەکەی و خانەکانی. ئەگەر لاپەڕەکە نەبێت، Chrome پەڕەی هەڵەی خۆی پیشان دەدات، کە `HTTP ERROR 404` ی تێدایە.

<!-- en -->
**Example 1.** With the server running, open this address. What is written in the **Full name** box?

```
http://localhost:8000/edit?id=2
```

- Option A: Ahmad Karim
- Option B: Sara Ali
- Option C: Nothing — the box is empty
- Option D: HTTP ERROR 404
<!-- /en -->

**ئەوەی دەیبینیت:**

فۆڕمی **Edit student** دەکرێتەوە، و لە خانەی Full name دا نووسراوە **Sara Ali**.

> <!-- en -->
> **Answer:** Option B — Sara Ali
> <!-- /en -->
> 
> `id=2` قوتابیی ژمارە 2 ـە، واتە Sara Ali. Edit فۆڕمەکە بە زانیارییەکانی ئەو پڕ دەکاتەوە — هەمان بەشی 9.8.

<!-- en -->
**Example 2.** Open this address, with no `?id=`. What is the page's heading?

```
http://localhost:8000/edit
```

- Option A: Edit student
- Option B: Register a new student
- Option C: HTTP ERROR 404
- Option D: Students
<!-- /en -->

**ئەوەی دەیبینیت:**

فۆڕمێکی بەتاڵ بە سەردێڕی **Register a new student**.

> <!-- en -->
> **Answer:** Option B — Register a new student
> <!-- /en -->
> 
> بەبێ `id`، کۆدەکە هیچ قوتابییەک ناخوێنێتەوە، بۆیە هەمان فۆڕمی تۆمارکردنی نوێ پیشان دەدات. بە `?id=9999` بوایە، `HTTP ERROR 404` دەبوو، وەک بەشی 9.8.

### شێوازی 4 — ئامرازی Inspect

**چی دەپرسرێت:** پرسیارەکە بەشێک لە لاپەڕەکە ناو دەبات، و دەپرسێت CSS ـەکەی چی دەڵێت. ئەمە ئەوەیە کە بەشی 6.6.1 ی ڕێنماییەکە فێری دەکات.

**چی دەکەیت:**

- لاپەڕەکە لە Chrome بکەرەوە.
- کلیکی ڕاست ڕێک لەسەر ئەو بەشە بکە کە پرسیارەکە ناوی دەبات ← **Inspect**.
- لە بەشی **Styles** ئەو ڕێسایە بدۆزەوە کە پرسیارەکە باسی دەکات، و بەهاکەی بخوێنەوە.

<!-- en -->
**Example 1.** On the home page the table's column headings are in capitals, like `FULL NAME`. Right-click one of them → **Inspect**. In Styles, which CSS line makes the letters capitals?

- Option A: `font-weight: bold`
- Option B: `text-transform: uppercase`
- Option C: `font-size: 13px`
- Option D: `color: #6b7280`
<!-- /en -->

**ئەوەی دەیبینیت:**

لە ڕێسای `thead th` دا: `text-transform: uppercase;`

> <!-- en -->
> **Answer:** Option B — `text-transform: uppercase`
> <!-- /en -->
> 
> `text-transform: uppercase` نووسینەکە بە پیتی گەورە پیشان دەدات، بەبێ ئەوەی HTML ـەکە بگۆڕێت: لە `list.html` دا هێشتا `Full name` نووسراوە.

<!-- en -->
**Example 2.** Right-click the big blue heading at the top, **Students** → **Inspect**. In Styles, what is its `font-size`?

- Option A: `16px`
- Option B: `20px`
- Option C: `24px`
- Option D: `32px`
<!-- /en -->

**ئەوەی دەیبینیت:**

لە ڕێسای `h1` دا: `font-size: 24px;`

> <!-- en -->
> **Answer:** Option C — `24px`
> <!-- /en -->
> 
> سەردێڕەکە `h1` ـە، و ڕێسای `h1` لە `style.css` دا `font-size: 24px` ی تێدایە.

### شێوازی 5 — تاقیکردنەوەی فۆڕم

**چی دەپرسرێت:** پرسیارەکە دەڵێت فۆڕمەکە چۆن پڕ بکەیتەوە، و دەپرسێت چی ڕوودەدات. ئەمە ئەوەیە کە بەشەکانی 8.9 و 9.8 ی ڕێنماییەکە دەیکەن.

**چی دەکەیت:**

- دڵنیابە سێرڤەرەکە کار دەکات و لاپەڕەی سەرەکی کراوەیە.
- فۆڕمەکە بکەرەوە، وەک پرسیارەکە دەڵێت: لینکی **Register a new student**، یان **Edit** لە تەنیشت قوتابییەک.
- خانەکان ڕێک وەک پرسیارەکە دەڵێت پڕ بکەرەوە، و دوگمەکە دابگرە.
- پەیامە سوورەکەی سەرەوەی فۆڕمەکە بخوێنەوە.

<!-- en -->
**Example 1.** Click **+ Register a new student**, and fill in the boxes like this:

- **Student ID:** `MIS-2025-001`
- **Full name:** `Test`
- **Department:** any one
- **Gender:** `Male`

Then press **Register student**. What appears?

- Option A: The student is added at the top of the list
- Option B: This student ID is already registered.
- Option C: The email address is not valid.
- Option D: Full name is required.
<!-- /en -->

**ئەوەی دەیبینیت:**

پەیامێکی سوور لە سەرەوەی فۆڕمەکە: **This student ID is already registered.** — و هیچ قوتابییەک زیاد ناکرێت.

> <!-- en -->
> **Answer:** Option B — This student ID is already registered.
> <!-- /en -->
> 
> `MIS-2025-001` ژمارەی Ahmad Karim ـە، و سێرڤەرەکە ژمارەی دووبارە ڕەت دەکاتەوە — هەمان بەشی 8.9.

<!-- en -->
**Example 2.** In the list, click **Edit** next to **Sara Ali**. Delete the name in the **Full name** box and type only one space — the Space key, once.

Then press **Save changes**. What appears?

- Option A: Sara's name becomes empty in the list
- Option B: Full name is required.
- Option C: This student ID is already registered.
- Option D: Student ID is required.
<!-- /en -->

**ئەوەی دەیبینیت:**

پەیامێکی سوور: **Full name is required.** — و ناوی Sara وەک خۆی دەمێنێتەوە.

> <!-- en -->
> **Answer:** Option B — Full name is required.
> <!-- /en -->
> 
> وێبگەڕەکە بۆشاییەک بە نووسین دەژمێرێت و ڕێگە دەدات، بەڵام سێرڤەرەکە بۆشاییەکانی سەرەتا و کۆتایی لادەبات (`strip`)، و ئیتر هیچ نامێنێت.
