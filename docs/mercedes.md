# "Mercedes" Decomposition

In the Story Map chapter, we discussed planning a software product as a whole, given that ML is an integral part. This chapter covers planning ML product itself. Consider the backlog of an ML project a big product hypothesis.

## Why planning is essential

Some argue that planning research project is pointless. Sometimes new information destroys plans, and engineers become frustrated with the idea of planning.

Let us see why planning is important and discuss how to make it work in a constantly changing environment.

## Proper Risk Management

Several months to create a model may not be a big deal for a data scientist. For a business, it is. The model should undergo many stages to demonstrate its real efficiency, including integration with other products, production deployment, and even real users' evaluation.

Imagine you put significant effort into the model. Finally, you push it into production and discover that training data crucial for the model functioning is not available, making it useless.

Perhaps you even deployed the model, and its A/B test demonstrates decent results, but the compliance issues disallow its usage.

Of course, we could consider these risks in advance and have saved a lot of time.

!> A plan should highlight the risks and help manage them. 

![Essence of Planning](_images/merce-mem1.png)

!> The whole team should participate in the planning.

Often, the DS Lead is the one who does the planning. They think hard, create the plan, split it into tasks, and assign them to team members. This method is straightforward, but it loses against team planning.

Team planning improves decision quality and ensures all the participants share the same goals and understanding of methods, limitations, and risks.

## Plan Requirements

What should an ideal plan look like? Here are the criteria:

!> The plan should be incremental and iterative.

The plan must be incremental. We start with quick and straightforward ways to achieve a goal and move on to more complex ones.

There are many reasons why some teams don't do that. For example, you want to do something exciting and not fiddle with simple methods. Sometimes the customer insists on a more complex approach.

Still, starting with a straightforward method is the best practice because it:

1. Establishes a baseline for all future improvements.
2. Enables getting all the stakeholders' feedback.
3. Implements the key integrations.

These three components reveal a significant part of all the risks earlier and allow you to deal with them at a minimal cost.

!> The plan must be flexible.

It should be able to accommodate new information as it emerges.

!> The plan should focus on validation

It makes sense to start implementation with the riskiest hypothesis that can potentially kill the project.

## Mercedes Method Planning

Let's discuss the ML-planning approach we call the "Mercedes" method. It allows you to create an iterative and incremental plan that considers all the critical risks.

Mercedes method planning consists of three steps:

1. Hypotheses brainstorming
2. Proof of Concept/MVP
3. The analysis of risk checklists

Key participants:

* DS team
* Domain experts

Other stakeholders may join as necessary:

* Related teams
* Business customers

## Planning Preparation

Draw three axes, as shown in the figure below:

![Decomposition Axes](_images/merce-axis.png)

## Step 1. Hypothesis Brainstorming

Place the following sticky notes along the three axes together with your team:

* Method Hypothesis. This axis accommodates method hypotheses—from simple to complex. For instance, heuristics may go first, then linear, and finally, neural networks.
* Data Hypothesis. The next is the data hypotheses axis, starting from the data available right away, then adding new sources in ascending order of data acquisition complexity.
* User Stories stay along the vertical axes. These parts of the project are directly related to software development necessary for the final result or functionality.
* Questions. You will raise several questions in the process. For instance, it may not be clear which data is at your disposal already and which would require additional integration. Add a sticky note of a different color with that question.
* Technical Tasks also go along the vertical line. They may encompass infrastructure and architecture, for example, model to backend integration, HDFS deployment, model launching infrastructure.

Here is how your result may appear:

![Decomposition Example](_images/merce-example.png)

## Step #2. Proof of Concept/MVP

You have generated many hypotheses in the previous step.

We remember that our top priority is the fastest product hypotheses validation. We need to decide what has the highest priority and what does not.

To do that visually, let's add two concentric circles and split the chart into three areas, as the figure shows:

* RAT (Riskiest Assumption Test). The riskiest hypothesis we can validate and kill the product before deploying it into production.
* MVP (Minimum Viable Product). Minimal product, which we can validate with a portion (segment) of end-users.
* SCALE. Additional improvements we can postpone to later stages.

Discuss and redistribute your hypotheses between these three categories. Do your best to minimize RAT and MVP. The closer the hypothesis is to the center, the higher its priority.

![Areas](_images/merce-circles.png)

## Step #3. The Analysis of Risk Checklists

Risk management means we identify and mitigate risks we would have to deal with later, at the early stages of the project. To help data teams, the LeanDS community collected a set of typical questions to identify these risks.

Examine the list with your team and try to answer each one using the following options:

* You have an answer. Skip it.
* The question is irrelevant. Skip it
* The question is relevant, and the answer is not clear. Place a sticky note on it.

![Usage of Questions](_images/merce-example2.png)

## Mercedes Method Benefits

* The team, stakeholders, and subject matter experts plan together and share their project vision and faith in success.
* The team generates good ideas dealing with arising problems because everyone understands them and their effect.
* The team has a risks list. By working through it early enough, it can avoid or at least alleviate most of the damage.
* RAT/MVP enforces the fast validation of critical and the riskiest hypotheses.
* The plan decomposition allows you the work in parallel and speeds up the project.

## Mercedes Approach Hints

* The session results in a set of hypotheses titles. One needs to formalize them into hypotheses in the form of "We believe..." and place them into the product backlog.
* Add risks to the backlog if they require team involvement.
* As you progress through the project, go back and update the plan regularly.
* The Mercedes session takes about one hour. Its review is usually quicker.

?> This book is the first written statement of Mercedes's approach for ML projects decomposition in the history of humankind.
