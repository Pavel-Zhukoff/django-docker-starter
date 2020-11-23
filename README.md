# Набор быстрого запуска приложения Django в связке gunicorn+nginx+postgres
В файле `env.example` лежат необходимые параметры для быстрого запуска приложения.
По-муолчанию в качестве БД используется PostgreSQL, но ее можно сменить при желании.
Докер имеет 2 варианта запуска dev и prod, расположенные в `docker-compose.dev.yml` и `docker-compose.prod.yml` соответственно. В prod варианте nginx стартует на 80 порте.
Контейнеры объеденены общей сетью, и выход "наружу" имеет только nginx.
## Запуск dev
`docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d`
## Запуск prod
`docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d`