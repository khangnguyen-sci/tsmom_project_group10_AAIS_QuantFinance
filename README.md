Hola, this is the first brick in completion of Group 7's final project for AAIS (2026) - MSc. Quantitative Finance - University of Warsaw.

We will only focus on ETFs

# Data: 
yfinance:<br>
  for: main implementation<br>
AQR: (https://www.aqr.com/insights/datasets/time-series-momentum-factors-monthly)<br>
  for: comparing the direction, broad performance characteristics and historical behaviour of our baseline against the published TSMOM factor.<br>

# Let's set up the workspace locally:
1. Create a folder "tsmom_project" in your device
2. open terminal run the following commands in order:
   2.1. point to the project's directory
   (ex: ```bash cd /Users/augustinenguyen/tsmom_project - change to your exact directory)```
   2.2. run these commands in order:
   
```bash
mkdir -p ~/tsmom_project/{data/raw,data/processed,data/external,notebooks,src,results}
cd ~/tsmom_project
python3 -m venv .venv
source ~/tsmom_project/.venv/bin/activate
python -m ipykernel install --user --name=tsmom --display-name="Python (tsmom)"
jupyter lab
```
!(from now on, always activate the environment by ```bash source ~/tsmom_project/.venv/bin/activate``` and In the notebook, switch the kernel to "Python (tsmom)")

# Current proposed architecture:
```text
tsmom_project/
│
├── data/                  
│   ├── raw/               
│   ├── processed/         
│   └── external/          
│
├── notebooks/             
│   ├── 01_data_collection.ipynb
│   ├── 02_data_quality.ipynb
│   ├── 03_momentum_signals.ipynb
│   ├── 04_volatility_estimation.ipynb
│   ├── 05_portfolio_construction.ipynb
│   ├── 06_backtesting.ipynb
│   └── 07_performance_analysis.ipynb
│
├── src/                   
│   ├── data.py            
│   ├── signals.py         
│   ├── volatility.py      
│   ├── portfolio.py       
│   └── backtest.py       
│
├── results/               
└── README.md
```
# To be continue
