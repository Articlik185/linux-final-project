**Практика Linux и Bash**

Учебный сценарий работы с каталогами, файлами, правами доступа, поиском, сортировкой и перенаправлением вывода.

**Где смотреть решение**

[Ветка first-iteration](https://github.com/Articlik185/linux-final-project/tree/first-iteration) содержит task.sh. [Учебный PR №1](https://github.com/Articlik185/linux-final-project/pull/1) открыт. В main находится только precode.sh с условиями задания.

**Проверка и запуск**

Требуются Bash и стандартные утилиты Linux; под Windows можно использовать WSL. Скрипт создаёт и затем удаляет каталог task относительно рабочей директории. Для запуска используйте отдельную временную папку:

    git switch first-iteration
    bash -n task.sh
    script_path="$(pwd)/task.sh"
    work_dir="$(mktemp -d)"
    (cd "$work_dir" && bash "$script_path")
    rmdir "$work_dir"

Среди строк вывода ожидается «Всем студентам, привет!».

precode.sh — исходное задание; task.sh — решение. Перед запуском можно прочитать оба файла и сопоставить команды с комментариями.
