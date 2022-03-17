# evernote-example
Упражнение на чтение кода. Взаимодействие с API Evernote.
## add_note2journal.py
Данный скрипт добавляет заметку в вашу записную книжку "Дневник", используя подготовденный шаблон заметки с указанием даты и дня недели.
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

## list_notebooks.py
Данный скрипт выводит в консоль все созданные блокноты и присваивает им уникальный идентификаторы
## config.py
Файл конфигурации. 
