FROM # указываем базовый образ
LABEL # Метаданные образа
ENV # Переменные окружения
ARG # Переменные во время сборки
RUN # Команда во время сборки 
   # 1. shell форма - apt update && apt install -y iputils-ping
   # 2. exec форма - ["apt", "update", "&&", "apt", "install", "-y", "iputils-ping"]
COPY --from=build /hello / # --from=nginx:latest /etc/nginx/nginx.conf /nginx.conf
     --chown	
     --chmod
     --link	
     --parents	
     --exclude
   # Копировать файлы и каталоги
ADD --keep-git-dir=true or false # trueпозволяет сохранить .git каталог.
    --checksum # позволяет проверить контрольную сумму удалённого ресурса.
    --chown	
    --chmod	
    --link	
    --exclude 
   # Поддерживает функции извлечения файлов с удаленных URL-адресов и Git, а также автоматическое извлечение tar-файлов при добавлении файлов из контекста сборки (извлекаются только локальные tar-архивы). 
   # Если источником является URL-адрес удалённого файла, у получателя будут разрешения 600 (rw-------). Не поддерживает аутентификацию.
   # При добавлении из репозитория Git биты прав доступа для файлов составляют 644. Если у файла в репозитории установлен бит исполнения, его права доступа будут установлены на 755. Для каталогов установлены права доступа на 755.
   # ADD file1.txt file2.txt /usr/src/things/
   # ADD https://example.com/archive.zip /usr/src/things/
   # ADD git@github.com:user/repo.git /usr/src/things/
   # docker build --ssh default .  # Чтобы смонтировать сокет SSH-агента в сборку
WORKDIR # Рабочая директория
USER # Пользователь
CMD # Команда по умолчанию
ENTRYPOINT # Исполняемый файл по умолчанию
EXPOSE # Открытые порты
VOLUME # Том для хранения данных
HEALTHCHECK # Проверка состояния контейнера при запуске
SHELL # Указывает оболочку по умолчанию
ONBUILD # Отложенные инструкции
STOPSIGNAL # Сигнал при остановке

