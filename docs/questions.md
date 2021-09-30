# Mercedes Method Risks Checklist

## Story Questions

1. How will the service work when we deploy the model to production?
2. What technical limitations are there for the service?
3. Which systems and teams depend on the service?
4. How will we validate the model in prod (A/B-test, ...)? How should the validation work?
5. What will happen if the service stops?
6. How long does the training data stay relevant, or how often should we re-train the model?
7. How can we monitor service performance in production?

## Data Questions

1. Do we have enough training data?
2. How strong is the predictive power of the training data we have?
3. Do we have enough data to train the model?
4. Is the training data labelled already?
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

1. Which state of the art (SOTA) methods are out there? What are the quality metrics?
2. How do the subject matter experts solve this problem these days?
3. Should the model be interpretable?
4. Do we need independent external model validation?
