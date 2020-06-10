# Лабораторная работа №1
1. [Скриншоты](https://github.com/MrXariz/lab/tree/master/lab1/screenshots)
2. [Скрипты](https://github.com/MrXariz/lab/tree/master/lab1/scripts)
## Suzen1

![suzen1](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/1.jpg)
 
Команда **ls** для просмотра содержимого каталога\
командой **cat** открываем файл формата .txt.
 
## Suzen2
 
![suzen2.1](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/2.jpg)
 
Командой **cat** соединяем файлы, начинающиеся с одного символа.

![suzen2.2](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/3.jpg)

Ключ в одном из файлов, которые начинаются с двоеточия.

## Suzen3

![suzen3](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/4.jpg)

Читаем файл с помощью **bash**:
 При помощи конструкции **while read line** читаем и сохраняем в line строки файла пока они не закончатся\
 Конструкция **do echo $line** выводит строку, которая храниться в line\
 **Done** показывает конец цикла\
 При помощи **(< ‘-diary.txt-‘ )** мы направляем данные из дневника на ввод скрипту.

## Suzen14

![suzen14](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/5.jpg)

При помощи команды **ls** чекаем названия каталогов и находим ключ.

## Suzen15

![suzen15](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/6.jpg)

При помощи **(cd ..)** выходим из начальной директории\
далее чекаем ее название через **ls**.

## Suzen16

![suzen16](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/7.jpg)

Чекнуть информацию о пользователях можно двумя способами:\
#1. Команда id\
Команда предназначена для вывода информации о пользователях\
Если не указывать параметр, то выведется информация о текущем пользователе и его группах\
#2. Команда groups\
Показывает группы, в которых состоит пользователь.

## Suzen17

![suzen17](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/8.jpg)

С помощью флага **–a** утилиты **ls** чекаем скрытые файлы.

## Suzen18

![suzen18](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/9.jpg)

Пользуемся утилитой **man** для прочтения мануала **diary**.

## Suzen19

![suzen19](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/10.jpg)

**mkdir** - создаем директории\
ключ **-p** создает каталоги, которые отсутсвуют.\
**Sleep** и **&&** используются для имитации скрипта, чтобы все выполнилось по порядку и ключ вывелся.

## Suzen20

![suzen20](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/11.jpg)

Переходим в **john**\
удаляем все файлы с помощью **rm**\
Флаг **–r** требуется для удаления каталогов.

## Suzen21

![suzen21](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/12.jpg)

Юзаем **rm** с выражениями для удаления файлов.\
Утилита **grep** с ключом **-o**  используется для поиска подстроки в выводe ls,\
которая удовлетворяет регулярному выражению '[0-9a-zA-Z]\{28\}':[0-9a-zA-Z]-\
подстрока состоит из только из букв и цифр\
{28}- длина подстроки равна 28.

## Suzen22

![suzen22](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/13.jpg)

Пишем скрип для создания файлов,\
**for i in `seq 1 999`** - построение цикла от 1 до 999.\
Файлы создаются с помощью утилиты **touch**.\
Комбинация ls и grep используется для быстрого, не ручного поиска.

## Suzen23

![suzen23](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/14.jpg)

Заходим в каталог **destination**\
при помощи **bash** и утилиты **mv** переименовываем все файлы, которые находятся в данной директории.\
заходим в **source** и перемещаем из данной директории в директорию **destination**, используя **mv**.

## Suzen24

![suzen24](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/15.jpg)

Создаем директорию **Music** в **suzen**.\
Переходим в **Desktop/Music** и копируем все содержимое утилитой **cp**.\
Флаг **–r** нужен для копирования подкаталогов и файлов, внутри данного каталога.

## Suzen25

![suzen25](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/16.jpg)

Через **ls** смотрим содержимое\
через **cat** открываем.

## Suzen26

![suzen26.1](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/17.jpg)

![suzen26.2](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/18.jpg)

![suzen26.3](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/19.jpg)

Открываем файл через **less**\
видим **FIRST_FLAG_PART**\
пользуемся поиском **(/…)**.

## Suzen27

![suzen27](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/20.jpg)

Запускаем утилиту **tail** флаг **-f** для чтения файла.\
Направляем вывод в **grep** для вывода только ключа.

## Suzen28

![suzen28.1](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/21.jpg)

Ищем похожее на название начального файла через утилиту **find**\
открываем и копируем все, кроме последней строчки.

![suzen28.2](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/22.jpg)

При помощи **cat** создаём файл, перенаправляя вывод в **diary**, пока не введем **EOF**.

![suzen28.3](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/23.jpg)

Две последние строчки вставляем через **echo** с флагом **–e**, чтобы исключить добавление **\n**.

![suzen28.4](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/24.jpg)

## Suzen29

![suzen29](https://github.com/MrXariz/lab/blob/master/lab1/screenshots/25.jpg)

**echo** для просмотра файлов в каталоге.\
Findим скрытый файл и открываем его через **echo**,\
видим прикол и находим флаг.











