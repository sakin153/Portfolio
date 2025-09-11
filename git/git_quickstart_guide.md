# Git - Быстрый старт для новичков

## Шаг 1: Установка

### Windows
1. Скачать Git с https://git-scm.com/download/win
2. Установить с настройками по умолчанию
3. Открыть Git Bash

### Linux (Ubuntu/Debian)
```bash
sudo apt install git
```

### macOS
```bash
brew install git
# или скачать с https://git-scm.com/download/mac
```

## Шаг 2: Первичная настройка

```bash
# Указать имя (обязательно)
git config --global user.name "Ваше Имя"

# Указать email (обязательно)
git config --global user.email "your.email@example.com"

# Проверить настройки
git config --list
```

## Шаг 3: Создание первого репозитория

### Вариант А: Начать с локального репозитория

```bash
# 1. Создать папку проекта
mkdir my-first-repo
cd my-first-repo

# 2. Инициализировать Git
git init

# 3. Создать первый файл
echo "# My First Repository" > README.md

# 4. Добавить файл в индекс
git add README.md

# 5. Сделать первый коммит
git commit -m "Add README file"
```

### Вариант Б: Клонировать существующий репозиторий

```bash
# Скопировать репозиторий с GitHub/GitLab
git clone https://github.com/username/repository.git
cd repository
```

## Шаг 4: Ежедневная работа

```bash
# Проверить статус (что изменилось)
git status

# Добавить изменения в индекс
git add filename.txt    # конкретный файл
git add .              # все изменённые файлы

# Зафиксировать изменения
git commit -m "Описание изменений"

# Отправить на сервер (если настроен удалённый репозиторий)
git push
```

## Шаг 5: Связь с GitHub

1. **Создать репозиторий на GitHub:**
   - Перейти на https://github.com
   - Нажать "New repository"
   - Указать имя и создать

2. **Связать локальный репозиторий с GitHub:**
```bash
# Добавить удалённый репозиторий
git remote add origin https://github.com/your-username/your-repo.git

# Отправить код в первый раз
git push -u origin main
```

## Основные команды на каждый день

```bash
# Проверить что происходит
git status

# Добавить файлы
git add .

# Зафиксировать изменения
git commit -m "Сообщение"

# Отправить на сервер
git push

# Получить изменения с сервера
git pull
```

## Полезные файлы

### .gitignore (игнорировать ненужные файлы)
Создать файл `.gitignore` в корне проекта:
```
# Игнорировать папку node_modules
node_modules/

# Игнорировать логи
*.log

# Игнорировать настройки IDE
.vscode/
.idea/

# Игнорировать конфигурацию
.env
```

### .gitkeep (сохранить пустые папки)
```bash
# Git не сохраняет пустые папки
# Чтобы сохранить пустую папку:
mkdir logs
touch logs/.gitkeep
git add logs/.gitkeep
```

## Частые ошибки новичков

### 1. Забыли настроить имя и email
**Ошибка:** `Please tell me who you are`
**Решение:**
```bash
git config --global user.name "Ваше Имя"
git config --global user.email "email@example.com"
```

### 2. Забыли добавить файлы в индекс
**Ошибка:** `nothing to commit`
**Решение:**
```bash
git add .
git commit -m "Your message"
```

### 3. Нет связи с удалённым репозиторием
**Ошибка:** `No such remote 'origin'`
**Решение:**
```bash
git remote add origin https://github.com/username/repo.git
```

## Проверочный чек-лист

- [ ] Git установлен (`git --version` показывает версию)
- [ ] Настроено имя (`git config user.name`)
- [ ] Настроен email (`git config user.email`)
- [ ] Создан первый репозиторий (`git init` или `git clone`)
- [ ] Сделан первый коммит (`git log` показывает коммиты)
- [ ] Настроен удалённый репозиторий (если нужен)

## Что дальше?

После освоения базы изучите:
- Работу с ветками (`git branch`, `git checkout`, `git merge`)
- Откат изменений (`git reset`, `git revert`)
- Просмотр истории (`git log`, `git diff`)
- Совместную работу (Pull Requests, конфликты)
- Git Flow (методология работы с ветками)
