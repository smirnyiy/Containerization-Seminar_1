Задание: необходимо продемонстрировать изоляцию одного и того же приложения (как решено на семинаре - командного интерпретатора) в различных пространствах имен.

Формат сдачи ДЗ: предоставить доказательства выполнения задания посредством ссылки на google-документ с правами на комментирование/редактирование.
Результатом работы будет: текст объяснения, логи выполнения, история команд и скриншоты (важно придерживаться такой последовательности).
В названии работы должны быть указаны ФИ, номер группы и номер урока.


Создаем директорию "GB"
mkdir GB

Копируем исполняемый файл командного интерпретатора /bin/bash в папку "GB/bin":
cp /bin/bash GB/bin

Создаем необходимые директории "GB/lib" и "GB/lib64":
mkdir GB/lib
mkdir GB/lib64
Копируем необходимые библиотеки в папку "GB/lib" и "GB/lib64". Пример:

cp /lib/x86_64-linux-gnu/libtinfo.so.6 GB/lib
cp /lib/x86_64-linux-gnu/libc.so.6 GB/lib
cp /lib64/ld-linux-x86-64.so.2 GB/lib64/
Запускаем команду chroot для изменения корневой папки:

chroot GB /bin/bash

cp /bin/ls GB/bin/
ldd /bin/ls
cp /lib/x86_64-linux-gnu/libselinux.so.1 GB/lib/
cp /lib/x86_64-linux-gnu/libpcre2-8.so.0 GB/lib/

/home/andrey/Изображения/Снимки экрана/Снимок экрана от 2023-07-10 19-05-04.png

<img src="[https://raw.githubusercontent.com/Terekhov-A-S/Containerization-Seminar_1/main/source/19-21-02.png](https://github.com/smirnyiy/Containerization-Seminar_1/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-07-10%2019-06-58.png)https://github.com/smirnyiy/Containerization-Seminar_1/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202023-07-10%2019-06-58.png" alt="sudo unshare -pf -n --mount-proc bash" style="max-width: 100%;">

