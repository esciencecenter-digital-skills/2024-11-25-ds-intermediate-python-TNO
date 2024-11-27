![](https://i.imgur.com/iywjz8s.png)


# Day 1 Collaborative Document TNO Intermediate research software development skills with Python (25th and 26th of November)

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: https://edu.nl/j4ek6

Collaborative Document day 1: https://edu.nl/j4ek6

Collaborative Document day 2: https://edu.nl/dpfeh

##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website

https://esciencecenter-digital-skills.github.io/2024-11-25-ds-intermediate-python-TNO

🛠 Setup

https://esciencecenter-digital-skills.github.io/python-intermediate-development-gitlab/setup.html

Lesson material

https://esciencecenter-digital-skills.github.io/python-intermediate-development-gitlab/

Wokshop GitLab subgroup

https://ci.tno.nl/gitlab/scientific-software-engineering-course/2024-11-25

## 👩‍🏫👩‍💻🎓 Instructors

Sven van der Burg, Claire Donnelly, Sander van Rijn, Carsten Schnober

## 🗓️ Agenda
09:30	Welcome and icebreaker:
    1. Ice breaker
    2. Netherlands eScience Center introduction
    3. Collaborative document introduction
    4. Course introduction    
09:45	Setting up Environment For Collaborative Code Development
10:30	Break
10:40	Setting up Environment For Collaborative Code Development
11:30	Break
11:40	Setting up Environment For Collaborative Code Development
12:30	Lunch Break
13:30	Setting up Environment For Collaborative Code Development / Ensuring Correctness of Software at Scale
14:30	Break
14:40	Ensuring Correctness of Software at Scale
15:30	Break
15:40	Ensuring Correctness of Software at Scale
16:15	Wrap-up
16:30	END

## 🏢 Location logistics
* wifi
* coffee
* toilets
* lunch
* emergency

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## 🗒 Optional exercises
* [Optional exercises section 1](https://esciencecenter-digital-skills.github.io/python-intermediate-development-gitlab/17-section1-optional-exercises/index.html)
* [Optional exercises section 2](https://esciencecenter-digital-skills.github.io/python-intermediate-development-gitlab/25-section2-optional-exercises/index.html)


## Collaborative Notes

- A link to the [TNO Gitlab template](https://codingguild.tno.nl/coding-at-tno/tno-templates/#gitlab-projects).

- When forking the project, choose the `scientific-software-engineering-course/2024-11-25/` namespace, and **add** your name to the **project name**. The project slug should update automatically.

- In the cloning instructions, the material refers to `gitlab.com`, while we are using the `ci.tno.nl` domain. This means your clone url probably looks like this instead:
  ```bash
  git clone git@ci.tno.nl:scientific-software-engineering-course/2024-11-25/python-intermediate-inflammation-<YOUR-NAME>.git
  ```
- Known problem on Windows: typing `python` in Git Bash 'hangs' and does not respond:
  - Paste the following command: `echo "alias python='winpty python.exe'" >> ~/.bashrc`
  - Restart Git Bash
  - Typing `python` should now work
  If not, please get in touch! Solution source: [StackOverflow](https://stackoverflow.com/questions/32597209/python-not-working-in-the-command-line-of-git-bash)
- Does the file remain empty when using `winpty python -m pip freeze > requirements.txt`? Adjust the alias to `alias python='winpty -Xallow-non-tty python'`
  - If that in turn adds strange characters, extend it further to  `alias python='winpty -Xallow-non-tty -Xplain python'`
  - [Solution source](https://superuser.com/a/1322277/519432)

- [CI matrix example for GitHub](https://carpentries-incubator.github.io/python-intermediate-development/23-continuous-integration-automated-testing/index.html#scaling-up-testing-using-build-matrices)
  - GitLab possibly supports something similar through the [`parallel.matrix`](https://docs.gitlab.com/ee/ci/yaml/#parallelmatrix) keyword, but we have no experience with this (yet)

## Feedback morning
Please help is adapt the course to your liking and improve it next time. Can you write down 1 thing that went well and 1 thing that can be improved?
### What went well:
* Great stuff, clear texts, good atmosphere
* It is super nice for everyone to have their own pace
* I really like the in-depth explanation of specific commands. I have executed a lot of these in the past, but for most I had no idea what they did in the background.
* Nice pace
* Pace in a slow mode dependent on the user
* Good overview/tutorial for Git.
* Nice off-topic discussions.
* Nice to see venv's and git
* Nice balance between some theory/slides, discussions and practise/exercise. 
* Each person having freedom to take time for certain components.
* Good to also learn from your practices and experiences (e.g. using windows terminal)
* Running through the tutorial is a breeze
* Great attention to people

### What can be improved:
* TNO IT support
* Some start up problems, slight differences between manual and practice.
* Too much setting up required, could have been done at home, so we can focus on how it works here.
* Explain for what type of project to set up an architecture as this, and for what type of projects a different architecture would be more beneficial (more complex or just use a single script)

## 🌡 Temperature check
I am currently at (add an emoji behind to indicate where you're at, you can copy from here: ❤️🙈🥸)

Section 1
- Python Code Style Conventions 🥸🥸🥸
- Verifying Code Style Using Linters ❤️
- Optional exercises for section 1

Section 2
- Section 2: Ensuring Correctness of Software at Scale 🥸
- Automatically Testing Software 🙈🥸🥸
- Scaling Up Unit Testing ❤️🥸❤️
- Continuous Integration for Automated Testing ❤️🥸🥸🤦‍♂️
- Diagnosing Issues and Improving Robustness
- Optional Exercises for Section 2

## Feedback **afternoon**
Please help us adapt the course to your liking and improve it next time. Can you write down 1 thing that went well and 1 thing that can be improved?
### What went well:
- Good intro to testing
- Made a start with CI/CD, that part was really new. Actually simpler than I thought.
- New to code formatting standards in Python, I like the idea of automated checking (should be standard...) 
- Great attention to people and breaks
- Wrote first tests and a CI is pending. Explanation helped.
- Assert testing == good
- Quick and good assistance in case of issues/questions
- Very practical guide on testing
- Done with section 2
- CI/CD reached. Now installing docker to create runners on my own PC.
### What can be improved:
- Something to be added: handling merge conflicts in Git (example of how to do it)
- 
-
-
-

 

## 📚 Resources
- [Slide with rules of thumbs for when to use which good practices](https://esciencecenter-digital-skills.github.io/digital-skills-slides/modules/good-practices-lesson/good-practices-slides#/5/0/8)
