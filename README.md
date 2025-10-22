# 🔧 Servis & Bakım Otomasyonu

[![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?logo=dotnet)](https://dotnet.microsoft.com/)
[![C#](https://img.shields.io/badge/C%23-12.0-239120?logo=csharp)](https://learn.microsoft.com/dotnet/csharp/)
[![WinForms](https://img.shields.io/badge/WinForms-Desktop-0078D4)](https://learn.microsoft.com/dotnet/desktop/winforms/)
[![SQLite](https://img.shields.io/badge/SQLite-3-003B57?logo=sqlite)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **HVAC, Asansör ve Jeneratör** bakım süreçlerinizi otomatikleştiren, **Excel ve WhatsApp'a veda etmenizi** sağlayan masaüstü çözümü.

---

## 🎯 Proje Vizyonu

Türkiye'de **100.000+** küçük teknik servis firması hala manuel süreçlerle çalışıyor. Bu proje, **sıfır abonelik ücreti** ile:

- ✅ Periyodik bakım takibini otomatikleştir
- ✅ Yasal uyumluluğu garantile (zorunlu bakım mevzuatı)
- ✅ Müşteri memnuniyetini artır (zamanında hatırlatma)
- ✅ Sahadan PDF raporlama yap
- ✅ Karmaşık ERP sistemlerine **20-50 bin ₺** ödemeden kurtul

---

## 🚀 Özellikler

### ✨ Şu An Aktif
*Henüz geliştirme aşamasında - yakında eklenecek*

### 📋 Planlanan Modüller

#### 1️⃣ **Müşteri Yönetimi**
- Firma/Bireysel müşteri kartları
- İletişim bilgileri (telefon, e-posta, adres)
- Cihaz envanteri (müşteri başına çoklu cihaz)
- Hızlı arama ve filtreleme

#### 2️⃣ **Cihaz Kartı**
- Cihaz tipi (HVAC, Asansör, Jeneratör, vb.)
- Seri numarası, marka, model
- Kurulum tarihi
- Bakım aralığı (15 gün, 1 ay, 3 ay, 6 ay, 1 yıl)
- Son bakım tarihi
- Garanti/Sözleşme durumu

#### 3️⃣ **Otomatik Hatırlatma Motoru**
- **Quartz.NET** ile arka plan zamanlayıcı
- Günlük bakım kontrolü
- Sistem tepsisi bildirimleri
- E-posta gönderimi (SMTP)
- WhatsApp Business API entegrasyonu (opsiyonel)
- Şablon yönetimi (özelleştirilebilir mesajlar)

#### 4️⃣ **Servis Formu & Raporlama**
- PDF çıktı (iTextSharp / QuestPDF)
- Teknisyen imzası
- Fotoğraf ekleme (bakım öncesi/sonrası)
- Malzeme kullanım listesi
- Müşteri onay imzası
- Toplu rapor çıkarma (aylık bakım özeti)

#### 5️⃣ **Dashboard & İstatistikler**
- Bugün yapılacak bakımlar
- Geciken bakımlar (kırmızı alarm)
- Bu ay tamamlanan işler
- Gelir/Gider takibi (basit muhasebe)
- Teknisyen performans raporu

---

## 🛠️ Teknoloji Yığını

| Katman | Teknoloji | Neden? |
|--------|-----------|--------|
| **Framework** | .NET 8 | Modern, performanslı, ücretsiz |
| **UI** | WinForms | Hızlı geliştirme, düşük donanım ihtiyacı |
| **Veritabanı** | SQLite | Dosya tabanlı, kolay yedekleme, sunucu gerektirmez |
| **Zamanlayıcı** | Quartz.NET | Güçlü cron ifadeleri, arka plan işleri |
| **PDF** | QuestPDF | Modern, kolay, ücretsiz (MIT) |
| **ORM** | Dapper / EF Core | Hafif veri erişimi |
| **E-posta** | MailKit | SMTP desteği |

---

## 📂 Proje Yapısı

```
ServisBakimOtomasyonu/
│
├── src/
│   ├── ServisBakim.UI/              # WinForms uygulaması
│   ├── ServisBakim.Core/            # İş mantığı (Business Logic)
│   ├── ServisBakim.Data/            # Veritabanı erişimi (Repository)
│   ├── ServisBakim.Models/          # Entity sınıfları
│   └── ServisBakim.Services/        # Harici servisler (E-posta, PDF)
│
├── database/
│   └── schema.sql                   # SQLite şema
│
├── docs/
│   ├── screenshots/                 # Uygulama ekran görüntüleri
│   └── user-guide.md                # Kullanım kılavuzu
│
├── tests/
│   └── ServisBakim.Tests/           # Birim testler
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🚦 Kurulum

### Gereksinimler
- **Windows 10/11** (64-bit)
- **.NET 8 Runtime** → [İndir](https://dotnet.microsoft.com/download/dotnet/8.0)

### Geliştirici Kurulumu

```bash
# Repoyu klonla
git clone https://github.com/fatihbugraayar/ServisBakimOtomasyonu.git
cd ServisBakimOtomasyonu

# Çözümü aç
dotnet restore
dotnet build

# Uygulamayı çalıştır
cd src/ServisBakim.UI
dotnet run
```

### Kullanıcı Kurulumu (İleriki Sürümler)
*Henüz yayınlanmış bir setup paketi yok. Geliştirme tamamlandığında `.msi` kurulum dosyası burada olacak.*

---

## 📸 Ekran Görüntüleri

*Yakında eklenecek*

---

## 🗺️ Yol Haritası

### 🔹 Faz 1: Temel Altyapı (Q4 2025)
- [x] Proje oluşturma
- [ ] SQLite şema tasarımı
- [ ] Repository pattern implementasyonu
- [ ] Temel CRUD işlemleri

### 🔹 Faz 2: Ana Modüller (Q1 2026)
- [ ] Müşteri yönetimi ekranları
- [ ] Cihaz kartı formu
- [ ] Bakım planı oluşturma
- [ ] Dashboard tasarımı

### 🔹 Faz 3: Otomasyon (Q2 2026)
- [ ] Quartz.NET entegrasyonu
- [ ] Hatırlatma motoru
- [ ] E-posta gönderim sistemi
- [ ] Bildirim yönetimi

### 🔹 Faz 4: Raporlama & PDF (Q2 2026)
- [ ] PDF şablon tasarımı
- [ ] Servis formu oluşturma
- [ ] Dijital imza desteği
- [ ] Toplu rapor çıkarma

### 🔹 Faz 5: İleri Özellikler (Q3 2026)
- [ ] WhatsApp Business API
- [ ] Mobil uygulama (MAUI)
- [ ] Bulut senkronizasyon (opsiyonel)
- [ ] Çok dilli destek

---

## 🤝 Katkıda Bulunma

Katkılarınızı bekliyoruz! İşte nasıl yardımcı olabilirsiniz:

1. **Fork** yapın
2. Feature branch oluşturun (`git checkout -b feature/harika-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -m 'Harika özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/harika-ozellik`)
5. **Pull Request** açın

### Katkı Alanları
- 🐛 Bug düzeltmeleri
- ✨ Yeni özellik önerileri
- 📝 Dokümantasyon iyileştirmeleri
- 🌍 Yerelleştirme (dil desteği)
- 🎨 UI/UX tasarım önerileri

---

## 📜 Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır - detaylar için [LICENSE](LICENSE) dosyasına bakın.

**Özet:** Ticari dahil her türlü kullanım serbesttir. Kaynak kodu değiştirilebilir ve dağıtılabilir.

---

## 💬 İletişim & Destek

- **Geliştirici:** [@fatihbugraayar](https://github.com/fatihbugraayar)
- **Issues:** [GitHub Issues](https://github.com/fatihbugraayar/ServisBakimOtomasyonu/issues)
- **Discussions:** [GitHub Discussions](https://github.com/fatihbugraayar/ServisBakimOtomasyonu/discussions)

---

## 🌟 Destekleyin

Projeyi beğendiyseniz ⭐ vermeyi unutmayın!

<p align="center">
  <sub>Türkiye'deki küçük işletmelerin dijitalleşmesine katkı 🇹🇷</sub>
</p>

---

## 📊 İstatistikler

![GitHub stars](https://img.shields.io/github/stars/fatihbugraayar/ServisBakimOtomasyonu?style=social)
![GitHub forks](https://img.shields.io/github/forks/fatihbugraayar/ServisBakimOtomasyonu?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/fatihbugraayar/ServisBakimOtomasyonu?style=social)

---

<p align="center">
  <strong>Made with ❤️ for Turkish service companies</strong>
</p>
