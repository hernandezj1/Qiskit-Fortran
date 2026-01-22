# Qiskit-Fortran

**Experimental SWIG-based Fortran bindings for the Qiskit C API**

This repository contains a very early-stage experiment in exposing the **Qiskit C API** to **Fortran** using **SWIG for Fortran**. It is *not* intended for end users and is currently closer to a proof-of-concept than a polished library.

## Overview

The goal of this project is to acces the Qiskit C API from Fortran native code via SWIG-generated bindings. At the moment, this repository:

- Uses **SWIG for Fortran** to generate bindings from C headers
- Targets the **Qiskit C extension (cext) API**
- Produces a minimal, low-level Fortran module
- Has **no high-level abstractions**, safety checks, or usability guarantees


## Repository Contents

The repository currently contains only two files:

- `fortranqiskit.f90`  
  The generated Fortran source file containing bindings to the Qiskit C API.

- `fortranqiskit.mod`  
  The corresponding compiled Fortran module file.

These files are intended for experimentation and inspection rather than direct consumption.

## Dependencies & Tooling

This project relies on:

- **SWIG for Fortran**  
  https://github.com/swig-fortran/swig

- **ORNL SWIG–Fortran instructions**  
  Based on guidance from Oak Ridge National Laboratory:  
  https://info.ornl.gov/sites/publications/Files/Pub158443.pdf

- **Qiskit C API**  
  The original C API exposed by Qiskit:  
  https://github.com/Qiskit/qiskit/tree/main/crates/cext


## Intended Audience

This repository is primarily useful for:

- Experimentation with SWIG Fortran bindings
- Exploration of calling Qiskit’s C API from Fortran
- Compiler / interoperability research

