![](https://i.imgur.com/iywjz8s.png)


# Day 2 Collaborative Document TNO Intermediate research software development skills with Python (25th and 26th of November)

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: https://edu.nl/dpfeh

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
Sven van der Burg, Claire Donnely, Sander van Rijn, Carsten Schnober

## 🗓️ Agenda
09:30	Welcome and recap
    1. Icebreaker
    2. Feedback yesterday
    3. Start hacking 💻
09:45	Software Development as a Process
10:30	Break
10:40	Software Development as a Process
11:30	Break
11:40	Software Development as a Process
12:30	Lunch Break
13:30	Collaborative Software Development for Reuse
14:30	Break
14:40	Collaborative Software Development for Reuse
15:30	Break
15:40	Collaborative Software Development for Reuse
16:00	
- Post-workshop Survey
- Recap exercise
- 
16:30	END


## 🏢 Location logistics
* wifi
* coffee
* toilets
* lunch
* emergency
* 

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## Intermediate 30 seconds
|        | Round 1 | Round 2 | Round 3 | **Total** |
| ------ | ------- | ------- | ------- | --------- |
| Team 1 | 3       | 3       | 2       | 8         |
| Team 2 | 3       | 1       | 4       | 8         |
| Team 3 | 2       | 2       | 4       | 8         |
| Team 4 | 2       | 3       | 4       | 9         |

### Round 1 concepts:
- Unit testing
- Integrated Development Environment
- Model-View-Controller architecture
- GitLab
- Coding guild

### Round 2 concepts:
- git commit
- merge conflict
- PEP8
- virtual environment
- SSH

### Round 3 concepts:
- git pull
- linter
- Continuous integration
- Forking
- Software engineering vs programming

## 🗒 Optional exercises section 3
Here follow some optional exercises for section 3 if you are done early or need some extra practice.
The exercises have an explorative nature, so feel free to go off in any direction that interests you.
You will be looking at some tools that either complement or are alternatives to those already introduced.
Even if you find something that you really like,
we still recommend sticking with the tools that were introduced prior to this episode when you move onto other sections of the course.

### Exercise: Apply to your own project(s)
Apply what you learned in this section to your own project(s). 
This is the time to ask any questions to your instructors or helpers.
Everyone has different preferences for tooling, so getting the input of experienced developers is a great opportunity.

### Exercise: 'advanced object-oriented programming for persistence' and 'databases'
There are two optional extra episodes which you may find interesting.

Both episodes cover the persistence layer of software architectures and methods of persistently storing data, but take different approaches. The episode on [persistence with JSON](https://carpentries-incubator.github.io/python-intermediate-development/persistence/) covers some more advanced concepts in Object Oriented Programming, while the [episode on databases](https://carpentries-incubator.github.io/python-intermediate-development/databases) starts to build towards a true multilayer architecture, which would allow our software to handle much larger quantities of data.

#### Patient class
You can use below code if you want to add the missing `Patient` class. You need it if you want to work on the `persistence` or `databases` extra episodes.

```python
class Observation:
    def __init__(self, day, value):
        self.day = day
        self.value = value

    def __str__(self):
        return str(self.value)

class Patient:
    """A patient in an inflammation study."""
    def __init__(self, name):
        self.name = name
        self.observations = []

    def add_observation(self, value, day=None):
        if day is None:
            try:
                day = self.observations[-1].day + 1

            except IndexError:
                day = 0

        new_observation = Observation(day, value)

        self.observations.append(new_observation)
        return new_observation

    def __str__(self):
        return self.name


alice = Patient('Alice')
obs = alice.add_observation(3)
```

## 🗒 Optional exercises section 4
Here follow some optional exercises for section 4 if you are done early or need some extra practice.
The exercises have an explorative nature, so feel free to go off in any direction that interests you.
You will be looking at some tools that either complement or are alternatives to those already introduced.
Even if you find something that you really like,
we still recommend sticking with the tools that were introduced prior to this episode when you move onto other sections of the course.

### Exercise: Apply to your own project(s)
Apply what you learned in this section to your own project(s). 
This is the time to ask any questions to your instructors or helpers.
Everyone has different preferences for tooling, so getting the input of experienced developers is a great opportunity.

### Exercise: Merge conflicts
1. Create a merge conflict (for example by committing a change in the same line of code in GitLab and locally)
2. Use [https://www.jetbrains.com/help/pycharm/resolve-conflicts.html](PyCharm) to resolve the merge conflicts
3. With a team member: Pick one of the bigger functions in one of your team's 'python-inflammation-analysis' projects. Now, you both refactor the function in a different feature branch. Merge one of the branches into main, and create a merge request merging the other feature branch into main. Resolve the resulting merge conflicts together.

### Exercise: GitLab collaboration
- As you've now seen, Merge Requests are a helpful way to keep new features separate until they've been reviewed. To force this behavior, even for yourself, you can [**protect a branch in GitLab**](https://docs.gitlab.com/ee/user/project/repository/branches/protected.html). Try this for yourself, and see what happens if you still commit to main locally and try to push it. How would you fix this when it happens?

### Exercise: Packaging
- Have a look at the [Python Packaging Guide](https://packaging.python.org/en/latest/)
- Try actually publishing your code to [test.pypi.org](https://test.pypi.org) based on the above guide


## Collaborative Notes
- Coding Guidelines of TNO: https://codingguild.tno.nl/coding-at-tno/#coding-guidelines
- If you want to exclude code blocks from code coverage (**not recommended!**), you can use `# pragma: no cover`; see [documentation](https://coverage.readthedocs.io/en/latest/excluding.html).
- The Python version you specify for the Docker image in `.gitlab-ci.yml` defines the Python version that the runner uses in the Gitlab instance. It does not have to be the same as your local Python version.
- [When I activate the virtual environment in python (PyCharm) my terminal doesn't see git and bash commands](https://stackoverflow.com/questions/67565613/when-i-activate-the-virtual-environment-in-python-pycharm-my-terminal-doesnt)

## 🌡 Temperature check
I am currently at (add an emoji behind to indicate where you're at, you can copy from here: 🤩🫡🤖😺)

Section 1
- Python Code Style Conventions 
- Verifying Code Style Using Linters 

Section 2
- Section 2: Ensuring Correctness of Software at Scale 
- Automatically Testing Software 
- Scaling Up Unit Testing 🤖
- Continuous Integration for Automated Testing 😺
- Diagnosing Issues and Improving Robustness 😺🤖😺🤖😺🤦‍♂️🥸 
- Optional Exercises for Section 2

Section 3
- Somewhere in section 3 🫡🤖🤩✌️

## Feedback
### What went well:
- Got a lot of help, despite me going through my own stuff
- New concepts introduced
- Practice "Advanced" topics (from my point of view)
- A lot of repetition of common tasks, to really drive home how things work.
- Great and clear lesson material
- Good introduction to CI/CD
- You made CI/CD look easy! Good job. Also helpful and interesting discussions

### What can be improved
- More explanation on GitLab runners. The process is really murky (not your fault), so extra explanation helps.
- We can learn more about CI we did yesterday
- A bit more time and focus (timewise) on the end of section 2 and 3, the intermediate part.
- Difficult to finish section2 and 3 "on time"
- Not your fault, but it will be a challenge to implement automated testing et al. in the TNO ICT environment.

## Wrap-up:
### 1. Questions about section 4
### 2. Netherlands eScience Center
### 3. Post-workshop survey
https://www.surveymonkey.com/r/6H775GM
![](https://codimd.carpentries.org/uploads/upload_7b63ba898f23f9c7559697e393b7696d.png)

### 4. Recap exercise:
Read through the TNO coding guidelines (https://codingguild.tno.nl/coding-at-tno/#coding-guidelines) and think of everything that you learned in the course. Appreciate that you learned a lot of skills to adhere to these guidelines. Write down your thoughts in the collaborative document:
* Which guidelines do you think are most useful for your work and which do you think are overkill? 
* Are there any guidelines that are still unclear to you? 

### 5. Ending slides
### 6. Discussion


## 📚 Resources
- Coding Guidelines of TNO: https://codingguild.tno.nl/coding-at-tno/#coding-guidelines
- Tip for people interested in design patterns such as MVC: https://sourcemaking.com/design_patterns. Design patterns are not a 'holy grail', but they may help you structure your code. Design Patterns were coined by the 'Gang of Four' book ([Amazon link](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/ref=sr_1_1?crid=236IMN34KZR9Z&dib=eyJ2IjoiMSJ9.mTRaTOPYqsPcUsGD8aznte8IMQZZiYjv7_Xwyyi1iS0K0wee15spp9QiPP_Esnq2hPINIj7vH4tRAjcIlA_0G2x-i0h7K-vdyuJHDUVzSye1Fk3nK4W8gtEncnlgf42M1jXjmHBgAe62irgcTiwmxPl4jNet09G15iBGb_k9KhexRKFhvnhG8vBvfbupG_zn-3nLM8ZCUjhx0FY1B1S--esa4Dowd25cX1zoceUWDiE.Q-6W4nk2sDXADSXfIiXJE_iDi2NiNRcZv9KZ5TzYhjY&dib_tag=se&keywords=design+patterns&qid=1732612498&sprefix=design+pattern%2Caps%2C171&sr=8-1)) (see also https://www.digitalocean.com/community/tutorials/gangs-of-four-gof-design-patterns)
- [Weights and Biases](https://wandb.ai): A (commercial) service for logging, monitoring, presenting, evaluating machine learning tasks.
- Something to keep you busy while having fun coding in December: https://adventofcode.com/
- [Pre-commit](https://pre-commit.com/): a tool for managing git (pre-commit) hooks. These can be used to automatically run your tests, linters, etc every time you make a commit. 