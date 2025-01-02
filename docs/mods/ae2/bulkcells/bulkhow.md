---
title: How To Use?
description: Setup guidance for partitions and more
authors: 
 - Boold (Original Author)
 - ArcTrooper (Editor)
---

# *How to do X, Y, Z???*

Here comes the main dish

Up to this point, you should already know what bulk is and why it matters as well as the **items required** for it (refer to the requirements in the [Concepts](bulkconcept.md) Chapter)

## Partition

1. You need a Cell & Cell Workbench
    ![](img-bulk/booldPartition1.png)
2. Move your cell into the slot on top-right corner
    ![](img-bulk/booldPartition2.png)
3. Move your desired items to partitions into the 7x9 empty slots (it's only 1 for Bulk Cells). You can drag from **inventory or JEI/EMI**
    ![](img-bulk/booldPartition3-jei.png) ![](img-bulk/booldPartition3-inv.png)

    !!! tip "Quick Tip"
        You can do ++shift+lbutton++ to quickly assign the items into the empty slot.

4. This step will vary, depending on what cell you used. Generally this is when you install **Card Upgrades** for the partitioned cells. Mainly **Overflow Destruction** and/or **Equal Distribution**

???+ tip "Bulk Cells only accept **Compression Cards**"
    !!! danger "They can't do any compression if there's no compression card installed"
    ![](img-bulk/booldPartition4-reg.png) ![](img-bulk/booldPartition4-bulk.png)
    !!! note "The ++shift+lbutton++ trick also applies when installing card upgrades"

## Basic Functional Setup

With the importance of **Decompression Module** & **Priority System**, at the very least your network should look like this.
![](img-bulk/booldBulkSetup.png)

* Top-left drive bay is for 'General Storage' with the lowest/lower priority
* Bottom-left drive bay is for 'Bulk Storage' with ** the highest priority**/higher than the general storage's
* **Decompression Module** is crucial to allow this network to decompress items stored inside a bulk cell
* Because they make a *ghost-pattern*, a basic **CPU multiblock** required (otherwise you can't decompress things)


> Applied Energistics 2 | [CurseForge](https://legacy.curseforge.com/minecraft/mc-mods/applied-energistics-2)  
> MEGA Cells | [CurseForge](https://legacy.curseforge.com/minecraft/mc-mods/mega-cells)  
> ExtendedAE | [CurseForge](https://legacy.curseforge.com/minecraft/mc-mods/ex-pattern-provider)
