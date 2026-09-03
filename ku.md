# ڕێنمایی قوتابی (بەشی پراکتیکی) — ئامادەکردنی م.ادریس قادر



## ئەم بەڵگەنامەیە بۆ کێیە؟

بۆ قوتابییەک کە:

- **پێویستە ئەمانە فێر بێت** — HTML و CSS و Python و SQL
- **Visual Studio Code**ـی لەسەر کۆمپیوتەرەکەیەتی
- ویندۆزەکەی چالاکە و پێویستی بە ئەکتیڤ کردن نییە
- ئۆفیسەکەی چالاکە و پێویستی بە ئەکتیڤ کردن نییە

## چۆن بەکاری دەهێنیت

١. **بە ڕیزبەندی بڕۆ.** هەنگاو مەبەزێنە — هەر هەنگاوێک لەسەر ئەوەی پێشووی بنیات نراوە.
٢. **کۆدەکە بە دەست بنووسە**، کۆپی مەکە. مێشک بە نووسین فێر دەبێت.
٣. **دوای هەر هەنگاوێک تاقی بکەرەوە.** هەرگیز مەچۆ بۆ هەنگاوی داهاتوو تا ئەوەی ئێستا کاری نەکردووە.
٤. **ئەگەر هەڵەیەک دەرکەوت**، لە خشتەی خوارەوە سەیری هەڵە باوەکان بکە.

## پێکهاتەی هەر هەنگاوێک

| بەش | واتە |
|-----|------|
| **چی دەکەین** | ئەرکی ئەم هەنگاوە بە یەک ڕستە |
| **بۆچی** | مەبەستەکەی — بەبێ ئەمە تەنها کۆپی دەکەیت |
| **کۆدەکە** | کۆدی تەواو، نەک بەشێکی |
| **چۆن تاقی بکەینەوە** | ڕاستەوخۆ دوای نووسینەکە |
| **چی دەبینیت** | ئەنجامی چاوەڕوانکراو |
| **ئەگەر هەڵە دەرکەوت** | باوترین هەڵەکان و چارەسەریان |

---

## ڕیزبەندی هەنگاوەکان

| # | هەنگاو | دۆخ |
|---|--------|-----|
| ١ | ئامادەکردنی کۆمپیوتەر (Python) | ✅ |
| ٢ | فۆڵدەری پڕۆژە و پێکهاتەکەی | ✅ |
| ٣ | یەکەم سێرڤەر — «Hello» | ✅ |
| ٤ | داتابەیس (`database.py`) | ✅ |
| ٥ | Templates و فەنکشنی `render()` | ✅ |
| ٦ | CSS — دیزاینی پەڕەکان | ✅ |
| ٧ | **R** — پیشاندانی لیستی قوتابیان | ✅ |
| ٨ | **C** — فۆڕمی تۆمارکردن + پشکنین | ⏳ |
| ٩ | **U** — دەستکاریکردن | ⏳ |
| ١٠ | **D** — سڕینەوە | ⏳ |
| ١١ | گەڕان | ⏳ |
| ١٢ | پاراستن — SQL Injection و XSS | ⏳ |
| ١٣ | تاقیکردنەوەی کۆتایی و `run.bat` | ⏳ |

> ⏳ = هێشتا نەنووسراوە. ئەم بەڵگەنامەیە هەنگاو بە هەنگاو تەواو دەبێت.

---

# هەنگاوی ١ — کۆمپیوتەرەکە ئامادە بکە

> ئەم هەنگاوە هیچ پەیوەندییەکی بە پڕۆژەکەوە نییە. تەنها دڵنیا دەبینەوە کە
> ئامرازەکانمان هەن. جارێک دەیکەیت و هەرگیز دووبارەی ناکەیتەوە.

## چی دەکەین

دڵنیا دەبینەوە **Python** لەسەر کۆمپیوتەرەکە دابەزێنراوە.

## بۆچی

ڤیژوەڵ ستۆدیۆ کۆد تەنها **ئەدیتۆرێکە** — دەفتەرێکی نووسینە بۆ کۆد.
ناتوانێت کۆدەکەت کار پێبکات. ئەوەی کۆدی Python کار پێدەکات پڕۆگرامێکی
جیایە بە ناوی **Python** خۆی. پێویستمان بە هەردووکیانە.

---

## ١.١ — تێرمیناڵ لە VS Code بکەرەوە

VS Code بکەرەوە، پاشان لە مێنیوی سەرەوە:

**Terminal → New Terminal**

> کورتەڕێ: `Ctrl` + `` ` `` (ئەو دوگمەیەی لەژێر `Esc`ـە)

پەنجەرەیەکی تاریک لە خوارەوە دەکرێتەوە. ئەمە **تێرمیناڵە** — شوێنێک کە
فەرمان دەنووسیت، نەک کۆد.

## ١.٢ — پرسیار بکە ئایا Python هەیە

ئەمە بنووسە و `Enter` لێبدە:

```bash
python --version
```

## چی دەبینیت

**ئەگەر Python هەبێت** — شتێکی وەک ئەمە دەردەکەوێت:

```
Python 3.13.14
```

✅ تەواو بوویت. بڕۆ بۆ خاڵی ١.٤.

**ئەگەر Python نەبێت** — یەکێک لەم دووانە ڕوودەدات:

- پەیامی `'python' is not recognized...`
- یان **Microsoft Store** خۆکارانە دەکرێتەوە

لەم حاڵەتەدا بڕۆ بۆ خاڵی ١.٣.

---

## ١.٣ — دابەزاندنی Python (تەنها ئەگەر پێویست بوو)

١. بڕۆ بۆ <https://www.python.org/downloads/>
٢. کلیک لە دوگمە زەردەکە بکە (**Download Python 3.x**)
٣. فایلە دابەزێنراوەکە بکەرەوە

> ### ⚠️ گرنگترین خاڵی ئەم هەنگاوە
>
> لە یەکەم پەنجەرەی دابەزاندندا، **پێش** کلیککردن لە هیچ شتێک، لە خوارەوە
> چوارگۆشەیەک هەیە بە ناوی:
>
> **☑ Add python.exe to PATH**
>
> **دەبێت ئەم چوارگۆشەیە نیشان بکەیت.** ئەگەر نەیکەیت، تێرمیناڵ هەرگیز
> Python نادۆزێتەوە و دەبێت هەموو دابەزاندنەکە دووبارە بکەیتەوە.

٤. پاشان کلیک لە **Install Now** بکە و چاوەڕێ بکە
٥. **VS Code بە تەواوی دابخە و دووبارە بیکەرەوە** — بەبێ ئەمە تێرمیناڵی
   کراوە هێشتا نازانێت Python دابەزێنراوە
٦. تێرمیناڵێکی نوێ بکەرەوە و دووبارە `python --version` بنووسە

---

## ١.٤ — دڵنیابوونەوە لە داتابەیس

ئێستا ئەمە بنووسە:

```bash
python -c "import sqlite3; print('SQLite OK')"
```

دەبێت ئەمە دەربکەوێت:

```
SQLite OK
```

**واتای چییە؟** SQLite ئەو داتابەیسەیە کە زانیاری قوتابیانی تێدا پاشەکەوت
دەکەین. خۆشبەختانە **لەگەڵ Python خۆیدا دێت** — پێویست ناکات هیچی تر
دابەزێنیت. نە XAMPP، نە MySQL، نە phpMyAdmin.

---

## ئەگەر هەڵە دەرکەوت

| پەیامی هەڵە | چارەسەر |
|-------------|---------|
| `'python' is not recognized` | PATH دانەنراوە. Python دووبارە دابەزێنە و ئەم جارە `Add python.exe to PATH` نیشان بکە |
| Microsoft Store دەکرێتەوە | Windows ڕێگری دەکات. بڕۆ بۆ Settings → Apps → Advanced app settings → App execution aliases، پاشان `python.exe` بکوژێنەوە |
| `Python 2.7.x` دەردەکەوێت | وەشانێکی زۆر کۆنە. `python3 --version` تاقی بکەرەوە |
| هیچ ڕوونادات | دڵنیابە `Enter`ت لێداوە و لە تێرمیناڵدا نووسیوتە، نەک لە فایلێکی کۆد |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

ئەم دوو فەرمانە کاردەکەن و ئەنجام دەدەن:

```bash
python --version                                →  Python 3.x.x
python -c "import sqlite3; print('SQLite OK')"  →  SQLite OK
```

**هیچ فایلێکمان دروست نەکردووە، هیچ کۆدێکمان نەنووسیوە** — تەنها
کارگەکەمان ئامادە کرد.

---

# هەنگاوی ٢ — فۆڵدەری پڕۆژە

> هێشتا کۆد نانووسین. تەنها شوێنێک ئامادە دەکەین کە کۆدەکەی تێدا بنووسین.

## چی دەکەین

فۆڵدەرێک بۆ پڕۆژەکە دروست دەکەین و لە VS Codeدا دەیکەینەوە.

## بۆچی

پڕۆژەیەک لە ڕاستیدا **فۆڵدەرێکە** — هیچی تر. هەموو فایلەکان پێکەوە لە یەک
شوێندا دەمێننەوە، بۆیە دەتوانیت هەموو پڕۆژەکە کۆپی بکەیت یان بینێریت.

هەروەها VS Code لەسەر **فۆڵدەر** کاردەکات، نەک لەسەر یەک فایل. کاتێک
فۆڵدەرەکە دەکەیتەوە، تێرمیناڵ خۆکارانە لە ناو ئەو فۆڵدەرەدا دەکرێتەوە —
ئەمە لە هەنگاوی ٣دا زۆر گرنگ دەبێت.

---

## ٢.١ — فۆڵدەرەکە دروست بکە

لە **File Explorer**، شوێنێک هەڵبژێرە کە دواتر بەئاسانی بیدۆزیتەوە — بۆ
نموونە فۆڵدەری `Documents`.

کلیکی ڕاست لە شوێنێکی بەتاڵ → **New** → **Folder**

ناوی لێبنێ:

```
student-system
```

> ### ⚠️ ناوی فۆڵدەرەکە
>
> دوو یاسا هەن، و هەردووکیان گرنگن:
>
> - **بە ئینگلیزی بێت** — نەک بە کوردی
> - **بۆشایی تێدا نەبێت** — `student system` ❌ ، `student-system` ✅
>
> Python و تێرمیناڵ لەگەڵ ناوی کوردی و بۆشاییدا کێشەیان دروست دەبێت، و
> دۆزینەوەی ئەو کێشەیە بۆ دەستپێکەرێک زۆر سەختە.

## ٢.٢ — لە VS Code بیکەرەوە

VS Code بکەرەوە، پاشان:

**File → Open Folder…** → فۆڵدەرەکە هەڵبژێرە → **Select Folder**

ئەگەر پرسیاری کرد *«Do you trust the authors of the files in this folder?»*
کلیک لە **Yes, I trust the authors** بکە.

> ⚠️ **Open File** بەکارمەهێنە. دەبێت **Open Folder** بێت — ئەمە جیاوازییەکی
> گرنگە، نەک وردەکاری.

## ٢.٣ — دوو فۆڵدەری ناوەوە دروست بکە

لە لای چەپی VS Code (ئەمە پێی دەگوترێت **Explorer**) ناوی پڕۆژەکە دەبینیت:
`STUDENT-SYSTEM`. کاتێک ماوسی بەسەردا دەبەیت، چەند ئایکۆنێک دەردەکەون.

کلیک لە **New Folder** بکە (ئایکۆنی فۆڵدەر لەگەڵ نیشانەی `+`)، پاشان دوو
فۆڵدەر دروست بکە:

```
templates
static
```

**بۆچی دوو فۆڵدەری جیا؟**

| فۆڵدەر | چی دەچێتە ناوی | لە کام هەنگاودا |
|--------|-----------------|------------------|
| `templates` | فایلەکانی HTML — شێوەی پەڕەکان | هەنگاوی ٥ |
| `static` | فایلی CSS — ڕەنگ و دیزاین | هەنگاوی ٦ |

ئێستا بەتاڵن. لە هەنگاوەکانی داهاتوودا پڕیان دەکەینەوە.

---

## ٢.٤ — تاقیکردنەوە

تێرمیناڵێک بکەرەوە (**Terminal → New Terminal**) و ئەمە بنووسە:

```bash
dir
```

## چی دەبینیت

```
    Directory: C:\Users\...\Documents\student-system

Mode      Name
----      ----
d-----    static
d-----    templates
```

دوو شت بپشکنە:

١. **هەردوو فۆڵدەرەکە دەردەکەون** — `static` و `templates`
٢. **لە سەرەتای دێڕی تێرمیناڵدا** ناوی `student-system` دەبینیت — واتە لە
   شوێنی دروستدایت

خاڵی دووەم گرنگترە لەوەی وا دەزانیت. لە هەنگاوی ٣دا فەرمانێک دەنووسین کە
تەنها لەم فۆڵدەرەدا کاردەکات.

---

## ئەگەر هەڵە دەرکەوت

| کێشە | چارەسەر |
|------|---------|
| تێرمیناڵ ناوی فۆڵدەرێکی تر پیشان دەدات | فایلێکت کردووەتەوە، نەک فۆڵدەر. دووبارە **File → Open Folder** بکە |
| لای چەپ هیچ نابینم | `Ctrl + Shift + E` بۆ کردنەوەی Explorer |
| `dir` هیچ ناگەڕێنێتەوە | فۆڵدەرەکان دروست نەبوون. بگەڕێوە بۆ خاڵی ٢.٣ |
| `templates` لەناو `static`دایە | کلیکی ڕاست → **Delete**، پاشان دووبارە دروستیان بکە. دڵنیابە پێش کلیککردن لە **New Folder**، هیچ فۆڵدەرێکی تر هەڵنەبژێردراوە |
| ناوی فۆڵدەرەکە بە کوردی نووسیوە | کلیکی ڕاست → **Rename** → بیکە بە `student-system` |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

پێکهاتەکەت وا دەبێت:

```
student-system/
├── templates/
└── static/
```

دوو فۆڵدەری بەتاڵ لەناو فۆڵدەری پڕۆژەکەدا.

**هێشتا هیچ کۆدێکمان نەنووسیوە** — بەڵام ئێستا شوێنێکمان هەیە بۆ نووسینی.
لە هەنگاوی داهاتوودا یەکەم فایلی Python دەنووسین و یەکەم پەڕەمان لە
وێبگەڕدا دەبینین.

---

# هەنگاوی ٣ — یەکەم سێرڤەر

> ئەمە یەکەم کۆدە. لە کۆتایی ئەم هەنگاوەدا شتێک لە وێبگەڕەکەتدا دەبینیت
> کە خۆت دروستت کردووە.

## چی دەکەین

سێرڤەرێکی زۆر بچووک دەنووسین کە تەنها وشەی **Hello** پیشان دەدات.

## بۆچی

پێش ئەوەی داتابەیس و فۆڕم و خشتە زیاد بکەین، دەبێت **یەک شت** تێبگەین:

> سێرڤەر پڕۆگرامێکە کە چاوەڕێ دەکات، وێبگەڕ داوای شتێکی لێدەکات، و ئەویش
> وەڵامی دەداتەوە.

هەموو ئەوانەی تر — قوتابی، تۆمارکردن، گەڕان — تەنها زیادکردنن لەسەر ئەم
بیرۆکە سادەیە.

---

## ٣.١ — فایلی `app.py` دروست بکە

لە VS Code، لە Explorerـدا کلیک لە **New File** بکە (ئایکۆنی کاغەز لەگەڵ `+`).

ناوی لێبنێ:

```
app.py
```

> ### ⚠️ دوو خاڵ
>
> - **`.py` لەبیر مەکە** — ئەوە بە Python دەڵێت کە ئەمە فایلی کۆدە
> - **لە ناوەوەی `templates` یان `static` دایمەنێ** — دەبێت ڕاستەوخۆ لەناو
>   فۆڵدەری پڕۆژەکەدا بێت

## ٣.٢ — کۆدەکە بنووسە

```python app.py
from http.server import BaseHTTPRequestHandler, HTTPServer


class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write("<h1>Hello</h1>".encode("utf-8"))


server = HTTPServer(("localhost", 8000), StudentAppHandler)
print("Server running at http://localhost:8000")
print("Press Ctrl + C to stop.")
server.serve_forever()
```

**پاشەکەوتی بکە:** `Ctrl + S`

> ⚠️ VS Code خۆکارانە پاشەکەوت **ناکات**. ئەگەر لە ناوی تابەکەدا خاڵێکی
> سپی ● دەبینیت، واتە هێشتا پاشەکەوت نەکراوە.

<!-- collapse -->
## ٣.٣ — ئەم کۆدە چی دەکات؟

| دێڕ | چی دەکات |
|-----|-----------|
| `from http.server import ...` | ئەو سێرڤەرە دەهێنێت کە لەگەڵ Python خۆیدا دێت |
| `class StudentAppHandler` | ئەم بەشە بڕیار دەدات چۆن وەڵامی داواکارییەکان بدرێتەوە |
| `def do_GET(self)` | ئەم فەنکشنە کاردەکات **هەر کاتێک** وێبگەڕ داوای پەڕەیەک بکات |
| `send_response(200)` | `200` واتە «باشە، هەموو شتێک ڕێکە» |
| `send_header("Content-Type"...)` | بە وێبگەڕ دەڵێت: ئەمە HTMLـە، و پیتەکانی بە UTF-8ن |
| `end_headers()` | کۆتایی زانیارییەکانی سەرەوە |
| `wfile.write(...)` | ناوەڕۆکی پەڕەکە دەنێرێت |
| `.encode("utf-8")` | دەق دەکاتە بایت — سێرڤەر بایت دەنێرێت، نەک دەق |
| `HTTPServer(("localhost", 8000), ...)` | لە کوێ و لە کام پۆرتدا گوێ بگرێت |
| `serve_forever()` | بەردەوام چاوەڕێ بکە — هەرگیز مەوەستە |

> **`charset=utf-8` زۆر گرنگە.** بەبێ ئەو، پیتی کوردی وەک `Ø¨Ø§` دەردەکەوێت.

---

## ٣.٤ — کاری پێبکە

لە تێرمیناڵدا:

```bash
python app.py
```

## چی دەبینیت

لە تێرمیناڵدا:

```
Server running at http://localhost:8000
Press Ctrl + C to stop.
```

پاشان **هیچ**. تێرمیناڵ وەستاوە و ناتوانیت هیچی تر بنووسیت.

> ### ⚠️ ئەمە هەڵە نییە
>
> ئەمە باوترین سەرلێشێواوییە لەم هەنگاوەدا. تێرمیناڵ **نەوەستاوە** —
> سێرڤەرەکە کاردەکات و چاوەڕێی داواکاری دەکات.
>
> سێرڤەرێک هەرگیز «تەواو نابێت». تا ئەو کاتەی تۆ نەیوەستێنیت، کاردەکات.

## ٣.٥ — لە وێبگەڕدا بیکەرەوە

وێبگەڕێک بکەرەوە و ئەمە بنووسە:

```
http://localhost:8000
```

دەبێت ئەمە ببینیت:

# Hello

**پیرۆزە** — یەکەم سێرڤەرت کاردەکات.

هەروەها سەیری تێرمیناڵ بکە: ئێستا دێڕێکی نوێ زیاد بووە کە داواکارییەکە
پیشان دەدات.

## ٣.٦ — بیوەستێنە

بگەڕێوە بۆ تێرمیناڵ و `Ctrl + C` دابگرە.

ئێستا تێرمیناڵ دەگەڕێتەوە بۆ دۆخی ئاسایی.

---

## ٣.٧ — تاقیکردنەوەیەکی گرنگ

ئەم تاقیکردنەوەیە شتێکت فێر دەکات کە دواتر زۆر بەکاردێت:

١. لە کۆدەکەدا `Hello` بگۆڕە بۆ ناوی خۆت
٢. `Ctrl + S` پاشەکەوتی بکە
٣. بڕۆ بۆ وێبگەڕ و `F5` لێبدە

**هیچ ناگۆڕێت.** بۆچی؟

چونکە سێرڤەرەکە هێشتا کۆدە کۆنەکە لە بیریدایە. دەبێت:

١. `Ctrl + C` — بیوەستێنە
٢. `python app.py` — دووبارە کاری پێبکە
٣. `F5` لە وێبگەڕدا

**ئێستا ناوەکەت دەبینیت.**

> **یاسا:** هەر گۆڕانکارییەک لە `app.py`دا، دەبێت سێرڤەرەکە بوەستێنیت و
> دووبارە کاری پێبکەیت. لەم هەنگاوەوە تا کۆتایی، ئەمە دووبارە دەکەیتەوە.

---

## ئەگەر هەڵە دەرکەوت

| پەیامی هەڵە | چارەسەر |
|-------------|---------|
| `can't open file 'app.py'` | لە فۆڵدەری هەڵەدایت. تێرمیناڵ دابخە و **File → Open Folder** دووبارە بکە |
| `[WinError 10048]` یان `address already in use` | سێرڤەرێک پێشتر کاردەکات. تێرمیناڵە کۆنەکە بدۆزەرەوە و `Ctrl + C` لێبدە |
| `IndentationError` | بۆشایی سەرەتای دێڕەکان ڕێک نییە. Python زۆر وردە — ٤ بۆشایی بەکاربهێنە، نەک Tab |
| `SyntaxError` | پیتێک یان کەوانەیەک کەمە. دێڕی ناو پەیامەکە بپشکنە |
| **This site can't be reached** | سێرڤەرەکە کارناکات. سەیری تێرمیناڵ بکە |
| پیتی کوردی وەک `Ø¨Ø§` دەردەکەوێت | `charset=utf-8` لە `Content-Type`دا نییە |
| گۆڕانکارییەکەم دیار نییە | سێرڤەرەکەت دووبارە نەکردەوە (بڕوانە ٣.٧) |
| خاڵێکی سپی ● لە تابەکەدایە | فایلەکە پاشەکەوت نەکراوە. `Ctrl + S` |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

```
student-system/
├── app.py          ← نوێ
├── templates/
└── static/
```

- `python app.py` سێرڤەرەکە هەڵدەستێنێت
- `http://localhost:8000` دەقێک پیشان دەدات
- `Ctrl + C` دەیوەستێنێت
- دەزانیت کە دوای هەر گۆڕانکارییەک، دەبێت دووبارە کاری پێبکەیت

**ئێستا سێرڤەرێکت هەیە.** لە هەنگاوی داهاتوودا داتابەیسەکە دروست دەکەین —
ئەو شوێنەی زانیاری قوتابیانی تێدا دەمێنێتەوە.

---

# هەنگاوی ٤ — داتابەیس

> لە کۆتایی ئەم هەنگاوەدا فایلێکی نوێ لە پڕۆژەکەتدا دەردەکەوێت کە خۆت
> دروستت نەکردووە — داتابەیسەکە.

## چی دەکەین

فایلی `database.py` دەنووسین و خشتەی `students` دروست دەکەین.

## بۆچی فایلێکی جیا؟

دەمانتوانی هەموو شتێک بخەینە ناو `app.py`ـەوە. بەڵام:

| فایل | ئەرکی |
|------|-------|
| `app.py` | بەشی وێب — پەڕەکان، فۆڕمەکان، بڕیارەکان |
| `database.py` | بەشی داتا — خشتەکە، خوێندنەوە، نووسین |

**سوودەکەی:** ئەگەر ڕۆژێک بمانەوێت لە SQLiteـەوە بچینە بۆ MySQL، تەنها یەک
فایل دەگۆڕین. `app.py` هیچی لێ ناگۆڕدرێت.

ئەمە هەمان بیرۆکەی **جیاکردنەوەی ئەرکەکانە** کە لە وانەی تیۆریدا باسکراوە.

---

## ٤.١ — فایلی `database.py` دروست بکە

لە VS Code، **New File** → ناوی لێبنێ:

```
database.py
```

لە هەمان شوێنی `app.py` بێت — ڕاستەوخۆ لەناو فۆڵدەری پڕۆژەکە.

## ٤.٢ — کۆدەکە بنووسە

```python database.py
import os
import sqlite3

DB_PATH = os.path.join(os.path.dirname(os.path.abspath(__file__)), "students.db")


def get_connection():
    connection = sqlite3.connect(DB_PATH)
    connection.row_factory = sqlite3.Row
    return connection


def init_db():
    with get_connection() as connection:
        connection.execute(
            """
            CREATE TABLE IF NOT EXISTS students (
                id          INTEGER PRIMARY KEY AUTOINCREMENT,
                student_id  TEXT NOT NULL UNIQUE,
                full_name   TEXT NOT NULL,
                department  TEXT NOT NULL,
                gender      TEXT NOT NULL,
                email       TEXT,
                phone       TEXT,
                created_at  TEXT NOT NULL DEFAULT (datetime('now', 'localtime'))
            )
            """
        )
```

`Ctrl + S` پاشەکەوتی بکە.

<!-- collapse -->
## ٤.٣ — ئەم کۆدە چی دەکات؟

| بەش | چی دەکات |
|-----|-----------|
| `import sqlite3` | داتابەیسەکە دەهێنێت — لەگەڵ Python خۆیدا دێت |
| `DB_PATH = os.path.join(...)` | ڕێڕەوی فایلی داتابەیس |
| `os.path.dirname(os.path.abspath(__file__))` | «هەمان فۆڵدەری ئەم فایلە» |
| `sqlite3.connect(DB_PATH)` | پەیوەندی دەکات — **ئەگەر فایلەکە نەبێت، دروستی دەکات** |
| `row_factory = sqlite3.Row` | ڕێگە دەدات ستوونەکە بە ناوەکەی بخوێنینەوە: `row["full_name"]` |
| `with get_connection() as ...` | دوای تەواوبوون، خۆی گۆڕانکارییەکان پاشەکەوت دەکات |
| `CREATE TABLE IF NOT EXISTS` | خشتەکە دروست دەکات — **ئەگەر پێشتر نەبووبێت** |

> **بۆچی `os.path.dirname(...)`؟**
> بەبێ ئەو، داتابەیسەکە لەو فۆڵدەرەدا دروست دەبێت کە تێرمیناڵ لێیەوە
> کاردەکات — نەک لەتەنیشت کۆدەکە. ئەمە هۆکاری هەڵەیەکی زۆر باوە:
> داتابەیسێک هەیە، بەڵام بەتاڵە، چونکە فایلێکی تری هەمان ناوە.

<!-- collapse -->
## ٤.٤ — ستوونەکان

| ستوون | جۆر | واتای |
|-------|-----|-------|
| `id` | INTEGER | ژمارەی ناوخۆیی، خۆی زیاد دەبێت |
| `student_id` | TEXT | ژمارەی زانکۆیی — **ناکرێت دووبارە بێتەوە** |
| `full_name` | TEXT | ناوی تەواو — پێویستە |
| `department` | TEXT | بەش — پێویستە |
| `gender` | TEXT | ڕەگەز — پێویستە |
| `email` | TEXT | دەکرێت بەتاڵ بێت |
| `phone` | TEXT | دەکرێت بەتاڵ بێت |
| `created_at` | TEXT | کاتی تۆمارکردن — خۆکارانە پڕ دەبێتەوە |

> **ژمارەی تەلەفۆن بۆچی `TEXT`ـە نەک `INTEGER`؟**
> چونکە `0770` سەرەتای سفرەکەی لەدەست دەدات، و هەندێک ژمارە `+` یان بۆشایی
> تێدایە. ژمارەیەک کە هەرگیز کۆی ناکەیتەوە، ژمارە نییە — دەقە.

---

## ٤.٥ — بەستنەوەی بە `app.py`

`database.py` بە تەنها هیچ ناکات — کەس بانگی نەکردووە. لە `app.py`دا
**دوو دێڕ** زیاد بکە:

```python app.py
from http.server import BaseHTTPRequestHandler, HTTPServer

import database                                    # ← نوێ


class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write("<h1>Hello</h1>".encode("utf-8"))


database.init_db()                                 # ← نوێ
server = HTTPServer(("localhost", 8000), StudentAppHandler)
print("Server running at http://localhost:8000")
print("Press Ctrl + C to stop.")
server.serve_forever()
```

`Ctrl + S` هەردوو فایلەکە پاشەکەوت بکە.

## ٤.٦ — تاقیکردنەوە

```bash
python app.py
```

## چی دەبینیت

سەیری **Explorer**ی VS Code بکە. فایلێکی نوێ دەردەکەوێت:

```
student-system/
├── app.py
├── database.py
├── students.db     ← نوێ، خۆکارانە
├── templates/
└── static/
```

**ئەمە داتابەیسەکەتە.** فایلێکی ئاسایی — دەتوانیت کۆپی بکەیت، بینێریت،
یان بیسڕیتەوە.

`Ctrl + C` بۆ وەستاندن.

## ٤.٧ — دڵنیابوونەوەی ورد

بۆ ئەوەی دڵنیا ببیت خشتەکە بەڕاستی دروست بووە، ئەمە لە تێرمیناڵدا بنووسە:

```bash
python -c "import database; print([r['name'] for r in database.get_connection().execute('SELECT name FROM sqlite_master')])"
```

دەبێت ئەمە دەربکەوێت:

```
['students', 'sqlite_autoindex_students_1', 'sqlite_sequence']
```

یەکەمیان خشتەکەی خۆمانە. ئەو دووانەی تر SQLite خۆی دروستی کردوون — یەکێک
بۆ `UNIQUE` و یەکێک بۆ `AUTOINCREMENT`.

---

## ⚠️ خاڵێک کە دواتر سەری لێدەشێوێنیت

`CREATE TABLE IF NOT EXISTS` تەنها کاردەکات ئەگەر خشتەکە **نەبووبێت**.

ئەگەر دواتر ستوونێک زیاد بکەیت یان بگۆڕیت، پاشان دووبارە کاری پێبکەیت:

> **هیچ ناگۆڕێت.** چونکە خشتەکە پێشتر هەیە، و SQLite دەڵێت «باشە، هەیە» و
> تێپەڕ دەبێت.

**چارەسەرەکە:** فایلی `students.db` بسڕەوە و دووبارە `python app.py` بکە.
خشتەیەکی نوێ بە پێکهاتەی نوێوە دروست دەبێت.

> لە کاتی فێربووندا ئەمە هیچ کێشەیەک نییە — هێشتا داتای گرنگت تێدا نییە.

---

## ئەگەر هەڵە دەرکەوت

| پەیامی هەڵە | چارەسەر |
|-------------|---------|
| `ModuleNotFoundError: No module named 'database'` | ناوی فایلەکە دروست نییە، یان لە فۆڵدەرێکی ترە. دەبێت `database.py` بێت، لەتەنیشت `app.py` |
| `sqlite3.OperationalError: near "..."` | هەڵەیەکی نووسین لە SQLەکەدا. کۆمای `,` نێوان ستوونەکان بپشکنە |
| `students.db` دەرنەکەوت | `database.init_db()`ت زیاد نەکردووە، یان `python app.py`ت نەکردووە |
| `no such table: students` | `init_db()` بانگ نەکراوە پێش بەکارهێنانی خشتەکە |
| ستوونێکم گۆڕی، بەڵام هیچ نەگۆڕا | خشتەکە پێشتر هەیە. `students.db` بسڕەوە (بڕوانە سەرەوە) |
| `IndentationError` | بۆشاییەکان ڕێک نین. ٤ بۆشایی بەکاربهێنە |
| فایلەکە لە Explorerدا نابینم | `Ctrl + Shift + E`، یان کلیکی ڕاست → **Refresh Explorer** |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

```
student-system/
├── app.py          ← دوو دێڕی نوێی تێدایە
├── database.py     ← نوێ
├── students.db     ← خۆکارانە دروست بوو
├── templates/
└── static/
```

- خشتەی `students` بوونی هەیە
- دەزانیت بۆچی داتا لە فایلێکی جیادایە
- دەزانیت ئەگەر خشتەکە بگۆڕیت، دەبێت `students.db` بسڕیتەوە

**ئێستا شوێنێکمان هەیە بۆ هەڵگرتنی زانیاری** — بەڵام هێشتا بەتاڵە، و
پەڕەکەشمان هێشتا `Hello` دەڵێت. لە هەنگاوی داهاتوودا فێر دەبین چۆن
پەڕەیەکی ڕاستەقینە دروست بکەین.

---

# هەنگاوی ٥ — Templates

> لەم هەنگاوەدا HTML لە کۆدی Python دەردەهێنین. ئەمە یەکێکە لە گرنگترین
> بیرۆکەکانی وێب.

## چی دەکەین

فایلی HTML جیا دەنووسین، و فەنکشنێک دەنووسین کە پڕیان دەکاتەوە.

## بۆچی

ئێستا HTMLـەکەمان لەناو Pythonـدایە:

```python
self.wfile.write("<h1>Hello</h1>".encode("utf-8"))
```

بۆ یەک دێڕ باشە. بەڵام پەڕەیەکی ڕاستەقینە ١٠٠ دێڕی HTMLـە. بیربکەرەوە:

- دیزاینەر ناتوانێت کاری تێدا بکات — کۆدی Pythonـە
- گۆڕینی ڕەنگێک واتە دەستکاریکردنی فایلی لۆژیک
- هیچ ئامرازێک ناتوانێت HTMLـەکەت بپشکنێت

**چارەسەرەکە:** HTML لە فایلی خۆیدا بمێنێتەوە، و شوێنی گۆڕاوەکان بە
`{{ ناو }}` نیشان بکەین.

---

## ٥.١ — `templates/layout.html`

لە VS Code، کلیک لەسەر فۆڵدەری `templates` بکە، پاشان **New File**:

```
layout.html
```

ئەمە بنووسە:

```html templates/layout.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ title }}</title>
</head>
<body>
  <h1>{{ title }}</h1>
  {{ content }}
</body>
</html>
```

**ئەمە چوارچێوەیە.** هەموو پەڕەکان هەمان سەرەوە و خوارەوەیان هەیە — تەنها
ناوەڕۆکەکەیان دەگۆڕێت.

> `<meta charset="UTF-8">` هەمان ئەرکی `charset=utf-8`ی هەنگاوی ٣ دەبینێت،
> بەڵام ئەم جارە لەناو خودی HTMLەکەدا.

## ٥.٢ — `templates/home.html`

فایلێکی تر لە هەمان فۆڵدەردا:

```html templates/home.html
<p>Welcome to the Student Registration System.</p>
<p>Students registered: {{ total }}</p>
```

**ئەمە ناوەڕۆکی پەڕەی سەرەکییە** — بەبێ `<html>` و `<body>`، چونکە ئەوانە
لە `layout.html`دان.

## ٥.٣ — فەنکشنی `render()`

لە `app.py`دا، ئەمانە زیاد بکە. سەرەتا لە سەرەوە:

```python app.py
import os
import re
from http.server import BaseHTTPRequestHandler, HTTPServer

import database

BASE_DIR = os.path.dirname(os.path.abspath(__file__))
TEMPLATE_DIR = os.path.join(BASE_DIR, "templates")


def render(template_name, **values):
    path = os.path.join(TEMPLATE_DIR, template_name)
    with open(path, encoding="utf-8") as file:
        page = file.read()

    def replace(match):
        return str(values.get(match.group(1), ""))

    return re.sub(r"\{\{\s*(\w+)\s*\}\}", replace, page)
```

## ٥.٤ — بەکارهێنانی

`do_GET` بگۆڕە بۆ ئەمە:

```python app.py
class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        body = render("home.html", total=0)
        page = render("layout.html", title="Students", content=body)

        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(page.encode("utf-8"))
```

**دوو جار بانگی دەکەین:**

١. `home.html` پڕ دەکەینەوە → دەبێتە ناوەڕۆک
٢. ئەو ناوەڕۆکە دەخەینە ناو `layout.html`ـەوە → دەبێتە پەڕەی تەواو

<!-- collapse -->
## ٥.٥ — ئەم کۆدە چۆن کاردەکات؟

| بەش | چی دەکات |
|-----|-----------|
| `**values` | ڕێگە دەدات چەند نرخێک بنێریت: `render("home.html", total=0)` |
| `open(path, encoding="utf-8")` | فایلەکە دەخوێنێتەوە |
| `re.sub(pattern, replace, page)` | بەدوای هەموو `{{ ناو }}`ـێکدا دەگەڕێت و دەیگۆڕێت |
| `\{\{\s*(\w+)\s*\}\}` | ئەم شێوەیە دەدۆزێتەوە: دوو کەوانە، ناوێک، دوو کەوانە |
| `\s*` | ڕێگە دەدات بۆشایی هەبێت: `{{title}}` و `{{ title }}` هەردووکیان کاردەکەن |
| `match.group(1)` | ئەو ناوەی نێوان کەوانەکان — بۆ نموونە `title` |
| `values.get(name, "")` | نرخەکەی دەدۆزێتەوە. ئەگەر نەبوو، بۆشایی دادەنێت |

> **`\w+` واتای چییە؟** یەک یان زیاتر پیت، ژمارە، یان `_`. بۆیە
> `{{ full_name }}` کاردەکات، بەڵام `{{ full name }}` نا.

---

## ٥.٦ — تاقیکردنەوە

```bash
python app.py
```

پاشان `http://localhost:8000`

## چی دەبینیت

# Students

Welcome to the Student Registration System.

Students registered: 0

> بۆ ئەوەی بزانیت بەڕاستی HTMLـە، کلیکی ڕاست بکە → **View page source**.
> دەبێت هەموو ئەو `<html>` و `<head>`ـە ببینیت کە لە `layout.html`دا
> نووسیوتە، بەڵام `{{ title }}` بووە بە `Students`.

---

## ٥.٧ — شتێکی خۆش

سێرڤەرەکە **مەوەستێنە**. `home.html` بکەرەوە و دەقەکەی بگۆڕە:

```html templates/home.html
<p>Hello from my own page!</p>
<p>Students registered: {{ total }}</p>
```

پاشەکەوتی بکە و لە وێبگەڕدا تەنها `F5` لێبدە.

**گۆڕانکارییەکە دەردەکەوێت** — بەبێ ئەوەی سێرڤەرەکە دووبارە بکەیتەوە.

**بۆچی؟** چونکە `render()` فایلەکە **لە هەر داواکارییەکدا** دەخوێنێتەوە.
بەڵام کۆدی Python تەنها یەک جار دەخوێنرێتەوە، لە کاتی هەڵسانی سێرڤەرەکەدا.

| چی دەگۆڕیت | پێویستە سێرڤەر دووبارە بکەیتەوە؟ |
|-------------|----------------------------------|
| `templates/*.html` | **نەخێر** — تەنها `F5` |
| `app.py` یان `database.py` | **بەڵێ** |

---

## ⚠️ هەڵەیەک کە بەڕاستی ڕوویدا

کاتێک ئەم پڕۆژەیە دروست دەکرا، لەناو `layout.html`دا کۆمێنتێک نووسرابوو:

```html
<!-- The changing part goes where {{ content }} is -->
```

**ئەنجام:** هەموو پەڕەکە **دوو جار** پیشان درا.

**بۆچی؟** `render()` جیاوازی نێوان کۆمێنت و کۆدی HTML **نازانێت**. تەنها
بەدوای `{{ }}`دا دەگەڕێت. بۆیە ئەوەی ناو کۆمێنتەکەشی گۆڕی.

> **یاسا:** لە کۆمێنتەکاندا هەرگیز `{{ }}` مەنووسە.
>
> ئەمە لە PHP و Django و Laravelیشدا هەمان شێوەیە — پرۆسێسەری template بە
> **دەقەکە** دەڕوانێت، نەک بە مانای HTML.

---

## ئەگەر هەڵە دەرکەوت

| پەیامی هەڵە | چارەسەر |
|-------------|---------|
| `FileNotFoundError: ...templates/home.html` | فایلەکە لە فۆڵدەری `templates`دا نییە، یان ناوەکەی هەڵەیە |
| لە پەڕەکەدا `{{ total }}` وەک خۆی دەردەکەوێت | ناوەکە یەک ناگرێتەوە. `render(..., total=0)` بپشکنە |
| پەڕەکە دوو جار دەردەکەوێت | `{{ }}`ت لە کۆمێنتێکدا نووسیوە (بڕوانە سەرەوە) |
| پیتی کوردی وەک `Ø¨Ø§` | `encoding="utf-8"` لە `open()`دا نییە |
| `NameError: name 're' is not defined` | `import re`ت لەبیر چووە |
| گۆڕانکاری `app.py` دیار نییە | سێرڤەرەکە دووبارە بکەرەوە |
| پەڕەکە بەتاڵە | `layout.html` بەتاڵە، یان `{{ content }}`ی تێدا نییە |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

```
student-system/
├── app.py
├── database.py
├── students.db
├── templates/
│   ├── layout.html     ← نوێ
│   └── home.html       ← نوێ
└── static/
```

- HTML لە فایلی خۆیدایە، نەک لەناو Pythonـدا
- `render()` شوێنە بەتاڵەکان پڕ دەکاتەوە
- دەزانیت template دەگۆڕێت بەبێ دووبارەکردنەوەی سێرڤەر
- دەزانیت بۆچی `{{ }}` لە کۆمێنتدا مەترسیدارە

**ئێستا دەتوانین پەڕەی ڕاستەقینە دروست بکەین** — بەڵام هێشتا ناشیرینن.
لە هەنگاوی داهاتوودا CSS زیاد دەکەین.

---

# هەنگاوی ٦ — CSS

> پەڕەکەمان کاردەکات، بەڵام ناشیرینە. لەم هەنگاوەدا دیزاینی پێدەدەین — و
> فێری شتێکی نوێ دەبین: سێرڤەرەکەمان دەبێت **فایلی جیا** بنێرێت.

## چی دەکەین

فایلی CSS دەنووسین، و فێری سێرڤەرەکە دەکەین کە بینێرێت.

## بۆچی دوو کار؟

لە HTMLـدا دەتوانیت CSS ڕاستەوخۆ بنووسیت. بەڵام لە فایلێکی جیادا:

- **یەک فایل بۆ هەموو پەڕەکان** — گۆڕینی ڕەنگێک لە یەک شوێندا
- **وێبگەڕ کاشی دەکات** — پەڕەکان خێراتر دەبنەوە
- **HTML پاک دەمێنێتەوە** — پێکهاتە لە دیزاین جیا دەبێتەوە

بەڵام مەرجێکی هەیە: وێبگەڕ فایلی CSS بە **داواکارییەکی جیا** دەخوازێت. تا
ئێستا سێرڤەرەکەمان تەنها یەک شت دەزانێت — هەمان پەڕە بۆ هەموو داواکارییەک.

---

## ٦.١ — `static/style.css`

کلیک لەسەر فۆڵدەری `static` بکە، پاشان **New File**:

```
style.css
```

```css static/style.css
:root {
  --brand: #2563eb;
  --text: #1f2937;
  --border: #e5e7eb;
  --background: #f4f6fb;
  --surface: #ffffff;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 24px;
  background: var(--background);
  color: var(--text);
  font-family: "Segoe UI", Tahoma, Arial, sans-serif;
  line-height: 1.6;
}

h1 {
  margin: 0 0 16px;
  color: var(--brand);
  font-size: 24px;
}

.card {
  max-width: 700px;
  padding: 20px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px;
}
```

> **`:root` چییە؟** شوێنێک بۆ دانانی ڕەنگەکان بە ناوەوە. پاشان بە
> `var(--brand)` بەکاریان دەهێنیت. ئەگەر ڕۆژێک بتەوێت ڕەنگی سەرەکی بگۆڕیت،
> **یەک دێڕ** دەگۆڕیت لەبری بیست دێڕ.

<!-- collapse -->
## ٦.١.١ — ئەم CSSـە چی دەکات؟

| ڕێسا | چی دەکات |
|------|-----------|
| `:root { --brand: ... }` | ناو دەداتە ڕەنگێک، تاکو لە یەک شوێنەوە بگۆڕدرێت |
| `* { box-sizing: border-box }` | پانی ئەلیمێنت بە پەراوێز و کەنارەوە دەژمێردرێت — بەبێ ئەمە دیزاینەکان تێکدەچن |
| `body { margin: 0 }` | ئەو بۆشاییە بنەڕەتییە لادەبات کە وێبگەڕ خۆی دایدەنێت |
| `padding: 24px` | بۆشایی نێوان ناوەڕۆک و کەناری پەنجەرەکە |
| `background: var(--background)` | ئەو ڕەنگە بەکاردەهێنێت کە لە `:root`دا ناومان نا |
| `font-family: "Segoe UI", Tahoma, Arial` | لیستێکی پاشەکەوت: ئەگەر یەکەمیان نەبوو، دووەمیان |
| `line-height: 1.6` | بۆشایی نێوان دێڕەکان — خوێندنەوە ئاسانتر دەکات |
| `h1 { color: var(--brand) }` | ناونیشان بە ڕەنگی سەرەکی |
| `.card { max-width: 700px }` | سندوقەکە لە ٧٠٠ پیکسڵ پانتر نابێت |
| `border-radius: 10px` | گۆشەکان نەرم دەکات |

## ٦.٢ — بەستنەوەی بە `layout.html`

`templates/layout.html` بکەرەوە و دوو گۆڕانکاری بکە:

```html templates/layout.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ title }}</title>
  <link rel="stylesheet" href="/static/style.css">
</head>
<body>
  <h1>{{ title }}</h1>
  <div class="card">
    {{ content }}
  </div>
</body>
</html>
```

**دوو شت زیاد بوون:** دێڕی `<link>`، و `<div class="card">` بەدەوری
ناوەڕۆکەکەدا.

## ٦.٣ — تاقیکردنەوەیەکی خێرا (کە سەرکەوتوو نابێت)

سێرڤەرەکە دووبارە بکەرەوە و `F5` لێبدە.

**هیچ ناگۆڕێت.** پەڕەکە هەر ناشیرینە.

بۆچی؟ کلیکی ڕاست بکە → **Inspect** → تابی **Network**. دەبینیت
`style.css` هەیە بەڵام **هیچ CSSـێکی تێدا نییە** — سێرڤەرەکە هەمان پەڕەی
HTML بۆ ناردووەتەوە.

> **هۆکارەکەی:** `do_GET`ی ئێمە **پرسیار ناکات چی داوا کراوە**. هەر
> داواکارییەک بێت، هەمان پەڕە دەنێرێتەوە.

ئێستا ئەوە چارەسەر دەکەین.

---

## ٦.٤ — ڕێنیشاندەر (router)

`app.py` بگۆڕە. سەرەتا لە سەرەوە:

```python app.py
import os
import re
import urllib.parse
from http.server import BaseHTTPRequestHandler, HTTPServer

import database

BASE_DIR = os.path.dirname(os.path.abspath(__file__))
TEMPLATE_DIR = os.path.join(BASE_DIR, "templates")
STATIC_DIR = os.path.join(BASE_DIR, "static")
```

پاشان کلاسەکە:

```python app.py
class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        url = urllib.parse.urlparse(self.path)

        if url.path == "/":
            self.page_home()
        elif url.path.startswith("/static/"):
            self.send_static(url.path[len("/static/"):])
        else:
            self.send_response(404)
            self.end_headers()

    def page_home(self):
        body = render("home.html", total=0)
        page = render("layout.html", title="Students", content=body)

        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(page.encode("utf-8"))

    def send_static(self, filename):
        safe_name = os.path.basename(filename)
        path = os.path.join(STATIC_DIR, safe_name)

        if not os.path.isfile(path):
            self.send_response(404)
            self.end_headers()
            return

        with open(path, "rb") as file:
            body = file.read()

        self.send_response(200)
        self.send_header("Content-Type", "text/css; charset=utf-8")
        self.end_headers()
        self.wfile.write(body)
```

<!-- collapse -->
## ٦.٥ — ئەم کۆدە چی دەکات؟

| بەش | چی دەکات |
|-----|-----------|
| `urllib.parse.urlparse(self.path)` | لینکەکە دەکاتە پارچە: ڕێڕەو، پارامەتەرەکان، … |
| `if url.path == "/"` | داوای پەڕەی سەرەکی کراوە |
| `elif url.path.startswith("/static/")` | داوای فایلێکی `static` کراوە |
| `else: 404` | ئەم پەڕەیە بوونی نییە |
| `os.path.basename(filename)` | تەنها ناوی فایلەکە دەهێڵێتەوە |
| `open(path, "rb")` | بە **بایت** دەیخوێنێتەوە، نەک دەق |
| `Content-Type: text/css` | بە وێبگەڕ دەڵێت: ئەمە CSSـە |

> ### ⚠️ `os.path.basename` پاراستنە، نەک ڕێکخستن
>
> بەبێ ئەو، کەسێک دەیتوانی ئەمە داوا بکات:
>
> ```
> /static/../database.py
> ```
>
> و کۆدی داتابەیسەکەت بخوێنێتەوە. `basename` هەموو ئەو `../`ـانە لادەبات
> و تەنها `database.py` دەهێڵێتەوە — کە لە فۆڵدەری `static`دا نییە، بۆیە
> وەڵامەکە `404`ـە.
>
> ئەمە بە **Path Traversal** ناسراوە، و یەکێکە لە باوترین هەڵەکانی
> سێرڤەرەکان.

> **بۆچی `"rb"`؟** CSS وەک خۆی دەنێردرێت، بەبێ هیچ گۆڕانکارییەک. دواتر
> ئەگەر وێنەش بنێریت، هەمان کۆد کاردەکات — چونکە وێنە دەق نییە، بایتە.

---

## ٦.٦ — تاقیکردنەوە

سێرڤەرەکە دووبارە بکەرەوە:

```bash
python app.py
```

پاشان `http://localhost:8000` — و ئەم جارە `Ctrl + Shift + R` لێبدە.

## چی دەبینیت

- پاشبنەمایەکی کاڵی شین-خۆڵەمێشی
- ناونیشانێکی شین
- سندوقێکی سپی بە کەنارەیەکی نەرمەوە

**دیزاینەکە کاری کرد.**

## ٦.٧ — دوو تاقیکردنەوەی زیاتر

**١. CSSەکە ڕاستەوخۆ ببینە:**

```
http://localhost:8000/static/style.css
```

دەبێت خودی کۆدی CSSەکە ببینیت. ئەمە هەمان ئەو شتەیە کە وێبگەڕ وەریدەگرێت.

**٢. پەڕەیەکی نەبوو داوا بکە:**

```
http://localhost:8000/nothing
```

دەبێت `404` ببینیت. ئێستا سێرڤەرەکەت **دەزانێت** چی داوا کراوە.

---

## ⚠️ کاشی وێبگەڕ

ئەگەر CSSەکە گۆڕی و گۆڕانکارییەکە دەرنەکەوت:

وێبگەڕ فایلی CSS **کاش دەکات** — واتە لە بیریدا دەیهێڵێتەوە تاکو خێراتر
بێت. `F5` بەس نییە.

**`Ctrl + Shift + R`** بەکاربهێنە — ئەمە کاشەکە ڕەت دەکاتەوە.

> ئەمە جیاوازە لە یاسای هەنگاوی ٥. CSS بەبێ دووبارەکردنەوەی سێرڤەر
> دەگۆڕێت، بەڵام پێویستی بە `Ctrl + Shift + R` هەیە.

---

## ئەگەر هەڵە دەرکەوت

| کێشە | چارەسەر |
|------|---------|
| دیزاینەکە کارناکات | `Ctrl + Shift + R` — کاشی وێبگەڕ |
| `style.css` وەڵامی `404` دەداتەوە | فایلەکە لە فۆڵدەری `static`دا نییە، یان ناوی هەڵەیە |
| CSSەکە دەبینم بەڵام کار ناکات | `Content-Type`ەکە `text/css` نییە |
| `TypeError: a bytes-like object is required` | `open(path, "rb")`ت بەکارنەهێناوە |
| هەموو پەڕەکان `404` دەدەنەوە | لە `do_GET`دا `if url.path == "/"` بپشکنە |
| `NameError: urllib is not defined` | `import urllib.parse`ت لەبیر چووە |
| پەڕەکە بەتاڵە | `{{ content }}` لە `layout.html`دا نەماوە |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

```
student-system/
├── app.py              ← ڕێنیشاندەری تێدایە
├── database.py
├── students.db
├── templates/
│   ├── layout.html     ← <link>ی تێدایە
│   └── home.html
└── static/
    └── style.css       ← نوێ
```

- پەڕەکە دیزاینی هەیە
- سێرڤەرەکە دەزانێت جیاوازی نێوان پەڕە و فایل
- دەزانیت `404` چییە و کەی ڕوودەدات
- دەزانیت بۆچی `basename` پاراستنە

**ئێستا هەموو ئامرازەکانمان هەن.** لە هەنگاوی داهاتوودا یەکەم پیتی
CRUD دەست پێدەکەین: **R** — پیشاندانی لیستی قوتابیان لە داتابەیسەوە.

---

# هەنگاوی ٧ — **R** لە CRUD: پیشاندانی لیستەکە

> ئێستا دەست بە CRUD دەکەین. یەکەم پیت **R**ـە — خوێندنەوە.

## چی دەکەین

قوتابییەکان لە داتابەیسەوە دەخوێنینەوە و لە خشتەیەکدا پیشانیان دەدەین.

## بۆچی سەرەتا R، نەک C؟

چونکە بەبێ پیشاندان، ناتوانیت بزانیت تۆمارکردنەکە کاری کردووە یان نا.
**سەرەتا شێوەی بینین دروست دەکەین، پاشان شێوەی زیادکردن.**

---

## ٧.١ — دوو فەنکشن بۆ `database.py`

لە کۆتایی `database.py` ئەمانە زیاد بکە:

```python database.py
def add_student(student_id, full_name, department, gender, email, phone):
    with get_connection() as connection:
        cursor = connection.execute(
            """
            INSERT INTO students (student_id, full_name, department, gender, email, phone)
            VALUES (?, ?, ?, ?, ?, ?)
            """,
            (student_id, full_name, department, gender, email, phone),
        )
        return cursor.lastrowid


def get_all_students():
    with get_connection() as connection:
        return connection.execute(
            "SELECT * FROM students ORDER BY id DESC"
        ).fetchall()
```

<!-- collapse -->
## ٧.١.١ — ئەم کۆدە چی دەکات؟

| بەش | چی دەکات |
|-----|-----------|
| `INSERT INTO ... VALUES (?, ?, ...)` | ڕیزێکی نوێ زیاد دەکات |
| `?` | شوێنی نرخێک — **هەرگیز نرخەکە ڕاستەوخۆ مەنووسە** |
| `cursor.lastrowid` | ژمارەی ئەو ڕیزەی تازە زیاد بوو |
| `SELECT *` | هەموو ستوونەکان |
| `ORDER BY id DESC` | نوێترین لە سەرەوە |
| `.fetchall()` | هەموو ڕیزەکان وەردەگرێت |

> ### ⚠️ بۆچی `?` بەکاردەهێنین؟
>
> ئەمە **تاکە ڕێگایە** بۆ ڕێگرتن لە **SQL Injection**.
>
> ئەگەر بنووسیت `"... VALUES ('" + full_name + "')"`، ئەوا کەسێک دەتوانێت
> ناوێک بنووسێت کە فەرمانی SQLـی تێدا بێت، و خشتەکەت بسڕێتەوە.
>
> بە `?`، SQLite دەزانێت ئەمە **نرخێکە، نەک فەرمان**. تەنانەت ئەگەر ناوەکە
> `'; DROP TABLE students; --`یش بێت، تەنها وەک ناوێک پاشەکەوت دەکرێت.
>
> ئەمە لە وانەی تیۆریدا بە وردی باسکراوە.

## ٧.٢ — داتای تاقیکردنەوە زیاد بکە

هێشتا فۆڕممان نییە. بۆیە دوو قوتابی لە تێرمیناڵەوە زیاد دەکەین:

```bash
python -c "import database; database.init_db(); database.add_student('MIS-2025-001', 'Ahmad Karim', 'MIS', 'Male', 'ahmad@example.com', '0770 111 1111')"
```

```bash
python -c "import database; database.add_student('MIS-2025-002', 'Sara Ali', 'Accounting', 'Female', 'sara@example.com', '0770 222 2222')"
```

> ئەگەر دووبارە هەمان فەرمان بکەیت، هەڵەیەک دەبینیت:
> `UNIQUE constraint failed` — داتابەیسەکە خۆی ڕێگری لە دووبارەبوونەوە
> دەکات، وەک لە هەنگاوی ٤دا دامانناوە.

---

## ٧.٣ — `templates/list.html`

فایلێکی نوێ لە فۆڵدەری `templates`:

```html templates/list.html
<p>{{ total }} student(s)</p>

<table>
  <thead>
    <tr>
      <th>#</th>
      <th>Student ID</th>
      <th>Full name</th>
      <th>Department</th>
      <th>Registered at</th>
    </tr>
  </thead>
  <tbody>
    {{ rows }}
  </tbody>
</table>
```

`<tbody>` بەتاڵە — ڕیزەکانی لە Pythonـەوە دێن.

## ٧.٤ — `templates/home.html` بگۆڕە

```html templates/home.html
<p>Welcome to the Student Registration System.</p>

{{ table }}
```

## ٧.٥ — دوو فەنکشن بۆ `app.py`

سەرەتا لە سەرەوە `import html` زیاد بکە، پاشان ئەم دوو فەنکشنە لەتەنیشت
`render()`:

```python app.py
def esc(value):
    return html.escape("" if value is None else str(value))


def build_table_rows(students):
    rows = []
    for number, student in enumerate(students, start=1):
        rows.append(
            """
            <tr>
              <td>{number}</td>
              <td>{student_id}</td>
              <td>{full_name}</td>
              <td>{department}</td>
              <td>{created_at}</td>
            </tr>
            """.format(
                number=number,
                student_id=esc(student["student_id"]),
                full_name=esc(student["full_name"]),
                department=esc(student["department"]),
                created_at=esc(student["created_at"]),
            )
        )
    return "".join(rows)
```

<!-- collapse -->
## ٧.٥.١ — ئەم کۆدە چی دەکات؟

| بەش | چی دەکات |
|-----|-----------|
| `enumerate(students, start=1)` | ژمارە دەداتە ڕیزەکان: ١، ٢، ٣ … |
| `student["full_name"]` | ستوونەکە بە ناوەکەی دەخوێنێتەوە — سوودی `row_factory`ی هەنگاوی ٤ |
| `"""...""".format(...)` | قاڵبێکی بچووک بۆ هەر ڕیزێک |
| `"".join(rows)` | هەموو ڕیزەکان دەکاتە یەک دەق |
| **`esc(...)`** | دەقەکە ئەمن دەکاتەوە — بڕوانە خوارەوە |

## ٧.٦ — `page_home` بگۆڕە

```python app.py
    def page_home(self):
        students = database.get_all_students()

        if students:
            table = render("list.html",
                           rows=build_table_rows(students),
                           total=len(students))
        else:
            table = "<p>No student is registered yet.</p>"

        body = render("home.html", table=table)
        page = render("layout.html", title="Students", content=body)

        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(page.encode("utf-8"))
```

> **ئەو `if`ـە بەشێکی گرنگە.** ئەگەر هیچ قوتابییەک نەبێت، خشتەیەکی بەتاڵ
> پیشان مەدە — پەیامێکی ڕوون بنووسە. ئەمە پێی دەگوترێت **empty state**، و
> جیاوازی نێوان پڕۆگرامێکی باش و خراپە.

## ٧.٧ — دیزاینی خشتەکە

لە کۆتایی `static/style.css`:

```css static/style.css
table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  padding: 8px 12px;
  border-bottom: 1px solid var(--border);
  text-align: left;
}

thead th {
  color: #6b7280;
  font-size: 13px;
  text-transform: uppercase;
}

tbody tr:last-child td {
  border-bottom: none;
}
```

<!-- collapse -->
## ٧.٧.١ — ئەم CSSـە چی دەکات؟

| ڕێسا | چی دەکات |
|------|-----------|
| `width: 100%` | خشتەکە هەموو پانییەکە دەگرێت |
| `border-collapse: collapse` | هێڵەکانی نێوان خانەکان تێکەڵ دەکات — بەبێ ئەمە دوو هێڵ لەتەنیشت یەک دەردەکەون |
| `padding: 8px 12px` | بۆشایی ناو خانەکان: ٨ لە سەرەوە و خوارەوە، ١٢ لە لاکاندا |
| `border-bottom` | تەنها هێڵێک لەژێر هەر ڕیزێکدا، نەک چوارچێوەیەکی تەواو |
| `text-align: left` | دەق لە چەپەوە دەست پێدەکات |
| `thead th { text-transform: uppercase }` | سەردێڕەکان بە پیتی گەورە |
| `tbody tr:last-child td { border-bottom: none }` | دوایین ڕیز هێڵی ژێرەوەی نابێت |

---

## ٧.٨ — تاقیکردنەوە

سێرڤەرەکە دووبارە بکەرەوە و `Ctrl + Shift + R` لێبدە.

## چی دەبینیت

```
2 student(s)

#   STUDENT ID     FULL NAME     DEPARTMENT   REGISTERED AT
1   MIS-2025-002   Sara Ali      Accounting   2026-09-03 06:07
2   MIS-2025-001   Ahmad Karim   MIS          2026-09-03 06:07
```

**سارا لە سەرەوەیە** چونکە `ORDER BY id DESC` — نوێترین یەکەم.

> سەیری ستوونی `#` بکە: سارا ژمارە **١**ـە، هەرچەندە `id`ـەکەی ٢ـە. ئەو
> ژمارەیە لە `enumerate()`ـەوە دێت و تەنها ڕیزبەندی ناو لاپەڕەکەیە — نەک
> `id`ی داتابەیس. ئەمە بە ئەنقەستە: قوتابی پێویستی بە `id`ی ناوخۆیی نییە.

> `created_at` خۆکارانە پڕ بووەتەوە — ئێمە هەرگیز نەمانناردووە. ئەوە
> `DEFAULT (datetime('now', 'localtime'))`ی هەنگاوی ٤ بوو.

---

## ٧.٩ — تاقیکردنەوەی پاراستن

ئێستا قوتابییەک زیاد بکە کە ناوەکەی کۆدە:

```bash
python -c "import database; database.add_student('MIS-2025-003', '<script>alert(1)</script>', 'MIS', 'Male', '', '')"
```

`F5` لێبدە.

**دەبێت ناوەکە وەک دەق ببینیت**، بەم شێوەیە:

```
<script>alert(1)</script>
```

نەک پەنجەرەیەکی ئاگادارکردنەوە.

**بۆچی؟** لەبەر `esc()`. ئەو `<` دەکات بە `&lt;`، بۆیە وێبگەڕ وەک **دەق**
لێی دەڕوانێت، نەک وەک **کۆد**.

> ئەگەر `esc()` لابەریت و دووبارە تاقی بکەیتەوە، پەنجەرەکە دەردەکەوێت.
> ئەمە **XSS**ـە — و ئەم سێ پیتە هۆکاری ڕێگریکردنیانە.
>
> لە پڕۆژەیەکی ڕاستەقینەدا، ئەو کۆدە دەتوانێت هەژماری بەکارهێنەران بدزێت.

پاشان بیسڕەوە:

```bash
python -c "import database; database.get_connection().execute('DELETE FROM students WHERE id = 3').connection.commit()"
```

---

## ئەگەر هەڵە دەرکەوت

| کێشە | چارەسەر |
|------|---------|
| `no such table: students` | `python -c "import database; database.init_db()"` بکە |
| `UNIQUE constraint failed` | هەمان `student_id` دووبارە زیاد دەکەیت — ژمارەکە بگۆڕە |
| خشتەکە بەتاڵە | داتاکەت زیاد نەکردووە (بڕوانە ٧.٢) |
| `{{ rows }}` وەک خۆی دەردەکەوێت | ناوەکە یەک ناگرێتەوە. `render("list.html", rows=...)` بپشکنە |
| `TypeError: tuple indices must be integers` | `row_factory = sqlite3.Row`ت لە `database.py`دا نییە |
| `NameError: name 'html' is not defined` | `import html`ت لەبیر چووە |
| پەنجەرەی `alert` دەردەکەوێت | `esc()`ت بەکارنەهێناوە |
| خشتەکە دیزاینی نییە | `Ctrl + Shift + R` |

---

## ✅ کاتێک ئەم هەنگاوە تەواو دەبێت

```
student-system/
├── app.py              ← esc() و build_table_rows()
├── database.py         ← add_student() و get_all_students()
├── students.db         ← داتای تێدایە
├── templates/
│   ├── layout.html
│   ├── home.html       ← گۆڕدرا
│   └── list.html       ← نوێ
└── static/
    └── style.css       ← دیزاینی خشتە
```

- قوتابییەکان لە داتابەیسەوە دەردەکەون
- نوێترین لە سەرەوەیە
- ئەگەر هیچ قوتابییەک نەبێت، پەیامێکی ڕوون دەردەکەوێت
- دەزانیت `?` و `esc()` چی دەپارێزن

**یەک لە چوار تەواو بوو.** لە هەنگاوی داهاتوودا **C** دروست دەکەین —
فۆڕمێک کە قوتابی خۆی زیاد بکات، بەبێ تێرمیناڵ.

---

> هەنگاوی ٨ لێرە زیاد دەکرێت.