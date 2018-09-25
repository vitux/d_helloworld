Использовал 
https://github.com/lmovsesjan/Fastcgi-Daemon
и инструкцию
https://habr.com/post/216181/

компиляция
g++ HelloFastCGI.cpp -O2 -fPIC -lfastcgi-daemon2 -shared -o libHelloFastCGI.so
старт сервиса
sudo service fastcgi-daemon2 start HelloFastCG

В браузере открывается http://localhost/hellofascgi

Не всё работало, например, нужно было
поменять в файле debian/compat репозитория число 4 на 5
