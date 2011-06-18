Lava Furnace 1.2 plugin 
		For Bukkit Minecraft server version 860.
by ArcWolf
		
***************************
Story: (because isn't it nice to have a immersing backstory?)
***************************

	It was dark... Really dark... the sounds of dripping water echoed in the distance. You curse as you fumble through your pack, trying to find a 
torch. If that stupid zombie hadn't been there you wouldn't have stumbled over the cliff edge. You strike your flint... Once... twice... Then you 
notice something. Way in the back of this dank hole something briefly catches the light. Finally, the fire springs to life at the head of the torch. 
As your eyes adjust to the light you make your way over to the ruins of an ancient furnace. Someone long ago worked here. It almost looks like this 
used to be a smiths forge. Long forgotten and slowly rotting away like the zombie you encountered moments earlier. As you look around the wreckage 
you come across a battered and warn workbench. Some half destroyed papers lay covered in dust and scattered about. But one... one piece of paper has 
drawings... Drawings of what seem to be a new type of furnace. It appears to be the furnace that is here before you. Amazing! you think. This 
furnace is far more advanced then the furnace you have been using. Just then your stomach growls, reminding you that you were headed back home 
before your zombie incident. You quickly look about and find a path back up out of the pit. With your new found treasure in your pack its only a 
matter of time before you possess a lava furnace of your own...

***************************
Commands:
***************************

There are not commands really. (well, just the sign... but we'll get to that later)

***************************
How to build:
***************************

I recommend checking out the YouTube tutorial I quickly threw together. Check it out here:

http://www.youtube.com/watch?v=RKGQ9moXv0I

But if you don't feel like it then here is a basic run down of a furnace in diagram form: Think of it as the papers you found
in the pit...

From the top down...

			 * O = Obsidian
			 * A = Air
			 * G = Glass
			 * S = Sign
			 * 
			 *  Level 1 (Sign Level)
			 *     S
			 *    OOO
			 *    GAA
			 *    OOO
			 * 		
			 * C = Cobblestone Stairs ascending toward the obsidian
			 * O = Obsidian
			 * A = Air
			 * F = Furnace
			 * H = Chest (optional)
			 * 
			 *  Level 2 (furnace Level)
			 *   HCACH
			 *   COFOC
			 *   COAOC
			 *   COOOC
			 *    CCC
			 * 
			 * 
			 * O = Obsidian
			 * 
			 *  Level 3 (base level)
			 *    OOO
			 *    OOO
			 *    OOO
			 * 
The basic requirements are to place a base of 9 Obsidian blocks for a floor, then create a U shape in obsidian with the furnace facing out in the 
end of the U shaped obsidan square. Next surround the U with cobblestone stairs. Then top the whole thing off with two rows of 3 obsidian each. 
Leave a 1x by 3x gap between the two rows of obsidian. Next, place a glass block directly between the two obsidian 1x3x lines you just created. It 
must be placed to the RIGHT of the furnace that is on the second level. Lastly you need to place a sign attached to the obsidian block above the 
furnace block. On it type [lavafurnace]  braces and all. If everything is done right a lightning bolt will strike the lava furnace crucible and the
sign text will turn white. 

If that happens you can now fill the crucible with lava. The glass door will move over the lava and the furnace will ignite and become ready to
smelt items.

(Optional)
New in version 1.2 are the production chests. These chests are optional addons to the lavafurnace.
If a user has permission and the server has this function enabled you may place a chest to either
side of the furnace per the example above. The Chest to the direct left of the furnace is the
supply chest. All valid ores and smeltable items can be placed into this chest. The chest to the
direct right of the furnace is the output chest. All smelted or processed items are placed inside
this chest when the furnace completes its processing.

*Note: Only 1 SMALL chest on each side. The furnace does not use large chests although it will 
still protect them with permissions. It will not use the extra capacity of a large chest. The magic
of the furnace does not extend far enough beyond the boundaries of the furnace. Keep that in mind.

***************************
Config File:
***************************

The config file defaults are set up for balance right now. However, if you want to change things up here is what each option means.


lava_furnace_timer=
(pretty self explanatory really, it is default set at 20000 which is nearly identical to a lavabucket being burned in a furnace)
(it accepts values from 1 to 32767  1 being ridiculously fast and 32767 being nearly 2x as long as a lava bucket burning I think)
(The lava in the crucible will decrease as set intervals based on how much time is left on the furnace)

infinite_lava=
(this accepts either true or false values)
(True means that when you first power a lava furnace it will never run out of power)
(false is recommended and the lava will run out based on the value set in the furnace timer)

max_player_furnaces=
(a value from 0 to a really REALLY big number is accepted here.)
(this value is used to determine how many lava furnaces a player may own)

allow_production_chests=
(this accepts either true or false values)
(True enables production chests)

Debug=
(a value of 1 allows users to put lava blocks into the furnace for power)
(1 is mainly for testing or cheating your choice. 2 & 3 are for debugging info in the console. 3 for creating, 2 for deleting)
(4 is for permissions checks)
(5 is to show exceptions traps)


***************************
Permissions
***************************
*note* case sensitive these must be entered EXACTLY as they are here
*note* permissions are not required, the plugin will default to OPs if no permissions are detected

LavaFurnace.admin.maxForgeOverride         <- overrides the max forge limit for admin or player

LavaFurnace.player.build                   <- Can build lava furnace
LavaFurnace.admin.build                    <- Can build lava furnace

LavaFurnace.admin.fuel                     <- can fuel any lava furnace... 
LavaFurnace.player.fuel                    <- can fuel only their own lava furnace... 

LavaFurnace.admin.destroy                  <- can destroy any lava furnace...
LavaFurnace.player.destroy                 <- can only destroy their own lava furnace...

LavaFurnace.admin.use                      <- can use any lava furnace
LavaFurnace.player.use                     <- can only use a lava furnace they create

LavaFurnace.chest                          <- can place production chests limited by config

***************************
Final notes:
***************************

Here are a few things to remember with the lava furnace. Depending on permissions a lava furnace can only be destroyed by
its owner. If any part of the lava furnace is broke the crucible will empty and the furnace will shut off. The sign over
the furnace will erase. 

However, there are at least 2 instances I know of were a furnace can be destroyed without a player interaction causing it
directly. Either a TNT explosion or a CREEPER explosion. There may be another dealing with water but I never tested that.
So just be sure to keep explosives and water away from the furnace and you will be OK. The magic is finicky like that.

Permissions are not required, the plugin will default over to Server OPs if GroupManager or niji based permissions are not detected.
Server OPs trumps permissions. So if you have both OPs and Permissions then the Server OPs are Admins in the eyes of the plugin.

Never directly edit the LavaFurnace Data base. Bad things can happen!

If something gets messed up with any of the data files. Delete the LavaFurnace directory and Lava Furnace plugin will recreate
everything to default values.

Keep all that in mind and you will be a happy owner of a fancy Lava Furnace!

Enjoy!




