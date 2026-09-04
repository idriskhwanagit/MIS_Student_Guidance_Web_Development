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

> **What does the copy button copy?** In the boxes that have colour in them,
> the button copies **the whole block** as it should look **after the
> change** — the green lines together with the uncoloured ones around them,
> but without the struck-through ones.
>
> **Why not the green lines alone?** Because on their own they are
> fragments, and you would not know where in the file they go. The whole
> block shows you its own position.
>
> So: **select that block in your file and paste over it** — do not paste it
> at the cursor.

## The shape of every step

| Part | Meaning |
| ---- | ------- |
| **What we do** | The job of this step, in one sentence |
| **Why** | The purpose — without this you are only copying |
| **The code** | The complete code, not a fragment |
| **Green lines** | The ones **you add**. Uncoloured lines are already in the file — they are there so you can see where |
| **Struck-through lines** | The ones that **must be removed** |
| **How to test it** | Immediately after you type it |
| **What you should see** | The expected result |
| **If you get an error** | The most common errors and their fixes |

---

## Every code box tells you what to do with it

The bar above every code box carries **two things**:

- **which file** — for example `database.py`
- **what to do** — a coloured badge, one of these four:

| Badge | Meaning | What you do |
| ----- | ------- | ----------- |
| **new file** | This file does not exist yet | Create it in VS Code and type the code into it |
| **add this** | The file already exists | Put this code **at the end** of it. Leave what is already there **alone** |
| **change this** | Part of the file changes | Find that part in your file and **paste over it** |
| **just read it** | This is here to be understood | Type nothing — only look at it |

> **And the boxes with no badge?** The ones headed `Terminal` are commands —
> type them in the terminal. The ones headed `Output` are what you **should
> see** — they have no copy button, because there is nothing to take.

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
| 8 | **C** — the registration form + validation | ✅ |
| 9 | **U** — editing | ✅ |
| 10 | **D** — deleting | ✅ |
| 11 | Search | ✅ |
| 12 | Security — SQL Injection and XSS | ✅ |
| 13 | Final testing and `run.bat` | ✅ |

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

```bash
python --version
```

## What you should see

**If Python is installed** — something like this appears:

```out
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

```bash
python -c "import sqlite3; print('SQLite OK')"
```

This should appear:

```out
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

These two commands work and produce output.

```bash
python --version
```

```out
Python 3.x.x
```

```bash
python -c "import sqlite3; print('SQLite OK')"
```

```out
SQLite OK
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

```bash
dir
```

## What you should see

```out
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

```out
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

```python app.py new
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

<!-- collapse -->
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

```bash
python app.py
```

## What you should see

In the terminal:

```out
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

## 3.4.1 — Want your terminal back?

While the server runs it holds the terminal. Try these in order:

| # | What to do |
| - | ---------- |
| 1 | **Click inside the terminal**, then press `Ctrl + C` |
| 2 | If nothing happens, press `Ctrl + C` two or three times |
| 3 | Kill the terminal — the **🗑** icon at the top of the panel |
| 4 | Open a new terminal (`+`) and run `taskkill /IM python.exe /F` |

> **The first one matters most.** `Ctrl + C` often does nothing because the
> focus is on the editor rather than on the terminal.

### The better way: two terminals

You do not have to stop the server to run another command.

Click **`+`** at the top of the terminal panel:

```out
Terminal 1:  python app.py      <- the server, leave it running
Terminal 2:  anything else
```

> ⚠️ But do **not** run `python app.py` again in the second terminal — two
> servers on one port cause trouble (see the end of this step).

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
| The server says *Server running*, but the browser says `ERR_CONNECTION_REFUSED` | Two servers on one port. See below |
| `IndentationError` | The spacing at the start of the lines is uneven. Python is strict — use 4 spaces, not a Tab |
| `SyntaxError` | A character or a bracket is missing. Check the line named in the message |
| **This site can't be reached** | The server is not running. Look at the terminal |
| Kurdish letters show as `Ø¨Ø§` | `charset=utf-8` is missing from the `Content-Type` |
| My change does not show | You did not restart the server (see 3.7) |
| A white dot ● in the tab | The file is not saved. `Ctrl + S` |

---

## ⚠️ A server that runs but does not answer

This is the most common problem in this project, and it comes with **no
error at all** — which is what makes it hard to find.

**The sign:** the terminal says *Server running at http://localhost:8000*,
but the browser says `ERR_CONNECTION_REFUSED`.

**The cause:** an old Python process still holds port 8000. When you press
`Ctrl + C`, the process sometimes does not die straight away. The new server
then starts and **takes the same port** — and neither of them answers.

**Check:**

```bash
netstat -ano | findstr :8000
```

If **more than one line** appears, that is the problem.

**Fix:**

```bash
taskkill /IM python.exe /F
```

> This kills every Python process. While working on this project that is
> safe — this server is the only one running.

Then `python app.py` again.

> **Avoiding it:** after `Ctrl + C`, wait for the `>` to come back before
> starting the server again. And do not open **two terminals** for one
> project.

---

## ✅ This step is finished when

```out
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

```python database.py new
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

<!-- collapse -->
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

<!-- collapse -->
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

```diff app.py edit
 from http.server import BaseHTTPRequestHandler, HTTPServer
+
+import database
 
 
 class StudentAppHandler(BaseHTTPRequestHandler):
     def do_GET(self):
         self.send_response(200)
         self.send_header("Content-Type", "text/html; charset=utf-8")
         self.end_headers()
         self.wfile.write("<h1>Hello</h1>".encode("utf-8"))
 
 
+database.init_db()
 server = HTTPServer(("localhost", 8000), StudentAppHandler)
 print("Server running at http://localhost:8000")
 print("Press Ctrl + C to stop.")
 server.serve_forever()
```

Save both files with `Ctrl + S`.

## 4.6 — Test it

```bash
python app.py
```

## What you should see

Look at the VS Code **Explorer**. A new file has appeared:

```out
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

```bash
python -c "import database; print([r['name'] for r in database.get_connection().execute('SELECT name FROM sqlite_master')])"
```

You should see:

```out
['students', 'sqlite_autoindex_students_1', 'sqlite_sequence']
```

The first one is our table. SQLite created the other two itself — one for
`UNIQUE` and one for `AUTOINCREMENT`.

<!-- collapse -->
### What does this command do?

| Part | What it does |
| ---- | ------------ |
| `python -c "..."` | Runs one line of Python without making a file |
| `import database` | Brings in our own `database.py` |
| `get_connection()` | Connects to the database |
| `SELECT name FROM sqlite_master` | Returns the name of everything SQLite is holding |
| `sqlite_master` | An internal table: the list of all the tables |
| `[r['name'] for r in ...]` | Pulls out only the `name` column, rather than the whole row |

---

### The table is empty — how do we know?

The table exists, but there is no student in it yet. Type this:

```bash
python -c "import database; print(database.get_connection().execute('SELECT COUNT(*) FROM students').fetchone()[0])"
```

You should see:

```out
0
```

**Zero means the table is empty** — which is right at this point. In Step 7
we put data in and this number changes.

<!-- collapse -->
### What does this command do?

| Part | What it does |
| ---- | ------------ |
| `SELECT COUNT(*)` | Counts the rows, rather than reading them |
| `FROM students` | In the students table |
| `.fetchone()` | Takes one row — the result of the count |
| `[0]` | The first column of that row, which is the number |

> This one is worth keeping. Whenever you are unsure whether something was
> saved, this command answers it.

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

```out
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

```python read
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

```html templates/layout.html new
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

```html templates/home.html new
<p>Welcome to the Student Registration System.</p>
<p>Students registered: {{ total }}</p>
```

**This is the content of the home page** — no `<html>` or `<body>`, because
those are in `layout.html`.

## 5.3 — The `render()` function

Add this to `app.py`. First at the top:

```diff app.py edit
+import os
+import re
 from http.server import BaseHTTPRequestHandler, HTTPServer
 
 import database
+
+BASE_DIR = os.path.dirname(os.path.abspath(__file__))
+TEMPLATE_DIR = os.path.join(BASE_DIR, "templates")
+
+
+def render(template_name, **values):
+    path = os.path.join(TEMPLATE_DIR, template_name)
+    with open(path, encoding="utf-8") as file:
+        page = file.read()
+
+    def replace(match):
+        return str(values.get(match.group(1), ""))
+
+    return re.sub(r"\{\{\s*(\w+)\s*\}\}", replace, page)
```

## 5.4 — Use it

In the `StudentAppHandler` class, change `do_GET` like this:

```diff app.py edit
 class StudentAppHandler(BaseHTTPRequestHandler):
     def do_GET(self):
+        body = render("home.html", total=0)
+        page = render("layout.html", title="Students", content=body)
+
         self.send_response(200)
         self.send_header("Content-Type", "text/html; charset=utf-8")
         self.end_headers()
-        self.wfile.write("<h1>Hello</h1>".encode("utf-8"))
+        self.wfile.write(page.encode("utf-8"))
```

**We call it twice:**

1. Fill in `home.html` → that becomes the content
2. Put that content into `layout.html` → that becomes the whole page

<!-- collapse -->
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

```bash
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

```diff templates/home.html edit
-<p>Welcome to the Student Registration System.</p>
+<p>Hello from my own page!</p>
 <p>Students registered: {{ total }}</p>
```

Save it and just press `F5` in the browser.

**The change is there** — without restarting the server.

**Why?** Because `render()` reads the file **on every request**. Python code,
on the other hand, is read once, when the server starts.

| If you change this | Then do this |
| ------------------ | ------------ |
| An HTML file in the `templates` folder | Just `F5` in the browser |
| `app.py` or `database.py` | `Ctrl + C` → `python app.py` → `F5` |

> **Why:** `render()` reads the HTML file on **every request**, so the change
> shows at once. Python code is read **once** — when the server starts.

---

## ⚠️ A bug that really happened

Do not read about it — **see it**. Two small changes, then we undo them.

**1.** Add a comment line at the top of `templates/home.html`:

```diff templates/home.html edit
+<!-- the home page -->
 <p>Hello from my own page!</p>
 <p>Students registered: {{ total }}</p>
```

**2.** And one in `templates/layout.html`, just above `{{ content }}`:

```diff templates/layout.html edit
   <h1>{{ title }}</h1>
+  <!-- the content goes here: {{ content }} -->
   {{ content }}
```

Save both and press `F5` in the browser. (Do not restart the server — the
rule from 5.7.)

### What you should see

```out
Hello from my own page!
Students registered: 0
-->                              <- this should not be there!
Hello from my own page!          <- twice!
Students registered: 0
```

**The page is broken.** The content appears twice, and a stray `-->` has
turned up in the middle of it.

### Why? Three points

**1.** `render()` does not know what a comment is — it only looks for
`{{ }}`. So it replaced the one **inside the comment** as well.

**2.** A comment ends at the **first** `-->`.

**3.** The content that went into the comment has a `-->` of its own,
because `home.html` now has a comment.

That `-->` **closed the comment early**. Everything after it was no longer
hidden — so it showed.

```out
<!-- the content goes here: <!-- the home page --> <p>Hello...</p> -->
                                                 ^
                                     the comment ends here
                                                   ^
                                          and this shows
```

Then further down, the real `{{ content }}` put the same thing in again.

### Now delete both comments **completely**

Those two lines were only for the test. Take them both out:

```diff templates/layout.html edit
   <h1>{{ title }}</h1>
-  <!-- the content goes here: {{ content }} -->
   {{ content }}
```

```diff templates/home.html edit
-<!-- the home page -->
 <p>Hello from my own page!</p>
 <p>Students registered: {{ total }}</p>
```

### And one last thing — put the sentence back

`Hello from my own page!` was written in 5.7, and that was only a test too.
Put it back as it was:

```diff templates/home.html edit
-<p>Hello from my own page!</p>
+<p>Welcome to the Student Registration System.</p>
 <p>Students registered: {{ total }}</p>
```

`F5` → the page is right again:

```out
Welcome to the Student Registration System.
Students registered: 0
```

> ⚠️ **Both of them matter.** If they stay, your files will not match the
> ones in the guide from here on, and the changes shown in later steps will
> not line up.

> **The rule:** never write `{{ }}` inside a comment.
>
> The same happens in PHP, Django and Laravel — a template processor looks
> at the **text**, not at the meaning of the HTML.

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

```out
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

```css static/style.css new
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

<!-- collapse -->
## 6.1.1 — What does this CSS do?

| Rule | What it does |
| ---- | ------------ |
| `:root { --brand: ... }` | Names a colour, so it can be changed in one place |
| `* { box-sizing: border-box }` | Widths count the padding and border — without it layouts break |
| `body { margin: 0 }` | Removes the margin the browser adds by default |
| `padding: 24px` | Space between the content and the edge of the window |
| `background: var(--background)` | Uses the colour we named in `:root` |
| `font-family: "Segoe UI", Tahoma, Arial` | A fallback list: if the first is missing, the second |
| `line-height: 1.6` | Space between lines — it makes reading easier |
| `h1 { color: var(--brand) }` | The heading in the main colour |
| `.card { max-width: 700px }` | The box never grows wider than 700 pixels |
| `border-radius: 10px` | Rounds the corners |

## 6.2 — Link it from `layout.html`

Open `templates/layout.html` and make two changes:

```diff templates/layout.html edit
 <!DOCTYPE html>
 <html lang="en">
 <head>
   <meta charset="UTF-8">
   <title>{{ title }}</title>
+  <link rel="stylesheet" href="/static/style.css">
 </head>
 <body>
   <h1>{{ title }}</h1>
-  {{ content }}
+  <div class="card">
+    {{ content }}
+  </div>
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

```diff app.py edit
 import os
 import re
+import urllib.parse
 from http.server import BaseHTTPRequestHandler, HTTPServer
 
 import database
 
 BASE_DIR = os.path.dirname(os.path.abspath(__file__))
 TEMPLATE_DIR = os.path.join(BASE_DIR, "templates")
+STATIC_DIR = os.path.join(BASE_DIR, "static")
```

Then the class:

```diff app.py edit
 class StudentAppHandler(BaseHTTPRequestHandler):
     def do_GET(self):
+        url = urllib.parse.urlparse(self.path)
+
+        if url.path == "/":
+            self.page_home()
+        elif url.path.startswith("/static/"):
+            self.send_static(url.path[len("/static/"):])
+        else:
+            self.send_response(404)
+            self.end_headers()
+
+    def page_home(self):
         body = render("home.html", total=0)
         page = render("layout.html", title="Students", content=body)
 
         self.send_response(200)
         self.send_header("Content-Type", "text/html; charset=utf-8")
         self.end_headers()
         self.wfile.write(page.encode("utf-8"))
+
+    def send_static(self, filename):
+        safe_name = os.path.basename(filename)
+        path = os.path.join(STATIC_DIR, safe_name)
+
+        if not os.path.isfile(path):
+            self.send_response(404)
+            self.end_headers()
+            return
+
+        with open(path, "rb") as file:
+            body = file.read()
+
+        self.send_response(200)
+        self.send_header("Content-Type", "text/css; charset=utf-8")
+        self.end_headers()
+        self.wfile.write(body)
```

<!-- collapse -->
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

```bash
python app.py
```

then `http://localhost:8000` — and this time press `Ctrl + Shift + R`.

## What you should see

- A pale blue-grey background
- A blue heading
- A white box with a soft border

**The design works.**

## 6.6.1 — What does each rule do? See for yourself

The table in 6.1.1 describes each rule. But **seeing beats reading**.

### 1. Right-click **on the white box itself**

Not on an empty part of the page — on the box. Then **Inspect**.

> **Why on the box itself?** Because then the browser **selects that part
> for you**. Click anywhere else and you have to go looking for it.

### 2. What the panel looks like

A new panel opens with tabs along its top:

```out
Elements   Console   Sources   Network   ...
```

**Elements** is the one you want — it opens there by default. Inside it are
two parts:

| Part | What is in it |
| ---- | ------------- |
| **Elements** (top or left) | The page's HTML, as a tree |
| **Styles** (bottom or right) | The CSS of whatever is selected |

In **Elements** this line is **highlighted** — because you right-clicked
that box:

```out
<div class="card">
```

### 3. Now look at the Styles part

**What you see is the very code you wrote:**

```out
Styles
──────────────────────────────────────────
.card {                      style.css:34
  ☑  max-width: 700px;
  ☑  padding: 20px;
  ☑  background: #ffffff;
  ☑  border: 1px solid #e5e7eb;
  ☑  border-radius: 10px;
}
```

Three things to learn here:

| What you see | What it means |
| ------------ | ------------- |
| `.card { ... }` | The same rule you wrote in `style.css` |
| `style.css:34` | **Which file and which line** — click it and you land on that line |
| ☑ beside each line | A checkbox — you can switch it off |

> **This is the best tool there is for learning CSS.** When a rule of yours
> does not seem to work, this is where you find out whether it reached the
> element at all.

### 4. Now switch the checkboxes off

Switch these three rules **off** one at a time — and watch the page:

| Switch this off | What happens |
| --------------- | ------------ |
| `background` | The white box **disappears** — the page background shows through |
| `border-radius` | The corners turn **sharp** |
| `padding` | The text **sticks** to the edge |

`padding` is the clearest of the three. The moment it is off, you can see
why it is there.

> ### 🤔 Have I broken my file?
>
> **No.** `style.css` was **never changed**. Those changes live only in the
> **browser's memory**.
>
> Press **`F5`** → everything comes back.

> **This is a working tool, not just a teaching one.** Everybody who builds
> for the web tries their CSS here first, and writes into the file only what
> worked.

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

You now have three cases — here is the whole table:

| If you change this | Then do this |
| ------------------ | ------------ |
| An HTML file in `templates` | `F5` |
| `static/style.css` | **`Ctrl + Shift + R`** |
| `app.py` or `database.py` | `Ctrl + C` → `python app.py` → `F5` |

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

```out
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

```python database.py add
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
## 7.1.1 — What does this code do?

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

```bash
python -c "import database; database.init_db(); database.add_student(student_id='MIS-2025-001', full_name='Ahmad Karim', department='MIS', gender='Male', email='ahmad@example.com', phone='0770 111 1111')"
```

```bash
python -c "import database; database.add_student(student_id='MIS-2025-002', full_name='Sara Ali', department='Accounting', gender='Female', email='sara@example.com', phone='0770 222 2222')"
```

> These two lines are long, and they are not part of the project — they are
> only test data. **Copying is allowed here.**

## What you should see

**Nothing.** The terminal prints an empty line and gives you back the `>`.

That is not a fault. Python says nothing unless you tell it to, and we did
not. `add_student()` records the student, but prints nothing.

> If you see a long red message starting with `Traceback`, that *is* an
> error. Read the **last line** — the reason is written there.

<!-- collapse -->
### What does this command do?

| Part | What it does |
| ---- | ------------ |
| `python -c "..."` | Runs one line of Python without making a file |
| `import database` | Brings in our own `database.py` |
| `database.init_db()` | Makes sure the table is there |
| `student_id='MIS-2025-001'` | The university number |
| `full_name='Ahmad Karim'` | The student's name |
| `department='MIS'` | Their department |
| `gender='Male'` | Gender |
| `email=` and `phone=` | Email and phone number |

> Each value carries its own name (`full_name=`), so you do not have to
> remember which one comes first. In Python this is called a
> **keyword argument**.

> Run the same command twice and you get an error:
> `UNIQUE constraint failed` — the database refuses the duplicate itself,
> exactly as we set up in Step 4.

## 7.2.1 — Make sure it worked

The commands above said nothing, so we have to ask for ourselves: **what
went into the database?**

```bash
python -c "import database; rows = database.get_all_students(); print(len(rows), 'students'); print([r['full_name'] for r in rows])"
```

## What you should see

```out
2 students
['Sara Ali', 'Ahmad Karim']
```

| If you see | It means |
| ---------- | -------- |
| `2 students` | Both commands worked ✅ |
| `0 students` | Nothing was added — run the commands above again |
| `1 students` | Only one worked — run the other one again |
| `no such table` | `init_db()` never ran — run the first command again |

> **Why is Sara first?** Because of `ORDER BY id DESC` — newest at the top.
> We wrote that in 7.1.

> This command **changes nothing** — it only reads. Use it whenever you are
> not sure what is in the database.

---

## 7.3 — `templates/list.html`

A new file in the `templates` folder:

```html templates/list.html new
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

> **Nothing changes yet.** The file exists, but nothing calls it — we do
> that in 7.6. Press `F5` now and the page looks exactly the same.

## 7.4 — Change `templates/home.html`

```diff templates/home.html edit
 <p>Welcome to the Student Registration System.</p>
-<p>Students registered: {{ total }}</p>
+
+{{ table }}
```

## What you should see

**Do not restart the server.** Just press `F5` in the browser.

> Remember from Step 5: a template file is read on **every request**, so a
> change inside one shows up immediately.

The line **Students registered: 0** is **gone** — the one that has been
on the page since 5.6, and was still there at the end of Step 6. Only
this is left:

```out
Welcome to the Student Registration System.
```

> If you see **`Hello from my own page!`** instead, you never put the
> sentence back at the end of Step 5. It is not serious — but put it back
> now, because 8.7 changes this line and it has to match the guide.

**Why?** We removed `{{ total }}`, and nothing has been passed to the new
`{{ table }}` yet. When `render()` meets a name it was given no value for,
it puts **an empty string** there — it does not raise an error.

> The page is nearly bare now. That is deliberate, and it is **the sign
> that your change worked**. We fill `table` in 7.6.

## 7.5 — Two functions for `app.py`

First at the top of the file:

```diff app.py edit
+import html
 import os
 import re
```

Then add these **two new functions**.

**Where exactly?** Between two fixed points:

- **After** the end of the `render()` function — the line ending in
  `return re.sub(...)`
- **Before** the line that starts with `class StudentAppHandler`

That is, in the gap that already sits between them. Leave two blank lines
between functions — that is how Python code is written.

```diff app.py edit
     return re.sub(r"\{\{\s*(\w+)\s*\}\}", replace, page)
 
 
+def esc(value):
+    return html.escape("" if value is None else str(value))
+
+
+def build_table_rows(students):
+    rows = []
+    for number, student in enumerate(students, start=1):
+        rows.append(
+            """
+            <tr>
+              <td>{number}</td>
+              <td>{student_id}</td>
+              <td>{full_name}</td>
+              <td>{department}</td>
+              <td>{created_at}</td>
+            </tr>
+            """.format(
+                number=number,
+                student_id=esc(student["student_id"]),
+                full_name=esc(student["full_name"]),
+                department=esc(student["department"]),
+                created_at=esc(student["created_at"]),
+            )
+        )
+    return "".join(rows)
+
+
 class StudentAppHandler(BaseHTTPRequestHandler):
```

> A new function must start **at the far left, with no indentation** — just
> like `render()` itself. If you indent the `def` by mistake, Python thinks
> it belongs inside another function and reports an error.


<!-- collapse -->
## 7.5.1 — What does this code do?

| Part | What it does |
| ---- | ------------ |
| `enumerate(students, start=1)` | Numbers the rows: 1, 2, 3 … |
| `student["full_name"]` | Reads the column by name — thanks to `row_factory` in Step 4 |
| `"""...""".format(...)` | A small template for each row |
| `"".join(rows)` | Joins every row into one piece of text |
| **`esc(...)`** | Makes the text safe — see below |

## What you should see

Press `Ctrl + S`, then restart the server:

```bash
python app.py
```

```out
Server running at http://localhost:8000
```

**The page does not change** — and that is right. The two functions are
written, but **nothing calls them yet**. We call them in 7.6.

**So what is the result of this section?** That the server **starts**. If
your indentation were wrong, it would show here — not two sections later.

| If you see | It means |
| ---------- | -------- |
| `Server running at ...` | Everything is right ✅ |
| `IndentationError` | There is a space before `def` — it must start at the far left |
| `SyntaxError` | A `)` or a `"""` was never closed. The line number is in the message |
| `unexpected indent` | The lines inside the function do not line up — use 4 spaces |

> **Do not forget `import html`.** If you left it out, the server still
> starts fine — because `esc()` has not been called yet. The error only
> appears in 7.8, as `NameError: name 'html' is not defined`.

## 7.6 — Change `page_home`

Change the `page_home` function like this:

```diff app.py edit
     def page_home(self):
-        body = render("home.html", total=0)
+        students = database.get_all_students()
+
+        if students:
+            table = render("list.html",
+                           rows=build_table_rows(students),
+                           total=len(students))
+        else:
+            table = "<p>No student is registered yet.</p>"
+
+        body = render("home.html", table=table)
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

```css static/style.css add
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
## 7.7.1 — What does this CSS do?

| Rule | What it does |
| ---- | ------------ |
| `width: 100%` | The table takes the full width |
| `border-collapse: collapse` | Merges the lines between cells — without it you get two side by side |
| `padding: 8px 12px` | Space inside the cells: 8 top and bottom, 12 at the sides |
| `border-bottom` | One line under each row, rather than a full grid |
| `text-align: left` | The text starts from the left |
| `thead th { text-transform: uppercase }` | The headings in capitals |
| `tbody tr:last-child td { border-bottom: none }` | The last row has no line under it |

---

## 7.8 — Test it

Restart the server and press `Ctrl + Shift + R`.

## What you should see

```out
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

```bash
python -c "import database; database.add_student(student_id='MIS-2025-003', full_name='<script>alert(1)</script>', department='MIS', gender='Male', email='', phone='')"
```

Press `F5`.

**You should see the name as text**, like this:

```out
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

```bash
python -c "import database; database.get_connection().execute('DELETE FROM students WHERE id = 3').connection.commit()"
```

<!-- collapse -->
### What does this command do?

| Part | What it does |
| ---- | ------------ |
| `get_connection()` | Connects to the database |
| `execute('DELETE ...')` | Runs the SQL statement |
| `WHERE id = 3` | Only the row whose `id` is 3 |
| `.connection.commit()` | Saves the change |

> In Step 10 we write a proper function for deleting. Here we use SQL
> directly, because it is a one-off.

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

```out
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

# Step 8 — **C** in CRUD: the registration form

> The biggest step. Here a student sends something **from the browser into
> the database** for the first time.

## What we do

Build a form that registers a new student — without the terminal.

## Why this one is different

Everything so far has been **reading** (`GET`). Now we are **changing**
(`POST`). Three new things are needed:

| Needed | Why |
| ------ | --- |
| `do_POST` | A `POST` request is handled separately from a `GET` |
| Validation | Users make mistakes — bad data must not reach the database |
| A redirect | So that `F5` does not register the student twice |

---

## 8.1 — A new function for `database.py`

Before registering, we need to know whether that number is already taken:

```python database.py add
def student_id_exists(student_id):
    with get_connection() as connection:
        row = connection.execute(
            "SELECT id FROM students WHERE student_id = ?", (student_id,)
        ).fetchone()
        return row is not None
```

### This is not a duplicate — though it looks like one

In Step 4 we wrote that `student_id` must be `UNIQUE`, which means the
database already refuses a repeated number. So why ask again?

Because both stop the same thing, but in **two very different ways**:

| | The database's `UNIQUE` | `student_id_exists()` |
| --- | --- | --- |
| When it acts | As the row is written | **Before** anything is written |
| What happens | The program crashes | An ordinary message |
| What the user sees | A red error page | The form, with their typing still in it |
| What they typed | **Lost** | Kept |

Without this function, one repeated number gives an `IntegrityError` and
everything the person typed is gone.

> **So why keep both?**
>
> `UNIQUE` is the **last line of defence** — we never drop it, because data
> can arrive another way (those terminal commands in 7.2, for instance).
>
> `student_id_exists()` is there **out of respect for the person** — someone
> arriving through the form deserves a human answer, not a `Traceback`.
>
> This is known as **defence in depth**: one guard is never enough.

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `SELECT id FROM students WHERE student_id = ?` | Looks for that number |
| `.fetchone()` | Just one row — we do not need more |
| `row is not None` | If it found something, it is already taken |

---

## 8.2 — `templates/form.html`

A new file:

```html templates/form.html new
<h2>{{ heading }}</h2>

{{ errors }}

<form method="POST" action="/add" class="student-form">

  <label class="field">
    <span>Student ID *</span>
    <input type="text" name="student_id" value="{{ student_id }}" required>
  </label>

  <label class="field">
    <span>Full name *</span>
    <input type="text" name="full_name" value="{{ full_name }}" required>
  </label>

  <label class="field">
    <span>Department *</span>
    <select name="department" required>
      <option value="">-- Choose a department --</option>
      {{ departments }}
    </select>
  </label>

  <div class="field">
    <span>Gender *</span>
    <div class="radio-row">
      <label><input type="radio" name="gender" value="Male" required> Male</label>
      <label><input type="radio" name="gender" value="Female"> Female</label>
    </div>
  </div>

  <label class="field">
    <span>Email</span>
    <input type="email" name="email" value="{{ email }}">
  </label>

  <label class="field">
    <span>Phone</span>
    <input type="text" name="phone" value="{{ phone }}">
  </label>

  <div class="form-actions">
    <button type="submit">Register student</button>
    <a href="/">Cancel</a>
  </div>

</form>
```

<!-- collapse -->
### What does this HTML do?

| Part | What it does |
| ---- | ------------ |
| `method="POST"` | Sends the data as a `POST`, not a `GET` |
| `action="/add"` | Which path it is sent to |
| `name="student_id"` | The name the server reads — it **must match** |
| `value="{{ student_id }}"` | If something is wrong, the typing is not lost |
| `required` | The browser itself refuses an empty field |
| `<select>` and `<option>` | A list to choose from |
| `type="radio"` with the same `name` | Only one can be chosen |
| `type="email"` | The browser checks the shape of the address |

> ⚠️ `required` and `type="email"` are **on the client** — they can be
> removed with `F12`. That is why step 8.5 checks the same things **on the
> server**.

## 8.3 — The list of departments

At the top of `app.py`, under `STATIC_DIR`:

```python app.py add
DEPARTMENTS = [
    "Management Information Systems",
    "Accounting",
    "Business Administration",
    "Computer Science",
    "Statistics",
]


def build_department_options(selected):
    parts = []
    for name in DEPARTMENTS:
        chosen = " selected" if name == selected else ""
        parts.append('<option value="%s"%s>%s</option>' % (esc(name), chosen, esc(name)))
    return "\n".join(parts)
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `DEPARTMENTS` | The departments in one place — easy to change |
| `selected` | The department already chosen |
| `" selected"` | If they match, that `<option>` is selected |
| `esc(name)` | The same protection as Step 7 |

---

## 8.4 — Three helpers for the class

Add these inside `StudentAppHandler`:

```python app.py add
    def send_html(self, content, status=200):
        body = content.encode("utf-8")
        self.send_response(status)
        self.send_header("Content-Type", "text/html; charset=utf-8")
        self.end_headers()
        self.wfile.write(body)

    def redirect(self, location):
        self.send_response(303)
        self.send_header("Location", location)
        self.end_headers()

    def read_form(self):
        length = int(self.headers.get("Content-Length", 0))
        raw = self.rfile.read(length).decode("utf-8")
        data = urllib.parse.parse_qs(raw)
        return {key: value[0].strip() for key, value in data.items()}
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `send_html` | The three lines that kept repeating, now in one place |
| `redirect` | Tells the browser to go to another path |
| `303` | The code for "it is over there" — used after a `POST` |
| `Content-Length` | How many bytes of data are coming |
| `self.rfile.read(...)` | Reads the body of the request |
| `parse_qs(raw)` | Turns `a=1&b=2` into `{"a": ["1"], "b": ["2"]}` |
| `value[0].strip()` | The first value, without spaces around it |

## 8.5 — Two new pages

Add these as well:

```python app.py add
    def page_form(self, errors="", values=None):
        values = values or {}
        body = render(
            "form.html",
            heading="Register a new student",
            errors=errors,
            student_id=esc(values.get("student_id", "")),
            full_name=esc(values.get("full_name", "")),
            email=esc(values.get("email", "")),
            phone=esc(values.get("phone", "")),
            departments=build_department_options(values.get("department", "")),
        )
        self.send_html(render("layout.html", title="New student", content=body))

    def save_student(self):
        form = self.read_form()

        problems = []
        if not form.get("student_id"):
            problems.append("Student ID is required.")
        if not form.get("full_name"):
            problems.append("Full name is required.")
        if not form.get("department"):
            problems.append("Please choose a department.")
        if not form.get("gender"):
            problems.append("Please choose a gender.")
        if form.get("email") and "@" not in form["email"]:
            problems.append("The email address is not valid.")
        if form.get("student_id") and database.student_id_exists(form["student_id"]):
            problems.append("This student ID is already registered.")

        if problems:
            items = "".join("<li>" + esc(p) + "</li>" for p in problems)
            return self.page_form('<div class="alert"><ul>' + items + "</ul></div>", form)

        database.add_student(
            form["student_id"], form["full_name"], form["department"],
            form["gender"], form.get("email", ""), form.get("phone", ""),
        )
        self.redirect("/")
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `values or {}` | If nothing was passed, an empty dictionary |
| `problems = []` | The list of errors — we show them all together |
| `if not form.get(...)` | An empty field |
| `"@" not in email` | A simple check on the address |
| `student_id_exists(...)` | A duplicate number |
| `return self.page_form(errors, form)` | The same form, **with the data** |
| `self.redirect("/")` | After success, go to the list |

> ### ⚠️ The most important line
>
> ```python
> return self.page_form('<div class="alert">...', form)
> ```
>
> That second `form` means: **give back what the user typed**.
>
> Without it, a student fills in every field, makes one small mistake, and
> **loses all of it**. It is the most common reason people give up on a form.

## 8.6 — The routes

Change `do_GET`, and add the new `do_POST` below it:

```diff app.py edit
     def do_GET(self):
         url = urllib.parse.urlparse(self.path)
 
         if url.path == "/":
             self.page_home()
+        elif url.path == "/add":
+            self.page_form()
         elif url.path.startswith("/static/"):
             self.send_static(url.path[len("/static/"):])
         else:
             self.send_response(404)
             self.end_headers()
+
+    def do_POST(self):
+        url = urllib.parse.urlparse(self.path)
+
+        if url.path == "/add":
+            self.save_student()
+        else:
+            self.send_response(404)
+            self.end_headers()
```

> **`/add` appears twice — but they are two different things:**
>
> | | What it does |
> |---|-------------|
> | `GET /add` | Shows the empty form |
> | `POST /add` | Takes the data and saves it |
>
> This is the ordinary shape of the web: one path, two actions.

## 8.7 — A link to the form

Add one line at the top of `templates/home.html`:

```diff templates/home.html edit
-<p>Welcome to the Student Registration System.</p>
+<p><a href="/add">+ Register a new student</a></p>
 
 {{ table }}
```

## 8.8 — Style the form

At the end of `static/style.css`:

```css static/style.css add
.student-form {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 480px;
}

.field {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.field > span {
  font-size: 13px;
  font-weight: 600;
}

.field input,
.field select {
  padding: 9px 12px;
  border: 1px solid var(--border);
  border-radius: 8px;
  font-size: 14px;
  font-family: inherit;
}

.radio-row {
  display: flex;
  gap: 18px;
}

.form-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

button {
  padding: 9px 18px;
  border: 0;
  border-radius: 8px;
  background: var(--brand);
  color: #fff;
  font-size: 14px;
  font-family: inherit;
  cursor: pointer;
}

.alert {
  margin-bottom: 16px;
  padding: 12px 16px;
  border: 1px solid #fecaca;
  border-radius: 8px;
  background: #fef2f2;
  color: #991b1b;
}

.alert ul {
  margin: 0;
  padding-left: 20px;
}
```

<!-- collapse -->
### What does this CSS do?

| Rule | What it does |
| ---- | ------------ |
| `display: flex; flex-direction: column` | The fields stack, rather than sitting side by side |
| `gap: 16px` | Space between the fields — without margins |
| `max-width: 480px` | The form never gets too wide to read |
| `.field > span` | The field's name, small and bold |
| `font-family: inherit` | Otherwise the inputs use a different font |
| `.radio-row { display: flex }` | Male and Female next to each other |
| `.alert` | The red box holding the errors |

---

## 8.9 — Test it

Restart the server, then `Ctrl + Shift + R`.

**1. Open the form** — click **+ Register a new student**

**2. Submit it empty** — click **Register student** without filling anything
in. The browser itself refuses (`required`).

**3. Test the server's own checks:**
- Fill in `student_id` and `full_name`
- Choose a department and a gender
- In the email field type: `abc`

If the browser refuses, change `type="email"` to `type="text"` for the test.
You should see the red **The email address is not valid.** — and
**everything you typed is still there**.

**4. Register a student** — fill it in properly and submit. You should come
back to the list with the student at the top.

**5. Submit it again** — register the same `student_id` twice.
The message **This student ID is already registered.**

---

## 8.10 — The `F5` test

This is the most important test in this step.

After a successful registration, press **`F5`** on the list page.

**Nothing happens** — the list simply reloads.

**Why?** Because of this line:

```python app.py read
self.redirect("/")
```

After the `POST`, the server does not say "done" — it says **"go to `/`"**.
So the page in front of you is a `GET /`, not a `POST /add`.

> **What would happen without that line?** `F5` would **send the `POST`
> again**, and the browser would ask "resend?". Every student who pressed
> `F5` would be registered twice.
>
> The pattern is called **PRG** — Post, Redirect, Get. It is covered in the
> theory lesson.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| `501 Unsupported method ('POST')` | You have not added `do_POST` |
| The form returns `404` | `elif url.path == "/add"` is missing from `do_GET` |
| `KeyError: 'student_id'` | The `name="student_id"` in the HTML does not match the code |
| My data is lost after an error | You did not pass `form` to `page_form` (see 8.5) |
| `F5` registers again | You are missing `self.redirect("/")` |
| The error message does not show | `{{ errors }}` is missing from `form.html` |
| `UnicodeDecodeError` | `.decode("utf-8")` is missing from `read_form` |
| The departments do not appear | Check `{{ departments }}` or `build_department_options` |

---

## ✅ This step is finished when

```out
student-system/
├── app.py              <- do_POST, validation, redirect
├── database.py         <- student_id_exists()
├── students.db
├── templates/
│   ├── layout.html
│   ├── home.html       <- a link to the form
│   ├── list.html
│   └── form.html       <- new
└── static/
    └── style.css       <- the form styling
```

- A student can be registered from the browser
- Empty fields and a bad email are refused
- A duplicate number is refused
- After an error, the typing is not lost
- `F5` does not register twice

**Two of four are done.** In the next step, **U** — editing, which reuses the
same form.

---

# Step 9 — **U** in CRUD: editing

> This step is shorter than you expect — because we reuse **the same form**.

## What we do

Let the details of a registered student be changed.

## Why not build a second form?

The edit form and the registration form have **the same fields**. With two
files:

- every change has to be made **twice**
- one day one of them is forgotten, and they drift apart

So we use one file and change only **two things**: where it submits to, and
the name on the button. The principle is called **DRY** — *Don't Repeat
Yourself*.

---

## 9.1 — Two functions for `database.py`

```python database.py add
def get_student(row_id):
    with get_connection() as connection:
        return connection.execute(
            "SELECT * FROM students WHERE id = ?", (row_id,)
        ).fetchone()


def update_student(row_id, student_id, full_name, department, gender, email, phone):
    with get_connection() as connection:
        connection.execute(
            """
            UPDATE students
               SET student_id = ?,
                   full_name  = ?,
                   department = ?,
                   gender     = ?,
                   email      = ?,
                   phone      = ?
             WHERE id = ?
            """,
            (student_id, full_name, department, gender, email, phone, row_id),
        )
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `get_student(row_id)` | Fetches one student by `id` |
| `.fetchone()` | One row, or `None` if there is none |
| `UPDATE ... SET` | Puts the new values in |
| `WHERE id = ?` | **Only that row** |
| The order of the `?` | Six values, then `row_id` — it **must match** |

> ### ⚠️ Never forget the `WHERE`
>
> ```sql
> UPDATE students SET department = 'MIS';
> ```
>
> That puts **every student** in MIS. Without a `WHERE`, `UPDATE` and
> `DELETE` apply to the whole table.
>
> It is one of the most dangerous mistakes in SQL, and it has happened at
> large companies.

## 9.2 — Change `student_id_exists`

Change the function like this:

```diff database.py edit
-def student_id_exists(student_id):
+def student_id_exists(student_id, ignore_row_id=None):
     with get_connection() as connection:
-        row = connection.execute(
-            "SELECT id FROM students WHERE student_id = ?", (student_id,)
-        ).fetchone()
+        if ignore_row_id is None:
+            row = connection.execute(
+                "SELECT id FROM students WHERE student_id = ?", (student_id,)
+            ).fetchone()
+        else:
+            row = connection.execute(
+                "SELECT id FROM students WHERE student_id = ? AND id <> ?",
+                (student_id, ignore_row_id),
+            ).fetchone()
         return row is not None
```

> ### 🤔 Why `ignore_row_id`?
>
> Think it through: you edit a student and change only the name — leaving the
> number as it was.
>
> The check says: *"that number already exists!"* — and it does, **on that
> same student**.
>
> `ignore_row_id` says: look for it, but **do not count this row**.
> `id <> ?` means "where `id` is not equal to".
>
> Without it, no student could ever be edited.

---

## 9.3 — Change `templates/form.html`

Three changes: a hidden field, a variable action, and a variable button.

```diff templates/form.html edit
 <h2>{{ heading }}</h2>
 
 {{ errors }}
 
-<form method="POST" action="/add" class="student-form">
+<form method="POST" action="{{ action }}" class="student-form">
+
+  <input type="hidden" name="id" value="{{ row_id }}">
 
   <label class="field">
     <span>Student ID *</span>
     <input type="text" name="student_id" value="{{ student_id }}" required>
   </label>
 
   <label class="field">
     <span>Full name *</span>
     <input type="text" name="full_name" value="{{ full_name }}" required>
   </label>
 
   <label class="field">
     <span>Department *</span>
     <select name="department" required>
       <option value="">-- Choose a department --</option>
       {{ departments }}
     </select>
   </label>
 
   <div class="field">
     <span>Gender *</span>
     <div class="radio-row">
-      <label><input type="radio" name="gender" value="Male" required> Male</label>
-      <label><input type="radio" name="gender" value="Female"> Female</label>
+      <label><input type="radio" name="gender" value="Male"{{ male_checked }} required> Male</label>
+      <label><input type="radio" name="gender" value="Female"{{ female_checked }}> Female</label>
     </div>
   </div>
 
   <label class="field">
     <span>Email</span>
     <input type="email" name="email" value="{{ email }}">
   </label>
 
   <label class="field">
     <span>Phone</span>
     <input type="text" name="phone" value="{{ phone }}">
   </label>
 
   <div class="form-actions">
-    <button type="submit">Register student</button>
+    <button type="submit">{{ submit_label }}</button>
     <a href="/">Cancel</a>
   </div>
 
 </form>
```

<!-- collapse -->
### What does this HTML do?

| Part | What it does |
| ---- | ------------ |
| `<input type="hidden" name="id">` | The user never sees it, but it is sent with the form |
| `action="{{ action }}"` | `/add` or `/edit` — Python decides |
| `{{ submit_label }}` | *Register student* or *Save changes* |
| `{{ male_checked }}` | When editing, the previous gender is selected |

> **Why a hidden field?** The server has to know **which student** is being
> changed. That `id` comes in through the URL (`/edit?id=2`), goes into the
> form, and returns with the `POST`.

## 9.4 — Change `page_form`

Change the function like this:

```diff app.py edit
-    def page_form(self, errors="", values=None):
-        values = values or {}
+    def page_form(self, row_id="", errors="", values=None):
+        student = database.get_student(row_id) if row_id else None
+
+        if row_id and student is None:
+            self.send_response(404)
+            self.end_headers()
+            return
+
+        if values is None:
+            values = dict(student) if student else {}
+
+        is_edit = student is not None
+        gender = values.get("gender", "")
+
         body = render(
             "form.html",
-            heading="Register a new student",
+            heading="Edit student" if is_edit else "Register a new student",
+            action="/edit" if is_edit else "/add",
+            submit_label="Save changes" if is_edit else "Register student",
+            row_id=esc(values.get("id", "")),
             errors=errors,
             student_id=esc(values.get("student_id", "")),
             full_name=esc(values.get("full_name", "")),
             email=esc(values.get("email", "")),
             phone=esc(values.get("phone", "")),
             departments=build_department_options(values.get("department", "")),
+            male_checked=" checked" if gender == "Male" else "",
+            female_checked=" checked" if gender == "Female" else "",
         )
-        self.send_html(render("layout.html", title="New student", content=body))
+        title = "Edit student" if is_edit else "New student"
+        self.send_html(render("layout.html", title=title, content=body))
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `if row_id else None` | With no `id`, this is the add form |
| `student is None` → `404` | An `id` was asked for that does not exist |
| `values is None` | First time round: use the saved values |
| `dict(student)` | Turns the database row into a dictionary |
| `is_edit` | One variable, three decisions taken from it |
| `gender == "Male"` | Which radio button is selected |

> **Note:** if `values` was passed in — meaning something went wrong — then
> what the user typed is used, not what is in the database. The same
> principle as Step 8.

## 9.5 — Change `save_student`

Change `save_student` like this:

```diff app.py edit
-    def save_student(self):
+    def save_student(self, is_edit=False):
         form = self.read_form()
+        row_id = form.get("id", "") if is_edit else ""
 
         problems = []
         if not form.get("student_id"):
             problems.append("Student ID is required.")
         if not form.get("full_name"):
             problems.append("Full name is required.")
         if not form.get("department"):
             problems.append("Please choose a department.")
         if not form.get("gender"):
             problems.append("Please choose a gender.")
         if form.get("email") and "@" not in form["email"]:
             problems.append("The email address is not valid.")
-        if form.get("student_id") and database.student_id_exists(form["student_id"]):
+        if form.get("student_id") and database.student_id_exists(
+            form["student_id"], ignore_row_id=row_id if is_edit else None
+        ):
             problems.append("This student ID is already registered.")
 
         if problems:
             items = "".join("<li>" + esc(p) + "</li>" for p in problems)
-            return self.page_form('<div class="alert"><ul>' + items + "</ul></div>", form)
+            return self.page_form(row_id, '<div class="alert"><ul>' + items + "</ul></div>", form)
 
-        database.add_student(
+        values = (
             form["student_id"], form["full_name"], form["department"],
             form["gender"], form.get("email", ""), form.get("phone", ""),
         )
+
+        if is_edit:
+            database.update_student(row_id, *values)
+        else:
+            database.add_student(*values)
+
         self.redirect("/")
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `is_edit=False` | One function, two jobs |
| `row_id = form.get("id")` | It comes from the hidden field |
| `ignore_row_id=row_id if is_edit else None` | When editing, do not count this row |
| `values = (...)` | The six values written once, not twice |
| `*values` | Unpacks the tuple into six arguments |
| `update_student(row_id, *values)` | Seven arguments: the `id` and the other six |

## 9.6 — The routes

In `do_GET`:

```diff app.py edit
     def do_GET(self):
         url = urllib.parse.urlparse(self.path)
 
         if url.path == "/":
             self.page_home()
         elif url.path == "/add":
             self.page_form()
+        elif url.path == "/edit":
+            query = urllib.parse.parse_qs(url.query)
+            self.page_form(query.get("id", [""])[0])
         elif url.path.startswith("/static/"):
             self.send_static(url.path[len("/static/"):])
         else:
             self.send_response(404)
             self.end_headers()
```

and in `do_POST`:

```diff app.py edit
     def do_POST(self):
         url = urllib.parse.urlparse(self.path)
 
         if url.path == "/add":
             self.save_student()
+        elif url.path == "/edit":
+            self.save_student(is_edit=True)
         else:
             self.send_response(404)
             self.end_headers()
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `url.query` | The part after the `?` — `id=2`, for example |
| `parse_qs(...)` | Turns it into `{"id": ["2"]}` |
| `.get("id", [""])[0]` | The first value, or empty if there is none |

> `/edit` now has two sides like `/add`: `GET` shows the form, `POST` saves
> it.

## 9.7 — An edit button in the table

Change `build_table_rows` like this — one more column:

```diff app.py edit
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
+              <td><a href="/edit?id={row_id}">Edit</a></td>
             </tr>
             """.format(
                 number=number,
+                row_id=student["id"],
                 student_id=esc(student["student_id"]),
                 full_name=esc(student["full_name"]),
                 department=esc(student["department"]),
                 created_at=esc(student["created_at"]),
             )
         )
     return "".join(rows)
```

And in `templates/list.html`, a new heading:

```html templates/list.html add
<p>{{ total }} student(s)</p>

<table>
  <thead>
    <tr>
      <th>#</th>
      <th>Student ID</th>
      <th>Full name</th>
      <th>Department</th>
      <th>Registered at</th>
      <th>Actions</th>
    </tr>
  </thead>
  <tbody>
    {{ rows }}
  </tbody>
</table>
```

> **Why no `esc()` on `row_id`?** Because it is a number the database
> assigned, not text a user typed. Anything that comes from a user gets
> `esc()`.

---

## 9.8 — Test it

Restart the server, `Ctrl + Shift + R`.

**1. Edit** — click **Edit** next to a student.

You should see the form **filled in with their details** — name, department,
gender, all of it. The heading says *Edit student* and the button says *Save
changes*.

**2. Change something** — change the name and save. It should be changed in
the list.

**3. The important test — leave the number alone:**
Edit the same student, change only the phone number, and save.

It should **work**. If you get *This student ID is already registered.*, your
`ignore_row_id` is not right (see 9.2).

**4. Take somebody else's number** — while editing, type another student's
number. It must be **refused**.

**5. Ask for an `id` that does not exist:**

```bash
http://localhost:8000/edit?id=9999
```

You should get a `404`.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| The form is empty when editing | Check `values is None` or `dict(student)` |
| I cannot save — it says the number exists | `ignore_row_id` is not right (9.2) |
| The change is not saved | `<input type="hidden" name="id">` is missing from the form |
| Every student changed! | You forgot `WHERE id = ?` in the `UPDATE` |
| I click `Edit` and get an empty form | The `id` is missing from the link, or `parse_qs` is wrong |
| `TypeError: ... takes 7 positional arguments` | Check the order of the arguments to `update_student` |
| The gender is not selected | `{{ male_checked }}` is missing from the HTML |

---

## ✅ This step is finished when

- Clicking **Edit** opens a filled-in form
- Changes are saved
- A student can be edited without changing their number
- Another student's number is still refused
- An `id` that does not exist gives a `404`

**Three of four are done.** In the next step, **D** — deleting, which is the
shortest step but carries an important point about safety.

---

# Step 10 — **D** in CRUD: deleting

> The shortest step — and the one with the most important safety question in
> it.

## What we do

Add a delete button, with a confirmation.

## Why deleting is different

`Create` and `Update` can be corrected — you can type it again.
**Deleting does not come back.** So two things are needed:

1. **A `POST`, not an ordinary link**
2. **A confirmation**

---

## 10.1 — A function for `database.py`

```python database.py add
def delete_student(row_id):
    with get_connection() as connection:
        connection.execute("DELETE FROM students WHERE id = ?", (row_id,))
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `DELETE FROM students` | Removes a row |
| `WHERE id = ?` | **Only that row** |
| `?` | The same protection against SQL Injection |

> ⚠️ `DELETE FROM students;` without a `WHERE` removes **every student**.
> The same warning as Step 9.

## 10.2 — The button in the table

Change `build_table_rows` again — the `Actions` column now holds two things:

```diff app.py edit
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
-              <td><a href="/edit?id={row_id}">Edit</a></td>
+              <td class="actions">
+                <a href="/edit?id={row_id}">Edit</a>
+                <form method="POST" action="/delete" class="inline"
+                      onsubmit="return confirm('Delete this student?');">
+                  <input type="hidden" name="id" value="{row_id}">
+                  <button type="submit" class="danger">Delete</button>
+                </form>
+              </td>
             </tr>
             """.format(
                 number=number,
                 row_id=student["id"],
                 student_id=esc(student["student_id"]),
                 full_name=esc(student["full_name"]),
                 department=esc(student["department"]),
                 created_at=esc(student["created_at"]),
             )
         )
     return "".join(rows)
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `<form method="POST">` | A small form on every row |
| `<input type="hidden" name="id">` | Which student to delete |
| `onsubmit="return confirm(...)"` | The confirmation — on `Cancel`, nothing happens |
| `class="inline"` | Stops the form starting a new line |
| `class="danger"` | The button in red |

> ### ⚠️ Why a form and not a link?
>
> If we had written:
>
> ```html
> <a href="/delete?id=3">Delete</a>
> ```
>
> then **anything that opens links** would delete students:
>
> - browsers **prefetch** links to feel faster
> - Google and other crawlers follow links
> - any browser extension
>
> The rule: **a `GET` must never change anything.** It is covered in the
> theory lesson.
>
> A `POST` is only sent when a person clicks.

> ### 🤔 Is `confirm()` protection?
>
> **No.** It is JavaScript, on the client — removable with `F12`, like the
> `required` in Step 8.
>
> But its purpose is different: it guards against **human error**, not
> against an attacker. Somebody who deletes on purpose is allowed to.

## 10.3 — The delete route

In `do_POST`:

```diff app.py edit
     def do_POST(self):
         url = urllib.parse.urlparse(self.path)
 
         if url.path == "/add":
             self.save_student()
         elif url.path == "/edit":
             self.save_student(is_edit=True)
+        elif url.path == "/delete":
+            form = self.read_form()
+            database.delete_student(form.get("id"))
+            self.redirect("/")
         else:
             self.send_response(404)
             self.end_headers()
```

> It is only in `do_POST` — **not** in `do_GET`. That is the rule we just
> talked about.

## 10.4 — Styling

At the end of `static/style.css`:

```css static/style.css add
.actions {
  display: flex;
  align-items: center;
  gap: 10px;
}

.inline {
  display: inline;
  margin: 0;
}

.danger {
  padding: 4px 10px;
  background: #fef2f2;
  border: 1px solid #fecaca;
  color: #dc2626;
  font-size: 13px;
}

.danger:hover {
  background: #dc2626;
  color: #fff;
}
```

<!-- collapse -->
### What does this CSS do?

| Rule | What it does |
| ---- | ------------ |
| `.actions { display: flex }` | *Edit* and *Delete* side by side |
| `.inline { display: inline }` | The form behaves like text, not a block |
| `.danger` | Red, so the user knows it is dangerous |
| `:hover` | It darkens as the mouse comes over it |

> Colour here is **information, not decoration**. A red button says "careful".

---

## 10.5 — Test it

Restart the server, `Ctrl + Shift + R`.

**1. Click Delete** — a question appears.

**2. Press `Cancel`** — nothing happens. The student is still there.

**3. Do it again and press `OK`** — the student is removed and the list
reloads.

**4. Delete them all** — you should see *No student is registered yet.*
That is the `else` we wrote in Step 7.

**5. Test the rule:**

```bash
http://localhost:8000/delete?id=1
```

Open that in the browser. You should get a **`404`**, and **nothing is
deleted** — because it is a `GET`, not a `POST`.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| The question does not appear | Check `onsubmit="return confirm(...)"` |
| Nothing is deleted | `elif url.path == "/delete"` is missing from `do_POST` |
| Every student was deleted! | You forgot `WHERE id = ?` |
| The button starts a new line | `class="inline"` is missing from the form |
| I get a `404` when clicking | The form is not `method="POST"` |
| The page does not refresh after deleting | `self.redirect("/")` is missing |

---

## ✅ This step is finished when

- A red *Delete* button sits beside each student
- A confirmation appears before deleting
- `Cancel` does nothing
- Deleting **cannot** be done with a `GET`
- When the list empties, the message appears

**🎉 All four letters of CRUD are done.**

The project works now. In the next two steps we add something new (search),
and then come back to security — the two attacks from the theory lesson, this
time in your own code.

---

# Step 11 — Search

> CRUD is done. Now we add something every real system has.

## What we do

Add a search box that looks by name, number or department.

## Why search matters

With ten students the list is enough. With **five hundred** it is unusable
without search. It is the difference between a class exercise and a real
program.

---

## 11.1 — Change `get_all_students`

Delete the old function and put this in:

```diff database.py edit
-def get_all_students():
+def get_all_students(search=""):
     with get_connection() as connection:
+        if search:
+            pattern = "%" + search + "%"
+            return connection.execute(
+                """
+                SELECT * FROM students
+                WHERE full_name  LIKE ?
+                   OR student_id LIKE ?
+                   OR department LIKE ?
+                ORDER BY id DESC
+                """,
+                (pattern, pattern, pattern),
+            ).fetchall()
+
         return connection.execute(
             "SELECT * FROM students ORDER BY id DESC"
         ).fetchall()
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `search=""` | With nothing passed in, return everyone |
| `LIKE` | "contains", rather than "equals" |
| `%` | "anything here" — like `*` when searching for files |
| `"%" + search + "%"` | `Ahmad` becomes `%Ahmad%` |
| `OR` three times | Look in the name, the number and the department |
| `(pattern, pattern, pattern)` | Three `?`, so three values |

> ### How `LIKE` and `%` work
>
> | Example | What it matches |
> | ------- | --------------- |
> | `LIKE 'Ahmad'` | Only exactly `Ahmad` |
> | `LIKE 'Ahmad%'` | Anything **starting with** `Ahmad` |
> | `LIKE '%Ahmad'` | Anything **ending with** `Ahmad` |
> | `LIKE '%Ahmad%'` | Anything **containing** `Ahmad`, anywhere |
>
> We want the third one, so we put a `%` on both sides.

> ### ⚠️ We are still using `?`
>
> This is **text the user typed** — the most dangerous place for SQL
> Injection there is.
>
> Look at where the `%` are added: in **Python**, and then the whole string
> is sent as a `?`. That way SQLite knows it is a value, not a command.
>
> Had we written `"... LIKE '%" + search + "%'"`, somebody could drop the
> table by typing the right thing into the search box.

## 11.2 — Change `templates/home.html`

Add the search form between the link and the table:

```diff templates/home.html edit
 <p><a href="/add">+ Register a new student</a></p>
 
+<form class="search" method="GET" action="/">
+  <input type="text" name="q" value="{{ search }}"
+         placeholder="Search by name, student ID or department...">
+  <button type="submit">Search</button>
+  <a href="/">Reset</a>
+</form>
+
 {{ table }}
```

<!-- collapse -->
### What does this HTML do?

| Part | What it does |
| ---- | ------------ |
| `method="GET"` | **Search is a `GET`** — it changes nothing |
| `action="/"` | Back to the same home page |
| `name="q"` | The name of the parameter — `q` for *query* |
| `value="{{ search }}"` | After searching, the text stays in the box |
| `placeholder` | Faint guidance while the box is empty |
| `<a href="/">Reset</a>` | Back to the whole list |

> **Why `GET` and not `POST`?** Because search **changes nothing**. The
> benefit: the search text goes into the link:
>
> ```
> http://localhost:8000/?q=Ahmad
> ```
>
> So you can **send that link to somebody**, or bookmark it. It is the same
> rule as Step 10, seen from the other side.

## 11.3 — Change `page_home`

Change `page_home` again, like this:

```diff app.py edit
-    def page_home(self):
-        students = database.get_all_students()
+    def page_home(self, search=""):
+        students = database.get_all_students(search)
 
         if students:
             table = render("list.html",
                            rows=build_table_rows(students),
                            total=len(students))
+        elif search:
+            table = "<p>No student matches &quot;" + esc(search) + "&quot;.</p>"
         else:
             table = "<p>No student is registered yet.</p>"
 
-        body = render("home.html", table=table)
-        page = render("layout.html", title="Students", content=body)
-
-        self.send_response(200)
-        self.send_header("Content-Type", "text/html; charset=utf-8")
-        self.end_headers()
-        self.wfile.write(page.encode("utf-8"))
+        body = render("home.html", search=esc(search), table=table)
+        self.send_html(render("layout.html", title="Students", content=body))
```

<!-- collapse -->
### What does this code do?

| Part | What it does |
| ---- | ------------ |
| `search=""` | With nothing passed in, everyone |
| `if students` | There are results → the table |
| `elif search` | A search was made, and found nothing |
| `else` | The database is empty |
| `esc(search)` | Text from the user — it **must** be escaped |

> **Three different states, three different messages.** This is the detail
> that separates a good program from a poor one:
>
> - "No student is registered yet" → **register one**
> - "No student matches *Ahmad*" → **change the text**
>
> If both said the same thing, the user would not know what to do.

## 11.4 — Change the route

In `do_GET`:

```diff app.py edit
         if url.path == "/":
-            self.page_home()
+            query = urllib.parse.parse_qs(url.query)
+            self.page_home(query.get("q", [""])[0])
```

> The same shape as `/edit?id=...` in Step 9 — with `q` this time.

## 11.5 — Styling

```css static/style.css add
.search {
  display: flex;
  gap: 8px;
  align-items: center;
  margin-bottom: 16px;
}

.search input {
  flex: 1;
  max-width: 380px;
  padding: 9px 12px;
  border: 1px solid var(--border);
  border-radius: 8px;
  font-size: 14px;
  font-family: inherit;
}
```

<!-- collapse -->
### What does this CSS do?

| Rule | What it does |
| ---- | ------------ |
| `display: flex` | The box and the button side by side |
| `flex: 1` | The search box fills the space |
| `max-width: 380px` | But never gets too long |

---

## 11.6 — Test it

Restart the server. Add a few students through the form first, then:

**1. Search by name** — type part of a name, `Ah` for example.
Only those should appear.

**2. Look at the link:**

```out
http://localhost:8000/?q=Ah
```

The search text is in it.

**3. Search by department** — type `Account`. The accounting students appear.

**4. Search for something that is not there** — type `zzz`.
The message *No student matches "zzz".*

**5. Press `Reset`** — back to the whole list.

**6. A security test** — type this into the search box:

```
' OR '1'='1
```

**Nothing** should be found — because it went through a `?`, so SQLite looks
for a student whose name is that text.

> Without the `?`, that text would have returned every row — because
> `'1'='1'` is always true. That is **SQL Injection**.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| Searching changes nothing | Check `page_home(query.get("q", [""])[0])` |
| The text does not stay in the box | `value="{{ search }}"` is missing, or `search=esc(search)` |
| It always returns everyone | `if search:` is missing from `get_all_students` |
| `Incorrect number of bindings` | Three `?` but not three values passed |
| The wrong message appears | Check the order of `if / elif / else` |
| The button changes the page | Check `action="/"` |

---

## ✅ This step is finished when

- Search works by name, number and department
- The search text is in the link and can be shared
- A search with no results gets its own message
- `Reset` brings back everyone

**The project is complete.** In the next step we add no features at all —
instead we **try to break what we built**.

---

# Step 12 — Security: break your own project

> In this step we add **no new features**. We take the defences out, watch
> what happens, and put them back.

## What we do

Break the project deliberately, so we can see what those two lines
**actually** do.

## Why this way?

We have said "use `?`" and "use `esc()`". A student does as they are told —
but does **not believe it** until they have seen the damage with their own
eyes.

> ⚠️ **Do this on your own project.** This is learning, not attacking. Never
> try any of it against somebody else's system.

---

## 12.1 — First attack: SQL Injection

### Take the defence out

In `database.py`, find `get_all_students`. Change **the search part** to this
**dangerous** version:

```diff database.py edit
         if search:
-            pattern = "%" + search + "%"
-            return connection.execute(
-                """
-                SELECT * FROM students
-                WHERE full_name  LIKE ?
-                   OR student_id LIKE ?
-                   OR department LIKE ?
-                ORDER BY id DESC
-                """,
-                (pattern, pattern, pattern),
-            ).fetchall()
+            # ❌ dangerous — for this test only
+            sql = ("SELECT * FROM students WHERE full_name LIKE '%"
+                   + search + "%' ORDER BY id DESC")
+            return connection.execute(sql).fetchall()
```

Restart the server.

### Now attack it

Type this into the search box:

```
' OR '1'='1
```

### What you should see

**Every student appears** — although none of them has that name.

<!-- collapse -->
### Why? Because the statement becomes this

```sql
SELECT * FROM students WHERE full_name LIKE '%' OR '1'='1%' ORDER BY id DESC
```

`'1'='1'` is **always true**, so the `OR` makes every row come back.

The user did not type data — they typed **part of the statement**.

> In a real system this is used to:
>
> - read every user's details
> - log in without a password
> - drop tables
>
> It is one of the oldest and most common attacks on the web.

### Put the defence back

Delete the dangerous code and restore the version from Step 11:

```diff database.py edit
         if search:
-            # ❌ dangerous — for this test only
-            sql = ("SELECT * FROM students WHERE full_name LIKE '%"
-                   + search + "%' ORDER BY id DESC")
-            return connection.execute(sql).fetchall()
+            pattern = "%" + search + "%"
+            return connection.execute(
+                """
+                SELECT * FROM students
+                WHERE full_name  LIKE ?
+                   OR student_id LIKE ?
+                   OR department LIKE ?
+                ORDER BY id DESC
+                """,
+                (pattern, pattern, pattern),
+            ).fetchall()
```

Restart the server and search for the same text again.

**Now nothing is found** — because SQLite is looking for a student whose name
is `' OR '1'='1`. Nobody is called that.

> **The difference:** with `?`, the text **never enters the statement**.
> SQLite parses the statement first, and puts the value in afterwards.

---

## 12.2 — Second attack: XSS

### Take the defence out

In `app.py`, find `esc` and change it to this:

```diff app.py edit
 def esc(value):
-    return html.escape("" if value is None else str(value))
+    # ❌ dangerous — for this test only
+    return "" if value is None else str(value)
```

Restart the server.

### Now attack it

Register a new student, and in the **Full name** field type:

```
<script>alert('XSS')</script>
```

### What you should see

When you come back to the list, **an alert box appears**.

That code now lives in the database. **Anybody** who opens that page runs it
too.

<!-- collapse -->
### Why is this dangerous?

`alert()` is harmless. But the same place could hold:

| What the code does | The result |
| ------------------ | ---------- |
| Sends `document.cookie` away | The user's session is stolen |
| Draws a fake login form | Passwords are stolen |
| Records the clicks | Surveillance |
| Sends requests as the user | Data changed without them knowing |

> **The key point:** the attacker types it **once**. After that it runs for
> **everyone** who opens the page — the teacher, the administrator, all of
> them.
>
> That is why it is called **stored XSS** — it is saved in the database.

### Put the defence back

```python app.py add
def esc(value):
    return html.escape("" if value is None else str(value))
```

Restart the server.

**Now the name appears as text:**

```out
<script>alert('XSS')</script>
```

<!-- collapse -->
### What does `html.escape` do?

| Character | Becomes |
| --------- | ------- |
| `<` | `&lt;` |
| `>` | `&gt;` |
| `&` | `&amp;` |
| `"` | `&quot;` |

The browser shows `&lt;` as **the character `<`**, but does not read it as
**the start of a tag**. So the code never runs.

> **The rule:** escape when **showing**, not when **saving**.
>
> Why? Because the same data may later go somewhere else — into a CSV, or an
> email — with different rules. Keep the data **clean**, and make it safe on
> the way out.

Then delete that student with the *Delete* button.

---

## 12.3 — Third attack: path traversal

This one has been **protected since Step 6**. Let us test it.

Open this in the browser:

```
http://localhost:8000/static/../database.py
```

**You should get a `404`.**

<!-- collapse -->
### Why does it not work?

In `send_static` we wrote this line:

```python read
safe_name = os.path.basename(filename)
```

`basename` keeps only **the file name**:

| Asked for | After `basename` | Result |
| --------- | ---------------- | ------ |
| `style.css` | `style.css` | ✅ sent |
| `../database.py` | `database.py` | not in `static` → `404` |
| `../../../etc/passwd` | `passwd` | not in `static` → `404` |

> Without that line anybody could read your server's code — which in a real
> project might hold passwords and keys.

---

## 12.4 — The list of defences

You now know where every defence is and what it does:

| Attack | Defence | Where it lives |
| ------ | ------- | -------------- |
| SQL Injection | `?` in place of values | Every `execute()` in `database.py` |
| XSS | `esc()` before showing | `build_table_rows`, `page_form`, `page_home` |
| Path traversal | `os.path.basename` | `send_static` in `app.py` |
| Duplicate registration | `UNIQUE` + `student_id_exists` | `database.py` |
| Deleting by accident | `POST` + `confirm()` | `build_table_rows` |
| `F5` registering twice | `redirect` (PRG) | `save_student` |

## 12.5 — What this project does **not** do

For honesty, know these too. A real system needs them; this one has none:

| Missing | Why it matters |
| ------- | -------------- |
| Login | Anybody can change everything |
| A CSRF token | Another page could submit your forms |
| HTTPS | The data travels unencrypted |
| Rate limiting | Somebody could register a thousand students |

> This is a **teaching project**, not a university system. Knowing the
> difference is the point.

---

## ✅ This step is finished when

- You have seen SQL Injection with your own eyes, and fixed it
- You have seen XSS with your own eyes, and fixed it
- You have tested path traversal
- **Both defences are back in place**

> ⚠️ **Make sure:** the `?` are in `database.py`, and `html.escape` is in
> `esc()`. If you forgot, your project is unsafe.

**One step left** — the final testing, and getting the project ready to hand
in.

---

# Step 13 — The final test

> The last step. We get the project ready for other people to use.

## What we do

Add a file that starts the project with a double-click, then test
**everything**.

---

## 13.1 — `run.bat`

Until now you have had to open a terminal and type a command every time. For
somebody who does not know Python, that is a barrier.

Create a new file called `run.bat`, beside `app.py`:

```bat run.bat
@echo off
cd /d "%~dp0"
start "" http://localhost:8000
python app.py
pause
```

<!-- collapse -->
### What does this file do?

| Line | What it does |
| ---- | ------------ |
| `@echo off` | Do not print the commands themselves, only their output |
| `cd /d "%~dp0"` | Go to the folder this file is in |
| `%~dp0` | "the path of this file" — so it works from anywhere |
| `start "" http://...` | Open the browser |
| `python app.py` | Start the server |
| `pause` | Keep the window open if something goes wrong |

> **Why does `cd /d "%~dp0"` matter?** Without it, if somebody opens the file
> from elsewhere, `python app.py` cannot find the file. The same problem as
> Step 3.
>
> **Why `pause`?** If there is an error, the window would close instantly and
> you would see nothing. `pause` waits for a key.

**Test it:** stop the server, then double-click `run.bat` in File Explorer.

The browser should open and the project should work.

---

## 13.2 — The complete test

Now test everything. **All of these must work:**

| # | Test | What should happen |
| - | ---- | ------------------ |
| 1 | Double-click `run.bat` | The browser opens and the list appears |
| 2 | An empty database | *No student is registered yet.* |
| 3 | Register a student | Back to the list, the student at the top |
| 4 | Submit an empty form | Four error messages |
| 5 | A bad email | *The email address is not valid.* |
| 6 | A duplicate number | *This student ID is already registered.* |
| 7 | After an error | What you typed is still there |
| 8 | `F5` after registering | Nothing is registered twice |
| 9 | Click *Edit* | A prefilled form |
| 10 | Change only the phone | It saves (their own number does not block them) |
| 11 | Another student's number | Refused |
| 12 | Click *Delete* → Cancel | Nothing happens |
| 13 | Click *Delete* → OK | Removed |
| 14 | Search by name | Only those appear |
| 15 | Search by department | Works |
| 16 | A search with no results | *No student matches "..."* |
| 17 | *Reset* | Everyone comes back |
| 18 | `/nothing` | `404` |
| 19 | `/edit?id=9999` | `404` |
| 20 | `/delete?id=1` in the browser | `404`, nothing deleted |
| 21 | A student named `<script>alert(1)</script>` | Shown as text |
| 22 | Searching for `' OR '1'='1` | Finds nothing |

> **If any one of them fails**, go back to the step it belongs to. The error
> table at the end of each step will help.

---

## 13.3 — Starting from a clean slate

Before handing the project in, it is worth testing it with a fresh database:

**1.** Stop the server (`Ctrl + C`)
**2.** Delete `students.db`
**3.** Open `run.bat` again

A new database should be built and *No student is registered yet.* should
appear.

> This proves the project also works on somebody else's computer — where
> there is no `students.db`.

---

## 13.4 — The finished structure

```out
student-system/
├── app.py              the server, the routes, validation
├── database.py         the table and the CRUD operations
├── run.bat             double-click to start
├── students.db         the database (automatic)
├── templates/
│   ├── layout.html     the shared frame
│   ├── home.html       search + table
│   ├── list.html       the students table
│   └── form.html       adding and editing
└── static/
    └── style.css       all the design
```

**Seven files.** The whole project.

<!-- collapse -->
### How many lines is each file?

| File | About |
| ---- | ----- |
| `app.py` | 150 lines |
| `database.py` | 90 lines |
| `style.css` | 120 lines |
| `templates/` | 100 lines together |

> Around **460 lines**. A complete CRUD system, with no external libraries.
>
> For comparison: the same thing in Django or Laravel takes less code — but
> much of the work is hidden inside the framework. You wrote **every line**
> and you know what it does.

---

## 13.5 — What you learned

| Subject | Where |
| ------- | ----- |
| HTML: forms, tables, tags | Steps 5, 7, 8 |
| CSS: colour, Flexbox, layout | Steps 6, 8 |
| SQL: `CREATE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`, `LIKE` | Steps 4, 7–11 |
| Python: functions, classes, lists, dictionaries | All of them |
| HTTP: `GET`, `POST`, `303`, `404` | Steps 6, 8, 10 |
| Security: SQL Injection, XSS, path traversal | Step 12 |
| Separation of concerns (MVC) | Steps 4, 5 |

---

## 13.6 — For those who want to go further

In order of difficulty:

1. **A new column** — add `stage` (year of study). Remember to delete
   `students.db`.
2. **Sort by name** — `ORDER BY full_name` instead of `id DESC`.
3. **Count male and female** —
   `SELECT gender, COUNT(*) FROM students GROUP BY gender`
4. **A page for one student** — `/student?id=2` showing all their details.
5. **Filter by department** — a dropdown beside the search box.
6. **Export to CSV** — `/export` that sends a CSV file.

> Every one of them builds on what you already know. None needs anything new.

---

## 🎉 Well done

You have built a complete information system — from an empty folder to a
working program.

**What matters is not that the project works.** It is that you know **why**
every line is in it.

---

## If you get an error

| Problem | Fix |
| ------- | --- |
| `run.bat` closes instantly | The `pause` at the end is missing |
| `python` is not found by `run.bat` | Step 1.3 — PATH |
| The browser opens too early and shows nothing | Wait a second and press `F5` |
| An error after deleting `students.db` | Make sure `database.init_db()` is in `app.py` |

---

**The guide ends here.** If you forget something, each step reads on its own
— use the contents list beside the page.