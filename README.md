# prestashop

```linux
docker network create prestashop-net
docker run -ti --name some-mysql --network prestashop-net -e MYSQL_ROOT_PASSWORD=admin -p 3307:3306 -d mysql:5.7
docker run -ti --name some-prestashop --network prestashop-net -e DB_SERVER=some-mysql -p 8080:80 -d prestashop/prestashop
```

```linux
docker exec -i -t 4a414a7bcb70 /bin/bash
```

# Modificamos el docker de MySQL
```linux
mysql -u root -px1234567890
create database prestashop;
```

```linux
la bd se llama : some-mysql
```

```linux
la bd se llama : some-mysql
```

# Modificamos el docker de Prestashop
```linux
docker exec -i -t 4a414a7bcb70 /bin/bash
rm -r install
mv admin admin123
```

# Conectar desde Python
```
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
