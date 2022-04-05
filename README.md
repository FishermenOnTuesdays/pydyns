pydyns
==============

Python wrapper for [DynS's C++ library](https://github.com/FishermenOnTuesdays/DynamicSystem) built with [pybind11](https://github.com/pybind/pybind11).
This requires Python 3.6+

Installation
------------

 - clone this repository with `git clone --recurse-submodules -j8 https://github.com/FishermenOnTuesdays/pydyns.git`
 - `pip install ./pydyns`
 
 if you will encounter any errors, just try installing again, that should run like butter.

Test call
---------

```python
import pydyns
dynamic_system = ds.DynamicSystem([1,2,3], ["x2","x3","1/4*10^3*(0-220*10^(-3)*x3-1000*10^(-3)*x2-x1)"], 'x1,x2,x3')
dynamic_system.SetDt(0.001)
trajectory = dynamic_system.GetTrajectory(5)
```
