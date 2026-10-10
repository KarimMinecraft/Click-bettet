# Click Better

Mod Geode untuk Geometry Dash. Memainkan **suara click** saat kamu menekan dan **suara release** ("kik" kecil) saat kamu melepas. Suaranya bisa dikustomisasi lewat clickpack, termasuk pack bergaya **ZCB3**.

## Fitur

- Suara click saat tekan, suara release saat lepas
- Pakai clickpack sendiri (taruh di folder config)
- Volume click dan release terpisah
- Variasi pitch acak biar tidak monoton
- Soft click otomatis saat spam (kalau pack punya folder `softclicks`)
- Opsi bunyi untuk Player 2

## Cara pasang clickpack (ZCB3)

1. Jalankan game dengan mod ini sekali, supaya folder config terbuat.
2. Buka folder config mod: `Geometry Dash/geode/config/karim.click-better/packs/`
   (di Android biasanya `Android/media/com.geode.launcher/game/geode/config/karim.click-better/packs/`)
3. Taruh folder clickpack di dalamnya, misalnya `ZCB3`.
4. Di pengaturan mod, isi **Nama pack** dengan nama folder tadi (default: `ZCB3`).

Struktur pack yang dikenali:

```
packs/
  ZCB3/
    clicks/          (wajib, suara tekan)
    releases/        (suara lepas)
    softclicks/      (opsional, dipakai saat spam)
    softreleases/    (opsional)
    hardclicks/      (opsional)
    hardreleases/    (opsional)
    microclicks/     (opsional)
    microreleases/   (opsional)
```

Format yang didukung: `.wav`, `.mp3`, `.ogg`, `.flac`. Kalau pack tidak punya folder sama sekali, file langsung di dalam folder pack dipakai (nama berisi "release" dianggap release, sisanya click).

## Cara build lewat HP (tanpa PC)

1. Buat akun GitHub, lalu buat repository baru (misal `click-better`).
2. Upload semua isi folder ini ke repository (lewat tombol **Add file → Upload files**). Pastikan folder `.github/workflows/build.yml` ikut terupload.
3. Buka tab **Actions**, tunggu build selesai (beberapa menit).
4. Buka hasil build terbaru, unduh **Build Output**, ekstrak, ambil file `karim.click-better.geode`.
5. Taruh file `.geode` itu di folder `geode/mods/` game, atau buka lewat Geode.

## Build di PC

Butuh [Geode CLI](https://docs.geode-sdk.org/getting-started/geode-cli) dan Geode SDK:

```
geode build
```

## Catatan

Kode ini belum diuji langsung di game. Kalau build error atau suara tidak muncul, kirim pesan error-nya biar diperbaiki.
