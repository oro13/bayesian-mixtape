blog post ideas

YOU ARE (BECOMING) AN ML EXPERT



heteroskedastic linear regression with tensorflow probability



bayesian a/b testing with tensorflow



Achieving and Demonstrating Deep Understanding of Bayesian Statistics, ML in production and Business Intelligence

network and pitch this angle and find the perfect job

write blog posts and do projects that are fun and/or demonstrate business intelligence/web development/useful for Basyn

prioritize what is worthwhile to display or has clear strategic benefits

## Find relevant materials in course lecture/assignments/notes

1. make notes for self and blog posts
2. low hanging fruit notebooks and projects
   1. assess how much material is available that would be impressive and worth effort to display

## Go through Bayesian Programming for Tensorflow Probability

1. Take extensive notes for yourself and blog posts
2. Do low hanging fruit example notebooks and 

## Go through Bayesian Data Analysis

1. assess topics I want to deep dive into
2. Take extensive notes for yourself and blog posts
3. Do low hanging fruit example notebooks and 

## Network, supplement, seek advice, put self in situations for compensated competence

1. ...? (attend webinars, watch relevant youtube videos, blogs, ask Elizabeth for pointers)
2. find an expert who does bayesian business intelligence/ml production code get their advice, ask them to review your materials
3. be aggressive and confident in the value you bring in your niche



### Logic of Science Notes

#### precourse 

pascal fermat's advice for 'fair odds' for gambling games..what math did it lead to?

- what's the correct decision to make during a gambling game, given you dont know what's gonna happen
- developed into frequentist tools

tools from measure theory (kolmogorov's contributions)

- random variable, expected value, law of large numbers, central limit theorem, markov process, random walk
- advanced - sigma algebra, filtration, brownian motion, stochastic calculus

connection of these fundamental ideas of probability with data questions in the real world

probability is a language of ideas, used all the time, in the news, 'chances are...', 'high probability of...', 'odds are against...'

conflict in ways people have understood probability, word is ambiguous

- correct legal judgments vs fair odds
- plausibility of evidence or belief vs frequency and fair odds (the major conflict in the interpretations of probablity)
  - what jaynes hopes to settle in the book

statistics

- first statisticians were measurements of the state like census

- always understood to have a measurement error

- sampling variation

- physicists, astronomy questions, had data to measure, how to combine for accurate

  - techniques developed by laplace
    - linear regression
    - theory of distribution of errors

- statistical inference

  - given we have all these measurements with some error, how do we infer the true state of being of the phenomenon
  - fisher vs pearson, 2 competing schools developed in 20th century, developed orthodox techniques
    - unbiased estimator, confidence interval, p value, type 1 and 2 error, hypothesis test
    - based on pascal and fermats early work in gambling rates
  - bayesian inference
    - how our probability estimates gets updated with new data
    - richard price in honor of bayes developed the theory

- still a tension in use of probability

  - kolmogorov's math doesnt resolve, all it tells us is how do probabilities combine and aggregate, once sample space and probability measure is defined
  - how can these be mapped onto the real world for practical understanding of proability

  - common usage of probability in language vs technical othodox
    - probability of future events for frequentists means parallel universes, but what differences between these universes lead to measured differences?
  - subjectivist view
    - probability means a degree of belief a statement is true, common usage in the language
    - tensions for uptake in 'objective' realist science applications

this helps break apart the confusion I felt starting in probability, as people fluidly jump from one to one

- kolomogorov's toolset of marginal and conditional probability favors frequentist
- vs data science applications building on bayes

to help solve this tension, jaynes considers probablity as an extension of logic

- the apparent separation between probability and statistics will dissipate 
- for situations of reasoning with incomplete information
- axioms of kolmogorov are derivable from more fundamental conditions of consistent logical reasonings
  - define the fundamental qualitative terms of logic we agree on, then derive the probability theory

- proposes to elevate bayes theorem to the same status of Aristotelean logic (his syllogism for example)
  - even bayes rule as a superset of this logic, with syllogism as a special case
  - bayes rule as the test for the statstical 'adhoccerys' and measured as how consistent they are
  - a thorough critique of standard statistics (fisher school)
    - the approach of you start with a null hypothesis (no difference in our control vs treatment)
    - stastitics asks what probabilities (frequencies) of the data due we observe, how freqeuently we expect them in a certain range
    - jaynes says no its the other way around: given we have a set of data, what probability we associate to the hypothesis that we actually care about, what we test about
      - ie, instead of hypothesis to data, we go from data to hypothesis
      - how again is this considered more subjective??? priors seem less subjective than hypothesis
    - book amounts to a demolition of the last hundred years of statistics
  - jaynes attempts a better grounding of subjectivist position
    - set of background assumptions/beliefs of probability can be incorrect, people can be deceived
  - broader understanding of probability that includes plausibility of a hypothesis, allows for sound logical statistical inference, when traditional techniques of stats breaks down
  - so much of modern science development depends on p tests, the stats could be holding it back
- 400 years of probabilty theory resolved, aristotelean logic around for thousands of years extended to new classes of problems for reasoning logically about things that couldnt be reasoned about before, a hundred years of stastics dismantled
  - ambitious book, broad range of concepts, monumentally impressive

#### ch1 Plausible Reasoning

main influence of the book

- r.t cox
  - consistency theorem
- polya

in this chapter, we consider the qualitative criteria we look for when reasoning with incomplete information, next ch will be quantitative terms

most reasoning is not deductive, we see clouds and think it may rain, we feel a pain and we go to a doctor for treatment

deductive reasoning is a strict usage similar to Aristotle's syllogism, a premise '
$$
{(P→Q)\\
{P}\\
{∴} \text{ Q}}
$$


{

if p is true then q is true, 

an observation (minor-premise) 'p is true', 

conclusion 'q is true'

}

Logically sound explanations of phenomena can't be discounted just because they're highly unlikely

deductive reasoning vs plausible inference

plausible inference could have a similar premise 


$$
{(P→Q)\\
{Q}\\
{∴}\text{ P} \text{ is more plausible}}
$$
aka if p then q, q, p is more plausible', 

personal observation:

- peirce isn't considered a bayesian, but this resonates with pragmatist notion of truth of inexhaustible lists of consequences of am organizing concept or idea, where new observations/experiences update the idea of the concept and whether or not the observed phenomena is desciribed by the concept
- e.g. hardness means you can rub a rock on it and it wont scratch it, takes a rock and rubs it on a diamond, a diamond is hard

observation: not that p is true but 'q is true', 

conclusion, p is 'more plausible'

whether evidence makes something more likely has to do with other hypotheses that may explain it better, and what prior probabilities we put on those hypotheses

in next chapter, finding
$$
P(A+B)
\\P(AB)
$$
grounds all the truth table of basic logic



#### Thought Experiment to Introduce Paradigm shift

How do we normally talk about probability (there's a  40%chance it's gonna rain)

A measure of belief

How frequentists view probability, a rate/frequency of an event occuring

this requires multiple universes to talk about forecasted events

thats absurd, but actually what classical statistics of the last 100 years and therefore most mainstream scientific studies require (think p value)

this is problematic bc if you get new information/data you have to start over, rather than update your model adaptively as new data comes in (this is why practically bayesian statistics is already being used far and wide in data science and business/operations studies, meanwhile scientific journals are beholden to p values, and arguably slow down the march of scientific progress where only 2 states can be compared all the time, and it favors the status quo heavily, and new data gets thrown out all the time because of the stastical model rather than throwing out the statistical model)

the solution is deductive logic is actually a subset of plausible reasoning/inference

instead of aristotles syllogism as the prime case of logic

a bird has wings

jerry the seagul has wings

jerry the seagul is a bird

its actually a subset of plausible reasoning, where we

a bird has wings

we see jerry the seagul has wings

we belief jerry could be a bird, theres a small chance hes something else, if we get new information that he has a beak and lays eggs, we would be more sure hes a bird

paradigm shifts in science historically happen, not super quickly, but they gain a lot of traction as new beliefs solve old outstanding problems, as is happening in physics and neuroscience with bayesian methods, and in this day in age as many scholars and academics take to other channels for their teaching and research, a paradigm shift may not be so slow as we wait for tradtional gatekeepers of knowledge to adjust policies (looking at biology and p values)

thoughts?

## Topics of Note

### Fundamental

frequentist/classical tools boil down to one framework [Alleny Downey post](https://allendowney.blogspot.com/2016/09/bayess-theorem-is-not-optional.html)



## $$P(B|A) = \frac{P(A|B)P(B)}{P(A)}$$





Moving between model and data

- "This is related to the serious scientific challenge posed at the  beginning here: if you know the underlying parameters/model, you can  figure out the distribution and the result, but often we have only the  experimental result and we're trying to figure out the most appropriate  model and parameters.

  It is Bayes' Theorem that lets us move between these." Eric Ma

distributions, their stories & shapes [1](https://docs.pymc.io/api/distributions/discrete.html) [2](http://bois.caltech.edu/dist_stories/t3b_probability_stories.html) 

tools from measure theory (kolmogorov's contributions)

- random variable, expected value, law of large numbers, central limit theorem, markov process, random walk

[ccross entropy loss](https://gombru.github.io/2018/05/23/cross_entropy_loss/)

[rmsprop mini-batch optimizer](https://www.cs.toronto.edu/~tijmen/csc321/slides/lecture_slides_lec6.pdf)

#### Project:

Simulate different distributions under different conditions

Bayesian Craps Advisor

- pascal fermat's advice for 'fair odds' for gambling games..what math did it lead to?

### Strategic

adding cost/loss functions to a bayesian posterior ('hybrid of stastistic and mechanistic model of the world' Eric Ma), useful for modeling the positive events but not so much the cost of implementing..?

Multilevel/hierarchical modeling

- https://docs.pymc.io/notebooks/multilevel_modeling.html

mixture model

shrinkage

- wild estimates being shrunk to estimation means
- modeling an underlying distribution that influences an array of dists

Bayesian T-Test

- Bayesiean Estimation Supersedes the t-test (BEST), paper by Kruschke
- freq vs bayesian
- approximating a probability to a normal dist is an approximation of an approximation (scipy 19 lecture), p is bound, normal is -inf to +inf

adjusting your prior according to prior knowledge

- baseball players have a low batting average, not a uniform beta distribution but between 1 and 4, or 1 and 40 for much narrower, 100 to 400, the larger numbers more narrow

Bootstrapping vs Bayes

- [stackoverflow article](https://stats.stackexchange.com/questions/181350/bootstrapping-vs-bayesian-bootstrapping-conceptually) 

### Advanced Topics

Bayesian Neural Net/probabilistic deep learning 

[TF Blog](blog.tensorflow.org)

[Data-Driven Dynamical Systems w/ ML](https://www.youtube.com/watch?v=Kap3TZwAsv0&list=PLMrJAkhIeNNR6DzT17-MM1GHLkuYVjhyt)

- [book](https://databookuw.com/)

Probability Theory As Extended Logic ET Jaynes

- [video series](https://www.youtube.com/watch?v=P6P1rjJuD_M&list=PL9v9IXDsJkktefQzX39wC2YG07vw7DsQ_)
- book

### Resources Digested

[Tensorflow Probability Deep Dive](https://colab.research.google.com/drive/1oXN6D6O6EG4kvBE4-ZEH018xY14vEeSt#scrollTo=BrTgat49gUoO) Viewed on 7-24 (worth revisiting)

[Bayesian Data Science: Probabilistic Programming SciPy Evan Ma](https://www.youtube.com/watch?v=2wvt6GPZl1U) Viewed on 7-25-20

 [Arun Subramaniyan](https://www.youtube.com/watch?v=ngFU7Rwl76g) Viewed on 7-25-20

- *"probability means solving problems in a fundamentally different way..encourage the practical and philosophical"* 6:55

Intro to TensorFlow Coursera Course 1 Viewed on 7-25-2020





Reach out to Jen Bricker <jen@datacamp.com> for a course proposal Bayesian Data Analysis with Python course







