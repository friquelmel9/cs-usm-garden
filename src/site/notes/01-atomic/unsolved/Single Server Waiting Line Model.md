---
{"dg-publish":true,"permalink":"/01-atomic/unsolved/single-server-waiting-line-model/","tags":["university/INF293"],"dg-note-properties":{"tags":["university/INF293"],"aliases":["M/M/1"],"reference":"[[03-resource/Investigación de Operaciones - Teoría de Colas\|Investigación de Operaciones - Teoría de Colas]]","source":"https://en.wikipedia.org/wiki/Queueing_theory"}}
---

> References: [[03-resource/Investigación de Operaciones - Teoría de Colas\|Investigación de Operaciones - Teoría de Colas]]
> Sources: https://en.wikipedia.org/wiki/Queueing_theory

The Single Server Waiting Line Model ( M/M/1 in [[01-atomic/unsolved/Kendall's Notation\|Kendall's Notation]]) is a model for [[01-atomic/unsolved/Queueing Theory\|Queueing Theory]]. In this model
- Is [[01-atomic/unsolved/Queueing Theory#Single Server\|Queueing Theory#Single Server]]
- The [[01-atomic/unsolved/Queueing Theory#Arrival Rate\|Queueing Theory#Arrival Rate]] follows a [[01-atomic/math/Poisson Probability Distribution\|Poisson Probability Distribution]] $(\lambda)$
- The [[01-atomic/unsolved/Queueing Theory#Service Time\|Queueing Theory#Service Time]] follows a [[01-atomic/math/Exponential Probability Distribution\|Exponential Probability Distribution]] $(\mu)$
- Must be [[01-atomic/unsolved/Queueing Theory#Stationary State\|Queueing Theory#Stationary State]], so $\lambda < \mu$

> [!formula] [[01-atomic/unsolved/Queueing Theory#Operating Characteristics\|Queueing Theory#Operating Characteristics]] for the Single Server Model
#formula $$
\begin{aligned} 
P_0 &= 1 - \rho \\ 
\quad P_n &= (1-\rho)\rho^n \\ 
\quad L_S &= \frac{\lambda}{\mu-\lambda} \\ 
\quad L_q &= \frac{\lambda^2}{\mu(\mu-\lambda)} \\ 
\quad W_S &= \frac{1}{\mu-\lambda} \\ 
\quad W_q &= \frac{L_q}{\lambda} \\ 
\quad P_W &= \frac{\lambda}{\mu} \\ 
\quad \rho &= \frac{\lambda}{\mu} 
\end{aligned}
$$
