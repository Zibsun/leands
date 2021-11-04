# Urgent Tasks (Expedites) and Swim Lanes

One of the clients has a problem: for some reason, the model in the production stopped showing good results. You create a new bug, and it immediately goes to Experimenting.

It's an emergency: the model doesn't work, and we're losing money. But what about the WIP restriction? The Experimenting column cannot have more than two tickets!

Indeed, we don't want to break the rules. The voluntary decision to put other tickets back to backlog doesn't seem reasonable, either.

![Expedite Swim Lane](_images/urgenttasks-expidite.png)

Instead, we create the dedicated swim lane for emergency tickets and set a new rule: the WIP constraint don't apply there.

Tickets of this type are called Expedite.

We also may have separate swim lanes for different ticket categories:

* ML products and product hypotheses
* Different stakeholders
* ... other
