# PETSIRD template for C++ use cases

The purpose of this repo is to provide a starting point for developing software that uses PETSIRD.
It is currently mostly needed/useful for C++ development.

## Background
The [Emission Tomography Standardization Initiative (ETSI)](https://etsinitiative.org/)
is working towards establishing a standard for PET Raw Data, called PETSIRD ("PET ETSI Raw Data").
More information is on https://github.com/ETSInitiative/PETSIRD.

## How to use this template?

These instructions will use `YourRepoName` for the name of your new repository. Obviously replace it with something appropriate.

#### Create a new repository based on this template

Easiest is to start from GitHub:
1. Navigate to the URL of this repo: https://github.com/ETSInitiative/PETSIRDUseCaseTemplate
2. Click on the `Use this template` button and create your own repo

### Using your repo

1. Open ***your*** repo in [GitHub Codespaces](https://code.visualstudio.com/docs/remote/codespaces) or
in a [VS Code devcontainer](https://code.visualstudio.com/docs/devcontainers/containers).
This codespace/container will contain all necessary tools, including `yardl` itself, as well as your repository.<br>
(Alternatively, clone to your local computer with `git clone --recurse-submodules <repository_url>`, download `yardl`, install dependencies etc.)
2. Start with basic house-keeping
   1. Search-and-replace all occurences of `PETSIRDUseCaseTemplate` with `YourRepoName`
   2. Update the README.md to remove references to this template and write something about what your repo is going to do
   3. Update the `environment.yml`to include what you need. For instance, if you need ROOT, add something like `- root=6.28.0`
   4. Make some other basic changes and commit
      ```sh
      git commit -a -m "Updated template to YourRepoName"
      git push
      ```
3. Start working in the [`cpp`](cpp/README.md) directory.
4. Edit the [`justfile`](justfile), e.g. to add a `@run` target
5. type `just build` (or `just run`)

Note: if you don't want to use `just`, you will have to use `yardl` to generate C++ and Python
code for the model:
```sh
cd YourRepoName
cd PETSIRD/model
yardl generate
cd ../..
```


