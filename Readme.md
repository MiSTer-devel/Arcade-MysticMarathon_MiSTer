# [Arcade: Mystic Marathon](https://en.wikipedia.org/wiki/Mystic_Marathon) for [MiSTer](https://mister-devel.github.io/MkDocs_MiSTer/)

![Mystic Marathon Logo](doc/banner.png)

Original core developed by [darfpga](https://github.com/darfpga)

Ported to MiSTer by [birdybro](https://github.com/birdybro) and [JasonA](https://github.com/JasonA-dev)

## Description

This is a simulation model of the **Mystic Marathon** hardware. Mystic Marathon is an early Sports style game where you are a Benkin racing other Benkins across a difficult obstacle course. It was programmed by [Kristina Donofrio](https://www.arcade-history.com/index.php?page=person&name=Kristina+Donofrio) and [Ken Graham](https://www.arcade-history.com/index.php?page=person).

Original source is located in `doc/`

## Controls

![Mystic Marathon Controls](doc/controlpanel.jpg)

There is only 1 player allowed to play at a time. If you play in 2 player mode, each player takes turns.

| Name     | Description                   |
| -------- | ----------------------------- |
| Jump     | You jump                      |
| Left     | You go left                   |
| Right    | You go right                  |
| Up       | You go up                     |
| Down     | You go down                   |
| Coin     | Put in a coin                 |
| 1P Start | Start the game with 1 Player  |
| 2P Start | Start the game with 2 Players |

## OSD Options

Mystic Marathon had a peculiar system of DIPs. See the manual in `doc/` for the original source of the information.

When you press the "Advance" button in the OSD, this enables you to access the bookkeeping totals by then pressing "Auto Up" in the OSD. Currently the data in here is not saved to the MiSTer but that may come at a later time. 

If you want to change any options, then press "Auto Up" again to see the Game Adjustments menu. Here you use up and and down to move to whatever option you want to change and then use the right and left inputs to modify the desired setting. You then push "Auto up" again to set the changes.

If you press "Advance" again, it will return to it's original state (not in service mode), but "Auto Up" now will cycle through various test programs that the arcade board used to have.

High Score reset is another internal button, and it makes the game pause for a second until the high score resets.

One of the coolest features of the Williams service menu was you could customize the attract mode screen with your own letters!

## Status

The game seems to play fine, colors are closer to what the original board would have output most likely, maybe a little muted, LUT needs some slight adjustments later.

## To-Do

* Pause.
* HiScore.
* MiSTer DIP system not implemented yet (DIPS are defined away as CPU behavior currently in the PIA due to them not being a standard DIP system, not sure if this is possible for me to do at the moment)

## ROM Files Instructions

ROMs are not included! In order to use this arcade core, you will need to provide the correct ROM file yourself.

To simplify the process .mra files are provided in the releases folder, that specify the required ROMs with their checksums. The ROMs .zip filename refers to the corresponding file from the MAME project.

Please refer to [https://github.com/MiSTer-devel/Main_MiSTer/wiki/Arcade-Roms-and-MRA-files](https://github.com/MiSTer-devel/Main_MiSTer/wiki/Arcade-Roms-and-MRA-files) for information on how to setup and use the environment.

Quick reference for folders and file placement:

```
/_Arcade/<game name>.mra  
/_Arcade/cores/<game rbf>.rbf  
/_Arcade/mame/<mame rom>.zip  
/_Arcade/hbmame/<hbmame rom>.zip  
```
