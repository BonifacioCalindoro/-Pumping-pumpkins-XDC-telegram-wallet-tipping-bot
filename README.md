# XDC Telegram tip bot, wallet included

## Quick setup
- pip install py-solc-x web3 cryptography python-telegram-bot
- change 'tg-token' with your telegram bot token
- python main.py

## Description

This bot allows you to create a wallet (or import an existing one), it will encrypt the private
key with the password given by the user for security. It allows to tip XDC to telegram users by
replying to their messages with the command '/tip <amount>'. 

Every transaction requieres the user to give the password to the bot in a private chat.

Additionally, it allows to start a fundraising campaign by pre-compiling and deploying a smart contract
through the /fundraise command. 

The user should announce in any chat his ongoing campaign with the /announce command. 

Anyone can then send funds to the smart contract and withdraw in case of failure, or transfer to the beneficiary in case of a successful campaign. 

Incoming features are the ability to interact with the campaign within the telegram chat.

Command list:
+ (P: private command. G: group command. B: both)
+ B- /start: starts the bot
+ P- /newwallet: Create or import a new wallet
+ P- /mywallet: See address and balance of your wallet
+ P- /secret: See you private key after inputing your password
+ P- /withdraw: withdraw all or part of your balance to a different address
+ G- /tip: Reply to someone's group message with /tip [amount] to invoke the tipping process
+ P- /fundraise: Start the fundraise creation process, and deploy the smart contract with the argumnts given
+ G- /announce: /announce [description] to publicly announce the fundraiser through the bot

PENDING
+ - /fund: Reply to a fundraising announcement with /fund [amount] and, after inputting your pass in private, it will send the funds.

## Links
+ [Public code Repository](https://github.com/BonifacioCalindoro/EBC-XDC-Hackathon)
+ [Publicly accessible demo for the bot](https://t.me/janlibtesting2bot)
