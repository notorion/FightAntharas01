To reactivate ancient antharas it is necessary to rename antharas.txt for antharas.java
Game/Data/Scripts/Ai/Bosses/Antharas/

For the area site to work, you need to rename the antharas.txt file for antharas.xml
Game/Data/Instances/Bosses

To enter the old antharas you must modify the call to enter the ID NPC '34543'.
Excerpt:
<Button align = left icon = "normal" action = "bypass -h npc_%Objectid%_Quest fightantharas"> fight antharas </button>
To:
<Button align = left icon = "normal" action = "bypass -h npc_%Objectid%_Quest antharas"> fight antharas </thton>

It is not advisable to use the scripts Fightantharas and Antharas, can generate conflicts, the generation of the old antharas can happen during Fightantharas.
Take your test before you put it live.

--- FightAntharas.java ---

Fightantharas:
Antharas is summed in the middle of the scenario.
With 75% of HP the Symbol are summed, and a buff is added to antharas that recover HP to the top.
Symbols need to be destroyed to the buff will be removed from the antharas.
In 50% of the HP of Antharas, 2 clones are summed, they have the same skills as Instance's original antharas.
15% of antharas HP, Symbols reappear by adding the buff to recover HP at the top. Players need to destroy all Symbols before Life do Boss recovers completely.
Overdue antharas, all players receive a box containing a random item.

Observations:
1. Any player can leave Instance and return while Antharas is in battle. This also works if the player has a DiscoNeCTe. The player reappears in the city.
2. Instance is completed if all players leave.
3. Unconnected Player can return to Instance while the battle is happening, no party to 'reentry'.