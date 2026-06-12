# DOTNET CLEAN ARCHITECTURE TEMPLATE

При использовании команды dotnet new Capi -n MyProject создаётся следующая структура:
```
MyProject/
├── README.md                 # Инструкции по проекту
├── MyProject.API/            # Слой Web API
├── MyProject.Application/    # Бизнес-логика
├── MyProject.Domain/         # Доменные модели
└── MyProject.Infrastructure/ # Данные и внешние сервисы
```
## БЫСТРЫЙ СТАРТ
- Добавить источник GitHub Packages
Создайте Personal Access Token на GitHub с правами
read:packages и выполните:

Шаблон
``dotnet nuget add source https://nuget.pkg.github.com/<GITHUB_USERNAME>/index.json \
  --name <CUSTOM_NUGET_NAME> \
  --username <YOUR_GITHUB_USERNAME> \
  --password <YOUR_PERSONAL_ACCESS_TOKEN> \
  --store-password-in-clear-text``

- Установить шаблон
``dotnet new install cone-prog.cleanarchitecture.template``

- Использовать шаблон
```
# Создать новый проект
dotnet new Capi -n MyMicroservice

# Перейти в проект и запустить
cd MyMicroservice
dotnet build
dotnet run --project MyMicroservice.API
```

# Управление шаблоном
- Проверить установку:
``dotnet new list``
- Обновить шаблон:
``dotnet new install cone-prog.cleanarchitecture.template --force``
- Удалить шаблон:
``dotnet new uninstall cone-prog.cleanarchitecture.template``
- Удалить источник:
``dotnet nuget remove source github_cone-prog``
