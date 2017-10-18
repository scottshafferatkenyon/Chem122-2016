# Molecular shape and architecture

Most molecules consist of several atoms connected in a particular network **architecture**, with chains, rings, branches, cages, or some combination thereof. While each center has its own local geometry, these may combine to form a complex molecular **shape**. In this tutorial, you will:

- draw the structural formula of linear-chain and branched molecules
- generate the SMILES string representing how a molecule's atoms are connected
- generate the three-dimensional coordinates from the SMILES string
- display each structure with Jmol 
- draw the projection of a 3D molecular structure 

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start the JSME web app

Search for an available JSME web app. (As of this writing, [Peter Ertl's demonstration page](http://peter-ertl.com/jsme/) works.) 

In JSME, click the single-bond tool (a simple line), and then click in the canvas area. It simply displays a line, which represents ethane (in **skeletal** notation). Click the double arrow button and **Copy as SMILES** (or click the smiley face button if available). Copy this string.


## Display the molecule in JSMol

Change into the directory `shape`. List its contents and confirm that the file `jmol-console.html` is there. Open it and **Run** it.

```bash
    $ cd shape
    $ ls
    $ c9 open jmol-console.html 
```

The Jmol `load` command can take a SMILES string and generate 3D coordinates for it based on VSEPR; just add a `$` in front of the string.

```java
    load $CC
    centerat average
```

Rotate the molecule and observe its appearance from different perspectives. 


## Exercise: generating the structure of alkanes

Draw the molecules below, generate their SMILES strings, and display each one using JSMol. 

- ethane: CH<sub>3</sub>CH<sub>3</sub>
- propane: CH<sub>3</sub>CH<sub>2</sub>CH<sub>3</sub>
- butane: CH<sub>3</sub>CH<sub>2</sub>CH<sub>2</sub>CH<sub>3</sub>
- 2-methylbutane: (CH<sub>3</sub>)<sub>2</sub>CH<sub></sub>CH<sub>2</sub>CH<sub>3</sub> *(This is based on butane, except you replace a H with a methyl group (CH<sub>3</sub>) branching at the 2nd C atom.)*
- isobutanol: (CH<sub>3</sub>)<sub>2</sub>CH<sub></sub>CH<sub>2</sub>CH<sub>2</sub>OH *(This is based on 2-methylbutane, except you replace a H with a hydroxyl group (–OH) at the end of the chain.)*


## Exercise: sketching alkanes

Follow the directions in class for orienting each molecule and then sketching it.
