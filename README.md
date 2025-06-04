Tweet Analiz Otomatı

Bu proje, kullanıcıdan alınan bir tweet bağlantısını analiz ederek Türkçe kısa özetini ve duygu durumunu (Olumlu, Olumsuz, Nötr) belirleyen bir React tabanlı web uygulamasıdır. Analiz sonuçları hem arayüzde görüntülenir hem de Airtable üzerinden bir tabloya kaydedilir.

Özellikler:

Tweet bağlantısından otomatik olarak tweet ID’sini ayrıştırır

Belirli ID’ler için sahte içerik veritabanı üzerinden içerik eşleştirir

Google Gemini API aracılığıyla özetleme ve duygu analizi gerçekleştirir

Sonuçları kullanıcı arayüzünde sade bir kart halinde gösterir

Airtable API ile analiz sonuçlarını tabloya kaydeder

Eksik veya hatalı durumlarda kullanıcıya açıklayıcı uyarılar sunar

Kullanılan Teknolojiler:

React (Frontend)

Google Gemini API (Doğal dil işleme)

Airtable API (Veri kaydı ve saklama)

Dotenv (.env dosyası ile çevresel değişken yönetimi)

Kurulum ve Çalıştırma:

Projeyi klonlayın:
git clone <repo-url>
cd tweet-analyzer

Bağımlılıkları yükleyin:
npm install

.env dosyasını oluşturun:
Proje kök dizininde .env adında bir dosya oluşturup aşağıdaki değişkenleri girin:
REACT_APP_GEMINI_API_KEY=...your Gemini API key...
REACT_APP_AIRTABLE_TOKEN=...your Airtable API token...
REACT_APP_AIRTABLE_BASE_ID=...your Airtable Base ID...

Uygulamayı başlatın:
npm start
Ardından http://localhost:3000 adresinden uygulamayı görüntüleyebilirsiniz.

Kullanım:

Uygulama başlatıldıktan sonra sahte tweet seçimi yapılabilir ya da elle bir tweet bağlantısı girilebilir.

“Analiz Et” butonuna tıklandığında, içerik Google Gemini API tarafından analiz edilir.

Sonuç, özet ve duygu durumu bilgileriyle birlikte ekranda gösterilir ve aynı zamanda Airtable tablosuna kaydedilir.

Geliştirici Notları:

Tweet içeriği yalnızca önceden tanımlanmış sahte veritabanındaki ID'lerle eşleştirilir. Gerçek içerik alınmaz.

Airtable’daki tablo ismi varsayılan olarak “Tweet Analysis” olarak ayarlanmıştır. Gerekirse koddan değiştirilebilir.

.env dosyası .gitignore içine dahil edilmelidir.

Ekran Görüntüsü:

![Ekran görüntüsü 2025-06-04 180444](https://github.com/user-attachments/assets/86bb8d16-eb57-427f-841d-1a184bf0aa46)
![Ekran görüntüsü 2025-06-04 180533](https://github.com/user-attachments/assets/8cf94c1d-a6c4-4c21-acfb-85057b3e7a17)
![Ekran görüntüsü 2025-06-04 180804](https://github.com/user-attachments/assets/e1d7942f-4277-4302-9ca5-eca7f5758978)
![Ekran görüntüsü 2025-06-04 180831](https://github.com/user-attachments/assets/4279c572-7149-4f3b-8792-8789a277fa2b)
![Ekran görüntüsü 2025-06-04 180513](https://github.com/user-attachments/assets/7dae8938-afe2-412f-b9b5-fed94dc60611)


Lisans:

MIT
