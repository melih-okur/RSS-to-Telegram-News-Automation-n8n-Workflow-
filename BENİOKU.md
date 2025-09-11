# 📡 RSS to Telegram Otomasyonu (n8n Workflow)

🌐 **Dil Seçimi:** [Türkçe](README.md) | [English](README.en.md)
---

Bu proje, **n8n** kullanarak birden fazla RSS kaynağından haberleri toplayıp **Telegram bot** üzerinden otomatik olarak paylaşan bir workflow içerir.  
Amaç: Belirli aralıklarla güncellenen haberleri, otomatik ve düzenli bir şekilde Telegram grubuna/kanalına iletmektir.


---

## 🚀 Özellikler
- Birden fazla RSS kaynağını destekler
- Tekrarlayan haberleri filtreler (duplicate check)
- Her 10 dakikada bir otomatik çalışır (Scheduler)
- Haberleri Telegram'a resim + başlık + özet olarak gönderir
- Kolay özelleştirilebilir
- Yeni RSS kaynakları veya farklı mesaj formatları eklenebilir.


---

## 🛠️ Kullanılan Teknolojiler
- [n8n](https://n8n.io/) – Otomasyon platformu
- [Telegram Bot API](https://core.telegram.org/bots/api) – Haber gönderimi için
- RSS Feed kaynakları

---

## 🔧 Kurulum ve Kullanım

1. **Projeyi indir**
   
   [İndirmek için tıkla](https://drive.usercontent.google.com/u/0/uc?id=1Swuaw-etASp2KgeeVL1HQ--QGfAKf4c8&export=download)


3. **n8n’i kur ve başlat**  
   - [Resmi doküman](https://docs.n8n.io/hosting/) üzerinden kurulumu yap.  
   - n8n arayüzünden `telegram_news_bot.json` dosyasını **Import Workflow** ile içe aktar.

4. **Telegram Bot oluştur**  
   - Telegram’da [@BotFather](https://t.me/BotFather) üzerinden /newbot komutu ile yeni bot oluştur.  
   - Token’ı (API) alıp n8n credentials bölümüne ekle.
   - Oluşturduğunuz botunuzu kanalınıza "yönetici" yetkisiyle ekleyin ve izinleri onaylayın. 
   - `Chat ID`’ni bulmak için:
     - Oluşturduğunuz gruba herhangi bir mesaj yazın ardından
     `https://api.telegram.org/bot<TOKEN>/getUpdates`
     - <TOKEN> yazan bölüme @BotFather tarafından gönderilen Tokeninizi yazın.
   - Açılan sayfada, mesajın detaylarını içeren bir JSON çıktısı göreceksiniz. Burada chat objesini bulun. Bu objenin içindeki id değeri, aradığınız Chat ID'dir.
   - Oluşturduğunuz botunuzu kanalınıza "yönetici" yetkisiyle ekleyin ve izinleri onaylayın.

6. **RSS kaynaklarını ekle**  
   - `RSS 1`, `RSS 2` node’larının içine RSS URL’lerini gir.
   - [RSS LİSTESİ](https://bakinazik.github.io/rss/)
   - Gerekirse ek RSS kaynakları için yeni (RSS READ) node ekle.

7. **Workflow’u çalıştır**  
   - Scheduler otomatik olarak her 10 dakikada bir tetiklenecek.  
   - Haberler duplicate check’ten geçecek ve Telegram’a iletilecek.

---

## 📸 Diyagram Görseli
![Workflow Diyagramı](docs/workflow-diagram.png)

---

## 🤝 Katkıda Bulunma
Katkı sağlamak için projeyi fork edip Pull Request açabilirsiniz.  

---

## 📄 Lisans
Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.
