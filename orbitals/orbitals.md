# Electronic structure of molecules

According to quantum theory, each electron can spread itself out over all the nuclei in a molecule, often with a distinctive shape. Each shape, which is defined mathematically by a *wavefunction*, determines a portion of the molecule's energy. There are two qualitative trends: (a) larger, extensive shapes tend to have lower energy, and (b) shapes with more nodes tend to have higher energy. 

In this tutorial, you will:

- load the output of a QM calculation with JSmol
- display the isosurface of a molecular orbital
- describe each MO's shape relative to atomic orbitals of isolated atoms (i.e., LCAO notation)

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start a JSmol web app

Change into the directory `orbitals`. List its contents and confirm that the file `jsmol-console.html` exists. Open this file using the command `c9 open`.

```bash
    $ cd orbitals
    $ ls
#   N2.out  Ne.out  ethene.out  jmol-console.html  methane.out  orbitals.md
    $ c9 open jmol-console.html
```

The code in this file defines a web app called JSMol. To run it, go to the Cloud9 menu and select **Run > Run with... > Apache**; or click the **Run** button if it is available. This should cause a new console to appear, with the message `Starting Apache httpd, serving ...` and showing a link. Click on the link and open it (or copy and paste the link into a new tab. A new browser tab should open and display the web app. By default, it should display a model of a Ne atom.


## Display different orbitals

Information about orbital shape is stored in the file but not displayed by default. You can reveal each orbital using the `MO` command in the Jmol console. Molecular orbitals are numbered from lowest to highest energy, beginning at 1. Orbital #1 is represented by a wireframe surface of the 1s orbital superimposed on the atom.

```java
    mo on
    mo 1
```

Each time you use this command and change the number, the previous orbital will be replaced. You can also step through them using `next` instead of a number. In each case, JSMol replace the 1s orbital with the larger, 2s orbital, and then with a 2p orbital. Rotate it to confirm its shape. 

```java
    mo 2     // shows the 2s
    mo 3     // shows the 2p
    mo next  // shows a different 2p
```

Repeat for MOs #4 and #5, which should look the same but aligned with different directions, as you would expect for p orbitals.

You can change some aesthetic properties, such as the fineness of the wireframe (`MO resolution`) and the colors of in-phase and out-of-phase electron density (`MO color`).

```java
    MO resolution 16    // finer, but loads slowly
    MO resolution 8     // coarser, but loads quickly
    MO color green maroon 
    MO color peru indigo
```

## Displaying a different molecule

The `orbitals/` directory contains several files with a `.out` ending. Each is a **GAMESS output** file that was produced by a [quantum-mechanical calculation](https://github.com/garcias/build-gamess#build-gamess) of a molecule's electronic structure. It contains the coordinates of the desired molecule and the shape of each molecular orbital. You can display the molecule in any file by using the `load` command in the Jmol console to the right of the display. Use the `centerat` command to set the origin to the center of gravity (i.e., average) of the molecule. Do this for an N<sub>2</sub> molecule.

```java
    load Ne.out
    centerat average
```

(If in doubt, switch back to the Cloud9 console and use `ls` to find out what other output files are available.)


## Exercise: Nitrogen

Load the GAMESS output for nitrogen. It displays the molecule with the bond axis parallel to the *x* axis. The lowest-energy molecular orbital, MO #1, shows the electron density highly localized to just the atomic centers. MO #2 looks nearly identical except for opposite phase on each atom. 

**Sigma bonding.** Display MO #3, which shows electron density spread throughout both atoms, and is usually notated &sigma;(2s) because it most resembles a combination of a 2s atomic orbital from each N. MO #4 is also spread among both atoms, but has a node half-way between cutting the bond axis, so it is ntoated &sigma;*(2s). Draw representations of these MOs using linear combinations of atomic orbitals.

**Pi bonding.** MO #5 is spread among the atoms, but with a node containing the atoms and the bond axis. It is notated &pi;(2p), because it resembles two parallel 2p<sub>y</sub> orbitals, one from each atom. MO #6 looks exactly the same, but rotated 90º, as if formed from two parallel 2p<sub>z</sub> orbitals. Note that the energies listed for each one are identical, so they are considered degenerate. Draw representations of these MOs using linear combinations of atomic orbitals.

MO #7 is like MO #3 in that it spreads across the molecule, but it contains two nodes, each one centered on an atom. The placement of these nodes is reminiscent of the 2p<sub>x</sub> atomic orbitals, so it is notated &sigma;(2p). Draw a representations of this MO using a linear combinations of atomic orbitals. To see its antibonding counterpart &sigma;*(2p), display MO #10.


## Exercise: ethene

Load the GAMESS output for ethene. It displays the molecule with the bond axis parallel to the *x* axis, and H atoms contained in the *xy* plane. As with nitrogen, the lowest-energy orbitals, MOs #1 and #2, show the electron density highly localized to the atomic centers. 

MO #3 spreads throughout the entire molecule. It therefore resembles a combination of 2s orbitals from the two C atoms, and 1s orbitals from the 4 H atoms. Draw a representation of the MO using a linear combination of these atomic orbitals.

MO #4 looks similar, but with a node bisecting the C-C bond. Its character is more complex: it is antibonding with respect to the C-C bond, but *bonding* with respect to the C-H bonds. You can represent it using the same atomic orbitals as for MO #3, but with half the orbitals in the opposite phase.

Display MOs #5 and #6. They both have nodes located on the C atoms. Their representations should therefore have C 2p orbitals. How would you characterize their bonding character, with respect to different bonds?

Display MOs #7 and #8. MO #8 is especially interesting because its node contains the entire *xy* plane, so we call it *nonbonding* with respect to C-H bonds. Its representation should only involve orbitals from the C atoms.


## Exercise: methane

Load the GAMESS output for methane. It displays the molecule with each C-H bond directed diagonally between the three axes. The lowest-energy orbital, MO #1, shows the electron density highly localized to the C atom. 

Display MOs #2 through #9 and describe the bonding character of each one. Identify any that are degenerate. Decide how to represent each one using a linear combination of atomic orbitals.
