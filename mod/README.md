# Overview

Are you a mod developer who is wishing for a quieter `error.log` while you debug with the Enigmatic Shipset active?  Then this mod is for you (and me)!  This mod does **NOT** redistribute any of the graphics from the Enigmatic Shipset, but does redefine and replace entity asset files in order to eliminate many error messages.

# Changes

Many entity definitions were tweaked to remove animations.  "Removed" code was commented out rather than deleted.  MadamLava, please feel free to harvest any of these adjustment for use in your mod directly.

* `common\graphical_culture\aoshtai_01_graphical_culture.txt` mark graphical culture as not having cities
* `gfx\models\ships\aoshtai_01_ships_entities.asset`
    * Remove animations from `aoshtai_01_corvette_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_destroyer_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_cruiser_entity` - the mesh is not animated
    * Enable missing locator `strike_craft_locator_01` on section `aoshtai_01_cruiser_mid_S2HB_entity`
    * Add missing locator `medium_gun_01` to section `aoshtai_01_cruiser_mid_L1M1_entity`
    * Remove animations from `aoshtai_01_battleship_entity` - the mesh is not animated
    * Add missing locators `strike_craft_locator_01` and `strike_craft_locator_02` to section `aoshtai_01_cruiser_mid_S2HB_entity`
    * Remove animations from `aoshtai_01_titan_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_construction_ship_entity` - the mesh is not animated
    * Remove the attached entity `aoshtai_01_construction_window_entity` from `aoshtai_01_construction_ship_entity` - the attachment entity does not exist
    * Remove animations from `aoshtai_01_transport_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_mining_station_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_mining_station_section_entity` - the mesh is not animated
    * Rename `machine_01_research_station_entity` to `aoshtai_01_research_station_entity` - looks like an error when renaming all the entities; would conflict with the Machine Shipset
    * Remove animations from `aoshtai_01_research_station_section_entity` - the mesh is not animated
    * Remove animations from `aoshtai_01_juggernaut_core_section_entity` - the mesh is not animated
    * Add missing locators to `aoshtai_01_juggernaut_core_section_entity`
        * `xl_gun_01`
        * `xl_gun_02`
        * `strike_craft_locator_01`
        * `strike_craft_locator_02`
        * `strike_craft_locator_03`
        * `strike_craft_locator_04`
        * `strike_craft_locator_05`
        * `strike_craft_locator_06`
        * `gun_1`
        * `gun_2`
        * `gun_3`
        * `gun_4`
        * `gun_5`
    * Add missing locators to `aoshtai_01_starbase_citadel_section_entity`
        * `medium_gun_010`
        * `medium_gun_011`
        * `medium_gun_012`
        * `medium_gun_013`
    * Add missing locator `strike_craft_locator_01` to `aoshtai_01_orbital_station_hangarbay_section_entity`
    * Remove animations from `aoshtai_01_gateway_entity` - the mesh is not animated
    * Adjust habitat entity definitions to use the same code for each level (which ensures the correct emissive color is used)
    * Change the spelling of `lenght` to `length` - Stellaris recognizes both, but proper spelling is preferred
    * Alter invalid particle reference `generic_big_1_25_exhaust_circle_moving` => `generic_1_25_exhaust_circle_moving`
    * Alter invalid particle reference `aoshtai_01_2_35_exhaust_idle_particle` => `mammalian_01_2_35_exhaust_idle_particle`
    * Alter invalid particle reference `aoshtai_01_2_35_exhaust_oblong_idle_particle` => `mammalian_01_2_35_exhaust_oblong_idle_particle`
    * Alter invalid particle reference `aoshtai_01_2_35_ship_exhaust_moving_particle` => `mammalian_01_2_35_ship_exhaust_moving_particle`
    * Alter invalid particle reference `aoshtai_01_2_35_ship_exhaust_oblong_moving_particle` => `mammalian_01_2_35_ship_exhaust_oblong_moving_particle`
    * Alter invalid particle reference `aoshtai_01_1_45_ship_exhaust_moving_particle` => `mammalian_01_1_45_ship_exhaust_moving_particle`
    * Alter invalid particle reference `aoshtai_01_3_35_ship_exhaust_moving_particle` => `mammalian_01_3_35_ship_exhaust_moving_particle`
* `gfx\models\ships\aoshtai_01_ships_meshes.gfx`
    * Adjust all mesh definition filepaths to have capitalization matching that of their file directories - mismatched casing can cause problems for users playing on the Mac or *nix operating systems
    * Fix filepath for mesh definition `aoshtai_01_battleship_bow_M1S2SHB_mesh` - the mesh filename is misspelled, so the definition's filepath needs to match it
    * Remove animations from mesh definition `aoshtai_01_construction_mesh` - the animation definitions do not exist
    * Remove mesh definition `aoshtai_01_colony_mesh` - the mesh file does not exist
* `gfx\models\ships\UNUSED_aoshtai_01_turret_meshes.gfx` adjust all mesh definition filepaths to have capitalization matching that of their file directories - mismatched casing can cause problems for users playing on the Mac or *nix operating systems

## Compatibility

Built for Stellaris version 3.1.\* "Lem."  Not compatible with achievements.

### Required Dependency Mods

[Enigmatic Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=) for the original graphics and other ship-related code.

### Recommended Companion Mods

[Aesthetic Terraform Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=2622411084) will give you back the very old-school terraform stations as visual markers for terraforming planets.

[Enigmatic Shipset Add-on: Aesthetic Terraform Station Compatibility](https://steamcommunity.com/sharedfiles/filedetails/?id=) this compatibility patch ensures the correct Enigmatic Shipset graphics are used for the above terraform stations.

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/enigmatic_shipset_no_error_logs)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.