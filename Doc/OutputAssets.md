# Output Assets

## MultiPacker Graph

![MPGraph](/MultiPacker/Images/assetMP.jpg)

- This is the default Asset of MultiPacker.
- The Graph process all the nodes to get the Assets Outputs, **all the Nodes are a Reference on the Asset**.
- The goal of MultiPacker is to have on minimal textures what you need, alowing you to save space, time loading and time developing with a fast system to work with them.
- Because for that **include the MultiPacker Graph on your Final Project is an Error**, if you include the Asset all the references will be included also, with the result you dont save space at all.
- All the Data needed for the nodes are on the **MultiPacker Database Asset**.

![References](/MultiPacker/Images/AssetReference.png)

![OutputAssets](/MultiPacker/Images/sc_OutputAssets.jpg)

## 1 - Output Texture

-This Texture Combines the result of all the nodes of the MultiPacker Graph, Depending of the option you will have one or Multiple Texture Outputs.

## 2 - MultiPacker Database

-On the MultiPacker Database all the Individual *Tiles* had a name and a association with their values, work with the Database allows a fast iteration to create new assets loading the *Tile* needed with the only information of the Name.

## 3 - MultiPacker Material Collection

-This Material Parameter Collection is like the Database but this intended to use on Materials Only, allows a fast use of the *Tiles* with the freedom of the Material Graph system, Its a little more complicated but its explained here with [Material Functions](https://cheke.github.io/MultiPacker/Doc/MaterialFunctions).

-Material Collection and MultiPacker Database Screenshot

![captures_database](/MultiPacker/Images/captures_database.jpg)

## MultiPacker Runtime Graph

![MPGraph](/MultiPacker/Images/sc_multipackerRuntimeAsset.jpg)

- MultiPacker Runtime Graph its like the normal Graph but works on Runtime, Only works with Materials.
- The Graph process all the nodes and generates a RenderTarget.
- The goal of MultiPacker Runtime Graph is to make some Textures who can be created by shaders, like noise or some type of shaders baked on runtime, allowing save that memory cost on disk, and processing it on runtime.
- The Graph save on a Internal Database the location of the Tiles, saving the cost of Calculate the BinPacking on Runtime, but have some blueprint functions to set more Materials on runtime.
- At difference of MultiPacker Graph this Asset needs to be cooked and be on the Build.

[**Home Docs**](https://cheke.github.io/MultiPacker)
