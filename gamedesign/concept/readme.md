
[Plan](plan.md)

# Game description

Game about building and launching rockets with robots, to explore space.

Mostly PVE with cooperation gameplay.

Player visit places on Earth and build structures. Then he connect structures together to convert raw resources to useful things.

Similar android games: Resources, Color Planet, Ingress.

[Screens](screens.md)

## Story

People discovered ancient robots on far-away stars. Robots are in hibernation state. Special signals could awake them and put to use for humanity. 

After several years of development, antenna inventions and specs were leaked by anonymous researchers. Now the are available to anyone.

## Gameplay

Player alone can't do much. Most of the game is focused around small [teams](teams.md). 

Build [Structures](structures.md), and facilities on earth to control robots in the galaxy.

[Gameplay example](gameplay-example.md)

### Endgame

#### Achievements. 

Megabase that cover whole world (connected structures).

Some achievements will require ~5 years of play.

Some achievements will require planning and commitment to get them.

Some achievement will require collaboration with other people.

Collection (list?) of stars that was surveyed.

 
[Achievements](achievements.md)

[Player specializations](player-specializations.md)



## Resources

There are only 2 raw resources in game. 

1. Knowledge - represent required information to make some action. Collect 5 random characters from street names, where streets are in 100->200m radius distance. Advanced research/buildings/actions requires more different characters, forcing player to travel more and trade.

2. Quanta - represent material, energy, etc and used to build things, power up systems. 


[Quanta](quanta.md)


Personal quanta collector collect 1 quanta. Cooldown is 1h.

Personal knowledge collector collect 5 knowledge. Cooldown is 1h.

## Rockets

[Rockets](rockets.md)


## Research

Each technology cost Knowledge and Quanta to unlock. Each lab require some knowledge and quanta per hour to operate. Each cluster on unconnected labs give +1% speed boost.

E.g. Team may have 10K labs in connected structures, and 50 labs in separate unconnected structures. Speed would be 1050 +50% = 1575

Team could research one technology at a time. If research switched, progress remains (except last hour, that is lost).

Basic resource costs are 3/3 or 10/10. Infinite research level 50 may cost 10K/100T. Level 500 may cost 50K/10E (which is impossible to get).

[Tech tree](tech-tree.md)

# Implementation notes

## Unicode

Max number of unicode characters 1,114,112

https://stackoverflow.com/questions/5924105/how-many-characters-can-be-mapped-with-unicode

https://en.wikipedia.org/wiki/List_of_Unicode_characters

https://en.wikipedia.org/wiki/Unicode

As of version 12.1, Unicode contains a repertoire of over 137,000 characters

Real number of characters from streets will be probably ~10-50K (version 2.0 or 3.0 could be enough)

Most of characters could be obtained from same location, by using multiple languages.
