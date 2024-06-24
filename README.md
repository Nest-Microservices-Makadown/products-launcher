# Products Launcher

Repositorio para lanzar los proyectos con Docker

## Dev

1. Clonar repo
2. Crear archivo .env
3. Ejecutar comando `git submodule update --init --recursive` para reconstruir submodulos
4. Crear archivos .env para cada submodulo (leer su respectivo README)
3. Ejecutar el comando `docker compose up --build`

### Pasos para crear los Git Submodules


1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)
```
git submodule add <repository_url> <directory_name>
```

ejemplos usados en este proyecto (reemplazar urls por los propios):
```
git submodule add https://github.com/Nest-Microservices-Makadown/client-gateway.git client-gateway
git submodule add https://github.com/Nest-Microservices-Makadown/products-ms.git products-ms
git submodule add https://github.com/Nest-Microservices-Makadown/orders-ms.git orders-ms
```


4. Añadir los cambios al repositorio (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
6. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```


## Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal. 

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.


## Recursos

https://www.prisma.io/docs/orm/overview/databases/mongodb

