# UGameInstance

parents: [UObject](UObject.md), [FExec](FExec.md)

## Description

GameInstance: high-level manager object for an instance of the running game.
Spawned at game creation and not destroyed until game instance is shut down.
Running as a standalone game, there will be one of these.
Running in PIE (play-in-editor) will generate one of these per PIE instance.
