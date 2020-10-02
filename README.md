# prestashop

```linux
docker network create prestashop-net
docker run -ti --name some-mysql --network prestashop-net -e MYSQL_ROOT_PASSWORD=admin -p 3307:3306 -d mysql:5.7
docker run -ti --name some-prestashop --network prestashop-net -e DB_SERVER=some-mysql -p 8080:80 -d prestashop/prestashop
```


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
