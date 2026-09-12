# Kyrone Discord Bot 🚀

Paket ini sudah disiapkan untuk deploy ke Railway menggunakan Docker, termasuk FFmpeg untuk `/gif convert`.

## File
- `kyrone.js` = bot utama
- `package.json` = dependency + start command
- `Dockerfile` = memasang FFmpeg otomatis
- `.env.example` = contoh variable, jangan isi token asli lalu upload ke GitHub

## Variable Railway
Tambahkan di Railway Variables:
- `DISCORD_TOKEN`
- `CLIENT_ID`
- `GUILD_ID`
- `OPENAI_API_KEY`
- `OPENAI_MODEL` (opsional, default `gpt-5.6-luna`)

## Jalankan lokal
```bash
npm install
node kyrone.js
```

## Catatan keamanan
Kalau token Discord pernah terkirim di chat/screenshot, reset token tersebut di Discord Developer Portal sebelum deploy. Jangan commit `.env` atau token ke GitHub.

## Catatan data
Bot saat ini memakai `kyrone-data.json`. Di hosting cloud, filesystem bisa tidak persisten saat redeploy. Untuk data ekonomi/XP yang benar-benar permanen, nanti sebaiknya pindah ke database.
