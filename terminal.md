# Шпаргалка по командной строке (Terminal / Bash)

## Содержание
1. [Навигация по файловой системе](#навигация-по-файловой-системе)
2. [Просмотр содержимого](#просмотр-содержимого)
3. [Создание файлов и папок](#создание-файлов-и-папок)
4. [Копирование, перемещение и переименование](#копирование-перемещение-и-переименование)
5. [Просмотр файлов](#просмотр-файлов)
6. [Удаление](#удаление)
7. [Полезные приемы](#полезные-приемы)

---

## Навигация по файловой системе
```bash
pwd
# print working directory — показывает полный путь к текущей папке
# Пример:
# /Users/username/projects
cd ~
# cd — change directory
# ~ — символ домашней директории
# Пример: из /usr/local/bin вы попадете в /Users/username
cd ..
# .. — обозначение родительской папки (на уровень выше)
# Пример: из /Users/username/projects вы попадете в /Users/username

# Клавиша Tab — автоматически дописывает имена файлов и папок
# Пример: набрать cd Docu + Tab → cd Documents/
# Если есть несколько вариантов, двойное нажатие Tab покажет все
```

## Просмотр содержимого
```bash
ls
# list — показывает содержимое текущей директории
# Пример вывода:
# Documents  Downloads  projects  file.txt
ls -a
# -a (all) — показывает все файлы, включая скрытые (начинающиеся с .)
# Пример вывода:
# .  ..  .bashrc  .git  Documents  file.txt
```

## Создание файлов и папок
```bash
touch filename.txt
# touch — создает пустой файл или обновляет время изменения существующего
# Пример:
touch script.js
# создаст файл script.js в текущей папке
mkdir folder_name
# make directory — создает новую папку
# Пример:
mkdir project
# создаст папку project в текущей директории
mkdir -p dir1/dir-inside/dir-deeper-inside
# -p (parents) — создает всю структуру папок, даже если промежуточных нет
# Пример: создаст папку dir-deeper-inside в папке dir-inside,
# которая находится в папке dir1 (все папки будут созданы)
```

## Копирование, перемещение и переименование
```bash
cp source destination
# copy — копирует файлы или папки
# Примеры:
cp file.txt backup.txt                    # копировать файл
cp file.txt ./folder/                      # копировать в папку
cp -r folder1 folder2                      # копировать папку целиком
mv source destination
# move — перемещает или переименовывает файлы и папки
# Примеры:
mv oldname.txt newname.txt                  # переименовать
mv file.txt ./Documents/                     # переместить
```

## Просмотр файлов
```bash
cat filename
# concatenate — выводит содержимое файла на экран
# Пример:
cat README.md
# выведет все содержимое файла README.md в терминал
```

## Удаление
```bash
rm filename
# remove — удаляет файл
# Пример:
rm temp.txt
# удалит файл temp.txt (безвозвратно)
rmdir folder_name
# remove directory — удаляет ТОЛЬКО пустые папки
# Пример:
rmdir empty_folder
# удалит empty_folder, если она пуста
rm -r folder_name
# -r (recursive) — рекурсивно удаляет папку и всё её содержимое
# Пример:
rm -r old_project
# удалит папку old_project со всеми файлами внутри
```

## Комбинирование команд
```bash
command1 && command2
# && (логическое И) — выполняет command2 только если command1 успешно завершилась
# Пример:
mkdir new_folder && cd new_folder
# создаст папку и сразу перейдет в нее
# Создать папку и перейти в нее
mkdir myapp && cd myapp

# Создать файл и открыть его в редакторе
touch notes.txt && nano notes.txt

# Скопировать и удалить оригинал (переместить)
cp file.txt backup.txt && rm file.txt

```


