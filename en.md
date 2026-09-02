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
| 4 | The database (`database.py`) | ⏳ |
| 5 | Templates and the `render()` function | ⏳ |
| 6 | CSS — designing the pages | ⏳ |
| 7 | **R** — showing the student list | ⏳ |
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

> Step 4 will be added here.