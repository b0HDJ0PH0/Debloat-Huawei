
Использование:
1. В adb определиться коммандой adb devices . Если вернется серийный номер, то
2. В raw  ctrl+A , ctrl+C => в adb ctrl+V 

Работает в пределах учетной записи пользователя, что позволяет, при необходимости,

 adb shell cmd package install-existing *пакет* 

 adb shell pm list cmd package install-existing *пакет* 

откатиться или восстановить нужный пакет, соответственно.

++

Получаем список всех пакетов

 adb shell pm list packages -f > c:\adb\pkg_list.txt 

Ключи :

list packages [] [--uid UID] [--user USER_ID] [FILTER]

adb shell pm list packages [] --user 0

[-f] [-d] [-e] [-s] [-3] [-i] [-l] [-u] [-U]

-f: этот мы уже знаем -d: только отключенные пакеты -e: только активные -s: системные -3: сторонние -i: установщик -l: это хлам, этот не нужен -U: покажет UID -u: все паки с уже удаленными