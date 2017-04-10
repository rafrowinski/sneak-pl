# SneakPL

## This script is made to:


- give guards a simple AI,
- give guards a line of sight,
- enable them to follow you,
- enable them to look for you
 


## In this script you can:


- hide behind obstacles to avoid detection
- hide inside objects to avoid detection (like the vase)
- kill and carry guards (lowers speed)
- attract guards attention by putting a corpse somewhere on their way


## Keys:

```
W - hide (face the vase)
S - go out of your hideout
D - back stub the guard
Q - pickup corpse
A - drop corpse
```

## How to use:


1. Download and unzip SneakPL archive,


2. Copy all three scripts

```
SneakPL
PathFinder
Event_window
```

3. Copy the guard wherever you like and set his move route.


you are good to go


## A brief explanation:


This is a script that lets the guards act much like those in Metal Gear Solid. They have a certain line of sight but can't see through obstacles. The rule here is simple. The line of sight is a tree of tiles that is being checked depth first (starts in rootNode variable uses Node class) https://en.wikipedia.org/wiki/Tree_(data_structure). If one of those tiles contains an obstacle deeper nodes are not checked. In other words once behind an obstacle you can not be seen. Once detected the position of the player is clear to all guards and they will try to catch him. However you are able to flee them. When last guard looses you from the line of sight he will proceed to search for you. The algorithm takes your last seen location and direction and makes a mark 10 (appr_fields variable) fields  further in that direction. From that point the guard will choose another point within a radius of 5 (search_radius variable) and go there with hope to find you there. If not he will choose another point. This works good when there are rooms nearby. Looks quite natural. All guards will look for you for 15 seconds (alarm_time variable). After that they will go back to their starting position.


## The guards have four states

```
A - attacks
B - is being carried
C - is searching 
D - is dead
```

## Some info:


I have made this script for my friend back in 2013. The game is long dead but maybe someone will find it useful. This was my first encounter with Ruby and first script for RPG Maker ever so please be gentle :D. Anyway if anyone finds this one interesting feel free to use it and don't forget to add me and the guys below in credits. The code has commentary in polish (log too). If anyone is interested in changing it let me know. I will translate it. 

```
And for those brave and curious https://www.duolingo.com/course/pl/en/Learn-Polish-Online
```


## Requires:


- PathFinder by Karanum
- Event_Window by Yanfly


## Credits:


All credits for path finding go to Karanum.
All credits for event window go to Yanfly.