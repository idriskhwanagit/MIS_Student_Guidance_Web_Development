# Mock and midterm guide — the practical questions

> **The mock and the midterm have 4 practical questions, 2 marks each.** In
> each one you do one small thing on your laptop, see what happens, and choose
> the answer that matches it.

> ⚠️ **Every practical question comes in one of these five ways only**, and is
> done exactly the same way. Examples of each way are in the Questions and
> Answers tab, but the questions will not come as the examples are: only the
> details change.

> **Every task only looks:** you change no file and nothing is saved.

> 💻 **On a laptop only** — not on a phone.

> 🔓 **On the exam day only this guide stays open.** The Web Dev Practical and
> the Questions and Answers tabs are closed, so do the five ways at home
> before.

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
  from [this link](https://drive.google.com/uc?export=download&id=1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ).

## Once at home, before the mock

**1.** Download the zip with [this link](https://drive.google.com/uc?export=download&id=1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ). If Google asks,
sign in with your university account, and the file downloads by itself. If it
does not, open [this Drive page](https://drive.google.com/file/d/1idEb8HPngN5aYx2i9M_dpxw5XgY885OJ/view?usp=drive_link): at the top of the page, under the
file's name, click the round button with a down arrow ⬇, next to **Comment**.
Then right-click the zip → **Extract All** → **Extract**. Inside the new
folder is a folder called `student-system-exam` — that is the project.

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

> 🔓 This guide is open on that day, but the site's other two tabs are
> closed. Know these beforehand.

**1.** The laptop with its charger. Your internet on, and Chrome signed in with
your university account.

**2.** In VS Code open the `student-system-exam` folder, and stop every other
server.

**3.** In the first terminal type `python app.py`. Open the second terminal
with **+**, for the commands.

**4.** Open two tabs in Chrome: one at `http://localhost:8000`, which must show
Sara Ali and Ahmad Karim, and the other with the exam form.

**5.** Answer everything on the laptop. In the form the answers are in a
different order from the examples, so choose them by what they say, not by
their letter.

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

For each way: what you are asked and what you do. Two examples of each way, with their answers, are in the Questions and Answers tab, in the part "Practical questions — worked examples".

### Way 1 — Asking the database

**What you are asked:** The question gives you a ready `python -c` command that reads something from the database, and asks what it prints. It is the same as sections 4.7, 7.2.1 and 8.1.1 of the guide.

**What you do:**

- Copy the command from the question.
- Paste it into the second terminal and press `Enter`.
- Read the line it prints, and choose the same among the answers.

### Way 2 — Reading the last line of an error

**What you are asked:** The question gives you a command with a mistake in it on purpose, and asks what the error says. It is what section 7.2 of the guide teaches: red text that starts with `Traceback`, and you read its last line.

**What you do:**

- Copy the command and run it in the second terminal.
- Red text appears. Read only its last line.
- Choose the answer that is that last line.

### Way 3 — Opening an address

**What you are asked:** The question gives you an address, and asks what the page shows. It is what sections 6.7 and 9.8 of the guide do.

**What you do:**

- Make sure the server is running.
- Put the address in Chrome's address bar and press `Enter`.
- Look at the page: its heading and its boxes. For a page that does not exist, Chrome shows its own error page, with `HTTP ERROR 404` on it.

### Way 4 — The Inspect tool

**What you are asked:** The question names a part of the page and asks what its CSS says. It is what section 6.6.1 of the guide teaches.

**What you do:**

- Open the page in Chrome.
- Right-click exactly on the part the question names → **Inspect**.
- In **Styles**, find the rule the question is about and read its value.

### Way 5 — Trying the form

**What you are asked:** The question tells you how to fill in the form, and asks what happens. It is what sections 8.9 and 9.8 of the guide do.

**What you do:**

- Make sure the server is running and the home page is open.
- Open the form as the question says: **+ Register a new student**, or **Edit** next to a student.
- Fill in the boxes exactly as the question says, and press the button.
- Read the red message at the top of the form.
