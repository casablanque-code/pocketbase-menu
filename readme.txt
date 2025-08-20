## Содержимое

- `docker-compose.yml` — сборка двух контейнеров: PocketBase и Nginx
- `pocketbase/` — бинарный файл `pocketbase` будет запускаться отсюда
- `pb_data/` — данные PocketBase (автоматически сохраняются)
- `nginx/html/index.html` — HTML-страница для отображения меню
- `nginx/conf.d/default.conf` — конфигурация Nginx с маршрутизацией


# 1. Распаковать проект
unzip pocketbase.zip
cd pocketbase

# 2. Перейти в нужную папку и скачать бинарник
cd pocketbase
curl -L -o pocketbase.zip https://github.com/pocketbase/pocketbase/releases/latest/download/pocketbase_0.22.11_linux_amd64.zip
unzip pocketbase.zip
chmod +x pocketbase
cd ..

# 3. Заменить index.html на свой
cp /home/ubuntu/*menu_page_name*.html ./nginx/html/index.html
то же с dish.html

# 4. Запуск
docker compose up -d