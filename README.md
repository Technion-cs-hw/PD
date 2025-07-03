🧠 Evolution of Cooperation in the Iterated Prisoner's Dilemma

This project explores the evolution of strategies in the Iterated Prisoner’s Dilemma (IPD) using simulations in Wolfram Mathematica. It studies how different strategies perform and evolve over time depending on parameters like memory length, number of rounds per game, and population selection dynamics.


### 📂 Project Structure
```
.
├── sim.nb                         # Main Mathematica notebook with simulation and plotting code
├── results.pdf                    # PDF summary of findings and generated graphs
├── benchmarks/
│   ├── predefined/                # Simulations with predefined strategies (Axelrod's tournament)
│   │   ├── roundStatistics_10p_50p_50r.json
│   │   └── ...
│   └── random/                   # Simulations with random strategies
│       ├── converged/            # Runs that successfully converged to cooperative behavior
│       │   ├── roundStatistics_100p_200p_400r.json
│       │   └── ...
│       └── failed/               # Runs that did not converge
│           ├── roundStatistics_100p_200p_200r.json
│           └── ...
└── README.md
```



🧪 Experiments
Three main experiments were conducted:
1. Random strategies with short memory (historyLength = 2)
→ Rare convergence to cooperation with short games (numRounds = 50).
2. Random strategies with longer memory (historyLength = 4)
→ Larger memory increases the number of possible histories exponentially, making it harder for evolution to discover successful strategies.
→ Tit-for-Tat-like behavior only emerges in long games and sufficiently long evolutionary runs.
3. Predefined strategies (from Axelrod’s tournament)
→ Tit-for-Tat consistently dominates only when the number of rounds per game is large (e.g., 200+).
*The random/ folder includes both converged and failed simulation runs for comparison.

📊 Summary
- Tit-for-Tat is optimal in the long term but not in short games.
- Increasing historyLength expands the strategy space, requiring more generations to evolve effective strategies.
- Cooperation is favored in longer interactions; short games lead to more defection.
*See results.pdf for detailed findings and plots.
