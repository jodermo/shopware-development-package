# Shopware 6 - Development Package
### ***this repository includes all\* you need for developing [Shopware 6](https://www.shopware.com) plugins***

*\* only Docker has to be installed*

###### *© 2021 - Moritz Petzka - [petzka.com](https://petzka.com/)*


### File Structure
- [log/](./log) *[shopware log files]*
- [plugins/](./plugins) *[directory for extension development]*
- [docker-compose.yml](./docker-compose.yml)


***Your extensions from inside the [plugins](./plugins) directory, automatically will be synchronized with the docker image***

***Log files from Shopware automatically will be dropped in the [log](./log) directory***

<br>

## Docker Deployment

#### Start Shopware 6 in Docker
- Run: `docker-compose up -d`

#### URLs in web browser
- Shopware Frontend : [http://localhost](http://localhost/)
- Shopware Backend : [http://localhost/admin](http://localhost/admin)
  - Username: `admin`, Password: `shopware`



## Change Shopware Version
You can change the Shopware Version to any other version, inside the [docker-compose.yml](./docker-compose.yml) file:
```yml
services:
  
  shopware:
    image: dockware/dev:latest
```
use either tag `latest` or any other version like `6.1.5`, e.g:

```yml
services:
  
  shopware:
    image: dockware/dev:6.1.5
```

<br>

## Download Shopware to the System
Download the current version of Shopware to your host into a `src` directory:
```
mkdir -p ./src
docker cp shopware:/var/www/html/. ./src
```

<br>

## Shopware Documentations

- [Official Shopware 6 Developer Documentation](https://developer.shopware.com/docs/)
  - [Developer Guides ](https://developers.shopware.com/developers-guide/)
    - [Developing plugins ](https://developers.shopware.com/plugin-guide/)
      - [Plugin quick Startup Guide](https://developers.shopware.com/developers-guide/plugin-quick-start/)
    - [Tutorials ](https://developers.shopware.com/developers-guide/tutorials/)