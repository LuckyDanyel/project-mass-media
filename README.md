// - сборка проекта для разработки
// Для сборки проекта в режиме develop требуется находится в корневой директории -> Mass media и прописать команду
docker compose -f docker-compose-develop.yml up --build -d
// Надо будет подождать пока все все сервисы установятся, наблюдать за этим можно:
docker compose -f docker-compose-develop.yml --follow

// Для того чтобы потушить контейнеры прописываем:
docker compose -f docker-compose-develop.yml down
// Зайти в сервисы:
docker compose -f docker-compose-develop.yml exec "name service" bash
// Пример
docker compose -f docker-compose-develop.yml exec node-engine bash


// - сборка проекта для production
// Для сборки проекта в режиме production требуется находится в корневой директории -> Mass media и прописать команду
docker compose -f docker-compose-production.yml up --build -d
// Надо будет подождать пока все все сервисы установятся, наблюдать за этим можно:
docker compose -f docker-compose-production.yml --follow

// Для того чтобы потушить контейнеры прописываем:
docker compose -f docker-compose-production.yml down
// Зайти в сервисы:
docker compose -f docker-compose-production.yml exec "name service" bash
// Пример
docker compose -f docker-compose-production.yml exec node-engine bash