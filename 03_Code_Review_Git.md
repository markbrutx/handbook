# Глава 3. Как отправить код на проверку (Git / GitHub)

Работаешь над задачей — значит, в какой-то момент нужно будет **отправить код на ревью**. Вот чёткий порядок действий:

---

## 1. Создай новую ветку под задачу

```bash
git checkout main
git pull
git checkout -b task66
```

`task66` — это номер задачи, над которой ты работаешь.  
В разных компаниях правила могут отличаться: `feature/task66`, `bugfix/66`, `fix-icon-bug` — вариантов много.  
Но если ты учишься у меня — называй ветку просто `task66`. Всё просто.

---

## 2. Почисти код

Открой `git diff` — в VS Code это `Ctrl + Shift + G`.  
Посмотри, **что ты изменил**, и **зачем ты это изменил**.

Пройдись по коду:

- убери лишние `console.log`
- выровняй отступы
- проверь названия переменных
- удали закомментированный мусор
- убедись, что код читабельный

---

## 3. Напиши понятный коммит

Коммит — это ответ на вопрос **"что делает этот код?"**.  
Не надо писать “fix” или “update”.

Примеры хороших коммитов:

```bash
git commit -m 'Добавляет переводы для всего приложения'
git commit -m 'Исправляет баг с иконкой в загрузочном экране'
```

---

## 4. Отправь ветку на GitHub

```bash
git push
```

Если это новая ветка — он сам подскажет, что нужно сделать:  
`git push origin task66`

---

## 5. Создай Pull Request (PR)

Иди на GitHub → появится кнопка “Compare & pull request” → нажимаешь.

- В заголовке укажи, что сделано: `task66 — добавляет переводы`
- В описании можешь кратко пояснить, если надо
- Ассайни ментора (меня)
- И **не забывай пинг**: просто напиши в тг.

## Всё. Ждёшь ревью.
