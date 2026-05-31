---
{"dg-publish":true,"permalink":"/01-atomic/unsolved/kendall-s-notation/","tags":["university/INF293","clippings"],"dg-note-properties":{"tags":["university/INF293","clippings"],"source":"https://en.wikipedia.org/wiki/Kendall's_notation"}}
---

> Source: https://en.wikipedia.org/wiki/Kendall's_notation

In [[01-atomic/unsolved/Queueing Theory\|Queueing Theory]] a discipline within the [[Mathematica\|Mathematical]] [[Probability Theory\|Probability Theory]], **Kendall's notation** is the standard system used to describe and classify a [[Queue\|Queue]] node.

It can be represented as **A/S/c** or **A/S/c/K/N/D**, where
- **A**: Times between queues ([[01-atomic/unsolved/Queueing Theory#Arrival Rate\|Queueing Theory#Arrival Rate]])
- **S**: Time of service ([[01-atomic/unsolved/Queueing Theory#Service Time\|Queueing Theory#Service Time]])
- **c**: Number of service channels open at the node  ([[01-atomic/unsolved/Queueing Theory#Queue Configuration\|Queueing Theory#Queue Configuration]])
- **K**: Capacity of the queue
- **N**: Size of the population
- **D**: [[01-atomic/unsolved/Queueing Theory#Queue Discipline\|Queueing Theory#Queue Discipline]]

Default values When the final three parameters are omitted (e.g. M/M/1), it is assumed **K = ∞**, **N = ∞**, and **D = [[First In First Out\|FIFO]].
## Parameters
### A: Arrival

Describes the [[01-atomic/unsolved/Queueing Theory#Arrival Rate\|Queueing Theory#Arrival Rate]]

| Symbol | Name                             | Description                                                                                                            | Example   |
| ------ | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | --------- |
| M      | Markovian / memoryless           | [[01-atomic/math/Poisson Probability Distribution\|Poisson]] arrival process; inter-arrival times follow an exponential distribution. | M/M/1     |
| M^X    | Batch Markov                     | Poisson process with random variable _X_ for the number of arrivals at one time.                                       | M^X/M^Y/1 |
| MAP    | Markovian arrival process        | Generalisation of the Poisson process.                                                                                 | —         |
| BMAP   | Batch Markovian arrival process  | Generalisation of MAP with multiple arrivals.                                                                          | —         |
| MMPP   | Markov modulated Poisson process | Poisson process where arrivals come in "clusters".                                                                     | —         |
| D      | Degenerate distribution          | Deterministic / fixed inter-arrival time.                                                                              | D/M/1     |
| E_k    | Erlang distribution              | Erlang distribution with _k_ as the shape parameter (sum of _k_ i.i.d. exponential r.v.s).                             | —         |
| G      | General distribution             | Arbitrary independent inter-arrival distribution (some authors use _GI_ to be explicit).                               | —         |
| PH     | Phase-type distribution          | Many of the above are special cases; often used in place of a general distribution.                                    | —         |

### S: Service

The distribution of the [[01-atomic/unsolved/Queueing Theory#Service Time\|Queueing Theory#Service Time]]

|Symbol|Name|Description|Example|
|---|---|---|---|
|M|Markovian / memoryless|Exponential service time.|M/M/1|
|M^Y|Bulk Markov|Exponential service time with random variable _Y_ for the batch size served at once.|M^X/M^Y/1|
|D|Degenerate distribution|Deterministic / fixed service time.|M/D/1|
|E_k|Erlang distribution|Erlang distribution with _k_ as the shape parameter.|—|
|G|General distribution|Arbitrary independent service time (some authors use _GI_ explicitly).|M/G/1|
|PH|Phase-type distribution|Often used in place of a general distribution.|—|
|MMPP|Markov modulated Poisson process|Exponential service times where the rate parameter is controlled by a Markov chain.|—|

### c: Number of Servers

The number of service channels (parallel servers) at the node.

- M/M/**1** → single server
- M/M/**c** → _c_ servers
### K: Capacity of Queue

The maximum number of customers allowed in the system (queue + servers combined). When this limit is reached, further arrivals are turned away.

- If omitted → capacity is **unlimited (∞)**.
### N: The Calling Population

The size of the source population from which customers originate. A small population noticeably reduces the effective arrival rate as more customers enter the system.

- If omitted → population is **unlimited (∞)**.
### D The Queue Discipline

The order in which customers waiting in the queue are served.

| Symbol      | Name                                         | Description                                                                                       |
| ----------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| FIFO / FCFS | First In First Out / First Come First Served | Customers are served in arrival order. **(Default)**                                              |
| LIFO / LCFS | Last In First Out / Last Come First Served   | Customers are served in reverse arrival order.                                                    |
| SIRO        | Service In Random Order                      | Customers are selected at random regardless of arrival order.                                     |
| PQ          | Priority Queuing                             | Options include Preemptive, Non-Preemptive, Class-Based Weighted Fair, and Weighted Fair queuing. |
| PS          | Processor Sharing                            | Server capacity is shared equally among all present customers.                                    |
