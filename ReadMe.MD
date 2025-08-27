# Возвращаем 1080p на Twitch

## Способы

### Бес(платный) VPN

Да, можно использовать VPN/Proxy ([список неплохих платных VPN тут](https://t.me/vpnconfession/27)). Для возвращения 1080p достаточно проксировать только `usher.ttvnw.net`

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

### [dns.malw.link](https://info.dns.malw.link)

Настроить DNS в браузере или на телефоне по инструкции. Рекомендуется использовать [DoH на Cloudflare Gateway](https://info.dns.malw.link/setup/cloudflare)

### [Hosts от dns.malw.link](https://info.dns.malw.link/hosts)

Перенаправлять `usher.ttvnw.net` на SNI прокси по IP `45.95.233.23`

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
