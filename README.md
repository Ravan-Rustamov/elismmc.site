# ELİS TİKİNTİ MMC — rəsmi sayt

Statik sayt. GitHub Pages üzərində host olunur, Cloudflare vasitəsilə `elismmc.site` domeninə bağlıdır.

## Struktur
```
index.html            Ana səhifə
404.html              Tapılmayan səhifə
CNAME                 Öz domen (elismmc.site)
robots.txt, sitemap.xml
favicon.svg
assets/css/style.css  Stillər
assets/js/main.js     Mobil menyu
assets/img/           Fotolar
```

## Yerləşdirmə
1. Bu faylları repo-nun kök qovluğuna yükləyin (`main` branch).
2. GitHub → Settings → Pages → Source: `Deploy from a branch`, `main` / `/ (root)`.
3. Settings → Pages → Custom domain: `elismmc.site` (CNAME faylı artıq var). "Enforce HTTPS" işarələyin.

## Cloudflare DNS
| Tip   | Ad  | Dəyər                         | Proxy |
|-------|-----|-------------------------------|-------|
| A     | @   | 185.199.108.153               | DNS only |
| A     | @   | 185.199.109.153               | DNS only |
| A     | @   | 185.199.110.153               | DNS only |
| A     | @   | 185.199.111.153               | DNS only |
| CNAME | www | `<istifadəçi>.github.io`      | DNS only |

GitHub sertifikat verib "Enforce HTTPS" aktiv olandan sonra Proxy-ni "Proxied" edə bilərsiniz.
SSL/TLS rejimini **Full (strict)** seçin, əks halda yönləndirmə dövrəsi yaranır.
