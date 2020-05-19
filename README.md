# BioImage-IT toolboxes

This repository contains a the configuration files of the toolboxes for the bioimage-IT project.
Toolboxes are organized as categories. A category correspond to an application like colocalization or tracking. Then categories are linked to each other with a parent child relationship. For example `particle tracking` is a sub-category of `tracking`.    


## Adding a toolbox

1. Open the toolboxes.json file
2. Add category like in the example below

```
{
    "id": "Object colocalization",
    "name": "Object colocalization",
    "thumbnail": "colocalization.png",
    "parent": "Colocalization"
}

```
**id** is the unique identifier of the toolbox, **name** is the printed name to the user, **thumbnail** is the image that illustrate the toolbox. This image file must be uploaded to the `thumbs/` directory of this repository, and parent is the **id** of the parent category in the toolbox. If a category has no parent, set `"parent": "root"`  

## Adding a tool

For the BioImage-IT project, there is no official tool repository. Each tool can be hosted anywhere as long as it has a public access. The file `tools.json` contains the list of the available tools. The link must point to a directory containing the tools wrappers (`*.xml` files) and toolboxes membership (`.shed` file).
For a tool to be accessible by the BioImage-IT tools (BioImagePy and BioImageApp), a tool have to be specified in this `tools.json` file.
