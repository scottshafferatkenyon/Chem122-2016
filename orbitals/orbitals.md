# Electronic structure of molecules

The shape of electrons in a molecule is 

Most molecules consist of several atoms connected in a particular network **architecture**, with chains, rings, branches, cages, or some combination thereof. While each center has its own local geometry, these may combine to form a complex molecular **shape**. In this tutorial, you will:

- load the output of a QM calculation with JSmol
- display the isosurface of a molecular orbital
- describe each MO's shape relative to atomic orbitals of isolated atoms

Before you start, make sure you have cloned the entire `Chem122-2016` repository into your Cloud9 workspace, which includes a Jmol server.


## Start a JSmol web app

Change into the directory `orbitals`. List its contents and confirm that the file `JSMol.html` exists. Open this file using the command `c9 open`.

```bash
    $ cd orbitals
    $ ls
    $ c9 open JSMol.html
```

The code in this file defines a web app called JSMol. To run it, go to the Cloud9 menu and click **Preview > Live Preview file**. This should cause a mini browser to appear in another pane and display the web app. By default, it should display a 3D representation of a Ne atom, with a wireframe surface of its 1s orbital superimposed on it. Resize the pane to ensure you can see the entire display.


## Display different orbitals

You can control the JSMol display using its internal menu. Right-click or Control-click anywhere on the app to bring up the menu, and then select: **Surfaces > Molecular Orbitals > #2**. JSMol will replace the 1s orbital with larger, 2s orbital. Repeat this for MO #3. You should now see a 2p orbitals instead; rotate it to confirm its shape. Repeat for MOs #4 and #5, which should look the same but aligned with different directions.


## Display a different molecule

This version of the web app always loads the file `current.out` in the `orbitals/` directory. This is a **GAMESS output** file that was produced by a quantum-mechanical calculation of a molecule's electronic structure. It contains the coordinates of the desired molecule and the shape of each molecular orbital. To display a different molecule, copy its `.out` file to `current.out` using the terminal.

Use the `ls` command to find out what `.out` files are available. One of them should be `N2.out`, which contains coordinates for N<sub>2</sub>. Copy it to `current.out`.

```bash
    $ ls
    $ cp N2.out current.out
```

Then use the `Preview` command in the Cloud9 menu to restart the web app and load the new molecule.


## Exercise: Nitrogen

Load the GAMESS output for nitrogen. It displays the molecule with the bond axis parallel to the *x* axis. The lowest-energy molecular orbital, MO #1, shows the electron density highly localized to just the atomic centers. Display MO #2, which looks nearly identical except for opposite phase on each atom. 

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
