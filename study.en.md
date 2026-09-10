# Questions and Answers — Prepared by M. Idris Qadir

> **This sheet is for revision.** The quiz questions come from it — know
> these and the quiz is straightforward.

> ⚠️ **The quiz comes in English only.** The sheet is in both languages so
> that you can follow it — but read the English side too, not only the
> Kurdish.

> The midterm and the final ask more besides, which are not here. The last
> page explains what kind those are and how to prepare for them.

---

## Step 1 — Preparing the computer

**1.** Which program runs Python code?

> **Answer:** Python
> 
> VS Code is only an editor — it writes code, it does not run it.

**2.** Which menu opens a terminal in VS Code?

> **Answer:** Terminal → New Terminal
> 
> Or the shortcut Ctrl + `

**3.** Which command shows whether Python is installed?

> **Answer:** python --version

**4.** `python --version` says *not recognized*. What does it mean?

> **Answer:** Python is either missing or not on PATH
> 
> *Add Python to PATH* must be ticked during installation.

**5.** What is the shortcut for opening a terminal in VS Code?

> **Answer:** Ctrl + `
> 
> The key below Esc.

**6.** Which box matters most when installing Python?

> **Answer:** Add Python to PATH
> 
> Without it the terminal cannot find `python`.

**7.** How do you know which folder the terminal is in?

> **Answer:** The path written before the `>`

---

## Step 2 — The project folder

**1.** What is the `templates` folder for?

> **Answer:** The HTML files
> 
> HTML in templates, CSS in static.

**2.** What is the `static` folder for?

> **Answer:** CSS and images
> 
> Things that do not change — hence static.

**3.** What is the project folder called?

> **Answer:** student-system

**4.** Why no spaces in the folder name?

> **Answer:** It causes trouble in the terminal
> 
> The terminal reads a space as the boundary between two things.

**5.** Where do we create the project?

> **Answer:** Documents
> 
> `Documents\student-system`

**6.** Which menu opens the project folder in VS Code?

> **Answer:** File → Open Folder
> 
> The folder is opened, not a single file.

**7.** What are the two folders inside the project called?

> **Answer:** templates and static

---

## Step 3 — The first server

**1.** Which command starts the server?

> **Answer:** python app.py

**2.** Which port does the server run on?

> **Answer:** 8000
> 
> HTTPServer(("localhost", 8000), …)

**3.** After `python app.py` the terminal stops responding. What does that mean?

> **Answer:** The server is running and waiting for requests
> 
> A server never finishes — not until you stop it.

**4.** How do you stop the server?

> **Answer:** Ctrl + C

**5.** You changed `app.py` and saved it. What must you do for the change to show?

> **Answer:** Stop the server and start it again
> 
> Python code is read once, when the server starts.

**6.** What is `BaseHTTPRequestHandler`?

> **Answer:** A class that handles the requests
> 
> It comes with Python, from `http.server`.

**7.** What does `self.send_response(200)` do?

> **Answer:** Tells the browser the request succeeded
> 
> `200` means OK. The content follows after it.

**8.** Why do we use `.encode("utf-8")`?

> **Answer:** Because a server sends bytes, not text

---

## Step 4 — The database

**1.** Which file holds the database?

> **Answer:** students.db
> 
> `database.py` is the code; `students.db` is the data.

**2.** What does `UNIQUE` on `student_id` do?

> **Answer:** Stops the same number being stored twice
> 
> A repeat gives `UNIQUE constraint failed`.

**3.** Why is the phone number `TEXT` and not `INTEGER`?

> **Answer:** A leading zero would be lost
> 
> `0770` becomes `770`. A number you never add up is text.

**4.** Who fills in `created_at`?

> **Answer:** The database itself
> 
> `DEFAULT (datetime('now', 'localtime'))`

**5.** You changed a column and nothing happened. Why?

> **Answer:** `CREATE TABLE IF NOT EXISTS` leaves an existing table alone
> 
> The fix: delete `students.db` and run it again.

**6.** What does `AUTOINCREMENT` do?

> **Answer:** Gives every new row the next number
> 
> It never reuses a number that has been deleted.

**7.** What does `sqlite3.connect(DB_PATH)` do if the file is missing?

> **Answer:** **Creates it**
> 
> That is why `students.db` appears on its own.

**8.** Which function creates the table?

> **Answer:** init_db()

---

## Step 5 — Templates

**1.** What is `{{ title }}` in a template?

> **Answer:** A blank that Python fills in
> 
> `render()` looks for `{{ }}` and replaces it.

**2.** What does `layout.html` hold?

> **Answer:** The frame every page shares — `<html>`, `<head>`, `<body>`
> 
> So it is not rewritten on every page.

**3.** You changed an HTML file inside `templates`. What do you do?

> **Answer:** Just F5 in the browser
> 
> A template is read fresh on every request.

**4.** You wrote `{{ total }}` but sent no value for it. What appears?

> **Answer:** Nothing — the space is left empty
> 
> `values.get(name, "")` — not found, empty string.

**5.** What goes into `{{ content }}` in `layout.html`?

> **Answer:** The content of whichever page is being shown
> 
> That is what lets one layout serve every page.

**6.** How many values does `render("home.html", total=0)` pass?

> **Answer:** One, called `total`
> 
> `**values` allows any number of them.

**7.** Why do we call `render()` twice?

> **Answer:** Once for the content, once to put it inside the layout

---

## Step 6 — CSS and the router

**1.** In `do_GET`, what does `if url.path == "/"` do?

> **Answer:** Shows the home page
> 
> `/` is the root of the site.

**2.** Without the router, why does the CSS not work?

> **Answer:** The server sends the same page for every request
> 
> It asks for `style.css` and gets HTML back.

**3.** What does `os.path.basename()` do?

> **Answer:** Strips every `../` and keeps only the file name
> 
> It guards against Path Traversal.

**4.** Without `basename`, what could someone do?

> **Answer:** Read a file outside `static`, such as `database.py`
> 
> `/static/../database.py`

**5.** You ask for a page that does not exist. What does the server return?

> **Answer:** 404
> 
> `else: self.send_response(404)`

**6.** What does `urllib.parse.urlparse(self.path)` do?

> **Answer:** Splits the link into parts: path, query, …
> 
> We then use `url.path` and `url.query`.

**7.** Why is the CSS read with `"rb"`?

> **Answer:** Because it is sent as bytes, not text
> 
> The same code then works for an image, which is bytes.

**8.** What is the `Content-Type` for a CSS file?

> **Answer:** text/css

---

## Step 7 — R — showing the list

**1.** What does `SELECT * FROM students` do?

> **Answer:** Reads every row
> 
> `*` means every column.

**2.** What does `ORDER BY id DESC` do?

> **Answer:** Newest at the top
> 
> `DESC` counts down.

**3.** What does `esc()` do?

> **Answer:** Turns `<` into `&lt;`, so it shows as text, not code
> 
> It guards against XSS.

**4.** Without `esc()`, what does a name like `<script>alert(1)</script>` do?

> **Answer:** Runs as code — a pop-up appears
> 
> That is XSS.

**5.** If no student is registered, what should be shown?

> **Answer:** A clear message such as *No student is registered yet*
> 
> This is called an empty state.

**6.** What does `.fetchall()` return?

> **Answer:** Every row
> 
> For one row, `.fetchone()`.

**7.** Why `start=1` in `enumerate(students, start=1)`?

> **Answer:** Because a reader counts from 1
> 
> Without it the first row would be numbered zero.

**8.** What does `"".join(rows)` do?

> **Answer:** Joins every row into one piece of text

---

## Step 8 — C — the form

**1.** Which method does the form use to send data?

> **Answer:** POST
> 
> `<form method="POST" …>`

**2.** What is the difference between `GET /add` and `POST /add`?

> **Answer:** `GET` shows the form, `POST` saves it
> 
> One path, two actions.

**3.** Why redirect after a successful save?

> **Answer:** So that `F5` does not save the data twice
> 
> This is PRG: Post, Redirect, Get.

**4.** Is `required` in HTML enough as validation?

> **Answer:** No — `F12` removes it, so we check on the server too
> 
> Nothing on the client side can be trusted.

**5.** The database already has `UNIQUE`. So why `student_id_exists()`?

> **Answer:** To show a clear message instead of a crash
> 
> The database refuses; we explain why.

**6.** What does `self.rfile.read(length)` read?

> **Answer:** The data the form sent
> 
> The length comes from `Content-Length`.

**7.** What does `parse_qs("a=1&b=2")` return?

> **Answer:** `{"a": ["1"], "b": ["2"]}`
> 
> Each value is in a list, which is why we take `value[0]`.

**8.** What does `.strip()` do in `read_form`?

> **Answer:** Removes the spaces at the start and the end

---

## Step 9 — U — editing

**1.** Which SQL command changes an existing row?

> **Answer:** UPDATE
> 
> `UPDATE students SET … WHERE id = ?`

**2.** You forgot `WHERE id = ?` in an `UPDATE`. What happens?

> **Answer:** **Every** row changes
> 
> A dangerous mistake — and it gives no warning.

**3.** What is `<input type="hidden" name="id">` for?

> **Answer:** So the server knows which student is being changed
> 
> Without it the server does not know which row to change.

**4.** You open `/edit?id=9999` but no such student exists. What do you see?

> **Answer:** 404
> 
> `if row_id and student is None: 404`

**5.** What does `get_student(row_id)` return when there is no such row?

> **Answer:** `None`
> 
> That is why we test `if student is None`.

**6.** What is `ignore_row_id` for in `student_id_exists`?

> **Answer:** So a student can keep their own number when editing
> 
> Without it, editing without changing the number would be refused.

**7.** Which form field carries the row's number?

> **Answer:** `<input type="hidden" name="id">`

---

## Step 10 — D — deleting

**1.** Which SQL command deletes a row?

> **Answer:** DELETE
> 
> `DELETE FROM students WHERE id = ?`

**2.** Why is deleting a `POST` and not an ordinary link?

> **Answer:** A link can be opened by accident and destroy something
> 
> A `GET` must never change anything.

**3.** You open `/delete?id=1` in the browser. What happens?

> **Answer:** 404 — and nothing is deleted
> 
> Because it is a `GET`, and `do_GET` has no `/delete` route.

**4.** Why use `confirm()` before deleting?

> **Answer:** So the user does not delete by accident
> 
> A deletion cannot be undone.

**5.** Where does `confirm()` run?

> **Answer:** In the browser
> 
> So it is not a defence — only a guard against a slip.

**6.** What does the server do after deleting?

> **Answer:** Redirects to the list
> 
> The same PRG as in Step 8.

**7.** Which function in `database.py` deletes a row?

> **Answer:** delete_student(row_id)

---

## Step 11 — Search

**1.** What does `LIKE` do in SQL?

> **Answer:** Matches part of the text
> 
> `LIKE '%ahmad%'` finds anything containing *ahmad*.

**2.** In `LIKE '%ali%'`, what does `%` mean?

> **Answer:** Any number of characters — possibly none
> 
> So *Ali* is found at the start, middle or end.

**3.** In `/?q=ahmad`, what is `q`?

> **Answer:** The search parameter in the link
> 
> `urllib.parse.parse_qs(url.query)` reads it.

**4.** Why is the search form a `GET` and not a `POST`?

> **Answer:** It changes nothing, and the link can be shared
> 
> Searching only reads — so `GET`.

**5.** What is `url.query` for `/?q=ahmad`?

> **Answer:** `q=ahmad`
> 
> Without the `?`. `parse_qs` then turns it into a dictionary.

**6.** What does the `Reset` button do?

> **Answer:** Goes back to `/` with no search
> 
> It is a plain link to `/`.

**7.** Why is `value="{{ search }}"` on the search box?

> **Answer:** So the word stays in the box after searching

---

## Step 12 — Security

**1.** What is SQL Injection?

> **Answer:** Someone types SQL into an input box
> 
> The guard: always use `?`.

**2.** What prevents SQL Injection?

> **Answer:** Using `?` instead of joining text
> 
> SQLite knows it is a value, not a command.

**3.** What is XSS?

> **Answer:** Code typed into a box runs inside the page
> 
> The guard: `esc()`.

**4.** What prevents XSS?

> **Answer:** `esc()` / `html.escape()`
> 
> `<` becomes `&lt;` — the browser reads it as text.

**5.** What does "defence in depth" mean?

> **Answer:** Several guards at once — one is never enough
> 
> `UNIQUE` in the database, and a check in `app.py`.

**6.** How many characters does `html.escape()` change?

> **Answer:** `<`, `>`, `&`, `"` and `'`
> 
> All the ones that mean something special in HTML.

**7.** Why is it called "Stored XSS"?

> **Answer:** Because the code is stored in the database
> 
> The attacker types it once; it runs for every viewer.

**8.** Which two defences do we remove and restore in Step 12?

> **Answer:** The `?` in the SQL, and `esc()` when displaying

---

## Step 13 — Finishing and run.bat

**1.** What does `run.bat` do?

> **Answer:** Starts the server with a double-click
> 
> Without opening a terminal.

**2.** What does status `200` mean?

> **Answer:** OK — here is your page
> 
> Success.

**3.** What does status `303` mean?

> **Answer:** Go to another path
> 
> Used after a `POST` — PRG.

**4.** What does status `404` mean?

> **Answer:** Not found
> 
> This page does not exist.

**5.** You are sending the project to a friend. Which file is **not** needed?

> **Answer:** students.db
> 
> `students.db` builds itself the first time it runs.

**6.** What does `@echo off` do in `run.bat`?

> **Answer:** Hides the commands from view
> 
> Only the output is shown.

**7.** Why is `pause` at the end of `run.bat`?

> **Answer:** So the window does not shut before you read it
> 
> Without it, an error flashes past unread.

**8.** Which three files and two folders make up the project?

> **Answer:** app.py, database.py, run.bat — and templates and static

---

# The midterm and the final — what to expect

None of this is a secret. Knowing what is coming is how you prepare for it.

|  | Quiz | Midterm | Final |
|---|---|---|---|
| Time | 15 minutes | 60 minutes | 60 minutes |
| Questions | 12 | 22 | 26 |
| Marks | ~15 | ~30 | ~36 |
| Which steps | whatever has been taught | 1 – 8 | all of them |
| From this sheet | **most of it** | about half | about 40% |
| Harder questions | a few | **most of it** | **most of it** |
| Written answers | 2 – 3 | 7 – 9 | 10 – 12 |

> **Memorise this sheet alone** and you will do well in the quiz.
>
> It is not enough for the midterm or the final. Those questions **put code
> in front of you** and ask you to read it — and that only comes from
> having written the project yourself.

---

# The harder questions — how to prepare

> **These questions are not on this sheet.** They appear in the midterm
> and the final, and memorising will not help — the code will be different.

> But there are four kinds, and knowing the kind tells you how to think.
> Each carries **two worked examples** with a full answer.

> ⚠️ **These examples themselves will not come back.**
>
> The same **kind** of question will, but **the code will be different**.
> Memorising these answers buys you nothing — what pays is understanding
> **how** each answer was reached.
>
> Learn to look for an `elif` that can never run and the habit works on any
> code. Memorise this one answer and it works on nothing else.

## 1. What does this code do?

You read a piece of code and say, in your own words, what happens.

**How to answer:**

- Read it line by line — do not skim.
- Ask: **when** does this line run? Once, or on every request?
- Ask: where does the result go?
- Start your answer with one sentence, then explain it.

**Example 1**

```
with get_connection() as connection:
    connection.execute(
        "INSERT INTO students (student_id) VALUES (?)",
        (student_id,),
    )
```

> **Answer:** It opens a connection, adds one row, and when the block ends it **commits the change and closes the connection by itself**. The number travels through a `?`, not joined onto the statement.

**Example 2**

```
def render(template_name, **values):
    path = os.path.join(TEMPLATE_DIR, template_name)
    with open(path, encoding="utf-8") as file:
        page = file.read()
    ...
```

> **Answer:** It reads the template file afresh **on every call**. That is why an HTML change shows without restarting the server — and why a Python change does not, since Python is read once.

## 2. What is the fault?

You are shown code that **fails, or works wrongly**. Find the fault and say why it is one.

**How to answer:**

- Check these four: a duplicate? a line that is never reached? a missing `WHERE`? a missing `?`?
- Ask: does Python **warn** about it? If not, it is worse.
- Do not just say "it is wrong" — say **what happens** because of it.

**Example 1**

```
def do_GET(self):
    if url.path == "/":
        self.page_home()
    if url.path.startswith("/static/"):
        self.send_static(...)
    else:
        self.send_response(404)
```

> **Answer:** The second `if` should be an `elif`. As written, a request for `/` sends the page, and then the `else` sends a `404` as well — **two answers to one request**.

**Example 2**

```
sql = "SELECT * FROM students WHERE full_name = " + name
connection.execute(sql)
```

> **Answer:** There is no `?` — the name goes straight into the statement. That is **SQL Injection**: someone can type SQL into the name field. It should be `execute("... = ?", (name,))`

## 3. Give two causes

You are given a symptom and asked for **more than one** possible cause.

**How to answer:**

- One cause is not enough — the marks are split between them.
- Look in two different places: the code, and what surrounds it (the server, the file, the browser).
- Think of the mistakes **you** made during the practical.

**Example 1**

> A student changed `style.css` and pressed `F5`.
> The design did not change.

> **Answer:** **1.** The browser is holding an old copy of the CSS — it needs `Ctrl + Shift + R`, not `F5`.
**2.** The `/static/` route is missing from `do_GET`, so the server never sends the file at all.

**Example 2**

> A student registers someone new.
> The page returns to the list, but the name is not there.

> **Answer:** **1.** `save_student` only redirects and never calls `database.add_student()`.
**2.** The row was stored, but `page_home` still does not call `get_all_students()`, so the list is stale.

## 4. Why is it written this way?

You are asked to justify a decision in the code — not what it does, but **why it was done that way**.

**How to answer:**

- Never write "because that is how it is written" — that is not an answer.
- Ask: **what happens without it?** That is the answer.
- Where you can, give an example from your own project.

**Example 1**

> Why does `students.db` live in the project folder rather than wherever the terminal happens to be?

> **Answer:** Because of `os.path.dirname(os.path.abspath(__file__))`. Without it, running `python app.py` from another folder makes **a second, empty database**, and it looks as though every student has vanished.

**Example 2**

> Why is the `id` field on the edit form `hidden` rather than shown?

> **Answer:** The server needs it to know which row to change, but it means nothing to the user — it is the database's own number. Showing it only confuses, and invites them to edit it.
