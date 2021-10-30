# Mercedes Method Risks Checklist

## Story Questions

1. How will the service work when we deploy the model to production?
2. What technical limitations are there for the service?
3. Which systems and teams depend on the service?
4. How will we validate the model in prod (A/B test, ...)? How should the validation work?
5. What will happen if the service stops?
6. How long does the training data stay relevant, or how often should we re-train the model?
7. How can we monitor service performance in production?

## Data Questions

1. Do we have enough training data?
2. How strong is the predictive power of the training data we have?
3. Do we have enough data to train the model?
4. Is the training data labeled already?
5. Can we purchase additional data?
6. Can we use public data?
7. How biased is the data?
8. How would the model get the data in production?
9. Are the train and production data the same?
10. How can we control the data quality in production?
11. How can we keep the data after deploying to production?
12. What legal risks may the data incur?
13. Are there any government regulations that the data is subject to?

## Method Questions

1. Which state-of-the-art (SOTA) methods are out there? What are the quality metrics?
2. How do the subject matter experts solve this problem these days?
3. Should the model be interpretable?
4. Do we need independent external model validation?

## Example Questions and Answers

Let's examine several question-and-answer examples for the product hypothesis decomposition.

**How will the service work when we deploy the model to production?**

> Do we understand how we will integrate it with the existing products? For instance, we have a user story "Interface for selecting hints". The current interface should send the model questions and get the suggested answer in return. Is there a sticky note for this integration on the chart? If not, we should add it as a Technical task.

**Should the model be interpretable?**

> If the model should be interpretable, we probablycannot use CNN and LSTM in it. So, these hypotheses must be replaced with interpretable ones.

**Do we have enough training data?**

> If there is insufficient training data, the whole decomposition becomes irrelevant. It is super-critical, and we will place it in the very center of RAT.

**How do the subject matter experts solve this problem these days?**

> Do we know how subject matter experts deal with the problem now? There may be a straightforward, effective method we could automate and use as a baseline.

**Could we use public data?**

> For some problem types, like NLP, external public data might be incredibly beneficial and would significantly improve your results. Are we aware of such datasets? How can we get and use them? If applicable, add these questions to the chart.
