
# Points to make:

- During my brainstorm, I came up with many workarounds
	- But will they be confident enough to work for a recruiter?

Let's think about it from the side of the bad actor

# Points of attack:
- use GPT
- get someone else to write the code for you
- use published code solutions on YouTube

From the start, we already have a behemoth of options for plagiarism, and it is very difficult to target the second two from a CLI. I will get to that.

reasonable to assume GPT would be the first instinct; easiest way to get results

Complex solution: get langchain to generate a GPT agent in the background, output to file, compare using Rabin Karp algorithm or fuzzy wuzzy library

Low-tech solution: monitor the timing of respondent, if it is fast, then automatically assume that it was copied and pasted.

Flaws:
Complex solution: combinations of temperature for example (Openai temperature 10 vs Openai temperature 0) variability within responses would mean that we would not flag plagiarized gpt responses

Low tech solution: maybe they code really fast, and also consider we don't know the problem that is going to be asked. What if it's fizzbuzz, a commonly known problem and the user can answer very fast?

I also considered a combination of the two, with logic like:
if it's high speed and the similarity is more than 70% then flag code red
50% then flag code yellow etc
Still does not account for other situations

---
What if they are smarter and get their code from somewhere less easily searchable? For example, Youtube would be extremely difficult for us to parse through transcripts to find solutions that they might have used

And someone else writing the code cannot be solved by a CLI.

---
Ways we could solve this in a web app:
I've used an OA called codesignal before and they use something that tracks keystrokes, if you copy paste they can easliy detect it

I'll demo this for you rn

With a web app we could also run stuff like
- webcam verification
- movement proctoring
- microphone detection
- hasLeftTab
- etc
