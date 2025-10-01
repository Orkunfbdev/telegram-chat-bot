# Telegram Chat Bot (n8n + OpenAI + Supabase)

Bu repo, n8n üzerinde çalışan Telegram chat botu için hazırlanmıştır.
- Telegram Trigger ile mesaj alır, OpenAI ile yanıt üretir
- Supabase Vector Store üzerinden bilgi tabanına erişir
- PostgreSQL üzerinde sohbet geçmişi saklayabilir

## 📂 Klasörler
- `workflows/` → n8n akış JSON dosyaları
- `db/` → Supabase/PostgreSQL kurulum SQL dosyaları

## 🚀 Kurulum (Özet)
1) Bu repoyu bilgisayarına indir (veya klonla).
2) n8n'e giriş yap → **Workflows → Import from file** ile `workflows/` içindeki JSON'ları içeri al.
3) Supabase/PostgreSQL tarafında `db/supabase_n8n_connect.sql` dosyasını çalıştır.
4) `.env` içine şu değişkenleri tanımla:
```
TELEGRAM_API_KEY=xxx
OPENAI_API_KEY=xxx
SUPABASE_URL=xxx
SUPABASE_KEY=xxx
POSTGRES_URL=xxx
```

> Not: API anahtarlarını asla repoya koyma. `.gitignore` içinde `.env` zaten korunur.

## ▶️ Çalıştırma
- n8n üzerinde workflow'ları **Activate** et.
- Telegram BotFather'dan aldığın token ile Telegram düğümünü yetkilendir.

## 📝 Lisans
MIT
