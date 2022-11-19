
# Mass media analytics and data collection

This project for University helpers in analyze mass media 


## Tech Stack

**Client:** Vue, Vuex

**Server:** Node(Nest js), Python, Ruby, Java


## Deployment develop

Build project for developers

Требуется находится в корневой директории -> Mass media

```bash
  docker compose -f docker-compose-develop.yml up --build -d
```

## Deployment production

Build project for production version

Требуется находится в корневой директории -> Mass media

```bash
  docker compose -f docker-compose-production.yml up --build -d
```

## Deployment helpers

Наблюдать за тем, пока все сервисы установятся

```bash
  docker compose -f docker-compose-develop.yml --follow
```
Потушить контейнеры

```bash
  docker compose -f docker-compose-develop.yml down
```

Зайти в сервис "name service" -> node-engine

```bash
  docker compose -f docker-compose-develop.yml exec "name service" bash
```
## Authors

- [@Даниил](https://vk.com/luckydanyel)
- [@Юра](https://vk.com/exe_shnik)
- [@Алим](https://vk.com/id504461497)
- [@Денис](https://vk.com/id171573907)
- [@Влада](https://vk.com/vladavarmaz)
- [@Света](https://vk.com/id161375814)
