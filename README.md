# 0.B. Installing thermo_pw

## Theory
`thermo_pw` is a QE-based driver package (developed by Dal Corso and collaborators) that automates and extends several multi-step DFT workflows already used in this repository — equation-of-state fitting, quasi-harmonic thermodynamic properties (Section 5), elastic constants, and related property calculations — by scripting the many individual `pw.x`/`ph.x` runs those workflows require, rather than needing that scripting done manually shell-script by shell-script. Because it is built as an add-on to QE rather than a standalone code, it must be compiled *inside* the same QE source tree it will drive, using a QE version it is explicitly compatible with (hence checking the QE version first). `make join_qe` merges thermo_pw's build files into QE's own `make.inc`/build system, after which QE's top-level `configure` and `make` need to be re-run so the combined build system picks up the newly added thermo_pw source, producing the `thermo_pw.x` executable alongside QE's existing binaries.

## Procedure
* Check your current QE version by typing pw.x
* https://dalcorso.github.io/thermo_pw/
* Download tar.gz files corresponding to your QE version
* Extract it
* Cut the thermo_pw folder and paste it inside the QE folder, where there are lots of other files and folders.
* Now, go inside thermo_pw, which is inside the QE folder, and there are lots of other files and folders
* Open Terminal and type the code
* make join_qe
* cd ..
* ./configure
* make thermo_pw
* thermo_pw.x
* congratulation!!!
* **Note:** the QE version downloaded for thermo_pw (Section 0.B) must match the QE version already compiled in Section 0 — a mismatched version is the most common cause of `make join_qe` or `make thermo_pw` failing.
