готов
1) Учебный сервис предварительной оценки заявки на заём под ПТС: принимает заявку (VIN, год, пробег, оценочная стоимость, сумма, срок), считает LTV и возвращает решение `approve` / `review` / `reject`.
2) `make up` (docker compose up -d --build, сервис на 8080), `make test` (PHPUnit), `make lint` (php -l), `make down`, `make seed`, `make logs`, `make ps`, `make help`; в docker-compose.yml — сервисы `backend` (php -S на 8080) и `db` (mysql:8.0, порт 3307).
3) Решение считается в `backend/src/Domain/` (DecisionEngine.php).
модель: training-2026-09-minimax-m3
