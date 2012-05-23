Lava Furnace 
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

/lfadd <username>  <-- adds a user to the list of player furnaces monitored for custom cook times
/lfrem <username>  <-- removes a user from the list of player furnaces monitored for custom cook times
/lfset <username> <itemname or itemid> <multiplier 1 - 4>  <-- changes the specified item to the specified multiplier for the specified player
/lflist <username>  <-- lists a given players custom cook time settings.


***************************
How to build: (default config)
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
			 *  Level 2 (furnace Level)             (optional: with belt blocks off)
			 *  HHCACHH                               HHAHH
			 *   COFOC                                 OFO
			 *   COAOC                                 OAO
			 *   COOOC                                 OOO
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
Under the default config the basic requirements are to place a base of 9 Obsidian blocks for a floor, then create a U shape in obsidian with the furnace facing out in the end of the U shaped obsidian square. Next surround the U with cobblestone stairs. Then top the whole thing off with two rows of 3 obsidian each. 
Leave a 1x by 3x gap between the two rows of obsidian. Next, place a glass block directly between the two obsidian 1x3x lines you just created. It 
must be placed to the RIGHT of the furnace that is on the second level. Lastly you need to place a sign attached to the obsidian block above the 
furnace block. On it type [lavafurnace]  braces and all. If everything is done right a lightning bolt will strike the lava furnace crucible and the
sign text will turn white. 

If that happens you can now fill the crucible with lava. The glass door will move over the lava and the furnace will ignite and become ready to
smelt items.

*Note*
Contact your system admin for your lavafurnce building requirements.
Version 1.5 adds several new features, an ability to use the source chest as a fuel source and the ability to get redstone outputs from the furnace. One thing to note, the redstone output for fuel only outputs when the furnace is fueled by lava. IE a lavafurnace fuel cycle(lava in the crucible or lava in the source chest)

Version 1.47 adds lavafurnace.furnacelimit. "groupname" to permissions. This allows the admin to assign users to specific groups. These groups are then assigned a their own furnace build limits. These limits and their groups names are located in the usergroups.ini More examples are explained in the usergroups.ini file.

Version 1.45 allows admins to set up custom smeltable items for production chests. The config has an option called "custom_smeltables=" it allows any number of comma separated block id numbers to be used.
             These custom smeltables are however not able to be assigned custom cook times.
			 Also, new in the version is production chest smelt priorities. Items placed in the production chest are smelted from TOP LEFT to TOP RIGHT and from TOP to BOTTOM. So, if you place ironore in the
			 top left corner of the production chest. The furnace will grab ironore and smelt it until there is no more iron ore left. Then move on to the next smeltable from the top left, row after row until 
			 the chest is empty.

Version 1.4 allows admins to set custom per item cook times for each player. Simply use the provided command either in the in game chat or inside the server console (must be enabled in config).

(Optional)
Version 1.35 allows production chests to be placed closer to the furnace block if belt blocks are set to 0 in the config(ie. turned off)
Example above.

New in version 1.3 is the ability to customize what blocks your furnace uses for construction. Valid blocks are in 
a separate file located in the zip file this plugin came in.
Lava Furnace will use large production chests if turned on in config.
If you set a cook time faster then normal. Then you can not use alternate fuels in the furnace as still receive the enhanced cook time.
IE. If you set cook time to 4x as fast and put coal into the lava furnace. You will only get normal cook times. Remove the coal. 4x as fast cook time.
Capitalization of the permissions nodes have been removed. Please make the necessary changes. LavaFurnace should now be lavafurnace.

New in version 1.2 are the production chests. These chests are optional addons to the lavafurnace.
If a user has permission and the server has this function enabled you may place a chest to either
side of the furnace per the examples above. The Chest to the direct left of the furnace is the
supply chest. All valid ores and smeltable items can be placed into this chest. The chest to the
direct right of the furnace is the output chest. All smelted or processed items are placed inside
this chest when the furnace completes its processing.

***************************
Config File:
***************************

The config file defaults are set up for balance right now. However, if you want to change things up here is what each option means.


lava_furnace_timer=
(pretty self explanatory really, it is default set at 20000 which is nearly identical to a lavabucket being burned in a furnace)
(it accepts values from 1 to 2147483647  1 being ridiculously fast and 2147483647 being nearly 3 and a half years real time)
(The lava in the crucible will decrease as set intervals based on how much time is left on the furnace)

cook_timer=
(this accepts a value from 1 to 4)
(1 is normal cook time, 4 is 4x faster then normal)

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

allow_freeforall=
(this accepts either true or false values)
(True will disable LavaFurnace permissions checks entirely)

allow_freeforall_chests=
(this accepts either true or false values)
(True will disable LavaFurnace permissions checks for opening chests only)

allow_source_chest_fuel=
(the accepts either true or false values)
(True will allow lavafurnace to check the source chest for fuel items)

use_large_chests=
(this accepts either true or false values)
(if set to true lavafurnace will use large chest capacity)

explosion_proof=
(this accepts either true or false values)
(if set to true the furnace can not be damaged by explosions)
(Protection in a 7 block radius from the center of the furnace)

piston_protection=
{this accepts either true or false values)
(if set to true no furnace block can be pushed or pulled by a piston)

console_commands=
{this accepts either true or false values)
(if set to true admins are allowed to enter LavaFurnace commands into the server console)

sign_show_fuel_level=
(this accepts either true or false values)
(if this is set to true the lavafurnace sign will update with the percentage of lava fuel left in the crucible)

custom_smeltables=
{this accepts comma separated integer values}
(any values entered here are accepted as valid smeltable items for a furnace
regardless of if they actually can be smelted)

custom_fuel=
{this accepts comma separated integer values}
(any values entered here are accepted as valid fuel items for a furnace
regardless of if they actually are fuels)

layer_one_blocks=
(this accepts defined valid block types for the top most layer of the furnace)

layer_two_blocks=
(this accepts defined valid block types for the second layer of the furnace)

layer_three_blocks=
(this accepts defined valid block types for the bottom layer of the furnace)

belt_blocks=
(this accepts defined valid block types for the belt that runs around the middle of the furnace)

door_block=
(this accepts defined valid block types for the crucible door of the furnace)

Debug=
(a value of 1 allows users to put lava blocks into the furnace for power, permissions node is listed below)
(1 is mainly for testing or cheating your choice. 2 & 3 are for debugging info in the console. 3 for creating, 2 for deleting)
(4 is for permissions checks)
(5 is to show exceptions traps)
(6 is for detailed building debugging *requires admin build permissions)

Compatibility=
(this is a comma separated list of plugins that lavafurnace should watch out for and try to be compatible with)
(use the proper name for the plugins here, the name can be found in the plugin.yml file in their respective jar files)


***************************
Permissions
(Groupmanager *1.0(alpha-5) anjocaido, PermissionsEX 1.17 t3hk0d3, BukkitPermissions, and most Niji based permissions supported)
***************************
*note* case sensitive these must be entered EXACTLY as they are here
*note* permissions are not required, the plugin fall back to bukkit permissions if no other permissions are detected and
       server ops if no bukkit permissions are set
*note* permission checks can be turned off with allow_freeforall=true in the config

lavafurnace.*                              <- gives all admin permissions + chest access
lavafurnace.admin.*                        <- gives all admin permissions
lavafurnace.player.*                       <- gives all player permissions

lavafurnace.admin.maxforgeoverride         <- overrides the max forge limit for admin or player

lavafurnace.player.build                   <- Can build lava furnace
lavafurnace.admin.build                    <- Can build lava furnace

lavafurnace.admin.fuel                     <- can fuel any lava furnace... 
lavafurnace.player.fuel                    <- can fuel only their own lava furnace... 

lavafurnace.admin.lavablockfuel            <- can fuel any lava furnace...
lavafurnace.player.lavablockfuel           <- can fuel only their own lava furnace...

lavafurnace.admin.destroy                  <- can destroy any lava furnace...
lavafurnace.player.destroy                 <- can only destroy their own lava furnace...

lavafurnace.admin.use                      <- can use any lava furnace
lavafurnace.player.use                     <- can only use a lava furnace they create

lavafurnace.chests                         <- can place production chests limited by config

lavafurnace.admin.lfadd                    <- can add users to the custom cook time database

lavafurnace.admin.lfrem                    <- can remove users from the custom cook time database

lavafurnace.admin.lfset                    <- can change a users custom cook time settings

lavafurnace.admin.lflist                   <- can list ANY players custom cook time settings

lavafurnace.player.lflist                  <- can ONLY list their own custom cook time settings

lavafurnace.furnacelimit.groupname         <- is used to set custom build limits for "groupname" permission

***************************
Final notes:
***************************

Here are a few things to remember with the lava furnace. Depending on permissions a lava furnace can only be destroyed by
its owner. If any part of the lava furnace is broke the crucible will empty and the furnace will shut off. The sign over
the furnace will erase. 

However, there is are at least 2 instances I know of were a furnace can be destroyed without a player interaction causing it
directly. Water or lava flowing into the furnace crucible and not places.
So just be sure to keep running water/lava away from the furnace and you will be OK.

Compatibility mode for now simply stops lavafurnace from outputting a furnace burn event when a user fuels the lavafurnace. This is so plugins that like to return lavabuckets wont erroneously return a bucket when no bucket
was used.

Permissions are not required, the plugin will default over to bukkit permissions if GroupManager or niji based permissions
are not detected. If no permissions are set at all the plugin will default to Server OPs.

Never directly edit the LavaFurnace Database or player database. Bad things can happen!

If something gets messed up with any of the data files. Delete the LavaFurnace directory and Lava Furnace plugin will recreate
everything to default values.

If you don't use permissions and don't want to mess with OPS then you may disabled LavaFurnace permissions checks entirely with
the allow_freeforall option in the config. Set it to true will allow anyone to create, use, fuel, and destroy any LavaFurnace.

Production chests can be placed closer to the furnace if the belt blocks are turned off. They will also work in the default
configuration if the belt blocks are turned off. See the example construction above.

If you choose to disable the belt around the furnace then anything placed where the belt used to be will be ignored by the furnace
detection methods.

Only the blocks defined in the config constitute a valid furnace. If a furnace was created with some other block setup then
that furnace will be invalid if the blocks are changed in the config.

To edit (/lfset) a players custom cook time settings the player must have already been added to the database.
Valid cook times for lfset are 1, 2, 3, or 4. No decimal values are accepted.

Any custom smeltable will be accepted in the custom smelt option. However it is very important that if you use this option
you are sure that the item you are adding to the smelt list is actually smeltable within the game.

Keep all that in mind and you will be a happy owner of a fancy Lava Furnace!

Enjoy!




