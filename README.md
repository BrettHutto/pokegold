# Pokémon Gold and Silver [![Build Status][ci-badge]][ci]

This is a disassembly of Pokémon Gold and Pokémon Silver.

It builds the following ROMs:

- Pokemon - Gold Version (UE) [C][!].gbc
- Pokemon - Silver Version (UE) [C][!].gbc
- mons2_gld_ps3_debug.bin 
- mons2_slv_ps3_debug.bin 

To set up the repository, see [INSTALL.md](INSTALL.md).

---------------------------------------------------------------------------------------------------------------------------
## Changes made for this fork

This fork is here to make silver version not need trading to get gold exclusives/evolve pokemon, make all gen II pokemon available before post game in silver, and make evolution stones easily available before post game.

* pokemon added to each route (changes in: data\wild\johto_grass.asm, data\wild\johto_water.asm, data\wild\kanto_grass.asm):

    pkmn | routes | % chance
    -----|----------|------------
    murkrow | 43 night, 42 night | 20%, 20%
    misdreavus | Ilex Forest night | 10%
    sneasel | ice path | 1%
    slugma | route 35 | 4%
    houndour | route 38 | 30%
    larvitar | dark cave route 45 side | 30%
    mankey | route 9, 42 |30%, 30%
    primeape | route 9 | 5%
    growlithe | route 7, 8 (morn/day, night), 36, 37 | 5%, (5%, 4%), 5%, 5%
    spinarak | route 2 (night), 30 (night), 31 (night), 37 (night) | 30%, 30%, 30%, 40%
    ariados | route 2 (night) | 5%
    gligar | route 45 | 5%
    teddiursa | route 45 | 20%
    ursaring | route 28, victory road, Mt. Silver Exterior, Mt. Silver 1F, Mt. Silver 2F Mt. Silver Summit, Mt. Silver Chambers | 1%, 10%, 1%, 10%, 5%, 20%, 10%
    mantine | route 41 | 10%
    
* Pokemon that evolved through trade now evolve at these levels (changes in: data\pokemon\evos_attacks.asm):
 
   pkmn | level
   -----|------
   Kadabra | lvl 29
   Machoke | lvl 37
   Graveler | lvl 34
   Haunter | lvl 34
    
    additionally, pokemon that evolved through trade while holding an item still require the item, but now evolve through level (changes in: data\pokemon\evos_attacks.asm, engine\pokemon\evolve.asm):
    
   pkmn | level | held item
   -----|-------|----------
   Poliwhirl | lvl 34 | king's rock
   Slowpoke | lvl 33 | king's rock
   Onix | lvl 24 | metal coat
   Seadra | lvl 41 | dragon scale
   Scyther | lvl 25 | metal coat
   Porygon | lvl 20 | upgrade
    
* The poke mart in Mahogany town that is ran by the old lady now sells these items (changes in: data\items\marts.asm):

    Fire Stone
    
    Thunder Stone
    
    Water Stone
    
    Leaf Stone
    
    Moon Stone
    
    TM46 (Thief)
    
    Additionally, the price of the moon stone has been set to 2100 in data\items\attributes.asm
