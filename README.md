# algo-statistics-bachelors-thesis

[Open the notebook](./src/statistic-in-trading.ipynb)

## Final Conclusion

This notebook explores foundational principles of **probability, randomness, and adaptive behavior** in trading through a series of stylized simulations. Each section incrementally builds intuition for why modeling and adaptability are central to robust trading strategies.

### Key Takeaways:

1. Stationary Games Reveal Baseline Behavior:
- In the Zero-Edge Game, both **time averages** and **ensemble averages** converge toward zero, reflecting no edge in the system.
- This simulates an efficient market with **no predictive advantage**—a model of pure randomness.

2. Adaptive Strategies Learn from the Past, but Lag Behind:
- When win probabilities drift over time (non-stationary environment), fixed strategies fail.
- Adaptive models (estimating win probability using historical windows) can exploit short-lived patterns, but:
	- They're always playing **catch-up**.
	- Their effectiveness depends heavily on **window size** (i.e., memory length).
	- Short windows are reactive but noisy; long windows are smoother but slow to adapt.

3. Not All "Positive Signals" Are Good Trades:
- Even when an adaptive strategy **estimates** high probability of success, if the underlying market is turning, it can still lose.
- The notebook visualizations clearly show instances where **the estimation deviates from reality**, leading to poor trades.

### Interpretation – For Trading Psychology / Systematic Research

- **Recency bias** and **overconfidence** are common trader behaviors. The adaptive models here mirror this, showing how traders overweight recent outcomes when making decisions.
- **Behavioral traps**: Traders with shorter memory windows tend to overreact to randomness, while long-term models may miss opportunities.
- The **importance of feedback**: By visualizing returns and estimation accuracy together, we can simulate how a trader learns and reacts (or misreacts).
- **Risk of confirmation**: When models "think" they're right (e.g., high estimated probability), but the reality doesn't match, it reflects real-world miscalibration—a central issue in systematic and discretionary trading alike.
- **Mix Models**, because in some period of time model X can be better than Y but after the market condions change, the model Y can make better outcomes. 

### Academic Notes & Conceptual Connections

- **Ergodicity**: Stationary game results highlight ergodic behavior—long-term time averages equal ensemble averages. Non-stationary games break this symmetry.
- **Bayesian Updating (implicitly)**: Adaptive estimation mimics a crude form of Bayesian belief update—using past wins/losses as data.
- **Lag vs. Noise tradeoff**: Classical signal processing dilemma, applied to trading: fast = responsive but noisy; slow = stable but delayed.
- **Model Risk**: We clearly observe the risk of using poorly aligned models—strategies can fail simply because the assumptions are no longer valid.
- **All models are wrong**: This notebook reflects that spirit—models are approximations. The key is whether they're useful in specific time of period.