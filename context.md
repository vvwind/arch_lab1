# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(admin, "Администратор")
Person(moderator, "Модератор")
Person(user, "Пользователь")

System(conference_site, "Сайт конференций", "Веб-сайт для работы с конференциями")



Rel(admin, conference_site, "Просмотр, добавление и редактирование информации о пользователях, докладах и конференциях")
Rel(moderator, conference_site, "Модерация контента и пользователей")
Rel(user, conference_site, "Регистрация, просмотр/изменение информации о конференциях и докладах")



@enduml
```
## Назначение систем
|Система| Описание|
|-------|---------|
| Сайт конференций | Веб-интерфейс, обеспечивающий доступ к информации по конференциям и докладам. Бэкенд сервиса реализован в виде микросервисной архитектуры |
