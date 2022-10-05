## In order to run the simulation

First, convert Fluent mesh to foam format

```bash
fluentMeshToFoam fluent_mesh.msh -writeZones
splitMeshRegions -cellZones -overwrite
chtMultiRegionFoam
```
To plot residuals on the fly use [PyFoam](https://pypi.org/project/PyFoam/) `pyFoamPlotRunner.py chtMultiRegionFoam` 
