# Local geometry

The arrangement of atoms and lone pairs around a central atom defines a specific **local geometry**. The valence-shell-electron-pair-repulsion (VSEPR) model can predict these geometries. In this tutorial, you will:

- view the three-dimensional structure of molecules that illustrate various local geometries
- draw the projection of each molecule's structure, as it appears from different perspectives

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start a JSmol web app

Change into the directory `vsepr`. List its contents and confirm that the file `jmol-console.html` exists. Open this file using the command `c9 open`.

```bash
    $ cd vsepr
    $ ls
#   CH4.mol  NH3.mol  NO2.mol  NO3.mol  OCN.mol  PCl5.mol  SF4.mol  SF6.mol  XeF4.mol  jmol-console.html  vsepr.md  water.mol    
    $ c9 open jmol-console.html
```

The code in this file defines a web app called JSMol. To run it, go to the Cloud9 menu and select **Run > Run with... > Apache**; or click the **Run** button if it is available. This should cause a new console to appear, with the message `Starting Apache httpd, serving ...` and showing a link. Click on the link and open it (or copy and paste the link into a new tab. A new browser tab should open and display the web app. By default, it should show a 3D representation of caffeine. 

## Rotate a molecule in JSMol

Click and drag on the web app, which rotates the molecule out of the plane of the screen. Hold down the `option` key and click-drag left-to-right; this should rotate the molecule *in* the plane of the screen. Finally, hold down the `shift` key and click-drag up and down; this should zoom in and out.


## Save a static image

Rotate the molecule until you like the perspective. In the Jmol console to the right, enter the command `write image water.png`. JSMol will generate an image and prompt you to download to your computer (if you want). 


## Displaying a different molecule

The `vsepr` directory contains several files with a `.mol` ending. They are **Molfile**s, each containing the coordinates of a molecule. For example `OCN.mol` contains coordinates for OCN<sup>-</sup>. You can display the molecule in any file by using the `load` command with any Molfile in the Jmol console to the right of the display. Use the `centerat` command to set the origin to the center of gravity (i.e., average) of the molecule.

```Java
    load OCN.mol
    centerat average
```

(If in doubt, switch back to the Cloud9 console and use `ls` to find out what Molfiles are available.)

## Exercise

Load each of the Molfiles in `vsepr/`. Follow the directions in class for orienting each molecule and then sketching it.

