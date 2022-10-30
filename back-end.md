# Backend Engineering Challenge: Course Search API

## The Problem

You are writing a web API for CourseTime, the next iteration of course exploration at Drofnats Wizarding University, and one important feature is searching for courses. You're going to write the API to search for courses!

The API should be called over an HTTP request. It should return JSON representing an ordered list of search results. The exact schema is left to your discretion; you are free (and encouraged) to borrow the input data format in whole or part.

The search functionality has two key requirements: a text search, and a filter.

You are free to use any framework or language to implement this. [Express](https://expressjs.com/) in JavaScript and [Flask](https://flask.palletsprojects.com/en/2.2.x/) in Python are two options, but there are many good choices and we have no preference.

**We expect this will take you about 1.5 - 2.5 hours.** If you've spent longer than that and are not finished, feel free to stop! We'd much rather see partial progress and the strengths you can demonstrate through that, than not see anything at all. Done is better than perfect. Your time is valuable and we want to respect that. If you don't finish the basic functionality, please tell us approximately how long you spent and give us a broad outline of what your next steps would have been.

It's open-ended, but not too long once you get a handle on the problem. For reference, one of our solutions in JavaScript is about 100 lines long (not including the hardcoded course data).

### Text Search

The search API should take a textual query: the user's search string. Based on this string, your backend will need to rank the relevance of various candidate results.

It is completely not expected to do anything fancy (e.g. Google-style negative matches or "multi-word quotes") with your query parsing. (If you want to, we won't stop you!)

You are deliberately left with a large amount of discretion for how to do this, but fret not! Your implementation need not be complicated, efficient, or functionally perfect. What's more important is you come up with a reasonable attempt to address the problem, and have a clear thought process and well-articulated tradeoffs. (I.e. in your README, you should discuss known shortfalls with your approach.)

Some things to think about:
- How should titles versus descriptions be handled, for relevancy matching?
- Should completely irrelevant results (with no overlap with the search query) be included? What constitutes "completely irrelevant"?
- If the user searches directly for a course code, how should that case be handled? (As a user, what would you expect in that case?)
- How should common grammatical "glue" like _and, or, the, a, an_ be handled?
- How should different parts of speech, conjugations, and pluralizations be handled (e.g. _computer_ vs _computing_ vs _compute_, or _basic_ vs _basics_)?

(It is entirely okay not to handle some of these cases! But do discuss the tradeoffs of doing so, e.g. is it easier at the cost of a more brittle search user experience?)

#### Some Starting Points
Here are some starting points you can choose to use if you'd like. Some are simpler than others, and some may take more time than others. It is _much more important_ to us that whatever approach you use is one whose tradeoffs you can describe, than that your approach makes a good or great production search algorithm. If you'd like, feel free to use what you see as relatively simple or easy from this list, or something simple and easy not on this list!

These starting points are also not complete algorithms -- they're key concepts that can be integrated into a solution.

- One starting point for an approach is to split a string into many small pieces, such as words [or, more fancily, word or character [n-grams](https://en.wikipedia.org/wiki/N-gram), or word roots or stems], yielding a sparse vector. There are a couple straightforward, plausible relevancy algorithms one can implement given vectors of word-like strings.
- Another potentially useful concept: the [Levenshtein distance](https://en.wikipedia.org/wiki/Levenshtein_distance) between two strings. 

There are other valid concepts! If you try something and it doesn't work very well in practice, that's a noteworthy takeaway.

### Filtering

There are various discrete fields in the course data (see _Input Data_ below) -- you should also include at least one optional, discrete filtering parameter. If this parameter is specified, then courses which do not match it should never be included in the output.

For instance, if a filtering parameter for `quarters` is included, and the filter quarter is specified as autumn, no course that is not offered in autumn should ever be included in the results, regardless of how good the text query match is.

### Input Data

Course data is provided for you in the `backend-course-data.json` file in this repository. Don't worry about a database or anything; feel free to read from this file into memory, hardcode the data, or otherwise do whatever's easiest to work with this data.

That file is a JSON array of course objects. The course objects have the following fields:
- `id`: Unique integer ID
- `title`: Course title (nonnullable)
- `description`: Course description (nullable)
- `course_code`: Course catalog listing code (nonnullable)
- `requirements`: 0 or more requirements (enumerated strings) that this course fulfills
- `units`: Integer array of length 2 with `units[1] >= units[0]`: the number of units you can take this course for. If `units[0] == units[1]`, then the course is not offered for variable units. Otherwise, students can take the course for any of `units[0], units[0] + 1, units[0] + 2, ..., units[1] - 1, units[1]` units.
- `quarters`: Array of length at-most 4 (enumerated strings): the quarters in which this course is offered


## What We Care About

Completing all or part of this challenge is a great way to demonstrate a very practically-aligned understanding of not just implementation, but also higher-level design of a web API and web-based system. Beyond that, we have a few things we're looking for:

### Readability
Carta lasts longer than any one student's time at Stanford, and the code written on Carta will need to be maintained by people not even currently at the university. Therefore, we care about readability and maintainability.

Similarly, in this exercise, people who don't know you or your code will be reading your submission. Please make sure it's easy to understand.

### Maintainability
Think about how your code might be tested, and might grow over time.
What are the most complicated pieces of logic, and what pieces of logic might need to be reused or change over time?
How can you structure your code to make it easy to test, and to increase confidence in its correctness?
How can you structure your code to allow reuse?  

### Thinking About the Big Picture
A course search API would not be used in isolation: it would be used by a frontend, which would be used by students like you trying to plan their academic career. When there are ambiguities or room for design choices, think about the broader impact. What might be useful for a frontend developer? What might be useful for an end user?

## Don't Worry About...
**Edge cases not covered in the provided dataset.** The Stanford course schema is chock-full of weird edge cases, and for purposes of this exercise, you don't have to think about them. Focus on getting something which works in the provided common cases, and in the use cases described.

**A database.** Don't worry about a database. Feel free to read the input course data from a file into memory, or to hardcode it directly in source code.

**Algorithmic complexity.** This is not a LeetCode algorithms challenge. Don't worry about an asymptotically optimal implementation (though if you notice something in your implementation that might be slow as the system scales, feel free to note it in your README or comments!). Naive algorithms are totally fine, as long as they make sense.

## Please don't spend too much time!

To reiterate: this problem mirrors a (more complex) variant that Carta has genuinely faced -- this means that even in the simplified version, there is plenty of complexity which you could easily spend many hours addressing. Please don't! Your time is valuable, and we've tried to focus this problem and our expectations on what we think is most important for our recruiting (and which we think poses an interesting challenge).

If you don't finish in the projected time range, it's okay to stop and submit what you have, describing what your next steps would have been!

## What We Expect
- Source code for a runnable program
  - The web server should expose a HTTP REST API endpoint to search for courses
  - The search endpoint should take a textual query parameter for text search of some kind. You have discretion over your exact search algorithm, as long as it is conceptually reasonable. It need not be complicated.
  - The search parameter should also take at least one filtering parameter of your choice (e.g. quarter offered, requirement fulfilled, or number of units). This parameter should be a strict filter on returned results (i.e. if the caller passes a quarter offered restriction on autumn, results not offered in autumn should _never_ be returned, regardless of the text query parameter).
  - You have discretion over the response format. Feel free to use the same format as the stored data.
- A README containing:
  - Instructions to compile (if needed) and run the program
  - A brief description of major design/architectural decisions (e.g. how you structured your search endpoint, your algorithm for  ordering search results, etc). This need not be long; pick about 2 important or nontrivial ones to talk about.
  - Rationale for the above design decisions ("I thought it would be easiest to get working quickly" or "I'm most comfortable with it" are valid contributing reasons), and notable tradeoffs.
  - (Optional) Anything else you'd like us to know about your project, or feedback on the challenge

Please email your deliverables to Glen (ghusman@stanford.edu) and Jared (jwasserman@stanford.edu) (Google Drive, ZIP file, private GitHub repository are all okay). Our GitHub usernames are @glen3b and @jwass91.

Good luck, thank you for considering joining Carta, and we hope to hear from you soon!