# Molecular shape and architecture

Most molecules consist of several atoms connected in a particular network **architecture**, with chains, rings, branches, cages, or some combination thereof. While each center has its own local geometry, these may combine to form a complex molecular **shape**. In this tutorial, you will:

- draw the structural formula of linear-chain and branched molecules
- generate three-dimensional coordinates for each molecule's atoms and bonds
- display each structure with Jmol 
- draw the projection of a 3D molecular structure 

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start the JSME web app

Change into the directory `shape`. List its contents and confirm that two files are there: `JSME.html` and `display.htm`. Open them both.

```bash
    $ cd shape
    $ ls
    $ c9 open display.htm JSME.html 
```

The code in `display.htm` defines a web app called JSMol. To run it, go to the Cloud9 menu and click **Preview > Live Preview file**. This should cause a mini browser to appear in another pane and display the web app. By default, it should display a 3D representation of water. Resize the pane to ensure you can see the entire molecule.

`JSME.html` is another web app called the **JavaScript Molecular Editor**. Run this one as well, it should create a browser in another tab.

In JSME, click the single-bond tool (a simple line), and then click in the canvas area. It simply displays a line, which represents ethane (in **skeletal** notation). Below the canvas click the button **Get smiles**, which should simply generate the string `CC`. This **SMILES** string is a special encoding of the structure of ethane. Copy this string.


## Install OpenBabel

OpenBabel is a molecular-file converter that can generate (approximate) 3D coordinates for a molecular structure. You can install using the `apt-get` command. Installation requires admin privileges, which you can invoke with `sudo`.

```bash
    $ sudo apt-get update
    $ sudo apt-get install obabel
```

## Generate coordinates for ethane

Use the `obabel` command to convert the SMILES string into a Molefile. The prefix `-:` tells `obabel` identifies the input as a SMILES string, while the prefix `-omol` tells it to produce a Molfile. Finally, `--gen3D` tells it to produce coordinates. The resulting output should show 8 lines of *xyz* coordinates.

```bash
    $ obabel -:"CC" -omol --gen3D
#  
#   OpenBabel10211622293D
#  
#    8  7  0  0  0  0  0  0  0  0999 V2000
#      0.9887   -0.0032   -0.0988 C   0  0  0  0  0  0  0  0  0  0  0  0
#      2.5006   -0.0032   -0.0988 C   0  0  0  0  0  0  0  0  0  0  0  0
#      0.6044   -0.9710    0.2370 H   0  0  0  0  0  0  0  0  0  0  0  0
#      0.6044    0.1900   -1.1048 H   0  0  0  0  0  0  0  0  0  0  0  0
#      0.6044    0.7715    0.5715 H   0  0  0  0  0  0  0  0  0  0  0  0
#      2.8849   -0.7778   -0.7690 H   0  0  0  0  0  0  0  0  0  0  0  0
#      2.8849   -0.1963    0.9072 H   0  0  0  0  0  0  0  0  0  0  0  0
#      2.8849    0.9646   -0.4345 H   0  0  0  0  0  0  0  0  0  0  0  0
#    1  2  1  0  0  0  0
#    1  3  1  0  0  0  0
#    1  4  1  0  0  0  0
#    1  5  1  0  0  0  0
#    2  6  1  0  0  0  0
#    2  7  1  0  0  0  0
#    2  8  1  0  0  0  0
#  M  END
#  1 molecule converted
```

Run the same command again, but use `>` at the end to send the output to a new file named `ethane.mol`. Then copy this file to `current.mol` for display in JSMol.

```bash
    $ obabel -:"CC" -omol --gen3D > ethane.mol
#   1 molecule converted
    $ cp ethane.mol current.mol
```

## Display the molecule in JSMol

Switch to the tab running JSMol. Use the `Preview` command in the Cloud9 menu to restart the web app and load the new molecule; you should now see ethane. Rotate the molecule and observe its appearance from different perspectives. 


## Exercise

Load each of the Molfiles in `vsepr/`. Follow the directions in class for orienting each molecule and then sketching it.

