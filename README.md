# PyBuilder: PySCF input builder and orbital viewer

**[Open PyBuilder](PyBuilder-integrated-orbitals.html)**

PyBuilder is a browser-based tool for preparing PySCF input scripts from molecular coordinates. It also provides a 3D molecule view and tools for inspecting molecular orbitals from Molden or orbital CUBE files.

## Getting started

1. Click **Open PyBuilder** above. If you downloaded the files, keep this README and `PyBuilder-integrated-orbitals.html` in the same folder, then open the HTML file in a browser.
2. Paste atom coordinates into **Coordinates**, or use **Open XYZ** to load a geometry. Click **Update Molecule** to refresh the 3D view.
3. Select the calculation settings, including the method, basis set, charge, and spin. For multireference calculations, enter the active electrons, active orbitals, and number of roots as appropriate.
4. Review the generated Python code. Use **Copy PySCF** to paste it into your editor, or **Download .py** to save it.
5. Run the saved Python script in an environment with PySCF installed. Check the molecular charge, spin, active space, and chosen method before submitting a calculation.

## Methods and visualization

The builder offers RHF, UHF, ROHF, and DFT as starting methods. Its second-method menu includes CASSCF, CASCI, ADC, and NEVPT2. Additional controls cover DFT functionals, ADC settings, SCF convergence, memory, and threads. Available combinations should be checked against the generated code and your installed PySCF version.

Use **Open Molden** to inspect orbitals and their phases. The orbital controls include orbital selection, isosurface level, phase colors, and display options. An orbital CUBE file can also be opened. In the animation panel, successive Molden orbitals are treated as frames; the `Ene=` field is a frame index there, not automatically a time in femtoseconds.

## What runs where

The page generates Python input and displays molecular data in your browser. It does not execute PySCF calculations or submit jobs to a cluster. You must run the downloaded script separately. The page loads 3Dmol.js and JSmol from external sources, so those viewer features may need an internet connection.

## Files

- [`PyBuilder-integrated-orbitals.html`](PyBuilder-integrated-orbitals.html): the application; open this file to use PyBuilder.
- `README.md`: this guide.
