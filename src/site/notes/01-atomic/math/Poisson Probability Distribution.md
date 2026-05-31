---
{"dg-publish":true,"permalink":"/01-atomic/math/poisson-probability-distribution/","tags":["math/probability"],"dg-note-properties":{"tags":["math/probability"],"aliases":["Poisson"],"source":"https://openstax.org/books/introductory-statistics-2e/pages/4-6-poisson-distribution"}}
---

# Poisson Probability Distribution
The Poisson [[Probability Distribution\|Probability Distribution]] is an [[Discrete Probability Distribution\|Discrete Probability Distribution]] often used to model the time elapsed between [[Event\|Events]]. 

The Poisson [[Probability Distribution\|Probability Distribution]] works based on two characteristics:
- Poisson gives the [[Probability\|Probability]] of a number of [[Event\|Event]] occurring in a fixed interval of time if these events happen with a known average rate and independently of the time since the last event
- Poisson may be used to approximate the [[Binomial Probability Distribution\|Binomial Probability Distribution]] if the probability of success is "small" (such as 0.01) and the number of trials is "large" (such as 1,000).

The [[Random Variable\|Random Variable]] $X$ follows the Poisson Distribution $x \sim P(\lambda)$.
## Formulas

> [!formula] [[Probability Mass Function\|PFM]] of Poisson Distribution
> #formula $$f(x) = \frac{\lambda^{k}e^{-\lambda}}{k!}$$

## Properties

> [!formula] [[01-atomic/math/Expected Value\|Expected Value]] of Poisson Distribution
> #formula $$E[X] = \lambda$$

> [!formula] [[01-atomic/math/Variance\|Variance]] of Poisson Distribution
> #formula $$Var(X) = \lambda$$

