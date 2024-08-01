# Longstaff-Schwartz Simulation Algorithm

## Overview
This project implements the Longstaff-Schwartz (LSM) algorithm for valuing American options by simulation. The LSM approach utilizes least-squares regression on simulated asset price paths to estimate the continuation value of the option, making it a versatile method for various types of options, including those that are path-dependent or involve multiple factors.

## Dataset
The simulation uses synthetic data generated through geometric Brownian motion dynamics for the underlying asset prices. This method allows for the evaluation of American options under different market conditions and parameters.

## Methodology
### Theoretical Framework
The project considers a complete probability space \((\Omega, \mathcal{F}, P)\) and a finite time horizon \([0, T]\). The state space \(\Omega\) represents all possible realizations of the stochastic economy between time 0 and \(T\). The objective is to value derivatives with random cash flows that may occur during \([0, T]\).

### Optimal Exercise Time
The optimal exercise strategy for an American option is determined by comparing the immediate exercise value with the continuation value, which is the expected value of the discounted future cash flows under the risk-neutral measure.

### Least Squares Approximation
To approximate the continuation value, the project uses a linear combination of basis functions. The regression analysis is applied to the in-the-money paths to estimate the conditional expectation of the continuation value.

### Implementation
1. **Simulation of Asset Prices:** Asset prices are simulated using geometric Brownian motion.
2. **Regression Analysis:** Least-squares regression is performed on the simulated paths to estimate the continuation value.
3. **Optimal Exercise Strategy:** The optimal exercise decision is determined by comparing the immediate exercise value with the estimated continuation value.
4. **Price Calculation:** The American option price is calculated by averaging the discounted cash flows over all simulated paths.

## Results
### Numerical Example
A numerical example is provided, demonstrating the implementation of the LSM algorithm and comparing the results with those reported in Longstaff and Schwartz (2001).

### American Option Pricing
The project explores the effect of different parameters (e.g., initial stock price, volatility, maturity) on the price of American options. Results are consistent with the findings of Longstaff and Schwartz (2001).

### Geometric-Mean American Option
The methodology is extended to value geometric-mean American options. The project examines the impact of various parameters on the option price and Delta.

## Usage
### Prerequisites
- Python 3.x
- Required libraries: numpy, pandas, matplotlib, scikit-learn, jupyter

### Instructions
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/longstaff-schwartz-algorithm.git
    ```
2. Navigate to the project directory:
    ```bash
    cd longstaff-schwartz-algorithm
    ```
3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter notebook:
    ```bash
    jupyter notebook Longstaff-Schwartz_simulation_algorithm.ipynb
    ```

## Conclusion
The Longstaff-Schwartz algorithm is a powerful tool for valuing American options. This project demonstrates the implementation of the LSM approach and extends it to various types of options, providing valuable insights into the behavior of American options under different market conditions.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References
- Longstaff, F. and E. S. Schwartz (2001). Valuing American options by simulation: A simple least-squares approach. Review of Financial Studies, 14(1), 113-47.
- Other references as per the project documentation.
