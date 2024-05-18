#### Bayesian Inference

A method of inference where the probability of a hypothesis is updated as new evidence becomes available:

1) begin with a prior distribution process p(H) - prior 
2) collect data to obtain the observed distribution p(E) - marginal likelihood
3) calculate the likelihood - how compatible is the evidence with the hypothesis p(E|H) 
4) obtain the posterior - the probability of our hypothesis given the observed evidence  p(H|E)

Computing the posterior 
P(H|E)  =  P(E|H) * P(H)/P(E)

#### Example 

Men

|Sex  | Height |Weight|
| ------------- | ------------- | ------------- |
|0  | 67  | 140 |
|0  | 69  | 145 |
|0  | 69  | 183 |
|0  | 71  | 175 |
|0  | 66  | 108 |

Women

|Sex  | Height |Weight|
| ------------- | ------------- | ------------- |
|1  | 67  | 150 |
|1  | 67  | 100 |
|1  | 62  | 185 |
|1  | 68  | 140 |
|1  | 64  | 123 |


