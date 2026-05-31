---
{"dg-publish":true,"permalink":"/01-atomic/unsolved/multiple-server-waiting-line-model/","tags":["university/INF293"],"dg-note-properties":{"tags":["university/INF293"],"aliases":["M/M/k"],"reference":"[[03-resource/Investigación de Operaciones - Teoría de Colas\|Investigación de Operaciones - Teoría de Colas]]","source":["https://en.wikipedia.org/wiki/Queueing_theory"]}}
---

# Multiple Server Waiting Line Model

> References: [[03-resource/Investigación de Operaciones - Teoría de Colas\|Investigación de Operaciones - Teoría de Colas]]
> Sources: https://en.wikipedia.org/wiki/Queueing_theory

The Multiple Server Waiting Line Model ( M/M/k in [[01-atomic/unsolved/Kendall's Notation\|Kendall's Notation]]) is a model for [[01-atomic/unsolved/Queueing Theory\|Queueing Theory]]. In this model
- Is [[01-atomic/unsolved/Queueing Theory#Multiple Servers\|Queueing Theory#Multiple Servers]]
- The [[01-atomic/unsolved/Queueing Theory#Arrival Rate\|Queueing Theory#Arrival Rate]] follows a [[01-atomic/math/Poisson Probability Distribution\|Poisson Probability Distribution]] $(\lambda)$
- The [[01-atomic/unsolved/Queueing Theory#Service Time\|Queueing Theory#Service Time]] follows a [[01-atomic/math/Exponential Probability Distribution\|Exponential Probability Distribution]] $(\mu)$
- Must be [[01-atomic/unsolved/Queueing Theory#Stationary State\|Queueing Theory#Stationary State]], so $\lambda < \mu$

 > [!formula] [[01-atomic/unsolved/Queueing Theory#Operating Characteristics\|Queueing Theory#Operating Characteristics]] for the Multiple Server 
 > #formula 
 > $$ \begin{aligned} 
 P_0 &= \frac{1}{\left[\sum_{n=0}^{k-2} \frac{(\rho k)^n}{n!}\right] \frac{(\rho k)^{k-1}}{(k-1)!(1-\rho)}}, \\
P_n &= \frac{(\rho k)^n}{n!} P_0 \ (n \leq k), \\
P_n &= \frac{\rho^n k^k}{k!} P_0 \ (n > k), \\
L_q &= \frac{\rho^{k+1} k^{k-1}}{(k-1)!(1-\rho)^2} P_0, \\
L_S &= L_q + \rho k, \\
W_q &= \frac{L_q}{\lambda}, \\
W_S &= W_q + \frac{1}{\mu} = \frac{L_s}{\lambda}, \\
P_W &= \frac{1}{k!} \left(\frac{\lambda}{\mu}\right)^k \left(\frac{k\mu}{k\mu - \lambda}\right) P_0, \\
\rho &= \frac{\lambda}{k\mu}
\end{aligned}$$
