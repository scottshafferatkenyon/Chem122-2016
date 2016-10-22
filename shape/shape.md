# Molecular shape and architecture

Most molecules consist of several atoms connected in a particular network **architecture**, with chains, rings, branches, cages, or some combination thereof. While each center has its own local geometry, these may combine to form a complex molecular **shape**. In this tutorial, you will:

- draw the structural formula of linear-chain and branched molecules
- generate three-dimensional coordinates for each molecule's atoms and bonds
- display each structure with Jmol 
- draw the projection of a 3D molecular structure 

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start the JSME web app

Change into the directory `shape`. List its contents and confirm that two files are there: `JSME.html` and `JSMol.html`. Open them both.

```bash
    $ cd shape
    $ ls
    $ c9 open JSMol.html JSME.html 
```

The code in `JSMol.html` defines a web app called JSMol. To run it, go to the Cloud9 menu and click **Preview > Live Preview file**. This should cause a mini browser to appear in another pane and display the web app. By default, it should display a 3D representation of water. Resize the pane to ensure you can see the entire molecule.

`JSME.html` is another web app called the **JavaScript Molecular Editor**. Run this one in the same way; it should create a browser in another tab.

In JSME, click the single-bond tool (a simple line), and then click in the canvas area. It simply displays a line, which represents ethane (in **skeletal** notation). Below the canvas click the button **Get JME string**, which should simply generate the a string starting with `2 1 C`.... This **JME string** is a special encoding of the structure of ethane. Copy this string.


## Display the molecule in JSMol

JSMol for this project is configured to load any molecule in the file `current.jme`. Open this file with `c9 open current.jme`. Select the JME string currently in the file and paste the JME string of ethane you copied earlier. Save the file.

Switch to the tab running JSMol. Use the `Preview` command in the Cloud9 menu to restart the web app and load the new molecule; you should now see ethane. Rotate the molecule and observe its appearance from different perspectives. 


## Exercise: alkanes

Draw the molecules below, generate their JME strings, and display each one using JSMol. Follow the directions in class for orienting each molecule and then sketching it.

- ethane: CH<sub>3</sub>CH<sub>3</sub>
- propane: CH<sub>3</sub>CH<sub>2</sub>CH<sub>3</sub>
- butane: CH<sub>3</sub>CH<sub>2</sub>CH<sub>2</sub>CH<sub>3</sub>

