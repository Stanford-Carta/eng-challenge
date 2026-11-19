# Carta Engineering Challenge

Congratulations, and thank you for considering joining Carta!

## The Challenge

**Design and build a feature that you think would be nice to have in Carta.**

Pick something you'd want as a student using Carta to plan your courses. A few examples to get you thinking:

- Recommending courses based on ones you've already taken or saved
- Comparing two or more courses side by side
- Any idea of your own is even better!!

The idea doesn't have to be big or new, since we mostly look at how you built it. Go as big as you want though!

## Time

**We expect this to take about 1.5–2.5 hours.** If you've spent longer than that and aren't finished, feel free to stop! We'd much rather see partial progress that shows your strengths than nothing at all. Done is better than perfect, and your time is valuable. If you don't finish, tell us roughly how long you spent and outline what your next steps would have been.

## Focus on Your Strengths

Your submission should be a working feature, but where you put your effort is up to you. Pick whichever side shows off your skills best and go deep on it. 2.5 hours isn't a lot of time, and we learn way more from one part done really well.

- **Frontend:** focus on the UI: component structure, state management, the user experience, and how it looks. The backend can be minimal (for example, reading from a JSON file or a mocked API).
- **Backend:** focus on the API and the data layer. The UI can be minimal (for example, a basic page, or no UI at all, with example requests in your README).

Even if you're comfortable across the stack, please still pick one. Tell us in your README which focus you chose and why.

## Design Decisions

This is the part we care most about. We want to see how you make design decisions while you build, and why. We aren't looking for any specific principles, so just write about what actually came up for you.

Pick the 2 or 3 decisions that mattered most. For each one, tell us what you went with and why you didn't go with the other options you considered. If you can, point us to the file or function.

It's also really helpful to hear about anything you changed your mind on halfway through, or the part of your design you're least happy with.

You can share your design decisions in one of two ways:

- **Video walkthrough (preferred):** Record a short video (around 5–10 minutes is plenty) where you demo what you built, walk us through your code, and explain your key design decisions. **Please share your whole screen**, not just a single window or tab, so we can follow along as you move between your app, editor, and terminal. A Zoom recording or any unlisted video link is fine.
- **Written writeup:** Include your design decisions in your README.

We strongly recommend the video since it's often faster for you and gives us a clearer picture of how you think.

Some notes either way:

- Feel free to use AI, for the code or for the decisions. Just let us know where it helped. For example: "Claude suggested putting the filtering logic in the API, but I kept it in the frontend because there are only 15 courses."
- Please explain it in your own words. Rough notes, bullet points, or an unscripted video are totally fine, we don't need anything polished.
- If we move forward, we'll go through your code and these decisions with you on a call.
- If you want some background reading, here are some we like:
  - Frontend: [Thinking in React](https://react.dev/learn/thinking-in-react) from the React docs
  - Backend: Hello Interview's [API Design](https://www.hellointerview.com/learn/system-design/core-concepts/api-design) and [Data Modeling](https://www.hellointerview.com/learn/system-design/core-concepts/data-modeling)
  - Either: The Odin Project's [OOP Principles](https://www.theodinproject.com/lessons/node-path-javascript-oop-principles) and Hello Interview's [Design Principles](https://www.hellointerview.com/learn/low-level-design/in-a-hurry/design-principles)

## Data

We've provided sample course data in [`course-data.json`](course-data.json). It's a JSON array of 15 courses, each with fields like `title`, `description`, `course_codes`, `min_units`/`max_units`, `seasons_offered`, `general_requirements`, instructor `ratings` by term, and section `offerings`. The data is nested and somewhat messy on purpose, much like real data. Deciding how to model it is part of the challenge.

**You're welcome to create synthetic data.** If your feature needs data we didn't provide (students, saved courses, schedules, reviews, more courses, and so on), make it up, by hand or with a script. You can also extend or ignore the provided data. Just tell us what you generated and how.

## Tech Stack

Use any language, framework, or database you like. We have no preference. For reference, Carta uses React and TypeScript on the frontend, so those are welcome but not required.

## What We Care About

- **Design:** Is your code clearly structured, and can you explain why you built it that way?
- **Code quality:** Can someone else read your code? Could they test it?
- **Tradeoffs:** Do you know the weak spots of your approach, and can you explain them?

## What We Want

- **Source code** for a runnable program
- **A README** containing:
  - Instructions to install and run the program
  - The feature you built, and why you picked it
  - Which focus you chose (frontend or backend), and why
  - Your **design decisions** (see above), or a link to your video walkthrough
  - How you used AI, if at all
  - Any synthetic data you created, and how you created it
  - Roughly how long you spent, and what you'd do next with more time

## Submission

Please email your deliverables to Grace (gyepark@stanford.edu) and Kelly (kkellyb@stanford.edu) (Google Drive, ZIP file, private GitHub repository are all okay). Our GitHub usernames are @graceparkk and @kkellybonilla.

The challenge is deliberately open-ended and leaves you room for judgment. If you have questions, please reach out to those email addresses!

Good luck, thank you for considering joining Carta, and we hope to hear from you soon!
