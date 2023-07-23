# Comparing `tmp/pmdsky_debug_py-7.0.4-py3-none-any.whl.zip` & `tmp/pmdsky_debug_py-7.0.5-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,16 +1,16 @@
-Zip file size: 864219 bytes, number of entries: 14
--rw-r--r--  2.0 unx     1831 b- defN 23-Jul-16 04:27 pmdsky_debug_py/__init__.py
--rw-r--r--  2.0 unx       30 b- defN 23-Jul-16 04:27 pmdsky_debug_py/_release.py
--rw-r--r--  2.0 unx   741315 b- defN 23-Jul-16 04:27 pmdsky_debug_py/eu.py
--rw-r--r--  2.0 unx   707741 b- defN 23-Jul-16 04:27 pmdsky_debug_py/eu_itcm.py
--rw-r--r--  2.0 unx   728791 b- defN 23-Jul-16 04:27 pmdsky_debug_py/jp.py
--rw-r--r--  2.0 unx   707741 b- defN 23-Jul-16 04:27 pmdsky_debug_py/jp_itcm.py
--rw-r--r--  2.0 unx   748733 b- defN 23-Jul-16 04:27 pmdsky_debug_py/na.py
--rw-r--r--  2.0 unx   707752 b- defN 23-Jul-16 04:27 pmdsky_debug_py/na_itcm.py
--rw-r--r--  2.0 unx   250307 b- defN 23-Jul-16 04:27 pmdsky_debug_py/protocol.py
--rw-r--r--  2.0 unx        0 b- defN 23-Jul-16 04:27 pmdsky_debug_py/py.typed
--rw-r--r--  2.0 unx     1320 b- defN 23-Jul-16 04:27 pmdsky_debug_py-7.0.4.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-16 04:27 pmdsky_debug_py-7.0.4.dist-info/WHEEL
--rw-r--r--  2.0 unx       16 b- defN 23-Jul-16 04:27 pmdsky_debug_py-7.0.4.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1155 b- defN 23-Jul-16 04:27 pmdsky_debug_py-7.0.4.dist-info/RECORD
-14 files, 4596824 bytes uncompressed, 862321 bytes compressed:  81.3%
+Zip file size: 881682 bytes, number of entries: 14
+-rw-r--r--  2.0 unx     1831 b- defN 23-Jul-23 04:24 pmdsky_debug_py/__init__.py
+-rw-r--r--  2.0 unx       30 b- defN 23-Jul-23 04:24 pmdsky_debug_py/_release.py
+-rw-r--r--  2.0 unx   752071 b- defN 23-Jul-23 04:24 pmdsky_debug_py/eu.py
+-rw-r--r--  2.0 unx   718165 b- defN 23-Jul-23 04:24 pmdsky_debug_py/eu_itcm.py
+-rw-r--r--  2.0 unx   739215 b- defN 23-Jul-23 04:24 pmdsky_debug_py/jp.py
+-rw-r--r--  2.0 unx   718165 b- defN 23-Jul-23 04:24 pmdsky_debug_py/jp_itcm.py
+-rw-r--r--  2.0 unx   759453 b- defN 23-Jul-23 04:24 pmdsky_debug_py/na.py
+-rw-r--r--  2.0 unx   718176 b- defN 23-Jul-23 04:24 pmdsky_debug_py/na_itcm.py
+-rw-r--r--  2.0 unx   252390 b- defN 23-Jul-23 04:24 pmdsky_debug_py/protocol.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-23 04:24 pmdsky_debug_py/py.typed
+-rw-r--r--  2.0 unx     1320 b- defN 23-Jul-23 04:24 pmdsky_debug_py-7.0.5.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 04:24 pmdsky_debug_py-7.0.5.dist-info/WHEEL
+-rw-r--r--  2.0 unx       16 b- defN 23-Jul-23 04:24 pmdsky_debug_py-7.0.5.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1155 b- defN 23-Jul-23 04:24 pmdsky_debug_py-7.0.5.dist-info/RECORD
+14 files, 4662079 bytes uncompressed, 879784 bytes compressed:  81.1%
```

## zipnote {}

```diff
@@ -24,20 +24,20 @@
 
 Filename: pmdsky_debug_py/protocol.py
 Comment: 
 
 Filename: pmdsky_debug_py/py.typed
 Comment: 
 
-Filename: pmdsky_debug_py-7.0.4.dist-info/METADATA
+Filename: pmdsky_debug_py-7.0.5.dist-info/METADATA
 Comment: 
 
-Filename: pmdsky_debug_py-7.0.4.dist-info/WHEEL
+Filename: pmdsky_debug_py-7.0.5.dist-info/WHEEL
 Comment: 
 
-Filename: pmdsky_debug_py-7.0.4.dist-info/top_level.txt
+Filename: pmdsky_debug_py-7.0.5.dist-info/top_level.txt
 Comment: 
 
-Filename: pmdsky_debug_py-7.0.4.dist-info/RECORD
+Filename: pmdsky_debug_py-7.0.5.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## pmdsky_debug_py/_release.py

```diff
@@ -1 +1 @@
-RELEASE = "v0.7.0+aa37f0ecb8"
+RELEASE = "v0.7.0+66b147366a"
```

## pmdsky_debug_py/eu.py

```diff
@@ -1829,19 +1829,21 @@
         [0x2013860],
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         [0x13890],
         [0x2013890],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         [0x138D0],
         [0x20138D0],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1864,15 +1866,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         [0x1392C],
         [0x201392C],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         [0x13974],
         [0x2013974],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2792,14 +2799,24 @@
         [0x245C0], [0x20245C0], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         [0x24688], [0x2024688], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        [0x250C8],
+        [0x20250C8],
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         [0x252A4],
         [0x20252A4],
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2974,14 +2991,25 @@
         [0x2A1DC],
         [0x202A1DC],
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        [0x2A6D8],
+        [0x202A6D8],
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         [0x2B3E0],
         [0x202B3E0],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3224,23 +3252,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         [0x49240],
         [0x2049240],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         [0x49268],
         [0x2049268],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         [0x492A0],
         [0x20492A0],
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4234,14 +4265,32 @@
     SetTeamName = Symbol(
         [0x50ECC],
         [0x2050ECC],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer",
     )
 
+    GetRankupPoints = Symbol(
+        [0x50EF0],
+        [0x2050EF0],
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        [0x50FAC],
+        [0x2050FAC],
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         [0x51248],
         [0x2051248],
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4837,20 +4886,37 @@
         [0x205332C],
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
         [0x53B18],
         [0x2053B18],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
+        [0x53BC8],
+        [0x2053BC8],
+        None,
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         [0x5414C],
         [0x205414C],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -12115,14 +12181,26 @@
         [0x2ED54],
         [0x230B8D4],
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        [0x32B64],
+        [0x230F6E4],
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         [0x32E20],
         [0x230F9A0],
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -13920,14 +13998,23 @@
     loadaddress = 0x238AC80
     length = 0xC60
     functions = EuOverlay28Functions
     data = EuOverlay28Data
 
 
 class EuOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        [0x23E0],
+        [0x22DEF60],
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         [0x281C],
         [0x22DF39C],
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -14427,14 +14514,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        [0x7710],
+        [0x22E4290],
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         [0x78E4],
         [0x22E4464],
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14488,20 +14584,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         [0xADEC],
         [0x22E796C],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        [0xB8F4],
+        [0x22E8474],
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         [0xBA90],
         [0x22E8610],
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14522,16 +14629,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         [0xBBD0],
         [0x22E8750],
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         [0xBC88],
         [0x22E8808],
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14862,28 +14970,56 @@
         [0x22EBDCC],
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        [0xF27C],
+        [0x22EBDFC],
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        [0xF37C],
+        [0x22EBEFC],
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         [0xF408],
         [0x22EBF88],
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        [0xF43C],
+        [0x22EBFBC],
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         [0xF64C],
         [0x22EC1CC],
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -15275,14 +15411,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        [0x19108],
+        [0x22F5C88],
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        [0x19134],
+        [0x22F5CB4],
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        [0x192F8],
+        [0x22F5E78],
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         [0x1AC50],
         [0x22F77D0],
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15750,14 +15915,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        [0x1FDD4],
+        [0x22FC954],
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        [0x200B0],
+        [0x22FCC30],
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         [0x20388],
         [0x22FCF08],
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15827,14 +16010,40 @@
         [0x220C8],
         [0x22FEC48],
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        [0x22178],
+        [0x22FECF8],
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        [0x221CC],
+        [0x22FED4C],
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        [0x22234],
+        [0x22FEDB4],
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         [0x2229C],
         [0x22FEE1C],
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -16342,14 +16551,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        [0x279C4],
+        [0x2304544],
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         [0x27B28],
         [0x23046A8],
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -17788,24 +18010,24 @@
         "Inflicts the Heal Block status condition on a target monster if"
         " possible.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: flag to"
         " log message\nr3: flag to only perform the check for inflicting without"
         " actually inflicting\nreturn: Whether or not the status could be inflicted",
     )
 
     MonsterHasEmbargoStatus = Symbol(
-        None,
-        None,
+        [0x3C5AC],
+        [0x231912C],
         None,
         "Returns true if the monster has the Embargo status condition.\n\nr0: pointer"
         " to entity\nreturn: bool",
     )
 
     LogItemBlockedByEmbargo = Symbol(
-        None,
-        None,
+        [0x3C5E0],
+        [0x2319160],
         None,
         "Logs the error message when the usage of an item is blocked by Embargo.\n\nr0:"
         " pointer to entity",
     )
 
     TryInflictEmbargoStatus = Symbol(
         None,
@@ -19952,30 +20174,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        [0x69728],
+        [0x23462A8],
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         [0x69AA8],
         [0x2346628],
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         [0x69B44],
         [0x23466C4],
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         [0x6A0CC],
         [0x2346C4C],
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -20009,22 +20244,30 @@
         "Checks whether any of the items in the bag or any of the items carried by team"
         " members has any of the specified flags set in its flags field.\n\nr0: Flag(s)"
         " to check (0 = f_exists, 1 = f_in_shop, 2 = f_unpaid, etc.)\nreturn: True if"
         " any of the items of the team has the specified flags set, false otherwise.",
     )
 
     AddHeldItemToBag = Symbol(
-        None,
-        None,
+        [0x6AF90],
+        [0x2347B10],
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        [0x6B0AC],
+        [0x2347C2C],
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         [0x6B344],
         [0x2347EC4],
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -22206,14 +22449,31 @@
         0xC,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        [0x2AC26C],
+        [0x22AC26C],
+        0x2,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        [0x2AC270],
+        [0x22AC270],
+        0x4B0,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         [0x2AC720],
         [0x22AC720],
         0x9878,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/eu_itcm.py

```diff
@@ -1765,19 +1765,21 @@
         None,
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1800,15 +1802,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2702,14 +2709,24 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        None,
+        None,
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         None,
         None,
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2875,14 +2892,25 @@
         None,
         None,
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        None,
+        None,
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3092,23 +3120,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         None,
         None,
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4069,14 +4100,32 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
     SetTeamName = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
+    GetRankupPoints = Symbol(
+        None,
+        None,
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        None,
+        None,
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         None,
         None,
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4666,20 +4715,37 @@
         None,
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
+        None,
+        None,
+        None,
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -11819,14 +11885,26 @@
         None,
         None,
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        None,
+        None,
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         None,
         None,
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -13609,14 +13687,23 @@
     loadaddress = None
     length = None
     functions = EuItcmOverlay28Functions
     data = EuItcmOverlay28Data
 
 
 class EuItcmOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        None,
+        None,
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         None,
         None,
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -13986,14 +14073,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        None,
+        None,
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         None,
         None,
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14047,20 +14143,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        None,
+        None,
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         None,
         None,
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14081,16 +14188,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         None,
         None,
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         None,
         None,
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14421,28 +14529,56 @@
         None,
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         None,
         None,
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         None,
         None,
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -14834,14 +14970,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         None,
         None,
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15260,14 +15425,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        None,
+        None,
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        None,
+        None,
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         None,
         None,
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15337,14 +15520,40 @@
         None,
         None,
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         None,
         None,
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -15852,14 +16061,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        None,
+        None,
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         None,
         None,
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -19447,30 +19669,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         None,
         None,
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         None,
         None,
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         None,
         None,
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -19512,14 +19747,22 @@
         None,
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         None,
         None,
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -21564,14 +21807,31 @@
         None,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        None,
+        None,
+        None,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        None,
+        None,
+        None,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         None,
         None,
         None,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/jp.py

```diff
@@ -1827,19 +1827,21 @@
         [0x2013788],
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         [0x137B8],
         [0x20137B8],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         [0x137F8],
         [0x20137F8],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1862,15 +1864,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         [0x13854],
         [0x2013854],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         [0x1389C],
         [0x201389C],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2790,14 +2797,24 @@
         [0x243B0], [0x20243B0], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         [0x24478], [0x2024478], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        None,
+        None,
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         None,
         None,
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2972,14 +2989,25 @@
         None,
         None,
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        None,
+        None,
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         [0x2B444],
         [0x202B444],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3222,23 +3250,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         [0x49290],
         [0x2049290],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         [0x492B8],
         [0x20492B8],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         [0x492F0],
         [0x20492F0],
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4232,14 +4263,32 @@
     SetTeamName = Symbol(
         [0x50EE4],
         [0x2050EE4],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer",
     )
 
+    GetRankupPoints = Symbol(
+        None,
+        None,
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        None,
+        None,
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         [0x51260],
         [0x2051260],
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4835,20 +4884,37 @@
         [0x20532E8],
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
         [0x53AD4],
         [0x2053AD4],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
+        None,
+        None,
+        None,
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         [0x54108],
         [0x2054108],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -12051,14 +12117,26 @@
         None,
         None,
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        None,
+        None,
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         None,
         None,
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -13853,14 +13931,23 @@
     loadaddress = 0x238B6A0
     length = 0xC60
     functions = JpOverlay28Functions
     data = JpOverlay28Data
 
 
 class JpOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        None,
+        None,
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         [0x281C],
         [0x22E00FC],
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -14230,14 +14317,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        None,
+        None,
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         [0x7844],
         [0x22E5124],
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14291,20 +14387,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         [0xAD4C],
         [0x22E862C],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        None,
+        None,
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         None,
         None,
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14325,16 +14432,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         [0xBB28],
         [0x22E9408],
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         [0xBBE0],
         [0x22E94C0],
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14665,28 +14773,56 @@
         [0x22ECA84],
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         [0xF360],
         [0x22ECC40],
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         [0xF5A4],
         [0x22ECE84],
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -15078,14 +15214,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         [0x1AB1C],
         [0x22F83FC],
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15507,14 +15672,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        None,
+        None,
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        None,
+        None,
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         [0x2001C],
         [0x22FD8FC],
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15584,14 +15767,40 @@
         [0x21D54],
         [0x22FF634],
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         [0x21F28],
         [0x22FF808],
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -16099,14 +16308,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        None,
+        None,
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         [0x278EC],
         [0x23051CC],
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -19706,30 +19928,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         [0x69520],
         [0x2346E00],
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         [0x695BC],
         [0x2346E9C],
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         [0x69B44],
         [0x2347424],
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -19771,14 +20006,22 @@
         None,
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         [0x6ADA4],
         [0x2348684],
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -21828,14 +22071,31 @@
         None,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        None,
+        None,
+        None,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        None,
+        None,
+        None,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         None,
         None,
         None,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/jp_itcm.py

```diff
@@ -1765,19 +1765,21 @@
         None,
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1800,15 +1802,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2702,14 +2709,24 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        None,
+        None,
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         None,
         None,
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2875,14 +2892,25 @@
         None,
         None,
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        None,
+        None,
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3092,23 +3120,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         None,
         None,
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4069,14 +4100,32 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
     SetTeamName = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
+    GetRankupPoints = Symbol(
+        None,
+        None,
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        None,
+        None,
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         None,
         None,
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4666,20 +4715,37 @@
         None,
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
+        None,
+        None,
+        None,
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -11819,14 +11885,26 @@
         None,
         None,
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        None,
+        None,
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         None,
         None,
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -13609,14 +13687,23 @@
     loadaddress = None
     length = None
     functions = JpItcmOverlay28Functions
     data = JpItcmOverlay28Data
 
 
 class JpItcmOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        None,
+        None,
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         None,
         None,
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -13986,14 +14073,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        None,
+        None,
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         None,
         None,
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14047,20 +14143,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        None,
+        None,
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         None,
         None,
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14081,16 +14188,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         None,
         None,
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         None,
         None,
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14421,28 +14529,56 @@
         None,
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         None,
         None,
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         None,
         None,
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -14834,14 +14970,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         None,
         None,
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15260,14 +15425,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        None,
+        None,
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        None,
+        None,
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         None,
         None,
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15337,14 +15520,40 @@
         None,
         None,
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         None,
         None,
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -15852,14 +16061,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        None,
+        None,
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         None,
         None,
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -19447,30 +19669,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         None,
         None,
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         None,
         None,
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         None,
         None,
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -19512,14 +19747,22 @@
         None,
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         None,
         None,
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -21564,14 +21807,31 @@
         None,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        None,
+        None,
+        None,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        None,
+        None,
+        None,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         None,
         None,
         None,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/na.py

```diff
@@ -1829,19 +1829,21 @@
         [0x20137B8],
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         [0x137E8],
         [0x20137E8],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         [0x13828],
         [0x2013828],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1864,15 +1866,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         [0x13884],
         [0x2013884],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         [0x138CC],
         [0x20138CC],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2792,14 +2799,24 @@
         [0x24360], [0x2024360], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         [0x24428], [0x2024428], None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        [0x24DFC],
+        [0x2024DFC],
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         [0x24FD8],
         [0x2024FD8],
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2974,14 +2991,25 @@
         None,
         None,
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        [0x2A3E4],
+        [0x202A3E4],
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         [0x2B0EC],
         [0x202B0EC],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3224,23 +3252,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         [0x48F24],
         [0x2048F24],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         [0x48F4C],
         [0x2048F4C],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         [0x48F84],
         [0x2048F84],
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4234,14 +4265,32 @@
     SetTeamName = Symbol(
         [0x50B94],
         [0x2050B94],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer",
     )
 
+    GetRankupPoints = Symbol(
+        [0x50BB8],
+        [0x2050BB8],
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        [0x50C74],
+        [0x2050C74],
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         [0x50F10],
         [0x2050F10],
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4837,20 +4886,37 @@
         [0x2052FB0],
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
         [0x5379C],
         [0x205379C],
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
+        [0x5384C],
+        [0x205384C],
+        None,
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         [0x53DD0],
         [0x2053DD0],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -12170,14 +12236,26 @@
         [0x2ECF8],
         [0x230AF38],
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        [0x32B08],
+        [0x230ED48],
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         [0x32DC4],
         [0x230F004],
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -14004,14 +14082,23 @@
     loadaddress = 0x238A140
     length = 0xC60
     functions = NaOverlay28Functions
     data = NaOverlay28Data
 
 
 class NaOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        [0x23E0],
+        [0x22DE620],
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         [0x281C],
         [0x22DEA5C],
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -14511,14 +14598,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        [0x76A0],
+        [0x22E38E0],
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         [0x7874],
         [0x22E3AB4],
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14572,20 +14668,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         [0xAD7C],
         [0x22E6FBC],
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        [0xB884],
+        [0x22E7AC4],
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         [0xBA20],
         [0x22E7C60],
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14606,16 +14713,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         [0xBB60],
         [0x22E7DA0],
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         [0xBC18],
         [0x22E7E58],
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14946,28 +15054,56 @@
         [0x22EB41C],
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        [0xF20C],
+        [0x22EB44C],
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        [0xF30C],
+        [0x22EB54C],
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         [0xF398],
         [0x22EB5D8],
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        [0xF3CC],
+        [0x22EB60C],
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         [0xF5DC],
         [0x22EB81C],
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -15359,14 +15495,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        [0x1908C],
+        [0x22F52CC],
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        [0x190B8],
+        [0x22F52F8],
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        [0x1927C],
+        [0x22F54BC],
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         [0x1ABD8],
         [0x22F6E18],
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15834,14 +15999,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        [0x1FD18],
+        [0x22FBF58],
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        [0x1FFF4],
+        [0x22FC234],
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         [0x202CC],
         [0x22FC50C],
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15911,14 +16094,40 @@
         [0x2200C],
         [0x22FE24C],
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        [0x220BC],
+        [0x22FE2FC],
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        [0x22110],
+        [0x22FE350],
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        [0x22178],
+        [0x22FE3B8],
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         [0x221E0],
         [0x22FE420],
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -16426,14 +16635,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        [0x278D8],
+        [0x2303B18],
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         [0x27A3C],
         [0x2303C7C],
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -20036,30 +20258,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        [0x6947C],
+        [0x23456BC],
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         [0x697FC],
         [0x2345A3C],
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         [0x69898],
         [0x2345AD8],
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         [0x69E20],
         [0x2346060],
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -20101,14 +20336,22 @@
         [0x2346F14],
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        [0x6ADF0],
+        [0x2347030],
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         [0x6B084],
         [0x23472C4],
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -22286,14 +22529,31 @@
         0xC,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        [0x2AB92C],
+        [0x22AB92C],
+        0x2,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        [0x2AB930],
+        [0x22AB930],
+        0x4B0,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         [0x2ABDE0],
         [0x22ABDE0],
         0x9878,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/na_itcm.py

```diff
@@ -1765,19 +1765,21 @@
         None,
         None,
         "Initializes a move info struct.\n\nThis sets f_exists and f_enabled_for_ai on"
         " the flags, the ID to the given ID, the PP to the max PP for the move ID, and"
         " the ginseng boost to 0.\n\nr0: pointer to move to initialize\nr1: move ID",
     )
 
-    GetInfoMoveCheckId = Symbol(
+    InitMoveCheckId = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: move\nr1: move ID",
+        "Same as InitMove, but the function ensures that the specified ID is not 0. If"
+        " it is, the move is initialized as invalid and nothing else happens.\n\nr0:"
+        " move\nr1: move ID",
     )
 
     GetInfoMoveGround = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: ground move\nr1: move ID",
@@ -1800,15 +1802,20 @@
         "Gets the type of a move\n\nr0: Pointer to move data\nreturn: Type of the move",
     )
 
     GetMovesetLevelUpPtr = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: monster ID\nreturn: ?",
+        "Given the ID of a monster in the current dungeon, returns a pointer to the"
+        " list of moves it learns by leveling up and the level in which each move is"
+        " learnt.\n\nThe list contains pairs of <encoded move ID, level>. The move ID"
+        " is encoded and can be 1 or 2 bytes long. GetEncodedHalfword must be used to"
+        " decode it. The end of the list is marked by a null byte.\n\nr0: monster"
+        " ID\nreturn: Pointer to encoded level-up move list",
     )
 
     IsInvalidMoveset = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: moveset_id\nreturn: bool",
@@ -2702,14 +2709,24 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
     SetStringPower = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes"
     )
 
+    GetBagNameString = Symbol(
+        None,
+        None,
+        None,
+        "Returns 'One-Item Inventory' or 'Treasure Bag' depending on the size of the"
+        " bag.\n\nr0: [output] Pointer to the buffer where the string will be"
+        " written\nreturn: Pointer to the buffer where the string was written (in other"
+        " words, the same value passed in r0)",
+    )
+
     GetDungeonResultString = Symbol(
         None,
         None,
         None,
         "Returns a string containing some information to be used when displaying the"
         " dungeon results screen.\n\nThe exact string returned depends on the value of"
         " r0:\n0: Name of the move that fainted the leader. Empty string if the leader"
@@ -2875,14 +2892,25 @@
         None,
         None,
         None,
         "Load and initialise the alert sprite, storing the result in"
         " ALERT_ANIMATION_CONTROL\n\nNo params.",
     )
 
+    PrintClearMark = Symbol(
+        None,
+        None,
+        None,
+        "Prints the specified clear mark on the screen.\n\nClear marks are shown on the"
+        " save file load screen. They are used to show which plot milestones have"
+        " already been completed.\n\nr0: Clear mark ID\nr1: X pos (unknown units,"
+        " usually ranges between 3 and 27)\nr2: Y pos (unknown units, normally"
+        " 14)\nr3: ?",
+    )
+
     CreateNormalMenu = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: layout_struct_ptr\nr1:"
         " menu_flags\nr2: additional_info_ptr\nr3: menu_struct_ptr\nstack[0]:"
         " option_id\nreturn: menu_id",
@@ -3092,23 +3120,26 @@
         " buffer\nr2: size\nreturn: status code",
     )
 
     CalcChecksum = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size",
+        "Calculates the checksum of the save file and stores it at the start of the"
+        " data.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in bytes",
     )
 
-    CheckChecksum = Symbol(
+    CheckChecksumInvalid = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer\nr1: size\nreturn:"
-        " check_ok",
+        "Calculates the checksum of the save file and compares it with the one stored"
+        " in it.\n\nr0: Pointer to a buffer containing the save data\nr1: Size in"
+        " bytes\nreturn: True if the calculated and stored checksums don't match, false"
+        " if they do.",
     )
 
     NoteSaveBase = Symbol(
         None,
         None,
         None,
         "Probably related to saving or quicksaving?\n\nThis function prints the debug"
@@ -4069,14 +4100,32 @@
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
     SetTeamName = Symbol(
         None, None, None, "Note: unverified, ported from Irdkwia's notes\n\nr0: buffer"
     )
 
+    GetRankupPoints = Symbol(
+        None,
+        None,
+        None,
+        "Returns the number of points required to reach the next rank.\n\nIf"
+        " PERFORMANCE_PROGRESS_LIST[8] is 0 and the current rank is RANK_MASTER, or if"
+        " the current rank is RANK_GUILDMASTER, returns 0.\n\nreturn: Points required"
+        " to reach the next rank",
+    )
+
+    GetRank = Symbol(
+        None,
+        None,
+        None,
+        "Returns the team's rank\n\nIf PERFORMANCE_PROGRESS_LIST[8] is 0, the maximum"
+        " rank that can be returned is RANK_MASTER.\n\nreturn: Rank",
+    )
+
     SubFixedPoint = Symbol(
         None,
         None,
         None,
         "Compute the subtraction of two decimal fixed-point numbers (16 fraction"
         " bits).\n\nNumbers are in the format {16-bit integer part, 16-bit"
         " thousandths}, where the integer part is the lower word. Probably used"
@@ -4666,20 +4715,37 @@
         None,
         None,
         "Checks if the string_buffer matches the name of the species\n\nNote:"
         " unverified, ported from Irdkwia's notes\n\nr0: string_buffer\nr1: monster"
         " ID\nreturn: bool",
     )
 
-    GetLvlStats = Symbol(
+    GetLvlUpEntry = Symbol(
+        None,
+        None,
+        None,
+        "Gets the level-up entry of the given monster ID at the specified level.\n\nThe"
+        " monster's entire level up data is also decompressed to"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER, and its ID is stored in"
+        " LEVEL_UP_DATA_MONSTER_ID.\n\nr0: [output] Level-up entry\nr1: monster ID\nr2:"
+        " level",
+    )
+
+    GetEncodedHalfword = Symbol(
         None,
         None,
         None,
-        "Note: unverified, ported from Irdkwia's notes\n\nr0: [output] level stats\nr1:"
-        " monster ID\nr2: level",
+        "Decodes a 2-byte value that may be encoded using 1 or 2 bytes and writes it to"
+        " the specified buffer.\n\nThe encoding system uses the most significant bit of"
+        " the first byte to signal if the value is encoded as a single byte or as a"
+        " halfword. If the bit is unset, the value is read as (encoded byte) & 0x7F. If"
+        " it's set, the value is read as ((first encoded byte) & 0x7F << 7) | (second"
+        " encoded byte) & 0x7F.\n\nr0: Pointer to encoded value\nr1: [output] Buffer"
+        " where the resulting 2-byte value will be stored.\nreturn: Pointer to the next"
+        " byte to decode",
     )
 
     GetEvoFamily = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nr0: monster_str\nr1:"
@@ -11819,14 +11885,26 @@
         None,
         None,
         None,
         "Used to calculate the items required to get a certain exclusive item in the"
         " swap shop.\n\nr0: ?\nr1: ?",
     )
 
+    GetDungeonMapPos = Symbol(
+        None,
+        None,
+        None,
+        "Checks if a dungeon should be displayed on the map and the position where it"
+        " should be displayed if so.\n\nr0: [Output] Buffer where the coordinates of"
+        " the map marker will be stored. The coordinates are shifted 8 bits to the"
+        " left, so they are probably fixed-point numbers instead of integers.\nr1:"
+        " Dungeon ID\nreturn: True if the dungeon should be displayed on the map, false"
+        " otherwise.",
+    )
+
     WorldMapSetMode = Symbol(
         None,
         None,
         None,
         "Function called by the script function 'worldmap_SetMode'\nDefine the mode of"
         " the world map, which can among other things be used to decide if the player"
         " character should appear on the world map\nThe mode is set even if no world"
@@ -13609,14 +13687,23 @@
     loadaddress = None
     length = None
     functions = NaItcmOverlay28Functions
     data = NaItcmOverlay28Data
 
 
 class NaItcmOverlay29Functions:
+    GetWeatherColorTable = Symbol(
+        None,
+        None,
+        None,
+        "Gets a pointer to the floor's color table given the current weather.\n\nThe"
+        " returned table contains 1024 color entries.\n\nr0: Weather ID\nreturn: color"
+        " table pointer",
+    )
+
     DungeonAlloc = Symbol(
         None,
         None,
         None,
         "Allocates a new dungeon struct.\n\nThis updates the master dungeon pointer and"
         " returns a copy of that pointer.\n\nreturn: pointer to a newly allocated"
         " dungeon struct",
@@ -13986,14 +14073,23 @@
         "Seems like a variant of PlayEffectAnimationEntity that uses pixel coordinates"
         " as its first parameter instead of an entity pointer.\n\nr0: Pixel position"
         " where the effect should be played\nr1: Effect ID\nr2: Unknown flag (same as"
         " the one in PlayEffectAnimationEntity)\nreturn: Same as"
         " PlayEffectAnimationEntity",
     )
 
+    AnimationDelayOrSomething = Symbol(
+        None,
+        None,
+        None,
+        "Called whenever most (all?) animations are played. Does not return until the"
+        " animation is over.\n\nMight wait until the animation is done? Contains"
+        " several loops that call AdvanceFrame.\n\nr0: ?",
+    )
+
     UpdateStatusIconFlags = Symbol(
         None,
         None,
         None,
         "Sets a monster's status_icon_flags bitfield according to its current status"
         " effects. Does not affect a Sudowoodo in the 'permanent sleep' state"
         " (statuses::sleep == 0x7F).\n\nSome of the status effect in monster::statuses"
@@ -14047,20 +14143,31 @@
     )
 
     LoadMappaFileAttributes = Symbol(
         None,
         None,
         None,
         "Note: unverified, ported from Irdkwia's notes\n\nThis function processes the"
-        " spawn list of the current floor, checking which species can spawn, capping"
-        " the amount of spawnable species on the floor to 14, randomly choosing which"
-        " 14 species will spawn and ensuring that the sprite size of all the species"
-        " combined does not exceed the maximum of 0x58000 bytes (352 KB). Kecleon and"
-        " the Decoy are always included in the random selection.\n\nr0:"
-        " quick_saved\nr1: ???\nr2: special_process",
+        " monster spawn list of the current floor, checking which species can spawn,"
+        " capping the amount of spawnable species on the floor to 14, randomly choosing"
+        " which 14 species will spawn and ensuring that the sprite size of all the"
+        " species combined does not exceed the maximum of 0x58000 bytes (352 KB)."
+        " Kecleon and the Decoy are always included in the random selection.\nThe"
+        " function also processes the floor's item spawn lists.\n\nr0: quick_saved\nr1:"
+        " ???\nr2: special_process",
+    )
+
+    GetItemIdToSpawn = Symbol(
+        None,
+        None,
+        None,
+        "Randomly picks an item to spawn using one of the floor's item spawn lists and"
+        " returns its ID.\n\nIf the function fails to properly choose an item (due to,"
+        " for example, a corrupted item list), ITEM_POKE is returned.\n\nr0: Which item"
+        " list to use\nreturn: Item ID",
     )
 
     MonsterSpawnListPartialCopy = Symbol(
         None,
         None,
         None,
         "Copies all entries in the floor's monster spawn list that have a sprite size"
@@ -14081,16 +14188,17 @@
         " not the raw list read from the mappa file).\n\nr0: Monster ID\nreturn: bool",
     )
 
     GetMonsterIdToSpawn = Symbol(
         None,
         None,
         None,
-        "Get the id of the monster to be randomly spawned.\n\nr0: the spawn weight to"
-        " use (0 for normal, 1 for monster house)\nreturn: monster ID",
+        "Randomly picks a monster to spawn using the floor's monster spawn list and"
+        " returns its ID.\n\nr0: the spawn weight to use (0 for normal, 1 for monster"
+        " house)\nreturn: monster ID",
     )
 
     GetMonsterLevelToSpawn = Symbol(
         None,
         None,
         None,
         "Get the level of the monster to be spawned, given its id.\n\nr0: monster"
@@ -14421,28 +14529,56 @@
         None,
         None,
         "Sets a monster's action to action::ACTION_PASS_TURN or action::ACTION_WALK,"
         " depending on the result of GetCanMoveFlag for the monster's ID.\n\nr0:"
         " Pointer to the monster's action field\nr1: Monster ID",
     )
 
+    GetItemToUseByIndex = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster given its"
+        " index.\n\nr0: Entity pointer\nr1: Item index\nreturn: Pointer to the item",
+    )
+
+    GetItemToUse = Symbol(
+        None,
+        None,
+        None,
+        "Returns a pointer to the item that is about to be used by a monster.\n\nr0:"
+        " Entity pointer\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.\nr2: Unused\nreturn: Pointer to the item",
+    )
+
     GetItemAction = Symbol(
         None,
         None,
         None,
         "Returns the action ID that corresponds to an item given its ID.\n\nThe action"
         " is based on the category of the item (see ITEM_CATEGORY_ACTIONS), unless the"
         " specified ID is 0x16B, in which case ACTION_UNK_35 is returned.\nSome items"
         " can have unexpected actions, such as thrown items, which have ACTION_NOTHING."
         " This is done to prevent duplicate actions from being listed in the menu"
         " (since items always have a 'throw' option), since a return value of"
         " ACTION_NOTHING prevents the option from showing up in the menu.\n\nr0: Item"
         " ID\nreturn: Action ID associated with the specified item",
     )
 
+    RemoveUsedItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item from the bag or from the floor after using it\n\nr0: Pointer"
+        " to the entity that used the item\nr1: Parameter index in"
+        " monster::action_data::action_parameters. Will be used to use to determine the"
+        " index of the used item.",
+    )
+
     AddDungeonSubMenuOption = Symbol(
         None,
         None,
         None,
         "Adds an option to the list of actions that can be taken on a pokémon, item or"
         " move to the currently active sub-menu on dungeon mode (team, moves, items,"
         " etc.).\n\nr0: Action ID\nr1: True if the option should be enabled, false"
@@ -14834,14 +14970,43 @@
         "Tries to change the current leader to the monster specified by"
         " dungeon::new_leader.\n\nAccounts for situations that can prevent changing"
         " leaders, such as having stolen from a Kecleon shop. If one of those"
         " situations prevents changing leaders, prints the corresponding message to the"
         " message log.\n\nNo params.",
     )
 
+    UseSingleUseItemWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Same as UseSingleUseItem, but the second parameter is determined automatically"
+        " from monster::action_data::action_parameter[1]::action_use_idx.\n\nr0: User",
+    )
+
+    UseSingleUseItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a single-use item. The item is deleted afterwards.\n\nThe"
+        " item to use is determined by the user's"
+        " monster::action_data::action_parameter[0].\n\nr0: User (monster who used the"
+        " item)\nr1: Target (monster that consumes the item)",
+    )
+
+    UseThrowableItem = Symbol(
+        None,
+        None,
+        None,
+        "Makes a monster use a throwable item.\n\nThe item to use is determined by"
+        " monster::action_data::action_parameter[0].\nIf the item's category is"
+        " CATEGORY_THROWN_LINE or CATEGORY_THROWN_ARC, the game will attempt to"
+        " decrement the count of the used item by 1. If it's not or there's only 1 item"
+        " left, it is destroyed instead.\n\nr0: User (monster who used the item)",
+    )
+
     ResetDamageData = Symbol(
         None,
         None,
         None,
         "Zeroes the damage data struct, which is output by the damage calculation"
         " function.\n\nr0: damage data pointer",
     )
@@ -15260,14 +15425,32 @@
         "Initializes stats, IQ skills and moves for a given monster\n\nMight only be"
         " used when spawning fixed room monsters.\n\nr0: Entity pointer\nr1: Fixed room"
         " monster stats index\nr2: Spawn direction? (when calling this function while"
         " spawning a fixed room monster, this is the parameter value associated to the"
         " spawn action, after converting it to a direction.)",
     )
 
+    InitEnemySpawnStats = Symbol(
+        None,
+        None,
+        None,
+        "Initializes dungeon::enemy_spawn_stats. Might do something else too.\n\nNo"
+        " params.",
+    )
+
+    InitEnemyStatsAndMoves = Symbol(
+        None,
+        None,
+        None,
+        "Initializes the HP, Atk, Sp. Atk, Def, Sp. Def and moveset of a newly spawned"
+        " enemy. Might do something else too.\n\nr0: Pointer to the monster's move"
+        " list\nr1: Pointer to the monster's current HP\nr2: Pointer to the monster's"
+        " offensive stats\nr3: Pointer to the monster's defensive stats",
+    )
+
     SpawnTeam = Symbol(
         None,
         None,
         None,
         "Seems to initialize and spawn the team when entering a dungeon.\n\nr0: ?",
     )
 
@@ -15337,14 +15520,40 @@
         None,
         None,
         None,
         "Spawns all the shopkeepers in the dungeon struct's shopkeeper_spawns"
         " array.\n\nNo params.",
     )
 
+    GetMaxHpAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the max HP of a monster given its level.\n\nr0: Monster ID\nr1:"
+        " Monster level\nreturn: Max HP at the given level",
+    )
+
+    GetOffensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Atk / Sp. Atk of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Atk, 1: Sp. Atk)\nreturn:"
+        " Atk / Sp. Atk at the given level",
+    )
+
+    GetDefensiveStatAtLevel = Symbol(
+        None,
+        None,
+        None,
+        "Returns the Def / Sp. Def of a monster given its level, capped to 255.\n\nr0:"
+        " Monster ID\nr1: Monster level\nr2: Stat index (0: Def, 1: Sp. Def)\nreturn:"
+        " Def / Sp. Def at the given level",
+    )
+
     GetOutlawSpawnData = Symbol(
         None,
         None,
         None,
         "Gets outlaw spawn data for the current floor.\n\nr0: [output] Outlaw spawn"
         " data",
     )
@@ -15852,14 +16061,27 @@
         "Attempts to level up the the target. Fails if the target's level can't be"
         " raised. The show show level up dialog bool does nothing for monsters not on"
         " the team.\n\nr0: user entity pointer\nr1: target entity pointer\nr2: bool"
         " message flag?\nr3: bool show level up dialog (for example 'Hey, I leveled"
         " up!' with a portrait)?\nreturn: success flag",
     )
 
+    GetMonsterMoves = Symbol(
+        None,
+        None,
+        None,
+        "Determines the moveset of a newly spawned monster given its species and"
+        " level.\n\nThe function loops the monster's learnset, adding moves to the list"
+        " in level-up order. Once all four slots are filled up, a random existing move"
+        " gets replaced to make room for the new one. This means that the monster will"
+        " always have the latest move it can learn given its level.\n\nr0: [output]"
+        " Pointer to move ID list (4 entries, 2 bytes each)\nr1: Monster ID\nr2:"
+        " Monster level",
+    )
+
     EvolveMonster = Symbol(
         None,
         None,
         None,
         "Makes the specified monster evolve into the specified species. Has a special"
         " case when\na monster evolves into Ninjask and tries to spawn a Shedinja as"
         " well.\n\nr0: user entity pointer?\nr1: target pointer to the entity to"
@@ -19447,30 +19669,43 @@
         " the floor.\n\nThis calls SpawnItemEntity, fills in the item info struct, sets"
         " the entity to be visible, binds the entity to the tile it occupies, updates"
         " the n_items counter on the dungeon struct, and various other bits of"
         " bookkeeping.\n\nr0: position\nr1: item pointer\nr2: some flag?\nreturn:"
         " success flag",
     )
 
-    SpawnEnemyItemDropWrapper = Symbol(
+    RemoveGroundItem = Symbol(
+        None,
+        None,
+        None,
+        "Removes an item lying on the ground.\n\nAlso updates dungeon::n_items.\n\nr0:"
+        " Position where the item is located\nr1: If true, update"
+        " dungeon::poke_buy_kecleon_shop and dungeon::poke_sold_kecleon_shop",
+    )
+
+    SpawnDroppedItemWrapper = Symbol(
         None,
         None,
         None,
-        "Wraps SpawnEnemyItemDrop in a more convenient interface.\n\nr0: entity\nr1:"
+        "Wraps SpawnDroppedItem in a more convenient interface.\n\nr0: entity\nr1:"
         " position\nr2: item\nr3: ?",
     )
 
-    SpawnEnemyItemDrop = Symbol(
+    SpawnDroppedItem = Symbol(
         None,
         None,
         None,
-        "Appears to spawn an enemy item drop at a specified location, with a log"
-        " message.\n\nr0: entity\nr1: item entity\nr2: item info\nr3: ?\nstack[0]:"
-        " pointer to int16_t[2] for x/y direction (corresponding to"
-        " DIRECTIONS_XY)\nstack[1]: ?",
+        "Used to spawn an item that was thrown or dropped, with a log"
+        " message.\n\nDetermines where exactly the item will land, if it bounces on a"
+        " trap, etc.\nUsed for thrown items that hit a wall, for certain enemy drops"
+        " (such as Unown stones or Treasure Boxes), for certain moves (like Pay Day and"
+        " Knock Off), and possibly other things.\n\nr0: entity that dropped or threw"
+        " the item\nr1: item entity. Contains the coordinates where the item should try"
+        " to land first.\nr2: item info\nr3: ?\nstack[0]: pointer to int16_t[2] for x/y"
+        " direction (corresponding to DIRECTIONS_XY)\nstack[1]: ?",
     )
 
     TryGenerateUnownStoneDrop = Symbol(
         None,
         None,
         None,
         "Determine if a defeated monster should drop a Unown Stone, and generate the"
@@ -19512,14 +19747,22 @@
         None,
         None,
         "Adds the monster's held item to the bag. This is only called on monsters on"
         " the exploration team.\nmonster::is_not_team_member should be checked to be"
         " false before calling.\n\nr0: monster pointer",
     )
 
+    RemoveEmptyItemsInBagWrapper = Symbol(
+        None,
+        None,
+        None,
+        "Calls RemoveEmptyItemsInBag, then some other function that seems to update the"
+        " minimap, the map surveyor flag, and other stuff.\n\nNo params.",
+    )
+
     GenerateItem = Symbol(
         None,
         None,
         None,
         "Initializes an item struct with the given information.\n\nThis wraps InitItem,"
         " but with extra logic to resolve the item's stickiness. It also calls"
         " GenerateMoneyQuantity for Poké.\n\nr0: pointer to item to initialize\nr1:"
@@ -21564,14 +21807,31 @@
         None,
         "The team name.\n\nA null-terminated string, with a maximum length of 10."
         " Presumably encoded with the ANSI/Shift JIS encoding the game typically"
         " uses.\n\nThis is presumably part of a larger struct, together with other"
         " nearby data.",
     )
 
+    LEVEL_UP_DATA_MONSTER_ID = Symbol(
+        None,
+        None,
+        None,
+        "ID of the monster whose level-up data is currently stored in"
+        " LEVEL_UP_DATA_DECOMPRESS_BUFFER.",
+    )
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER = Symbol(
+        None,
+        None,
+        None,
+        "Buffer used to stored a monster's decompressed level up data. Used by"
+        " GetLvlUpEntry.\n\nExact size is a guess (100 levels * 12 bytes per entry ="
+        " 1200 = 0x4B0).",
+    )
+
     TEAM_MEMBER_TABLE = Symbol(
         None,
         None,
         None,
         "Table with all team members, persistent information about them, and"
         " information about which ones are currently active.\n\nSee the comments on"
         " struct team_member_table for more information.\n\ntype: struct"
```

## pmdsky_debug_py/protocol.py

```diff
@@ -1122,15 +1122,15 @@
     ]
 
     InitMove: Symbol[
         Optional[List[int]],
         None,
     ]
 
-    GetInfoMoveCheckId: Symbol[
+    InitMoveCheckId: Symbol[
         Optional[List[int]],
         None,
     ]
 
     GetInfoMoveGround: Symbol[
         Optional[List[int]],
         None,
@@ -1762,14 +1762,19 @@
     ]
 
     SetStringPower: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetBagNameString: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     GetDungeonResultString: Symbol[
         Optional[List[int]],
         None,
     ]
 
     SetQuestionMarks: Symbol[
         Optional[List[int]],
@@ -1872,14 +1877,19 @@
     ]
 
     LoadAlert: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    PrintClearMark: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     CreateNormalMenu: Symbol[
         Optional[List[int]],
         None,
     ]
 
     FreeNormalMenu: Symbol[
         Optional[List[int]],
@@ -2042,15 +2052,15 @@
     ]
 
     CalcChecksum: Symbol[
         Optional[List[int]],
         None,
     ]
 
-    CheckChecksum: Symbol[
+    CheckChecksumInvalid: Symbol[
         Optional[List[int]],
         None,
     ]
 
     NoteSaveBase: Symbol[
         Optional[List[int]],
         None,
@@ -2667,14 +2677,24 @@
     ]
 
     SetTeamName: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetRankupPoints: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    GetRank: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     SubFixedPoint: Symbol[
         Optional[List[int]],
         None,
     ]
 
     BinToDecFixedPoint: Symbol[
         Optional[List[int]],
@@ -3047,15 +3067,20 @@
     ]
 
     StrcmpMonsterName: Symbol[
         Optional[List[int]],
         None,
     ]
 
-    GetLvlStats: Symbol[
+    GetLvlUpEntry: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    GetEncodedHalfword: Symbol[
         Optional[List[int]],
         None,
     ]
 
     GetEvoFamily: Symbol[
         Optional[List[int]],
         None,
@@ -7735,14 +7760,19 @@
     ]
 
     GetExclusiveItemRequirements: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetDungeonMapPos: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     WorldMapSetMode: Symbol[
         Optional[List[int]],
         None,
     ]
 
     WorldMapSetCamera: Symbol[
         Optional[List[int]],
@@ -9705,14 +9735,19 @@
     Overlay28FunctionsProtocol,
     Overlay28DataProtocol,
     Optional[int],
 ]
 
 
 class Overlay29FunctionsProtocol(Protocol):
+    GetWeatherColorTable: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     DungeonAlloc: Symbol[
         Optional[List[int]],
         None,
     ]
 
     GetDungeonPtrMaster: Symbol[
         Optional[List[int]],
@@ -9900,14 +9935,19 @@
     ]
 
     PlayEffectAnimationPixelPos: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    AnimationDelayOrSomething: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     UpdateStatusIconFlags: Symbol[
         Optional[List[int]],
         None,
     ]
 
     PlayEffectAnimation0x171Full: Symbol[
         Optional[List[int]],
@@ -9935,14 +9975,19 @@
     ]
 
     LoadMappaFileAttributes: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetItemIdToSpawn: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     MonsterSpawnListPartialCopy: Symbol[
         Optional[List[int]],
         None,
     ]
 
     IsOnMonsterSpawnList: Symbol[
         Optional[List[int]],
@@ -10110,19 +10155,34 @@
     ]
 
     SetActionPassTurnOrWalk: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetItemToUseByIndex: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    GetItemToUse: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     GetItemAction: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    RemoveUsedItem: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     AddDungeonSubMenuOption: Symbol[
         Optional[List[int]],
         None,
     ]
 
     DisableDungeonSubMenuOption: Symbol[
         Optional[List[int]],
@@ -10325,14 +10385,29 @@
     ]
 
     ChangeLeader: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    UseSingleUseItemWrapper: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    UseSingleUseItem: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    UseThrowableItem: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     ResetDamageData: Symbol[
         Optional[List[int]],
         None,
     ]
 
     FreeLoadedAttackSpriteAndMore: Symbol[
         Optional[List[int]],
@@ -10565,14 +10640,24 @@
     ]
 
     InitOtherMonsterData: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    InitEnemySpawnStats: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    InitEnemyStatsAndMoves: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     SpawnTeam: Symbol[
         Optional[List[int]],
         None,
     ]
 
     SpawnInitialMonsters: Symbol[
         Optional[List[int]],
@@ -10605,14 +10690,29 @@
     ]
 
     SpawnShopkeepers: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetMaxHpAtLevel: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    GetOffensiveStatAtLevel: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    GetDefensiveStatAtLevel: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     GetOutlawSpawnData: Symbol[
         Optional[List[int]],
         None,
     ]
 
     ExecuteMonsterAction: Symbol[
         Optional[List[int]],
@@ -10875,14 +10975,19 @@
     ]
 
     LevelUp: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    GetMonsterMoves: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     EvolveMonster: Symbol[
         Optional[List[int]],
         None,
     ]
 
     GetSleepAnimationId: Symbol[
         Optional[List[int]],
@@ -12750,20 +12855,25 @@
     ]
 
     SpawnItem: Symbol[
         Optional[List[int]],
         None,
     ]
 
-    SpawnEnemyItemDropWrapper: Symbol[
+    RemoveGroundItem: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
+    SpawnDroppedItemWrapper: Symbol[
         Optional[List[int]],
         None,
     ]
 
-    SpawnEnemyItemDrop: Symbol[
+    SpawnDroppedItem: Symbol[
         Optional[List[int]],
         None,
     ]
 
     TryGenerateUnownStoneDrop: Symbol[
         Optional[List[int]],
         None,
@@ -12785,14 +12895,19 @@
     ]
 
     AddHeldItemToBag: Symbol[
         Optional[List[int]],
         None,
     ]
 
+    RemoveEmptyItemsInBagWrapper: Symbol[
+        Optional[List[int]],
+        None,
+    ]
+
     GenerateItem: Symbol[
         Optional[List[int]],
         None,
     ]
 
     CheckActiveChallengeRequest: Symbol[
         Optional[List[int]],
@@ -14306,14 +14421,24 @@
     ]
 
     TEAM_NAME: Symbol[
         Optional[List[int]],
         Optional[int],
     ]
 
+    LEVEL_UP_DATA_MONSTER_ID: Symbol[
+        Optional[List[int]],
+        Optional[int],
+    ]
+
+    LEVEL_UP_DATA_DECOMPRESS_BUFFER: Symbol[
+        Optional[List[int]],
+        Optional[int],
+    ]
+
     TEAM_MEMBER_TABLE: Symbol[
         Optional[List[int]],
         Optional[int],
     ]
 
     ENABLED_VRAM_BANKS: Symbol[
         Optional[List[int]],
```

## Comparing `pmdsky_debug_py-7.0.4.dist-info/METADATA` & `pmdsky_debug_py-7.0.5.dist-info/METADATA`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pmdsky-debug-py
-Version: 7.0.4
+Version: 7.0.5
 Summary: pmdsky-debug symbols for Python.
 Author-email: Marco 'Capypara' Köpcke <hello@capypara.de>
 License: MIT
 Project-URL: repository, https://github.com/SkyTemple/pmdsky-debug-py
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.8
```

