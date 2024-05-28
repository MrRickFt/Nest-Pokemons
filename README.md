<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

# Ejecutar en desarrollo
1. Clonar el repositorio
2. Ejecutar 
```
npm install
```
3. Tener Nest CLI instalado
```
npm i -g @nestjs/cli
```
4. Levantar la base de datos
```
docker-compose up -d
```
5. Clonar el archivo __.env.template__ y renombrar la copia a __.env__

6. Llenar las variables de entorno definidas en el  __.env__

7. Ejecutar la aplicación de desarrollo en dev:
```
npm run start:dev
```

8. Reconstruir la base de datos con la semilla
```
http://localhost:3000/api/v2/seed
```

# Production Build
1. Crear el archivo ```.env.prod```
2. Llenar las variables de entorno para la producción
3. Crear la nueva imagen 
 ```
 docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
 ```

Puedes correr el contenedor luego del build también de esta forma:
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up
```

## Stack usado

<p align="left">
  <img src="https://www.svgrepo.com/show/331488/mongodb.svg" width="30" alt="MongoDB Logo" />
  <img src="https://nestjs.com/img/logo-small.svg" width="30" alt="NestJs Logo" />
  </p>
