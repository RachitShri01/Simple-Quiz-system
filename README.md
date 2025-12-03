# Local Quiz Studio – Single‑File Quiz System

This project is a simple, self‑contained quiz system built for an assignment using only one HTML file with embedded CSS and JavaScript. It runs entirely in the browser using local storage, so you can use it offline and later host the same file on any static hosting platform (GitHub Pages, Netlify, Vercel, etc.) without backend changes.[web:124]

---

## What this file does

- Provides a **login/signup portal** so multiple users can share the same browser but keep their quiz data separate.
- Creates a **personal dashboard** for each user with basic analytics: number of quizzes, total questions, and last updated time.
- Let every user **create, edit, and delete** their own quizzes without affecting anyone else.
- Includes a **quiz view page** where you can click options to check answers, with clear correct/incorrect feedback.
- Stores everything in **`localStorage`** in the browser, so there is no server and no external database required.

---

## How it works (short version)

- All data (accounts + quizzes) is saved in the browser’s local storage under a single key.  
- Each account has:
  - A username/email
  - A password (stored in plain text for simplicity in this assignment)
  - Its own list of quizzes
- A quiz contains:
  - A title
  - A list of questions, each with multiple options
  - A flag on exactly one option per question marking **which answer is correct**
- There is also a **default demo account**:
  - User: `demo@example.com`  
  - Password: `demo`  
  This account comes with a sample quiz, allowing you to preview the layout before creating anything.

---

## Using the app locally

1. **Download the file**
   - Save the provided code as `quiz-app.html` (or any `.html` name you like).

2. **Open in your browser**
   - Double‑click the file, or open it via “Open File” in Chrome / Edge / Firefox.
   - Make sure JavaScript is enabled; the app will not work without it.

3. **Sign in or sign up**
   - To explore quickly, use the demo account:  
     - Email/username: `demo@example.com`  
     - Password: `demo`
   - Or click **Sign up** and create your own account.
   - After sign‑in, you are taken to your **dashboard**.

4. **Create and manage quizzes**
   - From the dashboard:
     - Click **Create new quiz** to open the quiz editor.
     - Give the quiz a **title**.
     - For each question:
       - Enter the **question text**.
       - Add options using **Add option**.
       - Use the **round selector (radio button)** next to an option to mark it as the correct answer.
       - You can **add more questions** or **delete existing questions**.
     - Click **Save quiz** to store it under your account.
   - Back on the dashboard:
     - Click a quiz **card** to open the **quiz page**, where you can click options to check answers.
     - Use **Edit** or **Delete** buttons on each quiz to modify or remove it.

5. **Delete your account (and data)**
   - While signed in, click **Delete account** on the dashboard.
   - Re‑enter your username and password to confirm.
   - This completely removes your account and all related quizzes from local storage on that browser.

---

## Notes and possible extensions

- This is intentionally **frontend‑only**, designed for assignments, demos, and personal use.  
- Because everything is in local storage, data:
  - Is tied to a **single browser on a single device**.
  - Can be cleared if you reset your browser data.
- Later, the same UI and data model can be wired up to a real **database or backend API** (for example, using a REST or GraphQL server) while keeping most of the front‑end logic and layout unchanged.
