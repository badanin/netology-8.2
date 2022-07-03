### Установка clickhouse и vector

По завершению установки служба `vector` передает данные журнала `journald` в `clickhouse`.

- Установка `clickhouse`
  - Загрузка `.deb` дистрибутивов `clickhouse-common-static`, `clickhouse-client`, `clickhouse-server` в директорию `/tmp`
  - Установка `clickhouse-common-static`, `clickhouse-client`, `clickhouse-server`
  - Запускается служба `clickhouse-server`
  - Задержка 10 на запуск службы
  - Создание базы данных и таблицы с помощью `clickhouse-client`

- Уситановка `vector`
  - Загрузка дистрибутива `.tar.gz`
  - Создается директория для распаковки `/opt/vector`
  - Распаковка `.tar.gz`
  - Создается символьная ссылка на исполняемые файл в `/usr/bin/vector`
  - Создается пользователь и группа `vector`
  - Создается символьная ссылка на файл службы `vector`
  - Создается директория хранения данных `vector`
  - Создается директория хранения сонфигурационного файла `vector`
  - Копируется сонфигурационный файл в `/etc/vector/vector.toml`
  - Запускается служба `vector`
