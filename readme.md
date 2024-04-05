<div align="center">
    <h1>📟 SOLANA SNIPER BOT IN PYTHON 🪐</h1>
<img src="https://github.com/adharna/solana-sniper-bot/blob/main/Animation.gif?raw=true">
</div>
<p align="center">

<p align="center">
    <img src="https://img.shields.io/github/stars/snipe-it-com/solana-sniper-bot">
    <img src="https://img.shields.io/github/forks/snipe-it-com/solana-sniper-bot">
    <a href="https://discord.gg/qf9bgYUnJ5" target="_parent"><img src="https://img.shields.io/discord/1201826085655023616?color=5865F2&logo=Discord&style=flat-square"></a>
    <a href="https://colab.research.google.com/github/adharna/solana-sniper-bot/blob/main/Solana_Sniper_Bot.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
    <br>
</p>

# ✨ Quickstart

This code is written as proof of concept to demonstrate how we can buy new tokens immediately after the liquidity pool is open for trading.

Script listens to new Raydium USDC or SOL pools and buys tokens for a fixed amount in USDC/SOL.
Depending on the speed of the RPC node, the purchase usually happens before the token is available on Raydium UI for swapping.

This is provided as is, for learning purposes.

## 🛠️ Installation

💾 **Clone this repository**
```sh
git clone https://github.com/adharna/solana-sniper-bot
cd solana-sniper-bot/
```

💻 **Install dependences**
```sh
pip3 install -r requirements.txt
```

### Configuration explanation (config.ini)
```commandline
private_key     private key
is_buy          Whether to buy automatically (buy automatically (1) or not (0))
is_sell         Whether to sell automatically (sell automatically (1) or not (0))
pool_size       Buy when the capital pool is larger than
sol_amount      Buying amount (in solana)
wait_seconds    How long to sell after (in ms)
main_url        RPC URL     / I used helius for development
wss_url         RPC wss URL / I used helius for development
```

▶️ **Start CLI**
```sh
python main.py
```

# 🗨️ Q&A
### Where are my private keys?
*Your private keys are stored in `config.ini`.*
### Is there any fees when swapping using CLI?
*There are no additional fees when performing swaps via the CLI; the costs should be the same as using the Jupiter UI.*
### Does sniper bot remains running if I close the CLI?
*If you close the CLI, the sniper bot will stop running.*
### Is it possible to swap any tokens?
*You can only swap tokens that are listed on Jupiter based on their criterias.*

## Contact
[![](https://img.shields.io/discord/1201826085655023616?color=5865F2&logo=Discord&style=flat-square)](https://discord.gg/qf9bgYUnJ5)

### TODO

- Add Alt RPC (backup)
- Add JUPITER, ORCA, METEORA, FLUXBEAN liquidity pool
- Add rug check, burn and lock check
- Add profit/stop loss function
- Add ONE_TOKEN_AT_A_TIME
