- Latex and string formatting: `plt.title(r"Amplitudes $h_+$ ($\Lambda_1, \Lambda_2) = ({}, {}$)".format(lambda1, lambda2))`
- Reload packages into notebooks: `%load_ext autoreload %autoreload 2`

Download my own plot style
```python
# To get the relevant plot style
import requests
script_url = "https://raw.githubusercontent.com/ThibeauWouters/cheat_sheets/main/myploystyle.py"
exec(requests.get(script_url).text)
```


__JAX__


Show the architecture to the screen:
```python
net = MLP(layer_sizes = config.layer_sizes, act_func = config.act_func)
print(net.tabulate(jax.random.PRNGKey(0), jnp.ones(input_ndim)))
```

Use a specific GPU device:
```python
chosen_device = jax.devices()[2] # e.g. device with index 2
jax.config.update("jax_platform_name", "gpu")
jax.config.update("jax_default_device", chosen_device)
```
But even better, put this code at the top to select the GPU, but make sure it is placed BEFORE importing the relevant package
```python
import os
os.environ["CUDA_VISIBLE_DEVICES"] = "3"
```
