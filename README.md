# print_torch

It is often overwhelming to `print(tensor)` which may flash your screen and you just don't get any information useful.

Instead, use 

```
from print_torch import pt

pt(tensor)
```

and it will give you the size, dtype, device, min, max, std, mean, whether has nan, etc. in one line.

It also works for list of numbers and numpy tensors.

If you have a nested dict/list of pytorch/numpy tensors, you can also `pt` it, and it will list each element which may be again a tensor in one line.

For example, you can just `pt(locals())` in your `forward()` function to know all the stats of your local variables.

Don't hesitate to add this tool to your pocket!

```
pip install print_torch
```
