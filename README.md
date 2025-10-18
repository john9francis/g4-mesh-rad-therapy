# G4 Mesh Rad Therapy

A Geant4 application where the user can load in a mesh geometry and run radiation therapy with it.

# Todo
- [ ] Load G4 development environment
- [ ] Allow for import of mesh
- [ ] monoenergetic photon beam at first


# Docker dev environment
Docker image to use with devcontainers

Run command (macos)
```sh
docker run -id -v $(pwd)/:/home/g4-mesh-photon-therapy/ --name geant4 john9francis/geant4-debian:examples-datasets
```

# Compiling executable

(in linux container)
```sh
mkdir build
cd build
cmake -WITH_GEANT4_UIVIS=OFF ..
make -j10
./mesh_photon_therapy
```


# Useful websites
- [cadmesh for loading meshes into g4](https://github.com/christopherpoole/cadmesh)
- [Using TetGen to manually load in a tetrahedral mesh (much faster, but a lot more work on the coding side)](https://www.researchgate.net/publication/260510781_Fast_tessellated_solid_navigation_in_GEANT4)