# praktikum_new_diplom
Финальный проект курса ЯПрактикум по специализации Python-разработчик.

Проект сдаётся в два этапа. На первом этапе вы отдадите на проверку код, а на втором мы проверим инфраструктуру вашего проекта.

### Развертывание на локальном сервере

1. Установите на сервере `docker` и `docker-dompose`.
2. Создайте файл `/infra/.env`. Шаблон для заполнения файла нахоится в `/infra/.env.example`.
3. Выполните команду `docker-compose up -d --buld`.
4. Выполните миграции `docker-compose exec backend python manage.py migrate`.
5. Создайте суперюзера `docker-compose exec backend python manage.py createsuperuser`.
6. Соберите статику `docker-compose exec backend python manage.py collectstatic --no-input`.
7. Заполните базу ингредиентами `docker-compose exec backend python manage.py load_ingredients`.
9. Документация к API находится по адресу: <http://localhost/api/docs/redoc>.


### На втором этапе проверяется работа проекта в контейнерах в Яндекс.Облаке. 