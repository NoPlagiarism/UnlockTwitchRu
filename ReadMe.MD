# Возвращаем 1080p на Twitch

## Способы

### (Бес)платный VPN

Да, можно использовать VPN/Proxy ([список неплохих платных VPN тут](https://t.me/vpnconfession/27)). Для возвращения 1080p достаточно проксировать `usher.ttvnw.net` и `gql.twitch.tv`

---

> [!CAUTION]
> **Важное сообщение от 09.10.2025**
>
> Twitch обновил метод подтверждения IP, сломав некоторые способы обхода. Глобальный VPN или на домены, упомянутые выше - ещё работает
>
> Из методов ниже на данный момент работает [только решение от ReYohoho](#браузерное-расширение-от-reyohoho)

---

> [!WARNING]
> Далее идёт секция браузерных расширений. Убедитесь что используете только один из них

### [Браузерное Расширение от ReYohoho](https://github.com/reyohoho/twitch_quality_proxy)

- [**Chromium** (Chrome, Яндекс.Браузер, Opera и др.)](https://chromewebstore.google.com/detail/reyohoho-twitch-proxy/ohgphcndclpcmbglhldmnagagdbmkoef)
- [**Firefox**](https://addons.mozilla.org/ru/firefox/addon/reyohoho-twitch-proxy)
- [Userscript](https://github.com/reyohoho/twitch_quality_proxy/raw/refs/heads/userscript/twitch.user.js)
- [Подробнее здесь](https://github.com/reyohoho/twitch_quality_proxy)

### [Браузерное Расширение TTV LOL PRO](https://github.com/younesaassila/ttv-lol-pro)

> [!IMPORTANT]  
> При установке выбрать Unblock Best Quality

- [**Chromium** (Chrome, Яндекс.Браузер, Opera и др.)](https://chrome.google.com/webstore/detail/ttv-lol-pro/bpaoeijjlplfjbagceilcgbkcdjbomjd)
- [**Firefox**](https://addons.mozilla.org/ru/firefox/addon/reyohoho-twitch-proxy)
- [**GitHub репозиторий**](https://github.com/younesaassila/ttv-lol-pro)

---

> [!NOTE]
> Методы ниже связаны с DNS ([XBox DNS](https://xbox-dns.ru) & [dns.malw.link](https://info.dns.malw.link))

### DNS

Настроить DNS по всей системе или только в браузере

Инструкции по настройке DNS:

- [для Windows от Selectel](https://selectel.ru/blog/tutorials/change-dns-server)
- [для Windows, Android, macOS, iOS на Лайфхакер](https://lifehacker.ru/nastrojka-dns-servera)

<details>

<summary>Данные для подключения</summary>

- [XBox DNS](https://xbox-dns.ru)
  - [Актуальные данные есть в их Telegram (@xbox_dns)](https://t.me/xbox_dns)
  - Данные для подключения
    - DNS IPv4
      - `176.99.11.77`
      - `80.78.247.254`
    - DNS IPv6
      - `2a00:f940:2:4:2::5d1b`
      - `2a00:f940:2:4:2::21ed`
    - DNS over HTTPS (DoH)
      - `https://xbox-dns.ru/dns-query`
      - [Конфиг для MacOS / iOS](https://xbox-dns.ru/ios/xbox-dns.mobileconfig)
    - DNS over TLS (DoT)
      - `xbox-dns.ru`
- [dns.malw.link](https://info.dns.malw.link)
  - [Актуальные данные есть на сайте info.dns.malw.link](https://info.dns.malw.link) / [Telegram канал](https://t.me/immalware)
  - Данные для подключения
    - DNS IPv4
      - `84.21.189.133`
      - `64.188.98.242`
    - DNS IPv6
      - `2a12:bec4:1460:d5::2`
      - `2a01:ecc0:2c1:2::2`
    - DNS over HTTPS (DoH)
      - [Cloudflare gateway **(рекомендуется)**](https://info.dns.malw.link/setup/cloudflare)
        - `https://5u35p8m9i7.cloudflare-gateway.com/dns-query`
      - `https://dns.malw.link/dns-query`
    - DNS over TLS (DoT)
      - `dns.malw.link`
    - DNSCrypt stamp
      - `sdns://AgYAAAAAAAAADDQ1Ljk1LjIzMy4yMwANZG5zLm1hbHcubGluawovZG5zLXF1ZXJ5`

</details>

### Hosts

Если перенаправлять только `usher.ttvnw.net` на нужный IP, то можно не менять DNS глобально

> [!TIP]
> Пока [dns.malw.link имеет свой официальный Hosts](https://info.dns.malw.link/hosts), [XBox DNS](https://t.me/xbox_dns) не поддерживает подобного и не планирует в ближайшем будущем. Но продвинутые пользователи могут попробовать DNS Forwarding
>
> Для Windows - [YogaDNS](https://www.yogadns.com), а для Linux & OpenWRT - [dnsmasq](https://wiki.archlinux.org/title/Dnsmasq#DNS_addresses_file_and_forwarding)

#### ПК (Windows / Linux / MacOS)

[Найдите hosts файл](https://1cloud.ru/help/dns/file-hosts) и внесите туда следующую строку

```
45.95.233.23 usher.ttvnw.net
```

#### [AdAway (Android)](https://github.com/AdAway/AdAway)

<https://github.com/AdAway/AdAway>

Работает в режиме VPN (если non-root). Блокирует рекламу и также позволяет форсировать DNS запись через "перенаправление"

#### На всю сеть

Так же можно указать данную запись прямо в роутере или DNS сервисах вроде Pi-hole или Adguard Home
