# AutoFight Bot
Bot to play the CryptoBlades game on the BSC network.

The bot searches through all the weapons for each character and searches for the enemy with the best chance of winning.
If the probability is >= 92% fights and if it's >= 98% fight with all the stamina available for the character.

## How to use it
#### Clone this repo
```
git clone https://github.com/BatCoderDefi/cryptoblades-autofight.git
```
#### Install dependencies
```
npm install
```
#### Configure your user file
You will need a file `userSettings.json` with the next structure:
```
{
    "accounts": [
        "account1",
        "account2"
    ],
    "privateKeys": [
       "privateKet1",
       "privateKey2"
    ]
}
```
You can add many accounts as you want.
#### Run it
```
node cryptoBladesAutoFight.js
```