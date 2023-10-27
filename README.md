# PETSIRD template for use cases

The purpose of this repo is to provide a starting point for other software that uses PETSIRD.

## Background
The [Emission Tomography Standardization Initiative (ETSI)](https://etsinitiative.org/)
is working towards establishing a standard for PET Raw Data, called PETSIRD ("PET ETSI Raw Data").

The specification uses the [yardl](https://aka.ms/yardl) tool to define the model. `yardl` can be used to read the specification (in the `model` directory) and generate an PI for both C++ and API to read/write PETSIRD data.

Currently, a draft model is defined in https://github.com/ETSInitiative/PRDdefinition.

CAVEAT: the draft model generates code in the `prd` namespace. Nevertheless, we have used PETSIRD here
in most places.

