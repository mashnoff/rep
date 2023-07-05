# Многопоточный HTTP клиент + WebSocket сервер

Это инструкция по запуску и использованию многопоточного HTTP клиента и WebSocket сервера. Здесь описаны шаги для установки, настройки и запуска сервера и клиента.

## Требования

- Node.js (установленный на вашей системе)

## Установка и настройка

1. Склонируйте репозиторий с кодом проекта:

   ```
   git clone <ссылка_на_репозиторий>
   ```

2. Перейдите в каталог проекта:

   ```
   cd <каталог_проекта>
   ```

3. Установите зависимости для сервера:

   ```
   cd server
   npm install
   ```

4. Установите зависимости для клиента:

   ```
   cd ../client
   npm install
   ```

5. Настройте сервер:

   - Откройте файл `server.js` в текстовом редакторе.
   - В этом файле вы можете настроить следующие параметры:
     - `maxThreads` - максимальное количество одновременно выполняющихся потоков для загрузки контента.
     - `threadSpeed` - скорость загрузки контента для каждого потока.
     - `keywords` - список ключевых слов и соответствующих им URL-адресов.
   - Сохраните изменения.

## Запуск сервера

1. Перейдите в каталог сервера:

   ```
   cd server
   ```

2. Запустите сервер:

   ```
   npm start
   ```

   После запуска сервер будет доступен по адресу `http://localhost:6969`.

## Запуск клиента

1. Откройте новое окно командной строки (терминала).

2. Перейдите в каталог клиента:

   ```
   cd client
   ```

3. Запустите клиент:

   ```
   npm start
   ```

   После запуска клиент будет доступен по адресу `http://localhost:8080`.

## Использование

1. Откройте браузер и перейдите по адресу `http://localhost:8080`.

2. На странице клиента вы увидите поле ввода для ключевого слова. Введите ключевое слово и нажмите кнопку "Отправить".

3. Сервер передаст клиенту список URL, соответствующих ключевому слову.

4. В клиентском интерфейсе появится список URL. Выберите один URL из списка.

5. Клиент начнет загрузку контента с выбранного URL. В интерфейсе клиента будет отображаться статус загрузки: размер, количество запущенных потоков и прогресс загрузки.

6. После загрузки контента он будет сохранен в LocalStorage для возможности чтения оффлайн.

7. Вы можете просмотреть список загруженного контента, выбрать нужный элемент и просмотреть его.

## Ошибки

В случае возникновения ошибок, проверьте следующее:

- Убедитесь, что у вас установлена последняя версия Node.js.
- Убедитесь, что все зависимости успешно установлены.
- Проверьте настройки сервера в файле `server/config.js` и убедитесь, что они указаны корректно.

Если ошибка остается, обратитесь к документации проекта или создайте новый issue в репозитории на GitHub\GitLab\Bitbucket, предоставив подробную информацию о проблеме.
