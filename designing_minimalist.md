---
title: Designing Minimalist Interfaces For Teaching New Cognitive Tool Use
layout: default
---

# Case Study: Designing Minimalist Interfaces For Teaching New Cognitive Tool Use

Quantum Pilot is a SHMUP-puzzle about fighting clone ships that mirror how you attack them. The original game had a core mechanic but no way of teaching players beyond brutal trial & error. As the game design evovled, interfaces were tacked on to the screen. Eventually they cluttered the game to the point of confusing players & myself.

As a game designer, I am creating a new tool for cognitive use. According to "The Design of Everyday Things", tools should provide affordances -- uses obviously apparent by perceving the tool, and signifiers -- representations of functionality that are not immediately afforded to perception.

I wanted to build an entirely "minimalist" game, with no hand-holding on screen text. But without clear signifiers, players were lost. Instead of tweaking the UI to match the complexity of the gameplay I chose to redesign the game back around its fundamental loop.

This article describes major elements of the game, how communicating them hindered the user experience and how I (hopefully) have improved them. Initial feedback & increased sales suggests a success, but when it comes to teaching new cognitive tools there is always more to learn.

### Learning by Doing

The first many versions had no tutorial. Players had to learn how to move, shoot and that the clones copied their movements all at once.

I added in a zig zag line to show the player they could drag their ship, and a pulsing circle trying to say tap to fire. It didn't come across very well. The latest shows a dashed line from the player's ship to their first destination. There are no other elements on the screen. The dashed line triggers in player's memory the ideas of tracing, following, pathing, etc, and they drag their ship to the goal.

Once they reach the goal, movement is disabled and a flashing red crosshair zooms in around the newly appeared clone ship. The first designs weren't as "crosshair" looking, and most players tried to move up to the new ship. I put the flashing red crosshairs around the player ship to say "tap here" but that confused players because they wondered why they would be targeting their own ship. Freezing the player's movement, locking the crosshairs around the clone ship signify the "tap to shoot" action available to players.

With this in place, a new problem arose: Players would tap enthusiastically once they realized how to fire and then subsequent levels would feature enemies firing a constant stream of bullets -- impossible to overcome. I fixed this by only recording the *first* bullet the player shoots in this intro stage. I also remove the crosshair & re-enable player movement once the bullet is fired. 

On the next level, the clone ship immediately fires -- giving the players the opportunity to put their movement skills into practice by dodging and then their shooting skills into practice by hitting the new clone. While they dodged, a red line traces in mirror of their movements -- introducing the idea that their movements are copied by the clones.

### Communicating the Enemy

A number of players have requested some special signifier on the enemy ships to differentiate them from you. At this point I had the clones simply facing the opposite direction. Their ship color matched the color of the

### Mechanics of Conflict Resolution

Originally the game revolved around ships cloning your movement & attack from level to level. The player's weapon, which determines how bullets fire and thus how the enemy would *return fire*, was set on a 10-level repeating pattern. I had it setup like this to "show the player all the cool weapons" and provide "variance" and "strategy". It was too much. With a rapidly changing weapon, players felt like they were being punished for their advancement by having their core shooting mechanic change level to level.

### Difficulty by the Numbers

There was no limit to the number of clones that could exist and thus, no upper end of difficulty. Guranteeing player failure is dumb! I downgraded this down to 10, and later 8 clones. Completing a ninth level would replace the first clone, a tenth level would replace the second, etc.

### Compensation

Players needed a way to score points and feel accomplishment. I implemented a scoring system that rated players on Time, Accuracy and Pathing. This violated my goal of a minimalist experience and further, slowed players down by displaying & calculating score between levels.

I opted instead for single multiplier that increased as the players fired bullets & killed clones and decreased they drew a new path or took a hit. When a level was completed, the red Deadline, which functioned as the round's timer, changed to a friendlier color and zoomed towards the player. All the while their score atop the screen was racing upwards. This correlated the idea of speed with good play but is completely unobstrusive. Players who "just want to play" aren't bothered by a detailed scoring system.

### If at first..

To prevent the frustration in Defeat Me (Quantum Pilot's inspiration) of replaying the same (possibly impossible) level on losing, I sent the player back to the beginning of the game. I was happy with this until an IndieCade tester remarked "The game feels like a puzzle. I shouldn't have to replay puzzles that I've solved" and it resonated with my design instinct. 

I introduced a rolling clone system: the first time you lose on a level, you replay that level. When players lose at a challenge, their first instinct is to retry. I give players a second chance.

The second time you lose, the latest clone goes away and your level rewinds by 1. If you lose again before exceeding the furthest level you reached, 2 clones disappear, then 3, etc. If all clones disappear, the game resets. This gives players an opportunity to repattern the enemy in case they set themselves up for difficulty and introduces an element of momentum which is more satisfying than running linearly up a difficulty curve then resetting to 0.

### Conclusion

You may feel your game is complete once you've finished "the gameplay". But when players try your game and can't figure it out, it doesn't mean that they aren't thinking enough -- it means the tool you've given them, the controls of your game, are terrible. Redesigning the user interface can go a long way but a better approach is to redesign what the underlying function of the tool is and let its goal dictate its interface.

When building a game you are designing a new language that permits new form of expressions. Take the time and effort to ensure your players can learn the grammar.

### References

[>Quantum Pilot: Clone enemies remember how you killed them and fight back mirroring your attack](https://itunes.apple.com/us/app/quantum-pilot/id935956154?mt=8)

[>Defeat Me: Kenta Cho's inspirational clone-ship SHMUP](http://wonderfl.net/c/9ykQ/)

[>Design of Every Day Things](http://www.amazon.com/The-Design-Everyday-Things-Expanded/dp/0465050654)