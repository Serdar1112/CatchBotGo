28\.06.22, 00:49 CatchBotGo

**CatchBotGo![ref1]**

![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.002.png)

Inspired by: [RealAndroidBot](https://github.com/MerlionRock/RealAndroidBot)

I started programming CatchBotGo to gain some OpenCV and botting knowledge. I did not intend to sell it, but to make it freely available (without premium features), unlike RAB. But I didn't enjoy it anymore and stopped at some point, but it's already a pretty good version.

CatchBotGo is a software that works together with [**PGSharp**](https://www.pgsharp.com/). The last version of CatchBotGo was completed around March. It's not a full version yet, it still needs work, but I don't have any more interest in it. I don't know what the current version of PGSharp looks like, so I can't guarantee that this program is still running. That's why I release the source code, everyone is allowed to read, edit and publish. It is still buggy, but many things work.

Some folders in this project are redundant, but I can't remember which ones, so I'll leave them in just to be on the safe side.

**Features![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.003.png)**

- Automatically move PGSharp's Pokemon Radar to the corner so that Pokemon can be clicked.
- Click on Pokemon.
- Read Pokemon names during the catch cycle and catch Pokemon.
- Find pokestops nearby and click on them, if further away, click randomly to walk. (buggy)
- Checks if the Pokestop is used and exits the screen.
- Transfer Pokemon after catch.

Pokestop detection works via OpenCV, which has been trained for day mode and night mode. However, this training is not enough, which is why it often fails.

**Documentation![ref2]**

This describes the functions that are in the Python files.  

**main.py![ref3]**

Everything happens here, to run, run main.py. The last time I had used it, it had worked, but that was in March.

**catchPokemon.py![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.006.png)**

- **TakeScreen()** takes a screenshot and reads it.
- **catchLow()** catches a pokemon that doesn't fly.
- **GetPokemonName()** gets the Pokemon name at start of the catch cycle.
- **DrawCVCatch()** gets if the pokemon was caught or fled.
- **ExitPokemonCaught()** exits the caught screen, if the pokemon was caught, if transferPokemon = true, then transfer Pokemon, before exiting.

**checkPhone.py![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.007.png)**

- **CheckApplicationRunning(device)** checks if the PokemonGo app is running, puts it in foreground.
- **CheckScreenSize(device)** checks the screensize and sets it to 1080x1920

**checkPokestop.py![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.008.png)**

- **SearchStops()** searchs for stops, this is sometimes working and sometimes not. Please work on this.
- **CheckStopUsed()** checks if the clicked stop is already used or not.
- **TapSomeWhereRandom()** tabs somewhere random, because it couldn't find a stop.
- **CheckIfBagIsFulll()** not implementet yet.

**findPokemon.py![ref3]**

- **CheckRadarAvailable()** checks if the PGSharp Pokemon Radar is somewhere on the screen and places it on the corner.
- **PokemonClick()** clicks on the nearby radar on the first Pokemon.
- **CheckIfEncounter()** checks if the trainer is in an encounter.

**vision.py![](Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.009.png)**

- **CheckIfMenuButton()** checks if the menu button is visible (maybe to see if he is in the wrong screen).
- **CheckIfX()** checks if "X" is visible on screen, to press it **ClickOnX()**, if he is in the wrong screen.

**Download![ref1]**

Mega.nz: [CatchBotGo](https://mega.nz/folder/MZlGHCiT#aMMwXopCCq_8k6-tjtBC3g)

**Disclaimer![ref2]**

©2016 Niantic, Inc. ©2016 Pokémon. ©1995–2016 Nintendo / Creatures Inc. / GAME FREAK inc. © 2016 Pokémon/Nintendo Pokémon and Pokémon character names are trademarks of Nintendo. Other trademarks are the property of their respective owners. [Privacy Policy](http://www.pokemon.com/us/privacy-policy/)

[CatchBotGo](https://mega.nz/folder/MZlGHCiT#aMMwXopCCq_8k6-tjtBC3g) is intended for academic purposes and should not be used to play the game *PokemonGo* as it is unfair to the community. Use the bot **at your own risk**.
https://md2pdf.netlify.app 3/3

[ref1]: Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.001.png
[ref2]: Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.004.png
[ref3]: Aspose.Words.af3186c8-160f-4450-9976-9cf03f4557c8.005.png
