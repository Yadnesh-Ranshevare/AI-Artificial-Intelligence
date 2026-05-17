# Content
1. [Introduction](#introduction)
2. [t-test](#t-test)
3. [z-test](#z-test)
4. [ANOVA](#anova---analysis-of-variance)
5. [Comparison of t-Test, z-Test, and ANOVA](#comparison-of-t-test-z-test-and-anova)


---
# Introduction
Hypothesis testing is a statistical method used to make decisions or draw conclusions about a population based on sample data.

At its core, it helps answer questions like: “Is this effect real, or could it just be due to chance?”

### Key Ideas
1. **Hypothesis**
    - A statement or assumption about a population.
    - Two types:
        - Null hypothesis (H₀): Assumes no effect or no difference.
        - Alternative hypothesis (H₁ or Hₐ): Assumes there is an effect or difference.
2. **Test Statistic**
    - A value calculated from sample data (like a z-score or t-score) used to evaluate the hypothesis.
3. **Significance Level (α)**
    - A threshold (commonly 0.05) that determines how strong the evidence must be to reject H₀.
4. **P-value**
    - The probability of observing the data (or something more extreme) if the null hypothesis is true.

### How It Works (Step-by-Step)
1. State the null and alternative hypotheses
2. Choose a significance level (α)
3. Collect and analyze sample data
4. Calculate the test statistic and p-value
5. Make a decision:
    - If p-value ≤ α → reject H₀
    - If p-value > α → fail to reject H₀


[Go To Top](#content)

---
# t-test
A t-test is used to check whether the difference between means is statistically significant or just random variation.

You use a t-test when:

- Your sample size is small (typically < 30)
- Population standard deviation is unknown
- You’re comparing averages

### Intuition
A t-test basically asks:

> “Is the difference large enough compared to the randomness/noise in the data?”

If:

- Difference is large
- Variation is small

→ t-value becomes large\
→ stronger evidence against H₀

### Types of t-tests
| Type               | Use Case                                  |
| ------------------ | ----------------------------------------- |
| One-sample t-test  | Compare sample mean with a known value    |
| Independent t-test | Compare means of two unrelated groups     |
| Paired t-test      | Compare before/after values of same group |

### Example
**Problem**\
A teacher claims students score an average of 70 marks.

You take a sample of 10 students and get:

- Sample mean = 75
- Sample standard deviation = 8
- Sample size = 10

**Question:**\
Is the teacher’s claim wrong?

#### Step 1: Define Hypotheses
**Null Hypothesis (H₀):** The teacher is correct.

$$H_o : \mu = 70$$

**Alternative Hypothesis (H₁):** The teacher is wrong.

$$H_o: \mu \neq 70$$

#### Step 2: Formula

The t-test formula is:

$$t = \frac{\bar{x} - \mu}{\frac{\sigma}{\sqrt{n}}}$$

Where:
| Symbol    | Meaning                   |
| --------- | ------------------------- |
| $\bar{x}$ | Sample mean               |
| $\mu$     | Population mean           |
| $\sigma$       | Sample standard deviation |
| $n$       | Sample size               |

#### Step 3: Put Values
Given:

- $\bar{x}$ = 75
- $\mu$ = 70
-  $\sigma$ = 8
-  $n$ = 10

Substitute:

$$t = \frac{75 - 70}{8 / \sqrt{10}}$$

#### Step 4: Calculate

$$t≈1.98$$

#### Step 5: Degrees of Freedom

Formula

$$df=n−1$$

Therefore

$$df=10−1=9$$

#### Step 6: Compare with t-table
For:

- α = 0.05
- df = 9

Critical t-value ≈ 2.262

Now compare:
| Calculated t | Critical t |
| ------------ | ---------- |
| 1.98         | 2.262      |

Since:

$$1.98<2.262$$

We fail to reject H₀.

#### Final Conclusion
There is not enough evidence to say the teacher’s claim is wrong.

The observed difference could simply be due to random sampling variation.

[Go To Top](#content)

---
# z-test
A z-test is also used to test whether a mean is significantly different, but unlike the t-test, it is used when:

- Population standard deviation (σ) is known
- Sample size is large (typically n≥30)

The logic is exactly the same as the t-test.
The only real difference is:

- t-test uses sample standard deviation s
- z-test uses population standard deviation σ

### When to Use Z-Test
| Condition                           | Z-test?         |
| ----------------------------------- | --------------- |
| Population standard deviation known | Yes             |
| Large sample size                   | Yes             |
| Small sample + unknown σ            | No → use t-test |


In real life, true population standard deviation is rarely known.
That’s why t-tests are more common.

### Example Problem

A factory claims bulbs last 1000 hours on average.

You test 36 bulbs and find:

- Sample mean = 960
- Population standard deviation = 120
- Sample size = 36

Question:

Is the company’s claim false?


#### Step 1: Hypotheses

Null Hypothesis

$$H_0​:μ=1000$$

Alternative Hypothesis

$$H_1​:μ\neq1000$$

#### Step 2: Z-Test Formula

$$z = \frac{\bar{x}-\mu}{\sigma/\sqrt{n}}$$

Where:

| Symbol    | Meaning                       |
| --------- | ----------------------------- |
| $\bar{x}$ | Sample mean                   |
| $\mu$     | Population mean               |
| $\sigma$  | Population standard deviation |
| $n$       | Sample size                   |

#### Step 3: Substitute Values

Given:

- $\bar{x}$ = 960
- $\mu$ = 1000
-  $\sigma$ = 120
-  $n$ = 36

Substitute:

$$z = \frac{960-1000}{120/\sqrt{36}}$$

#### Step 4: Solve

$$z=−2$$

#### Step 5: Compare with Critical Value
For:

- α = 0.05

Accepted Region = 1 - α = 1 - 0.05 = 0.95

- look for value close to 0.95 in z table

Critical z-values are:

$$±1.96$$

Compare:
| Calculated z | Critical z |
| ------------ | ---------- |
| -2           | ±1.96      |


Since:

$$−2<−1.96$$

We reject $H_o$

#### Final Conclusion

There is enough statistical evidence to say the bulb life is probably not 1000 hours.

The company’s claim is doubtful.




[Go To Top](#content)

---
# ANOVA - Analysis of Variance
It is used to compare the means of 3 or more groups.

ANOVA checks:\
“Are the differences between group means larger than the random variation inside groups?”

If:

- between-group variation is large
- within-group variation is small

→ groups are likely genuinely different.

### Core Logic
ANOVA compares two variances:

$$F = \frac{\text{Variance Between Groups​}}{\text{Variance Within Groups​}}$$

This is called the F-statistic.

### Interpretation
| F-value | Meaning                     |
| ------- | --------------------------- |
| Near 1  | Groups are similar          |
| Large   | Groups differ significantly |

### Interpretation
Suppose test scores are:
| Group A | Group B | Group C |
| ------- | ------- | ------- |
| 70      | 85      | 95      |
| 72      | 88      | 96      |
| 68      | 84      | 94      |

Means:

- A ≈ 70
- B ≈ 86
- C ≈ 95

Clearly different.

ANOVA checks whether these differences are statistically significant.

### Hypotheses in ANOVA
Null Hypothesis

$$H_o:\mu_1 = \mu_2 = \mu_3$$

> All group means are equal.

Alternative Hypothesis

$$H_1: \text{At least one mean is different.}$$

Important:\
ANOVA does not tell which group differs.

Only:\
“Some difference exists.”

To find which groups differ, you use:

- Tukey test
- Post-hoc analysis

after ANOVA.

### Types of Variance in ANOVA
1. **Between-group variance**

    Measures:
    - how far group means are from overall mean

    Large value suggests real differences.
2. **Within-group variance**

    Measures:

    - spread inside each group

    Represents random noise/error.

### Simple Numerical Example
Three teaching methods are tested. 

Student scores:
| Method A | Method B | Method C |
| -------- | -------- | -------- |
| 8        | 12       | 18       |
| 9        | 11       | 17       |
| 10       | 13       | 19       |

Question:\
Are the teaching methods significantly different?

#### Step 1: Define Hypotheses
Null Hypothesis

$$H_o:\mu_A = \mu_B = \mu_C$$

> All means are equal.

Alternative Hypothesis

$$H_1: \text{At least one mean is different.}$$

#### Step 2: Calculate Group Means

Method A

$$\frac{8+9+10}{3} = 9$$

Method A

$$\frac{12+11+13}{3} = 12$$

Method A

$$\frac{18+17+19}{3} = 18$$

#### Step 3: Calculate Overall Mean

$$\bar{X} = \frac{8+9+10+12+11+13+18+17+19}{9} = \frac{117}{9} = 13$$

#### Step 4: Calculate Sum of Squares Between Groups (SSB)

Formula:

$$SSB = \sum n \left( \bar{X}_i - \bar{X} \right)$$

Where:
- $n$ = 3 for each group
- $\bar{X}_i$ = group mean
- $\bar{X}$ = overall mean

For Group A

$$3(9−13)^2=3(16)=48$$

For Group B

$$3(12−13)^2=3(1)=3$$

For Group C

$$3(18−13)^2=3(25)=75$$

Total SSB

$$48+3+75=126$$

#### Step 5: Calculate Sum of Squares Within Groups (SSW)

Formula:

$$SSB = \sum \left( X_{ij} - \bar{X}_i \right)^2$$

This measures variation inside each group.
- $\bar{X}_i$ = mean of group $i$
- $X_{ij}$ = $j_{th}$ value in group $i$

Group A - Mean = 9

$$(8−9)^2=1$$

$$(9−9)^2=0$$

$$(10−9)^2=1$$

$$Total = 2$$

Group B - Mean = 12

$$(12−12^)2=0$$

$$(11−12^)2=1$$

$$(13−12^)2=1$$

$$Total = 2$$

Group A - Mean = 9

$$(18−18)^2=0$$

$$(17−18)^2=1$$

$$(19−18)^2=1$$

$$Total = 2$$

Total SSW

$$2+2+2=6$$

#### Step 6: Degrees of Freedom

Number of groups:

$$k = 3$$

Total observations:

$$n = 9$$

Between Groups DOF

$$DOF_b = k - 1 = 3 - 1 = 2$$

Within Groups DOF

$$DOF_w = n - k = 9 - 3 = 6$$

#### Step 7: Mean Squares
Mean Square Between

$$MSB = \frac{SSB}{DOF_b} = \frac{126}{2} = 63$$

Mean Square Within

$$MSW = \frac{SSW}{DOF_w} = \frac{6}{6} = 1$$

#### Step 8: Calculate F-Statistic

$$F = \frac{MSB}{MSW} = \frac{63}{1} = 63$$

#### Step 9: Compare with Critical F-Value
At 
- $\alpha$ = 0.05
- $DOF_b$ = 2
- $DOF_w$ = 6

Critical F ≈ 5.14

Compare:
| Calculated F | Critical F |
| ------------ | ---------- |
| 63           | 5.14       |

Since:

$$63>5.14$$


Reject $H_o$

#### Final Conclusion
The teaching methods are significantly different.

At least one method produces different results.

[Go To Top](#content)

---
# Comparison of t-Test, z-Test, and ANOVA

| Feature                  | t-Test                         | z-Test                             | ANOVA                                           |
| ------------------------ | ------------------------------ | ---------------------------------- | ----------------------------------------------- |
| Purpose                  | Compare means                  | Compare means                      | Compare 3+ means                                |
| Number of groups         | Usually 1 or 2                 | Usually 1 or 2                     | 3 or more                                       |
| Population SD known?     | No                             | Yes                                | Usually No                                      |
| Sample size              | Small                          | Large                              | Any                                             |
| Distribution used        | t-distribution                 | Normal distribution                | F-distribution                                  |
| Test statistic           | t                              | z                                  | F                                               |
| Uses degrees of freedom? | Yes                            | No                                 | Yes                                             |
| Main idea                | Mean difference vs uncertainty | Mean difference vs known variation | Between-group variance vs within-group variance |
| Critical value source    | t-table                        | z-table                            | F-table                                         |
| Example                  | Compare marks of 2 classes     | Compare factory mean with standard | Compare 3 teaching methods                      |



[Go To Top](#content)

---