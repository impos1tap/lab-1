# Лабораторная работа №2
## Что же мы делали?

### Задание 1
#### Начало лабораторной работы: Установка ОС и настройка RAID и LVM
Делали все по инструкции

### Задание 2
#### В ходе работы падает один SSD, далее заменяем его с помощью LVM сохраняем все данные и копируем на новый диск

При проверке ВМ на работоспособность после отключения SSD была показана такая информация о дисках и RAID.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/2.png)

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/3.png)

Информация о дисках после замены SSD на новый и добавления его в RAID.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/5.png)

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/6.png)

Конечный результат Задания 2.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/7.png)
### Задание 3
#### В этой части у нас падает еще один SSD, мы заменяем его на новый 7 гб-товый и добавляем 2 новых HDD. Благодаря LVM и RAID мы спасли наши данные и включили новый ssd в наш VG.

Информация после удаления старого SSD 2.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/8.png)

Информация о дисках после добавления SSD 4, перемонтирования /boot и копирования на него файловой таблицы.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/11.png)

Информация после создания нового raid массива.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/13.png)

Информация pvs до и после создания нового физ. тома.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/14.png)

Var/Log/Root все еще на md0.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/16.png)

Результаты после перемещения всех LV. Теперь они на md63.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/17.png)

Удалили самый старый SSD, добавили новый, скопировали файловую таблицу, загрузочный раздел /boot и поставили на навый диск grub.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/19.png)

Добавили SSD 5 в RAID массив и увеличили размеры раздела на обоих дисках.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/20.png)

Теперь увеличили размеры самого массива.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/21.png)

Увеличили размеры VG и самих root и var, и получили конечный результат работ с SSD.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/24.png)

Создали на HHD логический том и отформатировали их под ext4.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/25.png)

Перемонтировали varlogs.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/27.png)

Поправили файл fstab.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/28.png)

Сняли последние pvs, lvs и vgs показания.

![alt text](https://github.com/MrXariz/lab/blob/master/lab2/screens/29.png)


### Наконец-то всё
