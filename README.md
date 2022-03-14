# A guide to Paco's Ways of Working

## Introduction

Over the years, I have worked in different companies and I've seen many ways to develop software and projects. I've always tried to keep the ways that were making me and my team more sucessful, and discarded the ones that for one reason or another, didn't work that well. 
In this guide, you will find a summarized set of ways of working that I have learnt over the last 15 years. Keep in mind that this is based on my personal experience, so in your particular case or organization, some of them may or may not make sense.

## This is the way

### Be your most demanding customer

If faced with a design decision, ask yourself: "_What would the customer prefer?_"
In the real world a customer usually is an external human being that decides to pay for your services. But in the IT world, a customer can be **anyone** that is consuming what you produce. A customer could be:
- A person that does not belong to the organization
- Another team within your organization
- A teammate
- Your line manager
- Your future self

Keeping a customer happy is probably the most difficult task when developing software. Making things easier for your customer, usually is the right way to go.

For example:_If I were a customer and I would be deciding if this API was useful for my team, what would help me decide?_:
- Superb documentation
- OpenAPI description
- Interactive examples
- Some kind of playground
- An intuitive API

In a nutshell: **Focus on the whole customer experience, not only on the commercial product**

### Data-driven over guess-driven.

Architectural decisions can have a big impact down the road. Experience is a great asset, but so are data and statistics. Try to evaluate ideas based on actual facts and not just on guesses:

- Is your idea improving the critical path / bottleneck? (Throughput)
- Is your idea solving a relevant use case or is an edge case? (Focus)
- How much % of customers will benefit from the time invested to implement it? (Impact of change)
- How much money will we spend to implement it and how much money will we save afterwards? (Return on investment)
- Is your idea solving edge case but this case could be catastrophic for the company? (Risk vs Reward)

Gathering metrics about your software in an automated way is as important as releasing features. Make sure your stakeholders understand this too.

In a nutshell: **Investing in metrics collection will allow you to take better decisions and justify them to stakeholders.**

### Devops culture: forks into swiss-knives

A service in production requires writing, connecting and maintaining a lot of components: the service's code itself, unit/functional/integration/E2E tests, CI/CD pipelines, documentation, monitoring tools, testing/performance environments, examples, demos, etc. And it is a **team effort** that every piece in the chain works properly.
E.g:
- Team members should know how to update and run functional / integration, E2E tests, locally or in a testing environment.
- Team members should be able to access staging/production monitoring tools.
- Team members should know how to build a Docker image and deploy it as a k8s pod to create a proof of concept.

In an ideal team, everyone can do everything. The reality is that there will be some specialists on some areas, but in general everyone will be able to do everything with some help and documentation.

Pros:
- Reduced _single point of failure_, since a team member getting sick does not block other team members.
- Team members learn new tools and technologies, new challenges always come up and team members motivation increases. Their career paths are also improved since they dominate more tools and technologies.
- Ownership and responsability of components belongs to the team rather than the one who created it in the first place.

Cons:
- It requires to invest time to train developers until they become devops.
- It requires a _devops_ attitude in the team members. Some devs prefer their silo-zone-of-comfort rather than a world of unkown components.

In a nutshell: **Devops culture will improve the peformance and the quality of your team in the long term, but it will have a cost in the short-term**

### Automate, automate, automate

There are two main reasons why you should automate a task whenever possible:
- The obvious one: to save time.
- The not obvious one: to save your team.

Nothing brings down motivation in a team more than repetitive tasks. Engineers need challenges and freedom for their creativity. Automating a task is interesting, doing the same task every month is not.
By bringing the culture of automation to the team, it keeps the team motivated and interested and it frees time for innovation and progress in the long run.

_Disclaimer_: `Urgent != Important`. Make sure your engineering manager prioritizes automation tasks based on impact!

In a nutshell: **Automation saves time and lowers attrition**

### Trust your team

A team lead / architect / engineering manager goal should be himself/herself redundant. A mature, cohesive and independent team does not need supervision for everyday problems. But to reach this point, a series of steps are needed:
- Teach the team good practices.
- Solve problems **with** them, and not **for** them.
- Give team members increased responsabilites over time. Make them go out of their comfort zone, so they keep expanding their skills.
- Be the safety net of your team, and let them know so. Tell your team that you trust them, and you will be there to help if something goes wrong.
- Give proper credit, visibility and kudos for effort, good ideas and accomplishments.
- When (and not "if", because it will) something goes wrong, solve it together. The only fingers you should point are to point out the solution. Make sure the team implements an (ideally automated) prevention for that problem.
- Encourage your team to experiment, research about solutions to current problems, present to other colleagues, do certifications.

In a nutshell: **Trust your team and switch supervision time for more important tasks**
