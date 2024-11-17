# EZPasswall (Русский)

[![Значок посетителя](https://img.shields.io/badge/Chat%20on-Telegram-blue.svg)](https://t.me/peditx) [![Лицензия: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

[**English**](README.md) | [**فارسی**](README_fa.md) | [**简体中文**](README-ch.md) | [**Русский**](README_ru.md)

### Что такое скрипт EZPasswall?

Этот скрипт позволяет легко оптимизировать ваше устройство OpenWrt с помощью современного и простого интерфейса, поддерживающего такие протоколы, как OpenVPN, Xray, V2Ray, WireGuard, Cloudflare Warp и другие. Вы также можете установить Passwall 1 и Passwall 2 (по отдельности или вместе) и наслаждаться стабильным интернет-соединением с сегментированным и непрерывным трафиком. Этот скрипт будет постоянно улучшаться со временем.

С уважением,  
[PeDitX](https://github.com/peditx)

## Как установить EZPasswall
![Изображение установки](https://github.com/peditx/iranIPS/blob/1f05bc52dae7b573742e0bcccf8430c8a46b94e4/.files/lowspc/main/photo_2024-10-27_21-15-16.jpg?raw=true)
![Изображение установки](https://github.com/peditx/iranIPS/blob/ffce5c185aecd61f1d92d100593ceecb2b905235/.files/lowspc/main/photo_2024-10-27_20-03-44.jpg?raw=true)
![Изображение установки](https://github.com/peditx/iranIPS/blob/main/.files/lowspc/main/new/photo_2024-10-31_17-15-33.jpg?raw=true)
![Изображение установки](https://github.com/peditx/iranIPS/blob/main/.files/lowspc/main/new/photo_2024-10-31_17-16-35.jpg?raw=true)
![Изображение установки](https://github.com/peditx/iranIPS/blob/main/.files/lowspc/main/new/photo_2024-10-31_17-17-44.jpg?raw=true)

### Системные требования для роутеров

- **Процессор:** `>= 700 MHz`
- **Оперативная память:** `>= 256 MB`

### Наши лучшие рекомендации по роутерам

- Google WiFi (Gale)
- Linksys EA8100
- Linksys EA8300
- Linksys E8450
- Belkin rt3200
- GL-iNet GL-A1300

### Минимальные системные требования для компьютеров
- **Процессор:** `AMD или Intel`
- **Оперативная память:** `2 GB`
- **Операционная система:** `Linux Ubuntu 20.04`

> ⚠ **Перед установкой:** Убедитесь, что `WAN-адрес` и `LAN-адрес` не совпадают.  
> **Пример:** 
> - WAN-адрес: `192.168.1.XXX`
> - LAN-адрес: `192.168.1.1`  
> Измените LAN-адрес на другой IP, например `10.1.1.1`.

### Установка Passwall

> 🔴 **Важно:** Для роутеров с `128 MB ОЗУ`, пожалуйста, выполните `понижение версии` до [OpenWrt 22.03.3](https://archive.openwrt.org/releases/22.03.3/targets/). 🔴

Запустите следующую команду в удалённом SSH OpenWrt:

```bash
opkg update
opkg install coreutils-base64 bash
rm -f ezp.sh && wget -qO - https://raw.githubusercontent.com/peditx/EZpasswall/refs/heads/main/ezp.b64 | awk '{print $1}' | base64 -d > ezp.sh && chmod +x ezp.sh && sh ezp.sh

```

Если вы хотите использовать сервис конвертации Linux в OpenWrt, просто введите следующую команду в удалённом SSH:

```bash
sudo apt-get update
sudo apt-get install curl
rm -f *.sh && wget https://raw.githubusercontent.com/peditx/easywrt/refs/heads/main/start.sh && bash start.sh

```
Или (для X86/X86-64) просто скачайте этот файл .iso, создайте загрузочную флешку и введите команду start.sh:

```bash
https://github.com/peditx/easywrt/releases/download/V101/PeDitXOs-101.iso

```

**Готово!**

### Поддерживаемые протоколы

- **VLESS:** (XRAY ✅, SING-BOX ✅)
- **VMESS:** (XRAY ✅, SING-BOX ✅)
- **REALITY:** (XRAY ✅, SING-BOX ❌)
- **TROJAN:** (XRAY ✅, SING-BOX ✅)
- **HYSTERIA2:** (XRAY ❌, SING-BOX ✅)
- **TUIC:** (XRAY ❌, SING-BOX ✅)
- **SHADOWSOCKS:** (XRAY ✅, SING-BOX ✅)
- **WIREGUARD:** (XRAY ✅, SING-BOX ✅)
- **SOCKS:** (XRAY ✅, SING-BOX ✅)
- **HTTP:** (XRAY ✅, SING-BOX ✅)

### Рекомендуемые роутеры

- Google WiFi (Gale)
- Linksys EA8300
- Linksys E8450
- Belkin rt3200
- GL-iNet GL-A1300
- Xiaomi AX3000T
- ~~Xiaomi 4a Gigabit~~
- TP-Link C6 v3
- Mikrotik Hap ac2
- GL.iNet AR300M (NOR)
- Linksys EA7500 (v1-v2)
- Linksys EA8100 (v1-v2)
- ASUS RT-N66U
- Xiaomi AX3600
- Xiaomi AX3200
- Xiaomi AX6000
- Netgear R7800

### Функции

- Полностью автоматическая установка в один шаг.
- Поддержка Passwall 1 и 2 на одном роутере.
- Установка exroot в один клик для роутеров с USB-портом.
- Инструменты X86 для конвертации Linux x86/x86-64 в OpenWRT, ImmortalWRT, PeDitXRT, MikroTik или пользовательские ОС для систем без прямой установки.
- Быстрая настройка Wi-Fi с помощью ввода SSID и пароля в разделе "Дополнительные инструменты".
- Очистка использованной памяти одним кликом в разделе "Дополнительные инструменты".
- Установка дополнительных пакетов, таких как OpenVPN, Sing-box, SoftEther, и IP-сегментация с Sing-box, для роутеров и тонких клиентов с объёмом памяти более 512 МБ в разделе "Дополнительные инструменты".
- Умная установка XRAY во временное пространство при ограниченном дисковом пространстве.
- Прямой трафик по иранским IP и доменам (100%).
- Повышенная производительность.
- Новый дизайн темы и логотипа.
- Исправлено подключение к серверу WARP.
- Включён по умолчанию kill switch.
- XRAY Fragment tlshello | 1-3.

### Особая благодарность

- [Команда OpenWrt](https://github.com/openwrt)
- [Тема Argon](https://github.com/jerrykuku)
- [Команда Passwall](https://github.com/xiaorouji)
- [Команда V2Ray](https://github.com/v2ray)
- [PeDitXrt](https://github.com/peditx/PeDitXrt)
- [Mohamadreza Broujerdi](https://t.me/MR13_B)
- [Amirhosein Choghaei](https://github.com/amirhosseinchoghaei)
- [Mashkouk](https://github.com/mashkouk)

[PeDitX](https://github.com/peditx) © 2024
