# Developer Guides

## Microsite untuk PIKOBAR mobile app

### Mendapatkan data user yang sedang login.

Dari aplikasi PIKOBAR, URL Webview yang akan di-launch adalah, contoh:
```
https://microsite.app?uid=XXXXXXX

uid = akan diisi oleh user ID user yang sedang login. Jika tidak login, maka nilainya akan kosong.
```

Untuk bisa mendapatkan data user yang memiliki UID tersebut, pada microsite yang dibangun harus melakukan request ke endpoint ini:
```
GET https://us-central1-jabarprov-covid19.cloudfunctions.net/getUserById?id=XXXXXXX

{
  "id": "XXXXXXX",
  "name": "Yoga Hanggara",
  "gender": "M",
  "photo_url": "https://lh3.googleusercontent.com/a-/AOh14Gid80TifVeqywmho56Nz4BaLYqYiZ6nFDuOtFtdIbg=s96-c",
  "province_code": "32",
  "city_code": "32.73"
}
```
