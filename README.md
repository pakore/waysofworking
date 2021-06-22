# A guide to Paco's Ways of Working

## Introduction

Over the years, I have worked in different companies and I've seen many ways to develop software and projects. I've always tried to keep the ways that were making me and my team more sucessful, and discarded the ones that for one reason or another, didn't work that well. 
In this guide, you will find a summarized set of ways of working that I have learnt over the last 15 years. Keep in mind that this is based on my personal experience, so in your particular case or organization, some of them may not make sense.

## This is the way

### Be your most demanding customer

If facing with a design decision, ask yourself: "_What would the customer prefer?_"
In the real world a customer usually is an external human being that decides to pay for your services. But in the IT world, a customer can be **anyone** that is consuming what you produce. A customer could be:
- A person that does not belong to the organization
- Another team within your organization
- A teammate
- Your line manager
- Your future self

Keeping a customer happy is probably the most difficult task when developing software. So if you have the chance to make things easier for your customer, usually is the right way to go. For example, I had to create a new service with a new API. I asked myself: "_If I were a customer and I would be deciding if this API was useful for my team, what would help me decide_". I answered myself:
- Superb documentation
- OpenAPI description
- Interactive examples
- Some kind of playground
- An intuitive API

And suddenly I had a list of items to work on that would make the customer happy. I was proud of the quality of my work, which made me happy too. Customers could find what they were looking for right away, so I did not have to invest much time answering questions, which allowed me to focus on the next iterations.

In a nutshell: **Imagine what your customer would want and your life will be easier.**

### Data-driven beats guess-driven

As an architect, I come up with ideas about how to improve my services all the time. But just because I think they are good ideas, does not mean they really are. You should encourage your team to come up with ideas, but to take a decision these ideas have to be backed up with real data:

- Is your idea improving the critical path / bottleneck? (Throughput)
- Is your idea solving a relevant use case or is an edge case? (Focus)
- How much % of customers will benefit from the time invested to implement it? (Impact of change)
- How much money will we spend to implement it and how much money will we save afterwards? (Return of investment)
- Is your idea solving edge case but this case could be catastrophic for the company? (Risk vs Reward)

Gathering metrics about your software in an automated way is as important as releasing features. Make sure your stakeholders understand this too.

In a nutshell: **It's easier to take decisions technically and politically when you have the data to back it up. Make sure you invest in the architecture and the tools to enable this.**

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

In a nutshell: **Devops culture will improve the peformance and the quality of your team in the long term, but it will cost in the short-term**
