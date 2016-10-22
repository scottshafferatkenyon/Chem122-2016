# Local geometry

The arrangement of atoms and lone pairs around a central atom defines a specific **local geometry**. The valence-shell-electron-pair-repulsion (VSEPR) model can predict these geometries. In this tutorial, you will:

- view the three-dimensional structure of molecules that illustrate various local geometries
- draw the projection of each molecule's structure, as it appears from different perspectives

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start a JSmol web app

Change into the directory `vsepr`. List its contents and confirm that the file `JSMol.html` exists. Open this file using the command `c9 open`.

```bash
    $ cd vsepr
    $ ls
    $ c9 open JSMol.html
```

The code in this file defines a web app called JSMol. To run it, go to the Cloud9 menu and click **Preview > Live Preview file**. This should cause a mini browser to appear in another pane and display the web app. By default, it should display a 3D representation of water. Resize the pane to ensure you can see the entire molecule.


## Rotate a molecule in JSMol

Click and drag on the web app, which rotates the molecule out of the plane of the screen. Hold down the `option` key and click-drag left-to-right; this should rotate the molecule *in* the plane of the screen. Finally, hold down the `shift` key and click-drag up and down; this should zoom in and out.


## Save a static image

Rotate the molecule until you like the perspective. Right click on the web app; a menu should drop down. Click **File > Export > Export PNG image**. JSMol will generate an image that you may download to your computer if you like. 


## Displaying a different molecule

This version of the web app always loads the file `current.mol` in the `vsepr` directory. This is a **Molfile**, which contains coordinates of the desired molecule. To display a different molecule, you simply copy its Molfile to `current.mol` using the terminal.

Use the `ls` command to find out what Molfiles are available. One of them should be `OCN.mol`, which contains coordinates for OCN<sup>-</sup>. Copy it to `current.mol`.

```bash
    $ ls
    $ cp OCN.mol current.mol
```

Then use the `Preview` command in the Cloud9 menu to restart the web app and load the new molecule.


## Exercise

Load each of the Molfiles in `vsepr/`. Follow the directions in class for orienting each molecule and then sketching it.

