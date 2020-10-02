# prestashop

```linux
import requests
import xmltodict


url = 'http://localhost:8080/api/carts/?ws_key=4EPECP9Y68EIQ8MZ3GLNP5BXQC7UT2DJ'

params = {
}

response = requests.get(url, params=params)
content = response.content
# ∫print(content)

doc_json = xmltodict.parse(content)
print(doc_json)

```
