### In order to run the simulation using pythonic scripting interface, We'll use [MPh](https://github.com/MPh-py/MPh)

```python
import mph

client = mph.start()
model = client.load('sqr-fuel-rod.mph')

# create mesh and solve
model.mesh()
model.solve()

# save the model with its solution
model.save()
```
