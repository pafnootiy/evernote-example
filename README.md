# evernote-example
Упражнение на чтение кода. Взаимодействие с API Evernote.
## add_note2journal.py
Данный скрипт добавляет заметку в вашу записную книжку "Дневник", используя подготовленный шаблон заметки с указанием даты и дня недели.
### Запуск скрипта
python add_note2journal.py

### Пример запуска
$ python add_note2journal.py

Title Context is:

{
    "date": "2022-05-31",
    "dow": "вторник"
}
Note created: Создана заметка
Done


## dump_inbox.py
Данный скрипт позволяет выгружать заметки в консоль, по-умолчанию 10 штук.Также позволяет настроить отображение заметок в консоле.
Структуру  тех или иных параметров можно настроить указав флаги `True`,`False` у соответствующих полей.

Пример
 ```python
    resultSpec = NoteStore.NotesMetadataResultSpec(
        includeTitle=True,
        includeContentLength=True,
        includeCreated=True,
        includeUpdated=True,
        includeDeleted=False,
        includeUpdateSequenceNum=True,
        includeNotebookGuid=False,
        includeTagGuids=True,
        includeAttributes=True,
        includeLargestResourceMime=True,
        includeLargestResourceSize=True,
    )
``` 
### Запуск скрипта
python dump_inbox.py

### Пример запуска

$ python dump_inbox.py

--------- 1 ---------

Пробная

--------- 2 ---------

Эта заметка о том как..

--------- 3 ---------

Here is the Evernote logo:


## list_notebooks.py
Данный скрипт выводит в консоль все созданные блокноты и присваивает им уникальный идентификаторы
### Запуск скрипта
python list_notebooks.py

### Пример запуска
$ python list_notebooks.py

b21f395e-c032-3bad-9df2-43cc0d14b07f - Первый  
56e54ec4-e5df-4f31-a768-6705c09a7aa5 - test
## config.py
Файл конфигурации. 
Проект настраивается через переменные окружения, указываются в файле .env. Передача значений происходит с использованием pydantic[dotenv].
### Параметры 
* EVERNOTE_PERSONAL_TOKEN         -- Токен
* JOURNAL_NOTEBOOK_GUID	          -- Блокнота для записи заметок-шаблонов
* JOURNAL_TEMPLATE_NOTE_GUID	     -- Заметки-шаблона
* INBOX_NOTEBOOK_GUID	            -- Блокнот для получения заметок
