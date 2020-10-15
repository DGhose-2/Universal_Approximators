# Universal Approximators

Can an LSTM develop the right internal representation and correct predictions for y=sin(x)? Sure.

How about for y=sin<sup>3</sup>(x)+sin(x/2)? Again, yes--but this time at a computational cost: you'll need the right activation function, a wide and deep enough network, and enough data to make hyperparameter tuning feasible.

Most deep-learning approaches are top-down: they take data of arbitrarily high real-world complexity and want to know what we can say about it. This project will adopt the opposite perspective. Let's play Devil's advocate: if our data is simulated from the simplest of simple functions--and y=sin<sup>3</sup>(x)+sin(x/2) is still really, really simple--yet our model misunderstands whole regions of behavior, can we trust that model to properly handle real-world data, with far more complicated underlying distributions?

Beginning with simple elementary functions like these, we will take the approach of testing and extending known algorithms, including LSTMs and other Turing-complete structures, implementing adaptations where necessary, in an effort to develop models which can precisely approximate the widest range of mathematical functions and behaviors up to the quite complex, with the minimum of computational burden, given sufficient data. Later we may consider whether our best models can be made relatively robust for few-shot applications (i.e., data shortage).

## Technical Introduction

To-do
(Add: Borel measurability of NN coverage, Universal Approximation Theorem, Turing-completeness)
(Goal: Maximize ratio of approximable information to computational burden, e.g. grid-searching hyperparameters is fine but will cost time, so needs to be worth it.)
(Some examples of mathematical functions we'll be looking at - less simple elementary functions, algebraic/implicit dependencies, transcendental functions found in real-world scenarios, recurrence relations, parametrized functions, solutions of differential, difference, integro-differential equations)

Why is it so important to see where LSTMs etc fail or require lots of gridsearching or heavily overparametrized models? -> This provides a new, important, and better perspective for understanding where LSTMs and other existing models break down in terms of the underlying patterns or behaviors in the data, and hence know what areas or issues we need pay closest attention to or allocate effort to rectify for future models. Ideally, these future models need to be constructed to have robust coverage of those types of behavior, which after all can and will exist in real-world data too.
