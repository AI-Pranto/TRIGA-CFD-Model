### To launch the case file in Fluent using a local Ansys installation, We'll use [PyFluent](https://github.com/pyansys/pyfluent)

```python
import ansys.fluent.core as pyfluent

# lauch fluent
solver = pyfluent.launch_fluent(precision="double", processor_count=4, mode="solver", case_filepath="sqr_fuel_rod.cas")

# Initialize and solve
solver.solution.initialization.hybrid_initialize()
solver.solution.run_calculation.iterate(number_of_iterations=500)

# Save and exit
solver.tui.write_case_data("sqr_fuel_rod")
solver.exit()
```
