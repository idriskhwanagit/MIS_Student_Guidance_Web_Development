# Practical questions — getting ready for the mock and the midterm

> **The mock and the midterm have 4 practical questions, 2 marks each.** In
> each one you do one small thing on your laptop, see what happens, and choose
> the answer that matches it.

> ⚠️ **These examples will not come back as they are.** But every practical
> question comes in **one of these five ways only**, and is done exactly the
> same way. Only the details change.

> **Every task only looks:** you change no file and nothing is saved.

> 💻 **On a laptop only** — not on a phone.

> 🔒 **On the exam day the guide page is closed.** Read this page before, and
> do the five ways at home.

## What you need

- **A laptop and its charger.** If your battery runs down fast, bring a
  power strip and sit near a socket.
- **The programs:** VS Code, Python and Chrome on the laptop — the ones from
  step 1.
- **Your university account:** Chrome on the laptop must be signed in with
  your `@epu.edu.iq` address, because the form takes university accounts
  only. If Google shows another account, choose **Switch account**.
- **Your own internet** for the laptop — your phone's hotspot, say — with
  enough balance. The phone is for the internet only, not for answering.
- **The exam copy:** `student-system-exam-step9.zip`, downloaded beforehand
  from [this link](https://drive.google.com/file/d/1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ/view?usp=drive_link).

## Once at home, before the mock

**1.** Download the zip from [this link](https://drive.google.com/file/d/1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ/view?usp=drive_link): on the Drive page press
**Download**, at the top right; if Google asks, sign in with your university
account. Then right-click the zip → **Extract All** → **Extract**. Inside the
new folder is a folder called `student-system-exam` — that is the project.

**2.** In VS Code: **File → Open Folder** → choose `student-system-exam`.

**3.** Open **Terminal → New Terminal**. The terminal line must end with
`student-system-exam`.

**4.** Stop every other server: if your own project is running, press
`Ctrl + C` in its terminal, or close its VS Code window. With two servers no
error appears, but Chrome shows the old server's pages.

**5.** In the **first terminal**, start the server — and leave that terminal
alone from then on:

```bash
python app.py
```

```out
Server running at http://localhost:8000
Press Ctrl + C to stop.
```

**6.** Open a **second terminal** with the **+** at the top of the terminal
panel. You type the questions' commands here, because the first one is busy
with the server.

**7.** Open this address in Chrome:

```
http://localhost:8000
```

You should see **exactly two students**: **Sara Ali** and **Ahmad Karim**. If
you see other names, your own project's server is answering: do step 4 again.

**8.** Do the five ways below and their examples, one by one. This is your
practice for the mock and the midterm.

## On the exam day

> 🔒 The guide page is closed, so know these beforehand.

**1.** The laptop with its charger. Your internet on, and Chrome signed in with
your university account.

**2.** In VS Code open the `student-system-exam` folder, and stop every other
server.

**3.** In the first terminal type `python app.py`. Open the second terminal
with **+**, for the commands.

**4.** Open two tabs in Chrome: one at `http://localhost:8000`, which must show
Sara Ali and Ahmad Karim, and the other with the exam form.

**5.** Answer everything on the laptop. In the form the answers are in a
different order from the examples here, so choose them by what they say, not
by their letter.

**6.** The closing time is written at the top of the form: press **Submit**
before it.

## If something goes wrong

| What you see | What to do |
|---|---|
| In Chrome: "This site can’t be reached", or `ERR_CONNECTION_REFUSED` | The server is not running. Type `python app.py` in the first terminal. |
| At `localhost:8000`, names other than Sara Ali and Ahmad Karim | Your own project's server is answering. Stop it, with `Ctrl + C` or by closing its window, then `F5`. |
| In the terminal: `can't open file ... app.py`, or `No module named 'database'` | The terminal is not in the `student-system-exam` folder. Open the folder in VS Code and open a new terminal. |
| Anything else broken, or a file changed by mistake | Delete the folder and extract the zip again. Everything is back as it was. |

## The basics

- **Copying a command:** in the form, click the command three times quickly
  so all of it is selected, and press `Ctrl + C`. Then `Ctrl + V` in the
  second terminal, and `Enter`.
- **Reading an error:** if red text starting with `Traceback` appears, read
  only its **last line** — the reason is written there.
- **Opening an address:** type or paste it into Chrome's address bar, then
  `Enter`.
- **Inspect:** right-click exactly on the part of the page the question
  names — on a touchpad, tap with two fingers — then **Inspect**. **Styles**
  shows that part's CSS rules.
- **Reloading a page:** `F5`.

## The five ways

For each way: what you are asked, what you do, and two examples with their answers. The examples were run on the exam copy, so if you do them yourself you will see exactly the same.

### Way 1 — Asking the database

**What you are asked:** The question gives you a ready `python -c` command that reads something from the database, and asks what it prints. It is the same as sections 4.7, 7.2.1 and 8.1.1 of the guide.

**What you do:**

- Copy the command from the question.
- Paste it into the second terminal and press `Enter`.
- Read the line it prints, and choose the same among the answers.

**Example 1.** How many columns does the `students` table have? Run this command:

```bash
python -c "import database; print(len(database.get_connection().execute('PRAGMA table_info(students)').fetchall()))"
```

- Option A: `6`
- Option B: `7`
- Option C: `8`
- Option D: `9`

**What you see:**

```out
8
```

> **Answer:** Option C — `8`
> 
> The command prints `8`: the eight columns of section 4.4, from `id` to `created_at`.

**Example 2.** Which department is the student whose `id` is 2 in? Run this command:

```bash
python -c "import database; print(database.get_student(2)['department'])"
```

- Option A: `MIS`
- Option B: `Accounting`
- Option C: `Management Information Systems`
- Option D: `Statistics`

**What you see:**

```out
Accounting
```

> **Answer:** Option B — `Accounting`
> 
> The command prints `Accounting`. Row 2 of the table is Sara Ali, added in section 7.2 with the department `Accounting`.

### Way 2 — Reading the last line of an error

**What you are asked:** The question gives you a command with a mistake in it on purpose, and asks what the error says. It is what section 7.2 of the guide teaches: red text that starts with `Traceback`, and you read its last line.

**What you do:**

- Copy the command and run it in the second terminal.
- Red text appears. Read only its last line.
- Choose the answer that is that last line.

**Example 1.** Run this command. What does the last line of the error say?

```bash
python -c "import database; print(database.get_connection().execute('SELECT * FROM student').fetchall())"
```

- Option A: `sqlite3.OperationalError: no such table: student`
- Option B: `sqlite3.OperationalError: no such column: student`
- Option C: `sqlite3.IntegrityError: UNIQUE constraint failed: students.student_id`
- Option D: `[]`

**What you see:**

```out
sqlite3.OperationalError: no such table: student
```

> **Answer:** Option A — `sqlite3.OperationalError: no such table: student`
> 
> The table is called `students`, with an `s`. The command asks for `student`, so SQLite says there is no such table.

**Example 2.** Run this command. What does the last line of the error say?

```bash
python -c "import database; print(database.get_student(5)['full_name'])"
```

- Option A: `TypeError: 'NoneType' object is not subscriptable`
- Option B: `IndexError: list index out of range`
- Option C: `KeyError: 'full_name'`
- Option D: `None`

**What you see:**

```out
TypeError: 'NoneType' object is not subscriptable
```

> **Answer:** Option A — `TypeError: 'NoneType' object is not subscriptable`
> 
> No student has `id` 5, so `get_student(5)` returns `None`, and `None['full_name']` gives this error.

### Way 3 — Opening an address

**What you are asked:** The question gives you an address, and asks what the page shows. It is what sections 6.7 and 9.8 of the guide do.

**What you do:**

- Make sure the server is running.
- Put the address in Chrome's address bar and press `Enter`.
- Look at the page: its heading and its boxes. For a page that does not exist, Chrome shows its own error page, with `HTTP ERROR 404` on it.

**Example 1.** With the server running, open this address. What is written in the **Full name** box?

```
http://localhost:8000/edit?id=2
```

- Option A: Ahmad Karim
- Option B: Sara Ali
- Option C: Nothing — the box is empty
- Option D: HTTP ERROR 404

**What you see:**

The **Edit student** form opens, and the Full name box says **Sara Ali**.

> **Answer:** Option B — Sara Ali
> 
> `id=2` is student number 2, Sara Ali. Edit fills the form with her details — the same as section 9.8.

**Example 2.** Open this address, with no `?id=`. What is the page's heading?

```
http://localhost:8000/edit
```

- Option A: Edit student
- Option B: Register a new student
- Option C: HTTP ERROR 404
- Option D: Students

**What you see:**

An empty form headed **Register a new student**.

> **Answer:** Option B — Register a new student
> 
> With no `id` the code reads no student, so it shows the form for a new one. With `?id=9999` it would have been `HTTP ERROR 404`, as in section 9.8.

### Way 4 — The Inspect tool

**What you are asked:** The question names a part of the page and asks what its CSS says. It is what section 6.6.1 of the guide teaches.

**What you do:**

- Open the page in Chrome.
- Right-click exactly on the part the question names → **Inspect**.
- In **Styles**, find the rule the question is about and read its value.

**Example 1.** On the home page the table's column headings are in capitals, like `FULL NAME`. Right-click one of them → **Inspect**. In Styles, which CSS line makes the letters capitals?

- Option A: `font-weight: bold`
- Option B: `text-transform: uppercase`
- Option C: `font-size: 13px`
- Option D: `color: #6b7280`

**What you see:**

In the rule `thead th`: `text-transform: uppercase;`

> **Answer:** Option B — `text-transform: uppercase`
> 
> `text-transform: uppercase` shows the text in capitals without changing the HTML: `list.html` still says `Full name`.

**Example 2.** Right-click the big blue heading at the top, **Students** → **Inspect**. In Styles, what is its `font-size`?

- Option A: `16px`
- Option B: `20px`
- Option C: `24px`
- Option D: `32px`

**What you see:**

In the rule `h1`: `font-size: 24px;`

> **Answer:** Option C — `24px`
> 
> The heading is an `h1`, and the `h1` rule in `style.css` has `font-size: 24px`.

### Way 5 — Trying the form

**What you are asked:** The question tells you how to fill in the form, and asks what happens. It is what sections 8.9 and 9.8 of the guide do.

**What you do:**

- Make sure the server is running and the home page is open.
- Open the form as the question says: **+ Register a new student**, or **Edit** next to a student.
- Fill in the boxes exactly as the question says, and press the button.
- Read the red message at the top of the form.

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

**What you see:**

A red message at the top of the form: **This student ID is already registered.** — and no student is added.

> **Answer:** Option B — This student ID is already registered.
> 
> `MIS-2025-001` is Ahmad Karim's number, and the server refuses a number twice — the same as section 8.9.

**Example 2.** In the list, click **Edit** next to **Sara Ali**. Delete the name in the **Full name** box and type only one space — the Space key, once.

Then press **Save changes**. What appears?

- Option A: Sara's name becomes empty in the list
- Option B: Full name is required.
- Option C: This student ID is already registered.
- Option D: Student ID is required.

**What you see:**

A red message: **Full name is required.** — and Sara's name stays as it was.

> **Answer:** Option B — Full name is required.
> 
> The browser counts a space as something typed and lets it through, but the server takes the spaces off both ends (`strip`), and nothing is left.
