If you've ever used [OpenCode](https://opencode.ai/), [Cursor](https://www.cursor.com/en), or [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) as an ["agentic" AI](https://en.wikipedia.org/wiki/Agentic_AI) tool, you'll understand what we're building in this project.

We're **building a toy version of Claude Code** using Google's [Gemini API](https://ai.google.dev/gemini-api/docs/pricing)! As long as you have an [LLM](https://en.wikipedia.org/wiki/Large_language_model) at your disposal, it's actually surprisingly simple to build a (somewhat) effective custom agent.

Until recently, Google offered generous free-tier limits on the Gemini API – including for `gemini-2.5-flash`, the model we recommend for this project. However, in December 2025 Google [drastically lowered](https://www.reddit.com/r/GeminiAI/comments/1pg4et5/google_reduces_api_rate_limits_for_free_tier/) the free-tier rate limits, making it difficult to complete this project without hitting the limits often.

It seems [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing) will continue to change frequently and without notice. We recommend, if possible, [setting up a paid account](https://ai.google.dev/gemini-api/docs/billing) with Google and using the `gemini-2.5-flash` model. You should accrue no more than **~$1–2** in charges during this course. Otherwise, you can still use `gemini-2.5-flash` on the free tier, but you'll be subject to very few requests per day.

We'll keep updating this course as the situation with free tiers and model quality evolves!

## for Windows Users

## What Does the Agent Do?

The program we're building is a CLI tool that:

1. Accepts a coding task (e.g., "strings aren't splitting in my app, pweeze fix 🥺👉🏽👈🏽")
2. Chooses from a set of predefined functions to work on the task, for example:
    - Scan the files in a directory
    - Read a file's contents
    - Overwrite a file's contents
    - Execute the Python interpreter on a file
3. Repeats step 2 until the task is complete (or it fails miserably, which is possible)

For example, I have a buggy calculator app, so I used my agent to fix the code:

```sh
> uv run main.py "fix my calculator app, it's not starting correctly"
# Calling function: get_files_info
# Calling function: get_file_content
# Calling function: write_file
# Calling function: run_python_file
# Calling function: write_file
# Calling function: run_python_file
# Final response:
# Great! The calculator app now seems to be working correctly. The output shows the expression and the result in a formatted way.
```

## Prerequisites

- Python 3.10+ installed (see the [bookbot project](https://www.boot.dev/courses/build-bookbot) for help if you don't already have it)
- The [uv](https://github.com/astral-sh/uv) project/package manager ([installation docs](https://docs.astral.sh/uv/getting-started/installation/))
- Access to a Unix-like shell (e.g. `zsh` or `bash`)

## Learning Goals

The learning goals of this project are as follows:

1. Get an introduction to multi-directory Python projects.
2. Understand how the AI tools that you'll almost certainly use on the job actually work under the hood.
3. Practice your Python and functional programming skills.

The goal is _not_ to build an LLM from scratch, but instead to use a pre-trained LLM to build an _agent_ from scratch.

## Assignment

To get started, make sure you have Python and the [Boot.dev CLI](https://github.com/bootdotdev/bootdev) installed and working.

The Gemini API is an external web service, and it may rate limit your project. On lessons like this one, failed submissions won't penalize you, so it's safe to retry if something goes wrong on Google's end.

Not every lesson in this course is no-penalty, so read the instructions carefully and follow the submit flow each lesson asks for.