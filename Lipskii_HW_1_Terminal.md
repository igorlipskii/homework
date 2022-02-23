1. Посмотреть где я\
 `pwd`
 
3. Создать папку\
`mkdir folder_1`

5. Зайти в папку\
`cd folder_1`

7. Создать 3 папки\
`mkdir folder_2 folder_3 folder_4`

9. Зайти в любоую папку\
`cd folder_2`

11. Создать 5 файлов (3 txt, 2 json)\
`touch file_1.txt file_2.txt file_3.txt j_1.json j_2.json`
13. Создать 3 папки\
`mkdir new_{1..3}`

15. Вывести список содержимого папки\
`ls -la`

17. Открыть любой txt файл\
`vim file_1.txt` (откроем через терминал) `open file_1.txt` (запустим программу)

19. Написать туда что-нибудь, любой текст.\
`i` `Hello world this is my first homework`

20. Сохранить и выйти.\
`esc`  `:`  `wq`

22. Выйти из папки на уровень выше\
`cd ..`

13. Переместить любые 2 файла, которые вы создали, в любую другую папку.\
`mv folder_2/{file_1,file_2}.txt folder_3`

15. Скопировать любые 2 файла, которые вы создали, в любую другую папку.\
`cp /users/igori/documents/HW/folder_1/folder_2/{j_1.json,file_3.txt} folder_2/new_1`

17. Найти файл по имени\
`find . -name "file_1.txt"`

19. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает.\
`tail -F folder_3/file_1.txt` или `tail -F folder_3/file_1.txt | grep 'this is my'`\
\* Команда grep даёт возможность вывести поиск строки `grep -i 'hello' folder_3/file_1.txt`
  
  
20. вывести несколько первых строк из текстового файла\
`head -3 /users/igori/documents/hw/lipskii_hw_1_terminal.txt`

22. вывести несколько последних строк из текстового файла\
`tail -4 ../lipskii_hw_1_terminal.txt`

24. просмотреть содержимое длинного файла (команда less) изучите как она работает.\
`less ../lipskii_hw_1_terminal.txt`

26. вывести дату и время\
`date "+%d.%m.%Y %H:%M:%S"`

+ Задание *

1. Отправить http запрос на сервер.\
`http://162.55.220.72:5005/terminal-hw-request`

1.1 `curl http://162.55.220.72:5005/terminal-hw-request`\
1.2 `curl "http://162.55.220.72:5005/get_method?name=igor&age=33"`

2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13.\
`vim script` `i`

``` bash

#!/bin/bash

cd /users/igori/documents/HW/folder_1
mkdir folder_{2..4}
cd folder_2
touch file_{1..3}.txt {js_1,js_2}.json
mkdir new_1 new_2 new_3
ls -la
mv {file_1,file_2}.txt ../folder_3
```
`esc` `:` `wq`

`chmod +x script`\
`./script`

+ В домашнем задании показал несколько возможностей по созданию папка и файлов, а так-же по копированию и перемещению с использованием абсолютного и относительного пути.
+ В 20 пункте заморочился с отображением даты и времени, так как у нас общепринятый формат это дата-месяц-год 
