#### Bayesian Inference

A method of inference where the probability of a hypothesis is updated as new evidence becomes available:

1) begin with a prior distribution process p(H) - prior 
2) collect data to obtain the observed distribution p(E) - marginal likelihood
3) calculate the likelihood - how compatible is the evidence with the hypothesis p(E|H) 
4) obtain the posterior - the probability of our hypothesis given the observed evidence  p(H|E)

Computing the posterior 
P(H|E)  =  P(E|H) * P(H)/P(E)

#### Example : Initial hypothesis: Probability of men/women/ have height 69

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

The priors are
p(c=M)  = 5/10 = 0.5
p(c=W) = 5/10 = 0.5

The mean for the two subsets

m_m = 68.4
m_w = 65.6

The standard deviation
sigma_m = 1.74
sigma_w = 2.24

New data comes in ... 

new_data  = 69 - likehood p(x)

p(x=69|m) = gaussian_formula  = A1 (likehood)
p(x=69|w) = gaussian_formula  = A2(likehood)

Then we can use these results to make predictions - Maximum a posteriori estimation C using Bayes rule

C_m = argmax(c in {m,w}) p (C|x)  = argmax(c in {m,w}) p(x|c)p(c)/p(x) = argmax(c in {m,w}) p(x|c)p(c)



