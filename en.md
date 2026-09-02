# From Zero to a Finished Project — Student Guide


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
| 2 | The project folder and its structure | ⏳ |
| 3 | The first server — "Hello" | ⏳ |
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

> Step 2 will be added here.