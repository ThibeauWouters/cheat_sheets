- Latex and string formatting: `plt.title(r"Amplitudes $h_+$ ($\Lambda_1, \Lambda_2) = ({}, {}$)".format(lambda1, lambda2))`
- Reload packages into notebooks: `%load_ext autoreload %autoreload 2`

Download my own plot style
```python
# To get the relevant plot style
import requests
script_url = "https://raw.githubusercontent.com/ThibeauWouters/cheat_sheets/main/myploystyle.py"
exec(requests.get(script_url).text)
```
