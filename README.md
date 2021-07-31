# AutoFight Bot
Bot to play the CryptoBlades game on the BSC network.

The bot searches through all the weapons for each character and searches for the enemy with the best chance of winning.
If the probability is >= 92% fights and if it's >= 98% fight with all the stamina available for the character.

`31/07/21 update:` Now the bot also verifies the unclaimed xp of each character and checks if with that xp the character would raise a critical level for the rewards of battles. That is, levels 11/21/31/41/51/etc.
If this is true, the bot claims the experience.

`31/07/21 update:` Added `options.json` file. In this file you can personalize your chance values to fight, set `CLAIM_EXP: false` if you don't want the bot to claim the experience, and choose between two ways to play:
1. `OPTIMIZE_STAMINA = false`. With this option the bot will play like before. Fighting if the win chance is equal or greater than `MIN_CHANCE` and using all stamina in a single fight if the win chance is equal or greater than `PREFERRED_CHANCE`.
2. `OPTIMIZE_STAMINA = false`. The bot will ignore the `MIN_CHANCE` value and fight using all the stamina if the win chane is equal or greater than `PREFERRED_CHANCE`.

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
At the end of the execution the bot will show you how many battles you won, how many you lost, the SKILL won and the date and in how many hours you will have a character with stamina at 200.
---
> All the CryptoBlades contract runs behind proxys, so they can change the functions at any time. Breaking the bot.
> Please report any change or issue.