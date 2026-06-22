# WHAT THE QUESTION MEANS:
- You're at step 0 (ground)
- Need to reach step n (top)
- At each step, you can move +1 or +2 steps
- Count how many different sequences of 1s and 2s sum to n

# HOW TO THINK (STEP-BY-STEP):

**Step 1: Ask "Can I reach step i?"**

- To reach step i, your last move was either:
  - From step `i-1` (took 1 step)
  - From step `i-2` (took 2 steps)
 
**Step 2: So if I know ways to reach `i-1` and `i-2`...**

- Ways to reach `i` = Ways to reach `i-1` + Ways to reach `i-2`

**Step 3: Build from bottom**

```text
dp[0] = 1  (1 way to stay at ground - do nothing)
dp[1] = 1  (only 1 way: take 1 step)

dp[2] = dp[1] + dp[0] = 1+1 = 2  (1+1, 2)
dp[3] = dp[2] + dp[1] = 2+1 = 3  (1+1+1, 1+2, 2+1)
dp[4] = dp[3] + dp[2] = 3+2 = 5
...and so on
```
