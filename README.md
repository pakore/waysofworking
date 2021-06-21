# A guide to Paco's Ways of Working

## Introduction

Over the years, I have worked in different companies and I've seen many ways to develop software and projects. I've always tried to keep the ways that were making me and my team more sucessful, and discarded the ones that for one reason or another, didn't work that well. 
In this guide, you will find a summarized set of ways of working that I have learnt over the last 15 years. Keep in mind that this is based on my personal experience, so in your particular case or organization, some of them may not make sense.

# This is the way

#### Be your most demanding customer

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

In a nutshell: Imagine what your customer would want and your life will be easier.

#### Data driven beats guess-driven

As an architect, I come up with ideas about how to improve my services all the time. But just because I think they are good ideas, does not mean they really are. You should encourage your team to come up with ideas, but to take a decision these ideas have to be backed up with real data:

- Is your idea improving the critical path / bottleneck? (Throughput)
- Is your idea solving a relevant use case or is an edge case? (Focus)
- How much % of customers will benefit from the time invested to implement it? (Impact of change)
- How much money will we spend to implement it and how much money will we save afterwards? (Return of investment)
- Is your idea solving edge case but this case could be catastrophic for the company? (Risk vs Reward)

Gathering metrics about your software in an automated way is as important as releasing features. Make sure your stakeholders understand this too.

In a nutshell: It's easier to take decisions technically and politically when you have the data to back it up. Make sure you invest in the architecture and the tools to enable this.
