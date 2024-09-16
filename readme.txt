You are free to use, modify, and publish these files as part of your custom Half-Life: Alyx addons, provided
that you credit the Fast Headcrab Restored team by linking to the Steam Workshop project page:

https://steamcommunity.com/sharedfiles/filedetails/?id=3308356996

WHAT'S NEW IN THIS PREFAB VERSION (2.0):

-Optional Half-Life 2 fast headcrab inspired texture, by khepera

-Animated fast headcrab leg texture, by khepera

INSTALLATION:

1) Merge the included animgraphs, maps, models, prefabs, soundevents, and sounds folders into your custom Half-Life: Alyx addon located at

\Steam\steamapps\common\Half-Life Alyx\content\hlvr_addons\[your_project_name]

If you would like to use the Half-Life 2 fast headcrab inspired texture, replace the default "models" folder with the "models" folder from within "HL2 Variant Material.zip"

2) In your addon resourcemanifests folder, open the resourcemanifest file and add the following to the list of manifests:

"soundevents/fast_headcrab_soundevents.vsndevts"

If you are adding to an existing list of manifests, your file should look something like this:

<!-- kv3 encoding:text:version{e21c7f3c-8a33-41c5-9977-a76d3a32aa0d} format:generic:version{7412167c-06e9-4698-aff2-e63eb59037e7} -->
{
	resourceManifest = 
	[
		[ 
			"soundevents/[your_addon]_soundevents.vsndevts",
			"soundevents/fast_headcrab_soundevents.vsndevts",
		]
	]
}

USAGE:

See the included "fast_headcrab_example.vmap" for a in-editor sample of the following:

Once installed, a .vmap prefab of the fast headcrab will appear in the Half-Life: Alyx asset browser titled "npc_headcrab_fast.vmap"
which can be dragged and dropped into your map

For basic NPC functionality, it can be spawned as a prefab:

1) Give the prefab a name from its "Object Properties" menu

2) Determine the spawn condition. For example, using an output from a logic_auto entity may look like:

My output named: OnMapSpawn
Target entities named: [Your Prefab Name]
Via this input: spawn

For advanced NPC functionality, such as use with a scripted_sequence or aiscripted_schedule, it is recommended to collapse the prefab

PREFAB LIMITATIONS AND KNOWN ISSUES

If you are knowledgeable in Source 2 and can help address any of the below issues, please reach out to the team!

1) The NPC’s navigation and collision is imperfect when compared to the completed headcrab NPCs:

○ It can visually clip through map geometry or other solid objects when near them.

○ If its attack lands its ragdoll under large physics props or into a tight space, it may get stuck in its ragdoll state (though it is freeable by the player).

○ The fast headcrab NPC lacks a powered ragdoll, and as such it does not wiggle about when in its ragdoll state.

○ In edge cases, after a successful attack, the NPC can become momentarily stuck in its standing pose, floating in front of the player’s face.

2) The fast headcrab NPC that shipped with the game files does not have associated sounds:

○ The NPC borrows the classic headcrab NPC sounds. This is consistent with the Half-Life 2 fast headcrab, which also uses the classic sounds.

○ The bite sound that plays when a player takes damage from this NPC has a necessarily makeshift implementation.
As such, in edge cases, the bite sound may trigger if the NPC nearly misses the player. Conversely, the sound may not trigger when the player is actually hit.

CREDITS:

The fast headcrab is brought to you by:

Resonλnce (Project Lead): General NPC implementation, gameplay design and balance, NPC material editing

FrostEpex: Scripting, NPC audio implementation, NPC animgraph editing

khepera: NPC texture art

chrjen: Original NPC animgraph troubleshooting

THG: Additional material resources

ambientCG: NPC color blood map was created using Leather 024 from ambientCG.com, licensed under the Creative Commons CC0 1.0 Universal License, https://ambientcg.com/a/Leather024