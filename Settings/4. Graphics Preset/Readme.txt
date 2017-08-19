|-------------------------------------------------------------------------------|
| Graphics Preset:       | Very Low | Low      | Medium   | High     | Amazing  |
|-------------------------------------------------------------------------------|
| Vertical Sync:         | Off      | Off      | On       | On       | On       |
| Depth of Field:        | Off      | Off      | Off      | On       | On       |
| Motion Blur:           | Off      | Off      | On       | On       | On       |
| Texture Quality:       | Low      | Low      | Medium   | Medium   | High     |
| Anisotropic Filtering: | None     | 2x       | 4x       | 8x       | 16x      |
| Anti-Aliasing:         | None     | Low      | Low      | Medium   | High     |
| FX:                    | Low      | Low      | Medium   | High     | Amazing  |
| Lighting:              | Very Low | Low      | Medium   | High     | Amazing  |
| Shadows:               | Very Low | Low      | Medium   | High     | Amazing  |
| City Life Density:     | Low      | Low      | Medium   | Medium   | High     |
| Draw Distance:         | Low      | Low      | Medium   | Medium   | High     |
|-------------------------------------------------------------------------------|

Notes:
* These registry files changes vertical sync as well.

* The game is locked to 30 FPS with in-game Vertical Sync enabled, and 62 FPS with Vertical Sync disabled. It's therefore recommended to disable Vertical Sync using the separate registry files included in folder "5. Vertical Sync" and force vertical sync through the display drivers instead. This will ensure locked 60 FPS 

* Setting Graphics Preset to Custom only changes a single thing: GraphicsPreset = 5. I have no idea what this is for, but it's possible that it tells the game to follow the QualitySettings registry key and ignore internal safety performance checks.

* Draw Distance can be raised to Amazing. This is EXTREMELY PERFORMANCE INTENSE, even on a high-end computer in 2017 on all resolutions. Because this setting is changed through the QualitySettings registry key, I've included "4. Amazing (inc. Draw Distance) - EXTREMELY TAXING!" which sets Amazing in everything including in Draw Distance.

* Minor Note: CityLifeDensity goes from 1->3 in GraphicsPreset.xml but from 0->2 in the registry, which is why Amazing sets the registry to 2.
