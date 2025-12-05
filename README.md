# OnchainVampireSurvivors
![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/logo.png?raw=true)
## Inspiration

I used to be obsessed with a very popular game called "Vampire Survivor" which can be played on Steam. I was addicted to this game some time ago. I would play it for at least half an hour, or even several hours each time.
I searched hard on web3 and couldn't find similar games, or even fun games. Aside from Dark Forest, most of the web3 games I've seen are boring airdrops or hype (or maybe I just don't find interesting games). However, if my guess is correct, this will lead to people only making money through web3 games and then maybe reopening steam after get off work.
I think only interesting web3 games are likely to be widely used, while games that rely solely on token airdrop or "play to earn" models will be difficult to maintain.

## What it does
OnchainVampireSurvivors is a time survival game with minimal gameplay and roguelite elements. It uses **Push SDK** (Push Chain) technology to allow players to use various methods, such as commonly used social accounts (Google, Apple, Facebook), email, mobile phone number, passkey and more than 350 web3 wallets through Universal Account (UEA) integration.
The game uses a unique algorithm mechanism to optimize the game value, so that players can immerse themselves in a state of continuous tension and excitement. I created a specific algorithm in the smart contract and created an on-chain ranking list, which is very likely to reduce gas consumption without affecting the sorting efficiency. At the same time, I also simply implemented a unique lottery mechanism for players to draw cards.

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/2.png?raw=true)

Using the introduction of the original Vampire Survivors game to explain the game values ​​of OnchainVampireSurvivors: Monsters are everywhere, and you are nowhere to escape. All you can do is survive as long as possible until death inevitably ends your struggle. Collect gold in each run to buy upgrades and help the next survivor.

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/7.png?raw=true)

[Click to play OnchainVampireSurvivors](https://catkevin.github.io/OnchainVampireSurvivors/)

Tips: Please use chrome browser to open.


## How to play it

### 1、Loading Scene
- Wait for the progress bar to end, select the wallet you want to interact with or log in with your social account, and then start the game
  
![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/1.png?raw=true)

### 2、Home Scene
- On the homepage, you can see various game data, such as the number of gold coins and diamonds, network icon, wallet address, etc., as well as game characters and weapons, and of course the scrolling background and LOGO I drew specifically for PUSH Testnet.
- The five buttons on the right have different functions: Home, Weapons, Characters, Lottery, and Onchain Rankings.
- Click the Start Game button, you need to pay 0.01 PUSH for the gas token, then wait for a moment and enter the game after the transaction is completed.
- When you start the game, you need to pay 0.01 PUSH as the ticket fee to participate in the game, and this fee will be directly distributed to outstanding players in the current ranking as a game incentive. (If you can maintain a high ranking, it means you can earn a huge amount of PUSH tokens)

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/2.png?raw=true)

#### 2.1 Weapon Page
- Players can select, purchase and upgrade weapons on this page.
- You can get gold coins by purchasing, drawing prizes and participating in games.
- You can only get diamonds and get cooler and more advanced weapons through lottery. (lottery is one of the easiest ways to get high-level weapons)

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/3.png?raw=true)

#### 2.2 Characters/Skins Page

- Players can purchase and upgrade game characters on this page. 
- I have drawn many characters of this type, but due to time constraints, I only show four characters here.

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/4.png?raw=true)

#### 2.3 Lottery Page

- Players need to pay 0.04 PUSH to participate in the lottery, and can draw gold coins, diamonds and advanced weapons.
- A VRF random extraction function is implemented to ensure the fairness and randomness of the lottery.
- If you want to experience the Howitzer and Gatling as soon as possible, please come and participate in our lucky draw!

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/5.png?raw=true)

#### 2.4 Onchain ranking page
- Here you can see the player ranking data, and you can see kills and time of each item.
- At the bottom you can view the update time of the current chain's ranking.
- This ranking list can be scrolled up and down, and currently stores the top ten data of rankings.

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/6.png?raw=true)

### 3、Game Scene
- After entering the game, players can use the "W", "S", "A" and "D" keys on the computer keyboard to control the character's movement up, down, left and right.（You can see this keyboard button in the lower right corner of the page）
- By controlling the player to avoid monsters, use weapons to kill monsters, then extract experience points, and obtain more interesting skills through upgrades.

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/7.png?raw=true)

- You can click on the avatar in the upper left corner to view the attributes of the current character.
- The top of the screen shows the character's level and skills.
- There is a bombing button and a magnet button on the right, which can bomb monsters and absorb experience points globally respectively. But it can only be used once per game!
- The rest is up to you to experience! I designed a very interesting algorithm to control the generation of monsters, so that players are always in a state of tension and immersed in the game.
- This is why I developed the game! I hope the game can bring happiness to everyone, not boring airdrops.
  
![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/10.png?raw=true)

- On the game settlement page, you need to click the Submit button to spread this valuable game data to PUSH Testnet, so that players around the world can see your outstanding performance!!

![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/9.png?raw=true)



## Technical Architecture

### Project Structure
```
OnchainVampireSurvivors/
├── gaming/              # Cocos Creator game project
│   ├── assets/          # Game assets, scripts, scenes
│   └── scripts/         # TypeScript game logic
├── web3-api/            # React bridge for Web3 integration
│   └── src/
│       └── App.tsx      # Push SDK integration layer
├── contracts/            # Hardhat smart contract project
│   └── contracts/
│       └── Contract.sol # ZKGameClient.sol
├── docs/                 # Built/deployed game version
└── images/               # Project screenshots and assets
```

### Technology Stack
- **Game Engine**: Cocos Creator (TypeScript)
- **Web3 Bridge**: React + TypeScript + Vite
- **Blockchain SDK**: Push SDK (`@pushchain/ui-kit`, `@pushchain/core`)
- **Smart Contracts**: Solidity ^0.8.22, Hardhat
- **Blockchain**: Push Chain Testnet
- **Contract Interaction**: ethers.js v6
- **Network**: PUSH Testnet (RPC: `https://evm.rpc-testnet-donut-node1.push.org/`)

### Integration Flow
```
Cocos Game (TypeScript)
    ↓
Web3Mgr (calls window functions)
    ↓
React App (App.tsx) - exposes Push SDK
    ↓
Push Chain Smart Contract
```

## How we built it
I completed this project during this days. The time was very tight and the workload was huge because it involved game planning, art, gameplay mechanisms and algorithms, as well as smart contracts and interaction logic with the PUSH Testnet.

### 1、logo
I use Photoshop to draw the game logo and most of the game assets
![Alt text](https://github.com/CatKevin/OnchainVampireSurvivors/blob/main/images/logo.png?raw=true)

### 2、Gaming (Cocos Creator)
I used Photoshop to draw most of the game UI and assets. I used **Cocos Creator** as the game engine, implemented various game mechanisms and algorithms, and completed the complete game logic. The game includes:

**Game Systems:**
- **Survival Mechanics**: WASD movement, monster avoidance, weapon combat
- **Progression System**: Experience points, leveling, skill upgrades
- **Weapon System**: Multiple weapon types with upgrade levels
- **Character System**: Character skins with stat upgrades
- **Monster AI**: Dynamic spawning algorithm for constant tension
- **Audio System**: Background music and sound effects
- **UI System**: Multiple pages (Home, Game, Rankings, Lottery, etc.)

**Manager Classes:**
- `CocosZ`: Main game controller
- `GameMgr`: Game state and logic management
- `Web3Mgr`: Web3 data management
- `UIMgr`: UI page management
- `ResMgr`: Resource loading and caching
- `AudioMgr`: Audio playback management
- `DataMgr`: Local data persistence

It took a lot of time to realize a complete game. I think most of the time was spent on designing game art and implementing game logic.

### 3、Push SDK & Web3 API Bridge
I use **Push SDK** (`@pushchain/ui-kit` and `@pushchain/core`) to greatly reduce the entry threshold for web2 players. Players may not need to create their own wallets, they only need their own social accounts (such as email etc.) to enter the game through Universal Account (UEA). Of course, it also supports the use of most wallets such as MetaMask to enter the game.

**Web3 API Bridge Architecture:**
Due to the limitations of the Cocos Creator game engine, I created a React-based Web3 API bridge (`web3-api/`) that exposes Push SDK functions to the game engine. This bridge:
- Handles wallet connection via Push Universal Account
- Provides read functions: leaderboard, player assets, weapons, skins, lottery results
- Provides write functions: start game, submit results, buy/upgrade items, lottery, mint gold
- Exposes all functions on the `window` object for the Cocos game to call
- Uses ethers.js for contract interactions

### 4、Hardhat and Smart Contract
I used **Hardhat** to write the game's smart contract (`ZKGameClient.sol`), which was designed to store various game data, including player assets (gold, diamonds), weapons, character skins, game logs, etc., to ensure the transparency and security of player data.

**Smart Contract Features:**
- **Asset Management**: Player gold, diamonds, weapons, and skins with upgrade levels
- **On-Chain Leaderboard**: Top 10 rankings using binary search algorithm for gas-efficient sorting
- **Cross-Chain Support**: Tracks players from different chains using UEAFactory integration
- **Lottery System**: VRF-based random extraction for fair rewards (gold, diamonds, weapons)
- **Reward Distribution**: Entry fees (0.01 PUSH) distributed to top-ranked players
- **Game Logging**: Complete game session tracking with timestamps and statistics

The smart contract was deployed to **PUSH Testnet** at address: `0x72d23067fFFB6C7eE6b2416e2bAFb3a0c8CB27e0`

### 5、Important!!
I used the Push SDK and the UEAFactory smart contract to implement a full-chain game leaderboard. This was previously unimaginable! Previously, player scores could only be ranked on a single chain!！！！

## Challenges we ran into
1. **Game Engine Limitations**: Due to the limitations of Cocos Creator game engine, I couldn't directly use Push SDK or Web3 SDK. I spent about a week thinking about this problem and eventually created a React-based bridge project (`web3-api/`) that exposes all Push SDK functions to the game engine via the `window` object. This innovative solution allows the game to successfully complete various functions supported by Push SDK while maintaining the game engine's performance and compatibility.

2. **Cross-Chain Leaderboard Implementation**: Implementing a full-chain game leaderboard using UEAFactory was a significant challenge, as it required understanding how Universal Accounts work across different chains and ensuring proper chain hash tracking for players from various networks.

## Accomplishments that we're proud of
- ✅ **Complete Game Implementation**: Completed full game logic including survival mechanics, weapon systems, character progression, and upgrade systems within the time limit.
- ✅ **Immersive Gameplay**: Implemented specific algorithms to keep gamers immersed in the game, maintaining constant tension and excitement through dynamic monster spawning and difficulty scaling.
- ✅ **Smart Contract Deployment**: Successfully deployed the smart contract to PUSH Testnet with comprehensive on-chain game data management.
- ✅ **Cross-Chain Leaderboard**: Implemented a full-chain game leaderboard using Push SDK and UEAFactory smart contract - this was previously unimaginable! Players from different chains (PUSH, Ethereum, Solana, Base, Arbitrum) can compete on a unified leaderboard.
- ✅ **Innovative Architecture**: Created a React bridge solution to integrate Push SDK with Cocos Creator, enabling seamless Web3 functionality in a game engine that doesn't natively support Web3 libraries.
- ✅ **Gas Optimization**: Designed efficient algorithms for on-chain ranking (binary search) and data storage to minimize gas consumption while maintaining functionality.
- ✅ **Universal Account Integration**: Successfully integrated Push Universal Account (UEA) system, allowing players to use social logins or 350+ Web3 wallets seamlessly.

## What we learned
- **Game Development**: How to use Cocos Creator game engine to realize complex game mechanics and create engaging gameplay experiences
- **Smart Contract Development**: How to write, test, and deploy smart contracts using Hardhat, including gas optimization techniques
- **Blockchain Integration**: How to deploy smart contracts to PUSH Testnet and interact with them using ethers.js
- **Cross-Chain Technology**: Understanding of Universal Accounts (UEA) and how to implement cross-chain functionality using UEAFactory
- **Web3 Architecture**: How to bridge Web3 SDKs with game engines that don't natively support them
- **Push SDK**: Deep understanding of Push Chain SDK and Universal Account system for seamless Web2/Web3 user onboarding
- **VRF Implementation**: How to implement verifiable random functions for fair lottery systems on-chain

## What's next for OnchainVampireSurvivors
- 🎨 **Enhanced UI/UX**: Design more interesting and polished game UI with improved visual feedback
- 💰 **Improved Reward Mechanism**: Enhance the reward distribution algorithm so that more top-ranked players can be reasonably allocated rewards, increasing player engagement and competition
- 🤖 **Generative AI Integration**: Introduce generative AI technology so that players can draw or generate custom weapons and character skins, greatly increasing the randomness and fun of the game
- 🚀 **Mainnet Deployment**: Deploy the game to PUSH Mainnet for production use
- 📊 **Analytics & Metrics**: Add comprehensive analytics to track player behavior and game performance
- 🎮 **Additional Game Modes**: Expand gameplay with new modes, challenges, and seasonal events
- 🔐 **Enhanced Security**: Implement additional security measures and potentially ZK-proof verification for game results



## Thank you for reading
Thank you for your patience in reading this document. It is very long and took you a lot of time! Thank you very much!
Of course, you are welcome to try my game! Feel the joy of roguelike game!

[Click to play OnchainVampireSurvivors](https://catkevin.github.io/OnchainVampireSurvivors/)
