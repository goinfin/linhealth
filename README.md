# linhealth
Лёгкий Bash-скрипт для быстрой диагностики Linux-сервера на системах с **systemd**.
Используются стандартные утилиты GNU/Linux. Вывод - простой текст в stdout.

## Возможности
- Система: дистрибутив, ядро, hostname, uptime, load average, количество CPU.
- Память/swap: объёмы из /proc/meminfo.
- Файловые системы: заполненность (%), иноды (%), предупреждения по порогам.
- Сервисы: systemctl --failed.
- Сеть: шлюз, адреса, DNS-резолв, ping до 77.88.8.8.
- Время: статус синхронизации timedatectl.
- Журналы: последние ошибки текущей загрузки.
- Коды возврата: 0=OK, 1=WARN, 2=CRIT.

## Установка
```bash
# Клонирование репозитория и установка исполняемого файла (скрипта)
git clone https://github.com/goinfin/linhealth.git
cd linhealth
sudo install -m 0755 ./linhealth /usr/local/bin/linhealth

