# Student Guide (Practical Part) — Prepared by M. Idris Qadir


## Who is this document for?

For a student who:

- **has all of this to learn** — HTML, CSS, Python and SQL
- has **Visual Studio Code** installed
- has an activated copy of Windows — nothing to activate
- has an activated copy of Office — nothing to activate

## How to use it

1. **Go in order.** Do not skip a step — each one builds on the one before it.
2. **Type the code by hand**, do not copy it. The brain learns by typing.
3. **Test after every step.** Never move to the next step until the current one works.
4. **If you get an error**, look in the table below for the common ones.

## The shape of every step

| Part | Meaning |
| ---- | ------- |
| **What we do** | The job of this step, in one sentence |
| **Why** | The purpose — without this you are only copying |
| **The code** | The complete code, not a fragment |
| **How to test it** | Immediately after you type it |
| **What you should see** | The expected result |
| **If you get an error** | The most common errors and their fixes |

---

## The steps

| # | Step | Status |
| - | ---- | ------ |
| 1 | Preparing the computer (Python) | ✅ |
| 2 | The project folder and its structure | ✅ |
| 3 | The first server — "Hello" | ✅ |
| 4 | The database (`database.py`) | ✅ |
| 5 | Templates and the `render()` function | ✅ |
| 6 | CSS — designing the pages | ✅ |
| 7 | **R** — showing the student list | ✅ |
| 8 | **C** — the registration form + validation | ⏳ |
| 9 | **U** — editing | ⏳ |
| 10 | **D** — deleting | ⏳ |
| 11 | Search | ⏳ |
| 12 | Security — SQL Injection and XSS | ⏳ |
| 13 | Final testing and `run.bat` | ⏳ |

> ⏳ = not written yet. This document is completed step by step.

---

# Step 1 — Prepare the computer

> This step has nothing to do with the project itself. We are only making sure
> we have the tools. You do it once and never again.

## What we do

Make sure **Python** is installed on the computer.

## Why

Visual Studio Code is only an **editor** — a notebook for writing code.
It cannot run your code. The thing that runs Python code is a separate
program called **Python** itself. We need both.

---

## 1.1 — Open a terminal in VS Code

Open VS Code, then from the top menu:

**Terminal → New Terminal**

> Shortcut: `Ctrl` + `` ` `` (the key below `Esc`)

A dark panel opens at the bottom. This is the **terminal** — a place where
you type commands, not code.

## 1.2 — Ask whether Python is there

Type this and press `Enter`:

```
python --version
```

## What you should see

**If Python is installed** — something like this appears:

```
Python 3.13.14
```

✅ You are done. Go to 1.4.

**If Python is not installed** — one of these two happens:

- the message `'python' is not recognized...`
- or the **Microsoft Store** opens by itself

In that case go to 1.3.

---

## 1.3 — Installing Python (only if you need to)

1. Go to <https://www.python.org/downloads/>
2. Click the yellow button (**Download Python 3.x**)
3. Open the downloaded file

> ### ⚠️ The most important point of this step
>
> On the very first installer screen, **before** you click anything, there is
> a checkbox at the bottom:
>
> **☑ Add python.exe to PATH**
>
> **You must tick this box.** If you don't, the terminal will never find
> Python and you will have to run the whole installation again.

4. Then click **Install Now** and wait
5. **Close VS Code completely and open it again** — without this, an already
   open terminal still does not know that Python was installed
6. Open a new terminal and type `python --version` again

---

## 1.4 — Confirm the database is there

Now type this:

```
python -c "import sqlite3; print('SQLite OK')"
```

This should appear:

```
SQLite OK
```

**What does that mean?** SQLite is the database in which we will store the
students' data. Happily it **ships with Python itself** — you do not need to
install anything else. No XAMPP, no MySQL, no phpMyAdmin.

---

## If you get an error

| Error message | Fix |
| ------------- | --- |
| `'python' is not recognized` | PATH was not set. Install Python again and this time tick `Add python.exe to PATH` |
| The Microsoft Store opens | Windows is getting in the way. Go to Settings → Apps → Advanced app settings → App execution aliases, then turn `python.exe` off |
| It shows `Python 2.7.x` | That is a very old version. Try `python3 --version` |
| Nothing happens | Make sure you pressed `Enter` and that you typed it in the terminal, not in a code file |

---

## ✅ This step is finished when

These two commands work and produce output:

```
python --version                                →  Python 3.x.x
python -c "import sqlite3; print('SQLite OK')"  →  SQLite OK
```

**We have not created a single file and not written a single line of code** —
we have only prepared the workshop.

---

# Step 2 — The project folder

> Still no code. We are only preparing the place the code will live in.

## What we do

Create a folder for the project and open it in VS Code.

## Why

A project really is just a **folder** — nothing more. All the files stay
together in one place, so you can copy or send the whole project at once.

VS Code also works on a **folder**, not on a single file. When you open the
folder, the terminal opens inside that folder automatically — which matters a
great deal in Step 3.

---

## 2.1 — Create the folder

In **File Explorer**, pick a place you will find again easily — your
`Documents` folder, for example.

Right-click an empty spot → **New** → **Folder**

Name it:

```
student-system
```

> ### ⚠️ About the folder name
>
> Two rules, and both of them matter:
>
> - **Use English letters** — not Kurdish ones
> - **No spaces** — `student system` ❌ , `student-system` ✅
>
> Python and the terminal run into trouble with Kurdish letters and spaces in
> a path, and that kind of trouble is very hard for a beginner to track down.

## 2.2 — Open it in VS Code

Open VS Code, then:

**File → Open Folder…** → select the folder → **Select Folder**

If it asks *"Do you trust the authors of the files in this folder?"*, click
**Yes, I trust the authors**.

> ⚠️ Do not use **Open File**. It has to be **Open Folder** — this is an
> important difference, not a detail.

## 2.3 — Create two folders inside

On the left of VS Code (this panel is called the **Explorer**) you can see the
project name: `STUDENT-SYSTEM`. Hover over it and a few icons appear.

Click **New Folder** (the folder icon with a `+`) and create two folders:

```
templates
static
```

**Why two separate folders?**

| Folder | What goes in it | Which step |
| ------ | --------------- | ---------- |
| `templates` | HTML files — the shape of the pages | Step 5 |
| `static` | The CSS file — colours and design | Step 6 |

They are empty for now. We fill them in the steps ahead.

---

## 2.4 — Test it

Open a terminal (**Terminal → New Terminal**) and type:

```
dir
```

## What you should see

```
    Directory: C:\Users\...\Documents\student-system

Mode      Name
----      ----
d-----    static
d-----    templates
```

Check two things:

1. **Both folders are listed** — `static` and `templates`
2. **The start of the terminal line** shows `student-system` — meaning you are
   standing in the right place

The second one matters more than it looks. In Step 3 we type a command that
only works inside this folder.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| The terminal shows a different folder name | You opened a file, not a folder. Do **File → Open Folder** again |
| I see nothing on the left | Press `Ctrl + Shift + E` to open the Explorer |
| `dir` returns nothing | The folders were not created. Go back to 2.3 |
| `templates` ended up inside `static` | Right-click → **Delete**, then create them again. Before clicking **New Folder**, make sure no other folder is selected |
| The folder name is in Kurdish letters | Right-click → **Rename** → make it `student-system` |

---

## ✅ This step is finished when

Your structure looks like this:

```
student-system/
├── templates/
└── static/
```

Two empty folders inside the project folder.

**We still have not written a single line of code** — but now there is a place
to write it. In the next step we write the first Python file and see our first
page in the browser.

---

# Step 3 — The first server

> This is the first code. By the end of this step you will see something in
> your browser that you built yourself.

## What we do

Write a very small server that shows one word: **Hello**.

## Why

Before adding a database, forms and tables, there is **one thing** to
understand:

> A server is a program that waits, a browser asks it for something, and it
> answers.

Everything else — students, registering, searching — is only an addition on
top of that one simple idea.

---

## 3.1 — Create the file `app.py`

In VS Code, in the Explorer, click **New File** (the page icon with a `+`).

Name it:

```
app.py
```

> ### ⚠️ Two things
>
> - **Do not forget the `.py`** — it tells Python this is code
> - **Do not put it inside `templates` or `static`** — it belongs directly in
>   the project folder

## 3.2 — Type the code

```python
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

**Save it:** `Ctrl + S`

> ⚠️ VS Code does **not** save on its own. A white dot ● in the tab name means
> the file is not saved yet.

## 3.3 — What does this code do?

| Line | What it does |
| ---- | ------------ |
| `from http.server import ...` | Brings in the server that ships with Python |
| `class StudentAppHandler` | This part decides how requests are answered |
| `def do_GET(self)` | Runs **every time** a browser asks for a page |
| `send_response(200)` | `200` means "fine, everything worked" |
| `send_header("Content-Type"...)` | Tells the browser: this is HTML, in UTF-8 |
| `end_headers()` | The end of the information above the page |
| `wfile.write(...)` | Sends the content of the page |
| `.encode("utf-8")` | Turns text into bytes — a server sends bytes, not text |
| `HTTPServer(("localhost", 8000), ...)` | Where and on which port to listen |
| `serve_forever()` | Keep waiting — never stop |

> **`charset=utf-8` matters.** Without it, Kurdish letters come out as `Ø¨Ø§`.

---

## 3.4 — Run it

In the terminal:

```
python app.py
```

## What you should see

In the terminal:

```
Server running at http://localhost:8000
Press Ctrl + C to stop.
```

And then **nothing**. The terminal is stuck and you cannot type anything else.

> ### ⚠️ This is not an error
>
> It is the most common confusion in this step. The terminal has **not
> frozen** — the server is running and waiting for requests.
>
> A server never "finishes". It runs until you stop it.

## 3.5 — Open it in the browser

Open a browser and type:

```
http://localhost:8000
```

You should see:

# Hello

**Well done** — your first server works.

Look at the terminal too: a new line has appeared showing the request.

## 3.6 — Stop it

Go back to the terminal and press `Ctrl + C`.

The terminal returns to normal.

---

## 3.7 — An important test

This test teaches something you will use constantly from now on:

1. In the code, change `Hello` to your own name
2. Save with `Ctrl + S`
3. Go to the browser and press `F5`

**Nothing changes.** Why?

Because the server still has the old code in memory. You have to:

1. `Ctrl + C` — stop it
2. `python app.py` — run it again
3. `F5` in the browser

**Now you see your name.**

> **The rule:** after every change to `app.py`, stop the server and start it
> again. From this step to the last one, you will repeat this constantly.

---

## If you get an error

| Error message | Fix |
| ------------- | --- |
| `can't open file 'app.py'` | You are in the wrong folder. Close the terminal and do **File → Open Folder** again |
| `[WinError 10048]` or `address already in use` | A server is already running. Find the old terminal and press `Ctrl + C` |
| `IndentationError` | The spacing at the start of the lines is uneven. Python is strict — use 4 spaces, not a Tab |
| `SyntaxError` | A character or a bracket is missing. Check the line named in the message |
| **This site can't be reached** | The server is not running. Look at the terminal |
| Kurdish letters show as `Ø¨Ø§` | `charset=utf-8` is missing from the `Content-Type` |
| My change does not show | You did not restart the server (see 3.7) |
| A white dot ● in the tab | The file is not saved. `Ctrl + S` |

---

## ✅ This step is finished when

```
student-system/
├── app.py          ← new
├── templates/
└── static/
```

- `python app.py` starts the server
- `http://localhost:8000` shows some text
- `Ctrl + C` stops it
- You know that every change needs a restart

**You now have a server.** In the next step we build the database — the place
where the students' information will live.

---

# Step 4 — The database

> By the end of this step a new file appears in your project that you did not
> create yourself — the database.

## What we do

Write `database.py` and create the `students` table.

## Why a separate file?

We could put everything in `app.py`. But:

| File | Its job |
| ---- | ------- |
| `app.py` | The web part — pages, forms, decisions |
| `database.py` | The data part — the table, reading, writing |

**The benefit:** if one day we move from SQLite to MySQL, only one file
changes. `app.py` is untouched.

This is the same **separation of concerns** discussed in the theory lesson.

---

## 4.1 — Create the file `database.py`

In VS Code, **New File** → name it:

```
database.py
```

It belongs beside `app.py` — directly in the project folder.

## 4.2 — Type the code

```python
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

Save with `Ctrl + S`.

## 4.3 — What does this code do?

| Part | What it does |
| ---- | ------------ |
| `import sqlite3` | Brings in the database — it ships with Python |
| `DB_PATH = os.path.join(...)` | The path to the database file |
| `os.path.dirname(os.path.abspath(__file__))` | "the same folder as this file" |
| `sqlite3.connect(DB_PATH)` | Connects — and **creates the file if it is not there** |
| `row_factory = sqlite3.Row` | Lets us read a column by name: `row["full_name"]` |
| `with get_connection() as ...` | Saves the changes for us when the block ends |
| `CREATE TABLE IF NOT EXISTS` | Creates the table — **only if it does not exist** |

> **Why `os.path.dirname(...)`?**
> Without it the database is created in whichever folder the terminal happens
> to be in, rather than next to the code. That causes a common and confusing
> error: there is a database, but it is empty — because it is a different file
> with the same name.

## 4.4 — The columns

| Column | Type | Meaning |
| ------ | ---- | ------- |
| `id` | INTEGER | The internal number, assigned automatically |
| `student_id` | TEXT | The university number — **no duplicates** |
| `full_name` | TEXT | Full name — required |
| `department` | TEXT | Department — required |
| `gender` | TEXT | Gender — required |
| `email` | TEXT | May be empty |
| `phone` | TEXT | May be empty |
| `created_at` | TEXT | When the row was created — filled in automatically |

> **Why is the phone number `TEXT` and not `INTEGER`?**
> Because `0770` would lose its leading zero, and some numbers contain a `+`
> or spaces. A number you never do arithmetic with is not a number — it is
> text.

---

## 4.5 — Connect it to `app.py`

`database.py` does nothing on its own — nobody has called it. Add **two
lines** to `app.py`:

```python
from http.server import BaseHTTPRequestHandler, HTTPServer

import database                                    # <- new


class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write("<h1>Hello</h1>".encode("utf-8"))


database.init_db()                                 # <- new
server = HTTPServer(("localhost", 8000), StudentAppHandler)
print("Server running at http://localhost:8000")
print("Press Ctrl + C to stop.")
server.serve_forever()
```

Save both files with `Ctrl + S`.

## 4.6 — Test it

```
python app.py
```

## What you should see

Look at the VS Code **Explorer**. A new file has appeared:

```
student-system/
├── app.py
├── database.py
├── students.db     <- new, created for you
├── templates/
└── static/
```

**That is your database.** An ordinary file — you can copy it, send it, or
delete it.

Press `Ctrl + C` to stop.

## 4.7 — A closer check

To be sure the table really exists, type this in the terminal:

```
python -c "import database; print([r['name'] for r in database.get_connection().execute('SELECT name FROM sqlite_master')])"
```

You should see:

```
['students', 'sqlite_autoindex_students_1', 'sqlite_sequence']
```

The first one is our table. SQLite created the other two itself — one for
`UNIQUE` and one for `AUTOINCREMENT`.

---

## ⚠️ Something that will confuse you later

`CREATE TABLE IF NOT EXISTS` only does anything when the table is **not**
there.

If you later add or change a column and run the program again:

> **Nothing changes.** The table already exists, so SQLite says "fine, it is
> there" and moves on.

**The fix:** delete `students.db` and run `python app.py` again. A new table
is built with the new shape.

> While learning this costs nothing — there is no data in it yet worth
> keeping.

---

## If you get an error

| Error message | Fix |
| ------------- | --- |
| `ModuleNotFoundError: No module named 'database'` | The file name is wrong, or it is in another folder. It must be `database.py`, beside `app.py` |
| `sqlite3.OperationalError: near "..."` | A typo in the SQL. Check the commas between the columns |
| `students.db` did not appear | You did not add `database.init_db()`, or did not run `python app.py` |
| `no such table: students` | `init_db()` was not called before the table was used |
| I changed a column and nothing changed | The table already exists. Delete `students.db` (see above) |
| `IndentationError` | The spacing is uneven. Use 4 spaces |
| I cannot see the file in the Explorer | `Ctrl + Shift + E`, or right-click → **Refresh Explorer** |

---

## ✅ This step is finished when

```
student-system/
├── app.py          <- two new lines in it
├── database.py     <- new
├── students.db     <- created automatically
├── templates/
└── static/
```

- The `students` table exists
- You know why the data lives in its own file
- You know that changing the table means deleting `students.db`

**We now have somewhere to keep information** — but it is still empty, and
the page still says `Hello`. In the next step we learn how to build a real
page.

---

# Step 5 — Templates

> In this step we take the HTML out of the Python code. It is one of the most
> important ideas in web work.

## What we do

Write the HTML in its own files, and write a function that fills them in.

## Why

Right now our HTML lives inside Python:

```python
self.wfile.write("<h1>Hello</h1>".encode("utf-8"))
```

Fine for one line. But a real page is a hundred lines of HTML. Think about it:

- A designer cannot work in it — it is Python code
- Changing a colour means editing the file that holds the logic
- No tool can check your HTML for you

**The fix:** let the HTML live in its own file, and mark the changing parts
with `{{ name }}`.

---

## 5.1 — `templates/layout.html`

In VS Code click the `templates` folder, then **New File**:

```
layout.html
```

Type this:

```html
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

**This is the frame.** Every page shares the same top and bottom — only the
content changes.

> `<meta charset="UTF-8">` does the same job as the `charset=utf-8` from
> Step 3, but this time inside the HTML itself.

## 5.2 — `templates/home.html`

Another file in the same folder:

```html
<p>Welcome to the Student Registration System.</p>
<p>Students registered: {{ total }}</p>
```

**This is the content of the home page** — no `<html>` or `<body>`, because
those are in `layout.html`.

## 5.3 — The `render()` function

Add this to `app.py`. First at the top:

```python
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

## 5.4 — Use it

Change `do_GET` to this:

```python
class StudentAppHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        body = render("home.html", total=0)
        page = render("layout.html", title="Students", content=body)

        self.send_response(200)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(page.encode("utf-8"))
```

**We call it twice:**

1. Fill in `home.html` → that becomes the content
2. Put that content into `layout.html` → that becomes the whole page

## 5.5 — How does this code work?

| Part | What it does |
| ---- | ------------ |
| `**values` | Lets you pass any number of values: `render("home.html", total=0)` |
| `open(path, encoding="utf-8")` | Reads the file |
| `re.sub(pattern, replace, page)` | Finds every `{{ name }}` and replaces it |
| `\{\{\s*(\w+)\s*\}\}` | Matches: two braces, a name, two braces |
| `\s*` | Allows spaces, so `{{title}}` and `{{ title }}` both work |
| `match.group(1)` | The name between the braces — `title`, for example |
| `values.get(name, "")` | Looks the value up. If there is none, puts nothing |

> **What does `\w+` mean?** One or more letters, digits or `_`. So
> `{{ full_name }}` works, but `{{ full name }}` does not.

---

## 5.6 — Test it

```
python app.py
```

then `http://localhost:8000`

## What you should see

# Students

Welcome to the Student Registration System.

Students registered: 0

> To see that it really is HTML, right-click → **View page source**. You will
> find all the `<html>` and `<head>` you wrote in `layout.html`, with
> `{{ title }}` replaced by `Students`.

---

## 5.7 — Something pleasant

Leave the server **running**. Open `home.html` and change the text:

```html
<p>Hello from my own page!</p>
<p>Students registered: {{ total }}</p>
```

Save it and just press `F5` in the browser.

**The change is there** — without restarting the server.

**Why?** Because `render()` reads the file **on every request**. Python code,
on the other hand, is read once, when the server starts.

| What you change | Restart needed? |
| --------------- | --------------- |
| `templates/*.html` | **No** — just `F5` |
| `app.py` or `database.py` | **Yes** |

---

## ⚠️ A bug that really happened

While this project was being built, `layout.html` contained a comment:

```html
<!-- The changing part goes where {{ content }} is -->
```

**The result:** the whole page appeared **twice**.

**Why?** `render()` does **not** know the difference between a comment and
real HTML. It only looks for `{{ }}`. So it replaced the one inside the
comment too.

> **The rule:** never write `{{ }}` inside a comment.
>
> The same is true in PHP, Django and Laravel — a template processor looks at
> the **text**, not at the meaning of the HTML.

---

## If you get an error

| Error message | Fix |
| ------------- | --- |
| `FileNotFoundError: ...templates/home.html` | The file is not in the `templates` folder, or the name is wrong |
| The page shows `{{ total }}` as it is | The names do not match. Check `render(..., total=0)` |
| The page appears twice | You wrote `{{ }}` inside a comment (see above) |
| Kurdish letters show as `Ø¨Ø§` | `encoding="utf-8"` is missing from `open()` |
| `NameError: name 're' is not defined` | You forgot `import re` |
| A change to `app.py` does not show | Restart the server |
| The page is empty | `layout.html` is empty, or has no `{{ content }}` |

---

## ✅ This step is finished when

```
student-system/
├── app.py
├── database.py
├── students.db
├── templates/
│   ├── layout.html     <- new
│   └── home.html       <- new
└── static/
```

- The HTML lives in its own files, not inside Python
- `render()` fills in the blanks
- You know a template changes without restarting the server
- You know why `{{ }}` in a comment is dangerous

**We can now build real pages** — they are just ugly. In the next step we add
CSS.

---

# Step 6 — CSS

> The page works, but it is ugly. In this step we give it a design — and
> learn something new: our server has to send a **separate file**.

## What we do

Write a CSS file, and teach the server to send it.

## Why two jobs?

You can write CSS directly inside the HTML. But in its own file:

- **One file for every page** — change a colour in one place
- **The browser caches it** — pages load faster
- **The HTML stays clean** — structure separated from design

There is a catch, though: the browser asks for the CSS file in a **separate
request**. So far our server only knows one thing — send the same page to
every request.

---

## 6.1 — `static/style.css`

Click the `static` folder, then **New File**:

```
style.css
```

```css
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

> **What is `:root`?** A place to give colours names. You then use them with
> `var(--brand)`. If one day you want to change the main colour, you change
> **one line** instead of twenty.

## 6.2 — Link it from `layout.html`

Open `templates/layout.html` and make two changes:

```html
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

**Two additions:** the `<link>` line, and `<div class="card">` around the
content.

## 6.3 — A quick test (that will fail)

Restart the server and press `F5`.

**Nothing changes.** The page is still ugly.

Why? Right-click → **Inspect** → the **Network** tab. You will see
`style.css` there, but with **no CSS in it** — the server sent back the same
HTML page.

> **The reason:** our `do_GET` **never asks what was requested**. Whatever
> comes in, it sends the same page back.

That is what we fix now.

---

## 6.4 — The router

Change `app.py`. First at the top:

```python
import os
import re
import urllib.parse
from http.server import BaseHTTPRequestHandler, HTTPServer

import database

BASE_DIR = os.path.dirname(os.path.abspath(__file__))
TEMPLATE_DIR = os.path.join(BASE_DIR, "templates")
STATIC_DIR = os.path.join(BASE_DIR, "static")
```

Then the class:

```python
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

## 6.5 — What does this code do?

| Part | What it does |
| ---- | ------------ |
| `urllib.parse.urlparse(self.path)` | Splits the URL into pieces: path, parameters, … |
| `if url.path == "/"` | The home page was asked for |
| `elif url.path.startswith("/static/")` | A file from `static` was asked for |
| `else: 404` | This page does not exist |
| `os.path.basename(filename)` | Keeps only the file name |
| `open(path, "rb")` | Reads it as **bytes**, not text |
| `Content-Type: text/css` | Tells the browser: this is CSS |

> ### ⚠️ `os.path.basename` is protection, not tidiness
>
> Without it, somebody could ask for this:
>
> ```
> /static/../database.py
> ```
>
> and read your database code. `basename` strips all those `../` and leaves
> only `database.py` — which is not in the `static` folder, so the answer is
> `404`.
>
> This is known as **path traversal**, and it is one of the most common
> server mistakes.

> **Why `"rb"`?** CSS is sent exactly as it is, unchanged. Later, if you send
> images, the same code works — because an image is not text, it is bytes.

---

## 6.6 — Test it

Restart the server:

```
python app.py
```

then `http://localhost:8000` — and this time press `Ctrl + Shift + R`.

## What you should see

- A pale blue-grey background
- A blue heading
- A white box with a soft border

**The design works.**

## 6.7 — Two more checks

**1. Look at the CSS directly:**

```
http://localhost:8000/static/style.css
```

You should see the CSS itself. That is exactly what the browser receives.

**2. Ask for a page that does not exist:**

```
http://localhost:8000/nothing
```

You should get a `404`. Your server now **knows** what was asked for.

---

## ⚠️ The browser cache

If you change the CSS and the change does not appear:

The browser **caches** the CSS file — it keeps it in memory to be faster.
`F5` is not enough.

Use **`Ctrl + Shift + R`** — that ignores the cache.

> This differs from the rule in Step 5. CSS changes without restarting the
> server, but it does need `Ctrl + Shift + R`.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| The design does not apply | `Ctrl + Shift + R` — the browser cache |
| `style.css` returns `404` | The file is not in `static`, or the name is wrong |
| I can see the CSS but it does nothing | The `Content-Type` is not `text/css` |
| `TypeError: a bytes-like object is required` | You did not use `open(path, "rb")` |
| Every page returns `404` | Check `if url.path == "/"` in `do_GET` |
| `NameError: urllib is not defined` | You forgot `import urllib.parse` |
| The page is empty | `{{ content }}` is missing from `layout.html` |

---

## ✅ This step is finished when

```
student-system/
├── app.py              <- has the router
├── database.py
├── students.db
├── templates/
│   ├── layout.html     <- has the <link>
│   └── home.html
└── static/
    └── style.css       <- new
```

- The page has a design
- The server knows the difference between a page and a file
- You know what a `404` is and when it happens
- You know why `basename` is protection

**We now have all the tools.** In the next step we start the first letter of
CRUD: **R** — showing the list of students from the database.

---

# Step 7 — **R** in CRUD: showing the list

> Now we start CRUD. The first letter is **R** — reading.

## What we do

Read the students out of the database and show them in a table.

## Why R first, and not C?

Because without a way to see the data, you cannot tell whether registering
worked. **First we build the way to look, then the way to add.**

---

## 7.1 — Two functions for `database.py`

Add these at the end of `database.py`:

```python
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

| Part | What it does |
| ---- | ------------ |
| `INSERT INTO ... VALUES (?, ?, ...)` | Adds a new row |
| `?` | A place for a value — **never write the value in directly** |
| `cursor.lastrowid` | The id of the row just added |
| `SELECT *` | Every column |
| `ORDER BY id DESC` | Newest at the top |
| `.fetchall()` | Takes all the rows |

> ### ⚠️ Why do we use `?`
>
> It is the **only** defence against **SQL Injection**.
>
> If you write `"... VALUES ('" + full_name + "')"`, somebody can type a name
> that contains SQL of their own, and drop your table.
>
> With `?`, SQLite knows this is **a value, not a command**. Even a name like
> `'; DROP TABLE students; --` is stored as nothing more than a name.
>
> This is covered in detail in the theory lesson.

## 7.2 — Add some test data

We have no form yet. So we add two students from the terminal:

```
python -c "import database; database.init_db(); database.add_student('MIS-2025-001', 'Ahmad Karim', 'MIS', 'Male', 'ahmad@example.com', '0770 111 1111')"
```

```
python -c "import database; database.add_student('MIS-2025-002', 'Sara Ali', 'Accounting', 'Female', 'sara@example.com', '0770 222 2222')"
```

> Run the same command twice and you get an error:
> `UNIQUE constraint failed` — the database refuses the duplicate itself,
> exactly as we set up in Step 4.

---

## 7.3 — `templates/list.html`

A new file in the `templates` folder:

```html
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

`<tbody>` is empty — the rows come from Python.

## 7.4 — Change `templates/home.html`

```html
<p>Welcome to the Student Registration System.</p>

{{ table }}
```

## 7.5 — Two functions for `app.py`

Add `import html` at the top, then these two functions beside `render()`:

```python
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

| Part | What it does |
| ---- | ------------ |
| `enumerate(students, start=1)` | Numbers the rows: 1, 2, 3 … |
| `student["full_name"]` | Reads the column by name — thanks to `row_factory` in Step 4 |
| `"""...""".format(...)` | A small template for each row |
| `"".join(rows)` | Joins every row into one piece of text |
| **`esc(...)`** | Makes the text safe — see below |

## 7.6 — Change `page_home`

```python
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

> **That `if` matters.** When there are no students, do not show an empty
> table — write a clear message. This is called an **empty state**, and it is
> part of what separates a good program from a poor one.

## 7.7 — Style the table

At the end of `static/style.css`:

```css
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

---

## 7.8 — Test it

Restart the server and press `Ctrl + Shift + R`.

## What you should see

```
2 student(s)

#   STUDENT ID     FULL NAME     DEPARTMENT   REGISTERED AT
1   MIS-2025-002   Sara Ali      Accounting   2026-09-03 06:07
2   MIS-2025-001   Ahmad Karim   MIS          2026-09-03 06:07
```

**Sara is at the top** because of `ORDER BY id DESC` — newest first.

> Look at the `#` column: Sara is number **1**, although her `id` is 2. That
> number comes from `enumerate()` and is only the position on the page — not
> the database `id`. That is deliberate: a student has no need for the
> internal id.

> `created_at` filled itself in — we never sent it. That was the
> `DEFAULT (datetime('now', 'localtime'))` from Step 4.

---

## 7.9 — A security test

Now add a student whose name is code:

```
python -c "import database; database.add_student('MIS-2025-003', '<script>alert(1)</script>', 'MIS', 'Male', '', '')"
```

Press `F5`.

**You should see the name as text**, like this:

```
<script>alert(1)</script>
```

and not an alert box.

**Why?** Because of `esc()`. It turns `<` into `&lt;`, so the browser reads it
as **text** rather than as **code**.

> Remove `esc()` and try again and the box appears. That is **XSS** — and
> those three letters are the reason it does not.
>
> In a real system that code could steal other people's accounts.

Then delete it:

```
python -c "import database; database.get_connection().execute('DELETE FROM students WHERE id = 3').connection.commit()"
```

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| `no such table: students` | Run `python -c "import database; database.init_db()"` |
| `UNIQUE constraint failed` | You are adding the same `student_id` twice — change the number |
| The table is empty | You have not added the data (see 7.2) |
| `{{ rows }}` appears as it is | The names do not match. Check `render("list.html", rows=...)` |
| `TypeError: tuple indices must be integers` | `row_factory = sqlite3.Row` is missing from `database.py` |
| `NameError: name 'html' is not defined` | You forgot `import html` |
| An `alert` box appears | You did not use `esc()` |
| The table has no styling | `Ctrl + Shift + R` |

---

## ✅ This step is finished when

```
student-system/
├── app.py              <- esc() and build_table_rows()
├── database.py         <- add_student() and get_all_students()
├── students.db         <- has data in it
├── templates/
│   ├── layout.html
│   ├── home.html       <- changed
│   └── list.html       <- new
└── static/
    └── style.css       <- table styling
```

- The students appear, out of the database
- The newest is at the top
- With no students, a clear message appears instead
- You know what `?` and `esc()` protect against

**One of four is done.** In the next step we build **C** — a form so a student
can be added without the terminal.

---

> Step 8 will be added here.