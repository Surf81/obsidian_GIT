## Редактирование старых коммитов

>Пользоваться осторожно! Можно потерять репозиторий!

Для редактирования старых коммитов используется маленькая хитрость. Находясь в ветке в команде `rebase` указать саму себя
[Подробнее про команду `rebase`](GIT%20%слияние%20%веток#git%20rebase)

```bash
git rebase -i HEAD~3
```

>Нужно указать коммит за один до того, который мы хотим изменить.
>Обязательно нужно изменить сообщение первого коммита, чтобы изменилась его хэш-сумма, иначе ничего не получится 

Список команд:
1.  **p**, **pick <коммит>** – просто использовать коммит, ничего не менять
2.  **r**, **reword <коммит>** – использовать коммит, но поменять его сообщение
3.  **e**, **edit <коммит>** – использовать коммит, но остановить ребейз, чтобы добавить в коммит больше файлов
4.  **s**, **squash <коммит>** – использовать коммит, объединив его с предыдущим
5.  **f**, **fixup <коммит>** – как **squash**, но удаляет информацию об объединенном коммите из истории.
