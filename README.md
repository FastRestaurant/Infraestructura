# FastRestaurant - Infraestructura

Docker Compose para levantar el frontend, los microservicios y SQL Server en local.

## Requisitos

- Docker Desktop abierto.
- Repos clonados al mismo nivel:

```txt
GitHub/
  Infraestructura/
  MicroservicioAuth/
  MenuService/
  MicroservicioOrder/
  MicroservicioKitchen/
  MicroservicioStock/
  Frontend/
```

## Levantar

Crear el `.env` local:

```powershell
Copy-Item .env.example .env
```

Levantar todo:

```powershell
docker compose up -d --build
```

## URLs

```txt
Frontend  http://localhost:5053
Auth      http://localhost:5155/swagger
Menu      http://localhost:5127/swagger
Orders    http://localhost:5231/swagger
Kitchen   http://localhost:5207/swagger
Stock     http://localhost:5093/swagger
SQL       localhost,1433
```

## Credenciales de prueba

```txt
admin      / Admin123!
Ncamarero  / Camarero123!
Jcocinero  / Cocinero123!
Gcajero    / Cajero123!
```

## Detener

```powershell
docker compose down
```

Detener y borrar los datos de SQL Server:

```powershell
docker compose down -v
```
