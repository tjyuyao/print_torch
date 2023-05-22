# print_torch

It is often overwhelming to `print(tensor)` which may flash your screen and you just don't get any information useful.

Instead, use `pt(tensor)` and it will give you the size, dtype, device, min, max, std, mean, whether has nan, etc. in one line.

```py
>>> import torch
>>> from print_torch import pt
>>> tensor = torch.randn((2,3,4,5))
>>> pt(tensor)
tensor(shape=(2, 3, 4, 5), dtype=float32, min=-2.803, max=2.49, std=1.019, mean=-0.06855, data=[-0.8246, -1.135, 0.1368, 1.56, ... ], device="cpu")                                  >>>
```

It also works for list of numbers and numpy tensors. 

If you have a nested dict/list of pytorch/numpy tensors, you can also `pt` it, and it will list each element which may be again a tensor in one line.

For example, you can just `pt(locals())` in your `forward()` function in the breakpoint to know all the stats of your local variables.

Don't hesitate to add this tool to your arsenal!

```sh
pip install print_torch
```
