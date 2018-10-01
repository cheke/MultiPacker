# MultiPacker Graph

Create an MultiPacker like another assets

![Marketplace](/MultiPacker/Images/MultiPackerGraphAssetCreation.jpg)
![Marketplace](/MultiPacker/Images/assetMP.jpg)

The MultiPacker Graph looks and works like the Material Graph but with have some little differences.

![Marketplace](/MultiPacker/Images/graph.jpg)

1. Toolbar Menu

    An explanation of the different buttons:

    1.1. "Apply Changes" Process the Graph.

    1.2. "Graph settings" show on the Details Panel the propertys of the graph.

    1.3. "Compile Materials" MultiPacker uses some materials on the internal Process to do the Output Texture, you need to press this button and compile all the materials who MultiPacker Graph needs, on the future I will try to set this automatically on the first run. Without the materials compiled the Output Texture will be show black.

    1.4. "Save" this saves the Graph

    1.5. "Browse" Show on the Content Browser where is the MultiPacker Graph Asset.

2. Graph Nodes

    Here you will have the Textures and Material Nodes to Process then and Make the Output Texture.

    Texture Nodes have 6 pins to select manually the Channel where you like to extract the Texture Information, also on the Details Panel for the Texture Node you can set the PinOutput.

3. Content Browser
    
    This is like a normal Content Browser from the Editor, you can drag and drop Textures and Materials to the Graph, You can drop a Selection at the same time.

4. Details Panel
    
    On this Panel all the Information related to the Graph and the Nodes will show up, here you can change all the options.

[**Home Docs**](https://cheke.github.io/MultiPacker)
