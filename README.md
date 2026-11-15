# Carta Engineering Challenge

Congratulations, and thank you for considering joining Carta!

## The Challenge

**Design and build a feature that you think would be nice to have in Carta.**

Pick something you'd want as a student using Carta to plan your courses. A few examples to get you thinking:

- Recommending courses based on ones you've already taken or saved
- Comparing two or more courses side by side
- Any idea of your own is even better!!

## Focus on Your Strengths

Your submission should be a working feature, but where you put your effort is up to you:

- **If you're more experienced in frontend**, focus on the UI: component structure, state management, the user experience, and how it looks. The backend can be minimal (for example, reading from a JSON file or a mocked API).
- **If you're more experienced in backend**, focus on the API and the data layer. The UI can be minimal (for example, a basic page, or no UI at all, with example requests in your README).
- **If you're comfortable across the stack**, feel free to build both parts, with a real UI talking to your own API and database. We'd love to see that! Since the time limit is the same, it's fine if each part is a bit lighter than it would be with a single focus.

Tell us in your README which focus you chose.

## Database Design

Your submission must include a database design for your feature. **If you're focusing on backend or full stack, the database design is one of the most important parts of your submission**.

At minimum, describe your schema: the tables (or collections), their fields and types, keys, and the relationships between them. A diagram, a SQL schema file, or ORM models are all fine. Explain the main choices you made, for example:

- How you normalized (or chose not to normalize) the provided data
- Which indexes you'd add, and which queries they support
- How the schema would change as the feature grows

**Backend or full stack focus:** we'd like to see the schema actually implemented, with your API reading from and writing to a real database. SQLite is perfectly fine, and so is Postgres, MySQL, or anything else you like.

**Frontend focus:** a written schema in your README is enough. You don't need to implement it.

## Data

We've provided sample course data in [`course-data.json`](course-data.json). It's a JSON array of 15 courses, each with fields like `title`, `description`, `course_codes`, `min_units`/`max_units`, `seasons_offered`, `general_requirements`, instructor `ratings` by term, and section `offerings`. The data is nested and somewhat messy on purpose, much like real data. Deciding how to model it is part of the challenge.

**You're welcome to create synthetic data.** If your feature needs data we didn't provide (students, saved courses, schedules, reviews, more courses, and so on), make it up, by hand or with a script. You can also extend or ignore the provided data. Just tell us what you generated and how.

## Tech Stack

Use any language, framework, or database you like. We have no preference. For reference, Carta uses React and TypeScript on the frontend, so those are welcome but not required.

## Time

**We expect this to take about 1.5–2.5 hours.** If you've spent longer than that and aren't finished, feel free to stop! We'd much rather see partial progress that shows your strengths than nothing at all. Done is better than perfect, and your time is valuable. If you don't finish, tell us roughly how long you spent and outline what your next steps would have been.

## What We Care About

- **Product thinking:** Is the feature useful, and is the scope sensible?
- **Design:** Are the API, the database, and the components clearly structured?
- **Code quality:** Can someone else read your code? Could they test it?
- **Tradeoffs:** Do you know the weak spots of your approach, and can you explain them?

## What We Want

- **Source code** for a runnable program
- **A README** containing:
  - Instructions to install and run the program
  - The feature you built, who it's for, and why you picked it
  - Which focus you chose (frontend, backend, or full stack)
  - Your **database design**: the schema and the reasoning behind it
  - About 2 important design decisions, the reasons for them, and their tradeoffs
  - Any synthetic data you created, and how you created it
  - Roughly how long you spent, and what you'd do next with more time

## Submission

Please email your deliverables to Grace (gyepark@stanford.edu) and Kelly (kkellyb@stanford.edu) (Google Drive, ZIP file, private GitHub repository are all okay). Our GitHub usernames are @graceparkk and @kkellybonilla.

The challenge is deliberately open-ended and leaves you room for judgment. If you have questions, please reach out to those email addresses!

Good luck, thank you for considering joining Carta, and we hope to hear from you soon!
