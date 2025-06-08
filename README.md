# Tweet Analiz Otomatı

Bu proje, girilen bir tweet linkini analiz ederek Türkçe özetini ve duygu durumunu (Olumlu, Olumsuz, Nötr) otomatik olarak çıkaran bir React tabanlı web uygulamasıdır. Analiz sonuçları hem ekranda gösterilir hem de Airtable tablosuna kaydedilir.

## Özellikler

- Tweet linkinden tweet ID'sini otomatik tespit eder.
- Sahte tweet veritabanı üzerinden içerik simülasyonu yapar.
- Google Gemini API ile tweetin özetini ve duygu analizini alır.
- Sonuçları kullanıcıya sade bir kartta gösterir.
- Analiz edilen verileri Airtable'a kaydeder.
- Hatalar ve eksik ayarlar için kullanıcıya bilgilendirici uyarılar sunar.

## Kullanılan Teknolojiler

- React (frontend)
- Google Gemini API (doğal dil işleme için)
- Airtable API (veri saklama)
- .env ile gizli anahtar yönetimi

## Kurulum ve Çalıştırma

1. **Depoyu klonlayın:**
   ```bash
   git clone <repo-url>
   cd tweet-analyzer
   ```
2. **Bağımlılıkları yükleyin:**
   ```bash
   npm install
   ```
3. **.env dosyasını doldurun:**
   Proje kök dizinindeki `.env` dosyasını aşağıdaki gibi doldurun:
   ```env
   REACT_APP_GEMINI_API_KEY=GoogleGeminiAPIKey'iniz
   REACT_APP_AIRTABLE_TOKEN=AirtableAPIToken'ınız
   REACT_APP_AIRTABLE_BASE_ID=AirtableBaseID'niz
   ```
4. **Uygulamayı başlatın:**
   ```bash
   npm start
   ```
   Ardından [http://localhost:3000](http://localhost:3000) adresinde uygulamayı görüntüleyebilirsiniz.

## Kullanım

1. Açılan ekranda bir sahte tweet seçin veya tweet linkini girin.
2. "Analiz Et" butonuna tıklayın.
3. Tweetin özeti ve duygu analizi birkaç saniye içinde ekranda görüntülenecek.
4. Sonuçlar otomatik olarak Airtable tablonuza kaydedilir.

## .env Açıklamaları

- `REACT_APP_GEMINI_API_KEY`: Google Gemini API anahtarınız.
- `REACT_APP_AIRTABLE_TOKEN`: Airtable API erişim token'ınız.
- `REACT_APP_AIRTABLE_BASE_ID`: Airtable Base ID'niz.

> Uygulama, gerçek tweet içeriği yerine örnek bir tweet veritabanı kullanır. Google Gemini API ve Airtable ile entegrasyon için kendi anahtarlarınızı girmeniz gerekir.

## Örnek Ekran Görüntüsü

![Ekran Görüntüsü](docs/screenshot.png)

## Geliştirici Notları
- Tweet içeriği bulunamazsa "Bu tweetin içeriği bilinmiyor." mesajı döner.
- API anahtarları eksikse uygulama çalışmaz ve uyarı verir.
- Airtable tablosu adı "Tweet Analysis" olarak hardcoded'dur, gerekirse koddan değiştirilebilir.

## Lisans
MIT
