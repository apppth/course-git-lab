# Отчёт по Git, занятие 1

## Что сделал

1. Проверил `git config`: имя и email совпадают с аккаунтом GitHub.
2. Учебного репозитория от преподавателя не было, поэтому сделал свой `course-git-lab` с ветками `main` и `develop`.
3. Hotfix: `hotfix/apppth-typo` от `main`, поправил «Helo» в `sandbox/hello.txt`. Влил в `main` с тегом `v0.1.1`, потом в `develop`.
4. Фича `feature/apppth-intro` от обновлённого `develop`: ABOUT, NOTES, таблица Git Flow, `.env.example`. PR #1 в `develop`.
5. Конфликт: в `feature/apppth-title` и `feature/apppth-intro` по-разному поменял строку `title` в `sandbox/config.txt`. При слиянии получил конфликт, убрал маркеры, оставил обе части заголовка.
6. ДЗ в отдельной ветке `feature/apppth-hw1`: `pages/index.html` и `pages/styles.css`, PR тоже в `develop`.

## Команды, которыми пользовался чаще всего

- `git status`: после каждого шага, чтобы понимать, что в индексе
- `git switch -c`: новая ветка
- `git log --oneline --graph --all`: смотреть, что куда влилось
- `git merge --no-ff`: чтобы в истории было видно слияние hotfix
- `gh pr create --base develop`: PR сразу в правильную ветку

## Что было непонятно

Сначала не понял, зачем hotfix вливать ещё и в `develop`, если он уже в `main`. Дошло, когда посмотрел на граф: `develop` от `main` не обновляется сам, и без второго слияния следующий релиз снова привёз бы опечатку.
