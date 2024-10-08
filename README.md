**Shell-emulator with GUI**
<br>

## 1. Общее описание
Shell Emulator — это эмулятор командной строки, который позволяет пользователям выполнять команды, такие как `ls`, `cd`, `head` и `wc`, в виртуальной файловой системе, основанной на архиве tar. Эмулятор обеспечивает графический интерфейс для удобного взаимодействия с командной строкой и файлами.

## 2. Описание всех функций и настроек
### Класс `ShellEmulator`
- **`__init__(self, user_name, host_name, vfs_path)`**: Инициализация эмулятора с заданным именем пользователя, именем хоста и путем к tar-архиву виртуальной файловой системы.
- **`load_vfs(self)`**: Загрузка виртуальной файловой системы из tar-архива.
- **`prompt(self)`**: Возвращает текст подсказки для командной строки.
- **`execute_command(self, command)`**: Парсит и выполняет введенную команду.
- **`ls(self)`**: Список содержимого текущего каталога.
- **`cd(self, path)`**: Изменяет текущий каталог.
- **`head(self, file_name)`**: Показывает первые строки файла.
- **`wc(self, file_name)`**: Подсчитывает количество строк, слов и символов в файле.
- **`exit_emulator(self)`**: Завершает работу эмулятора.

### Класс `ShellGUI`
- **`__init__(self, emulator, master=None)`**: Инициализация графического интерфейса с эмулятором.
- **`create_widgets(self)`**: Создает элементы интерфейса.
- **`display_output(self, text)`**: Отображает текст в области вывода.
- **`run_command(self, event)`**: Обрабатывает выполнение команды.

## 3. Описание команд для сборки проекта
Для сборки и запуска проекта необходимо выполнить следующие команды в терминале:

```bash

# Перейти в директорию проекта
cd <имя_директории>

# Запустить эмулятор
python main.py <username> <hostname> <path_to_tar>

To run unit tests yoo need execute this command: *python -m unittest test_shell_emulator.py*
```
## 4. Примеры использования
<img width="584" alt="image" src="https://github.com/user-attachments/assets/54b00eba-b476-4a86-9dea-ba7ff53ae774">

## 5. Результаты прогона тестов
$ python -m unittest test_shell_emulator.py
..
----------------------------------------------------------------------
Ran 5 tests in 0.012s

OK
