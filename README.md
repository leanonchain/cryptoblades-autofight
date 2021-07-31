# AutoFight Bot
Bot to play the CryptoBlades game on the BSC network.

The bot searches through all the weapons for each character and searches for the enemy with the best chance of winning.
If the probability is >= 92% fights and if it's >= 98% fight with all the stamina available for the character.

``31/07/21 update:`` Now the bot also verifies the unclaimed xp of each character and checks if with that xp the character would raise a critical level for the rewards of battles. That is, levels 11/21/31/41/51/etc.
If this is true, the bot claims the experience.

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
---
> All the CryptoBlades contract runs behind proxys, so they can change the functions at any time. Breaking the bot.
> Please report any change or issue.