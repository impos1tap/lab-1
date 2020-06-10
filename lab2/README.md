# Лабораторная работа №2
## Здесь я постараюсь полностью рассказать и показать на что у меня ушло много часов жизни

### Part 1
#### Начало лабораторной работы: Установка ОС и настройка RAID и LVM

Самое начало работы
просто менюшка с информацией о дисках

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part1/1.nachalo_ustanovki.png)


На этом скрине мы уже настроили RAID

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part1/4.Nastroika_RAID.png)

Туть мы закончили настройку LVM

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part1/7.konechnaya_nastroika_LVM.png)

Вот такую красивую информацию о дисках и RAID мы получили в начале работы, после копирования раздела /boot

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part1/10.pervaya_informatsiya_o_diskah.png)
![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part1/11.pervaya_informatsiya_o_RAID.png)

### Part 2
#### В ходе работы отпадает один SSD, мы на ходу заменяем его и благодаря LVM сохраняем все данные и копируем на новый диск

При проверке ВМ на работоспособность после отключения SSD была показана такая информация о дисках и RAID

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part2/2.VM_rabotaet.png)
![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part2/3.proverka_statusa_RAID_posle_udaleniya_ssd1.png)

Информация о дисках после замены SSD на новый и добавления его в RAID

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part2/5.dobavlenie_v_RAID_ssd3.png)
![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part2/6.rezultat_v_mdstat.png)

Конечный результат части 2

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part2/7.rezultat_zadaniya2.png)

### Part 3
#### В этой части у нас падает еще один SSD, мы заменяем его на новыенький на 7 гб и добавляем 2 новых HDD. Благодаря LVM и RAID мы спасли наши данные и включили новый ssd в наш VG.

Вот такая информация о дисках и RAID была получена после удаления старенького SSD 2.

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/1.informatsiya_o_diskah_posle_udaleniya_SSD2.png)
![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/2.Informatsiya_v_mdstat_posle_udaleniya_ssd2.png)


Информация о дисках после добавления SSD 4, копирования на него файловой таблицы и перемонтирования /boot:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/5.Informatsiya_posle_montirovaniya_boot_na_ssd4.png)


Информация после создания нового RAID масиива:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/6.informatsiya_posle_sozdaniya_novogo_RAID_massiva.png)


Информация pvs до и после создания нового физ.тома:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/7.izmeneniya_pvs_do_i_posle_sozdaniya_novogo_fiz.toma.png)


Log, root и var все пока еще находятся на md0

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/9.log%2Croot%2Cvarnahodyatsya_na_md0.png)


А здесь результаты после перемещения всех LV. Теперь они находятся на md63:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/10.Rezultaty_posle_peremescheniya_LV.png)


Удалили самый старый SSD, добавили новый, скопировали файловую таблицу, загрузочный раздел /boot и поставили на навый диск grub.

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/12.informatsiya_o_diskah_posle_kopirovaniya_tablitsy_faylov_i_sda1.png)


Добавили SSD 5 в RAID массив и увеличили размеры разедела на обоих дисках:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/13.informatsiya_posle_dobavleniya_ssd5_v_RAID_i_uvelicheniya_razmerov_razdelov_na_oboih_diskah.png)


Теперь увеличили размеры самого массива:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/14.razmery_sda(e)2%3Dmd127.png)


Увеличили размеры VG и самих root и var, и получили конечный результат работ с SSD:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/17.konechnyi_rezultat_raboty_s_ssd.png)


Создали на HHD логический том и отформатировали их под ext4:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/19.informatsiya_o_diskah_posle_formatirovaniya_razdelov.png)


Перемонтировали варлоги:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/20.informatsiya_o_diskah_posle_peremontirovaniya_varlogov.png)


Поправили файл fstab:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/21.izmeneniye_fayla_fstab.png)


Сняли последние pvs, lvs и vgs показания:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/22.poslednaya_proverka_pvs%2Clvs%2Cvgs.png)


Сделали последнюю проверку на работоспособность машины и сняли последние показания о дисках и RAID:

![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/23.poslednaya_proverka_i_.informatsiya_o_diskahpng)
![alt text](https://github.com/2kazbek/lab_git/blob/master/lab2/screenshots/part3/24.poslednaya_informatsiya-o_RAID)


### Примерно на это ушло в сумме примерно 10 часов жизни)))