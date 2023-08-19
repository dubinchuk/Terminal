### Homework #1 Basic Linux commands / GitBash

**1. Посмотреть где я**
```
pwd
```
**2. Создать папку**
```
mkdir folder1
```
**3. Зайти в папку**
```
cd folder1
```
**4. Создать 3 папки**
```
mkdir folder2 folder3 folder4
```
**5. Зайти в любоую папку**
```
cd folder2
```
**6. Создать 5 файлов (3 txt, 2 json)**
```
touch 1.txt 2.txt 3.txt 1.json 2.json
```
**7. Создать 3 папки**
```
mkdir folder5 folder6 folder7
```
**8. Вывести список содержимого папки**
```
ls
```
**9. Открыть любой txt файл**
```
vim 1.txt
```
**10. Написать туда что-нибудь, любой текст.**
Нажать `i` или `Insert` для начала редактирования файла и написать:
```
Simplified testing classification
By code execution:
- Static testing
- Dynamic testing
By access to application code and architecture:
- White box method
- Black box method
- Gray box method
By automation level:
- Manual testing
- Automated testing
By specification level (by testing level):
- Unit testing
- Integration testing
- System testing
By functions under test importance (decreasingly) (by functional testing level):
- Smoke testing
- Critical path testing 
- Extended testing
By ways of dealing with application:
- Positive testing
- Negative testing
```
**11. Сохранить и выйти.**

Нажать `Esc` → `:wq` → `Enter`

**12. Выйти из папки на уровень выше**
```
cd ..
```
**13. Переместить любые 2 файла, которые вы создали, в любую другую папку.**
```
mv folder2/{1.json,1.txt} folder3
```
**14. Скопировать любые 2 файла, которые вы создали, в любую другую папку.**
```
cp folder2/{2.json,2.txt} folder2/folder5
```
**15. Найти файл по имени**
```
find -name 2.json
```
**16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает.**

`tail -f folder3/1.txt | grep "testing"` - вывод строк с совпадением по тексту "testing" из файла 1.txt в терминал

Нажать `Ctrl+C` для выхода

**17. Вывести несколько первых строк из текстового файла**
```
head -n 7 folder3/1.txt
```
**18. Вывести несколько последних строк из текстового файла**
```
tail -n 5 folder3/1.txt
```
**19. Просмотреть содержимое длинного файла (команда less) изучите как она работает.**
```
less folder3/1.txt
```
Нажать `q` для выхода

**20. Вывести дату и время**
```
date
```
___

#### Задание *
**1. Отправить http запрос на сервер. http://162.55.220.72:5006/terminal-hw-request**
```
curl "http://162.55.220.72:5006/terminal-hw-request"
curl "http://162.55.220.72:5005/get_method?name=Evgeny&age=35"
```
**2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13**
Создаём файл hw_1.sh с содержимым:
```
#!/bin/bash
cd folder1
mkdir folder2 folder3 folder4
cd folder2
touch 1.txt 2.txt 3.txt 1.json 2.json
mkdir folder5 folder6 folder7
ls
mv 1.json 1.txt folder5
```
Запуск скрипта в Git Bash: `bash hw_1.sh`
