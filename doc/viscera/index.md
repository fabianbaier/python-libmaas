# _Viscera_: High-level Python client API


## Some example code

```python
#!/usr/bin/env python3.5

from pprint import pprint

from maas.client import viscera


profile, origin = viscera.Origin.login(
    "http://localhost:5240/MAAS/", username="alice",
    password="wonderland")

# List all the tags.
print(">>> origin.Tags.read()")
pprint(origin.Tags.read())
print(">>> Or: list(origin.Tags)")
pprint(list(origin.Tags))

# List all the nodes.
print(">>> origin.Nodes.read()")
pprint(origin.Nodes.read())
print(">>> Or: list(origin.Nodes)")
pprint(list(origin.Nodes))
```
