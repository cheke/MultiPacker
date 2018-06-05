# Output Assets

## MultiPacker Graph

![MPGraph](/MultiPacker/Images/assetMP.jpg)

- This is the default Asset of MultiPacker.
- The Graph process all the nodes to get the Assets Outputs, **all the Nodes are a Reference on the Asset**.
- The goal of MultiPacker is to have on minimal textures what you need, alowing you to save space, time loading and time developing with a fast system to work with them.
- Because for that **include the MultiPacker Graph on your Final Project is an Error**, if you include the Asset all the references will be included also, with the result you dont save space at all.
- All the Data needed for the nodes are on the **MultiPacker Database Asset**.

![References](/MultiPacker/Images/AssetReference.png)

## Output Texture

![Tex](/MultiPacker/Images/AssetTex.jpg)

-This Texture Combines the result of all the nodes of the MultiPacker Graph, Depending of the option you will have one or Multiple Texture Outputs.

## MultiPacker Database

![Database](/MultiPacker/Images/AssetDatabase.jpg)

-On the MultiPacker Database all the Individual *Tiles* had a name and a association with their values, work with the Database allows a fast iteration to create new assets loading the *Tile* needed with the only information of the Name.

## MultiPacker Material Collection

![MAtCol](/MultiPacker/Images/AssetMatCol.jpg)

-This Material Parameter Collection is like the Database but this intended to use on Materials Only, allows a fast use of the *Tiles* with the freedom of the Material Graph system, Its a little more complicated but its explained here with [Material Functions](https://cheke.github.io/MultiPacker/Doc/MaterialFunctions).

-Material Collection and MultiPacker Database Screenshot

![captures_database](/MultiPacker/Images/captures_database.jpg)

[**Home Docs**](https://cheke.github.io/MultiPacker)
