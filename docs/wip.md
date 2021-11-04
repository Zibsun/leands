# Little's Law

Imagine being in line at Starbucks for a glass of your favorite drink (I prefer a cappuccino with coconut milk). There are ten people in the queue. About one person per minute leaves the cafe. How long before you get your drink? You'll have to wait about 10 minutes = ten people/one person per minute.

![Starbucks Queue](_images/wip-starbucks.png)

There is a law (Little's Law) in the queueing theory. It states that the average service time of an element in the system equals the element's number divided by the total system service speed.

![Little's Law](_images/wip-littleslaw.png)

In my example, you are an element of the system:

* Lead Time is the average queue waiting time.
* Work in Progress is the average number of people in the queue.
* Throughput is the average service rate: the average number of people leaving the store with a drink per minute.

Little's Law works for any mass service system. You can find yourself in a large shopping mall with coffee points, shops, and restaurants. Even so, your average time in there is the average number of people inside a mall divided by the average rate of people leaving.

Let's apply Little's Law to the Kanban tickers. To reduce the average implementation time, we must either reduce the board tickets number or increase our system's bandwidth (processing rate).

It is now clear why we need to limit the maximum tickets number on our Kanban board. This constraint is called a WIP limit (Work in Progress limit).

## How WIP Limit Works in Kanban

Above each column, we write the maximum number of tickets (WIP) that it may have:

![WIP for Kanban Board](_images/wip-kanbanwithwip.png)

Joe has finished the model. The next step is to review it before the integration. It falls into Becky's Evaluation stage. She finds the problem.

Joe is free now and can take a new fascinating job in the Experimenting column, but the WIP=2 constraint doesn't allow that. He'll have to fix the bug first, and only then can he switch to a new hypothesis.

The WIP limitation helps the team focus on finishing things by working together:

* We can't ignore blockers anymore. If there are too many, we must deal with them.
* If one of the team members is overworked, there will be queues on the board. And again, the constraint will prevent us from ignoring them.
* Anybody who finished their job will take on the highest priority next.

![Blockers](_images/wip-illustration.png)

Illustration from the cover of David Anderson's book, "Kanban: Successful Evolutionary Change for Your Technology Business"
