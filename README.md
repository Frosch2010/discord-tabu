# discord-taboo

Taboo about playing Discord?
This is now possible with this Python Discord bot.

Define own terms or let the server users add their own terms. Everything is possible. Easy to understand and simple to implement.

<img src="https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/explainer_react.png" height="250" width="383">

## Features

* Players can add terms without the admin -> Create your own version:

    ![alt text](https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/ADD-Terms.png?raw=true)

* Automatic check whether a term already exists. If so, the forbidden words are added to the term, if they do not exist. Later the bot will randomly select 5 out of them when the term comes.
* Used terms can be saved. -> Guarantees that a term will not come back until all others have been used.
* After the win: Graph for the score development

    <img src="https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/win_graph.png" height="337" width="465">

* Completely freely configurable
* Pause the game between a team change:
    
    <img src="https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/Waiting.png" height="91" width="353">
    <img src="https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/PauseGame.png" height="91" width="353">

## Other Screenshots

**Start game...**

![alt text](https://github.com/Frosch2010/discord-taboo/blob/main/Screenshots/start_message.png?raw=true)

## Installation

**What is needed?**
* Python 3.X
* Discord-Server

**Which Python packages are needed?**
* discord 1.5.X
* matplotlib

**Everything available?**
1. Download all files
2. Set up the bot (settings-file)
3. Add your own terms (terms-file)
4. **And your are ready to play with your friends.**

## Commands


The following commands are only for the following channels.

**Join Channel:**
```
!tabu join                          - Join taboo
!tabu start [points to win]         - Start taboo [A score other than the default to win can be specified]
```

**Team-1 & Team-2 Channel:**
```
!tabu stop                          - Stops the game before a team has won
!tabu pause                         - Pause the game when changing teams
!tabu unpause                       - Unpause the game when changing teams
```

**Bot-Admin Channel:**
```
!tabu load cards                    - Loads all terms from the Add-Terms Channel (Shutdown the bot once to save it)
!tabu shutdown                      - Shutdown the bot and saves depending on the settings
!tabu shutdown without save         - Shutdown the bot and without saving
!tabu shutdown with save            - Shutdown the bot and with saving
```

## Settings-file

```
Join Channel-ID       = Through this channel players can join taboo.
Team-1 Channel-ID     = Channel for team 1.
Team-2 Channel-ID     = Channel for team 2.
Add-Terms Channel-ID  = This channel allows players to add cards on their own. 
                        Scheme: "Term:forbidden word,forbidden word,..."
                        When the bot is online, the terms are automatically added to the game.
                        Otherwise they have to be reloaded with the Load command.
Out-Terms Channel-ID  = Comes in the future. Please specify the same channel as Add-Terms.
Bot-Admin Channel-ID  = Channel for the Bot-Admin commands, like shutdown.

Bot-Token             = Your Bot-Token
Default-Save-Terms    = Should the current state of the term pool etc. be saved when the bot is shut down without further arguments.

Default-Points-To-Win = Points to win
Round-Lenght          = How long a team gets time to explain until it is the turn of the other team. (Seconds)
Switching-Lenght      = Time waited between team changes (Seconds)
Min-Players           = Minimum number of players for the start
```

## Wishes, Issues, Help needed?
Make a pull request. :)


## License
All code is under the [MIT](https://choosealicense.com/licenses/mit/) license.
