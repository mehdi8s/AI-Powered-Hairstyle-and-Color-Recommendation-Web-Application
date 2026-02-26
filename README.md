# 💇 Ai_Kesim — AI-Powered Barber Appointment & Hair Analysis Web App

<p align="center">
  <img src="https://img.shields.io/badge/ASP.NET_Core-8.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white"/>
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white"/>
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
</p>

<p align="center">
  Sakarya Üniversitesi · Bilgisayar Mühendisliği Bölümü · Web Programlama Ödevi
</p>

---

## 📌 Proje Hakkında

**Ai_Kesim**, kullanıcıların fotoğraf yükleyerek yapay zeka destekli saç modeli ve renk önerileri alabileceği, aynı zamanda berber randevusu oluşturabileceği modern bir web uygulamasıdır.

Uygulama, yüklenen fotoğrafı analiz ederek kullanıcının yüz şekline, ten rengine ve genel karakteristik özelliklerine uygun saç modeli önerileri sunar. Bunun yanı sıra çalışan yönetimi, uzmanlık alanları ve randevu takip sistemi içerir.

---

## ✨ Özellikler

- 📷 **AI ile Saç Analizi** — Fotoğraf yükle, yapay zeka saç modeli öner
- 📅 **Randevu Sistemi** — Çalışan ve uzmanlık bazlı randevu oluşturma
- 🔐 **Kullanıcı Kayıt / Giriş** — Kimlik doğrulama sistemi
- 🛠️ **Admin Paneli** — Çalışan ekleme, düzenleme, silme ve randevu yönetimi
- 👨‍💼 **Çalışan & Uzmanlık Yönetimi** — Maaş, uzmanlık alanı ve randevu saatleri

---

## 🛠️ Kullanılan Teknolojiler

| Katman | Teknoloji |
|---|---|
| Backend | C#, ASP.NET Core 8 MVC |
| Veritabanı | Microsoft SQL Server, Entity Framework Core |
| Frontend | HTML5, CSS3, JavaScript, Bootstrap |
| Yapay Zeka | TensorFlow / PyTorch |
| Kimlik Doğrulama | ASP.NET Core Identity |

---

## 🗃️ Veritabanı Modeli

### Tablolar

**Calisan**
| Alan | Tip | Açıklama |
|---|---|---|
| Id | int | PK, Otomatik Artan |
| Isim | nvarchar(max) | Zorunlu |
| Soyisim | nvarchar(max) | Zorunlu |
| Maas | int | Zorunlu |

**Uzmanlik**
| Alan | Tip | Açıklama |
|---|---|---|
| Id | int | PK, Otomatik Artan |
| Ad | nvarchar(max) | Zorunlu |
| Ucret | int | Zorunlu |

**Randevu**
| Alan | Tip | Açıklama |
|---|---|---|
| Id | int | PK, Otomatik Artan |
| CalisanId | int | FK → Calisan |
| UzmanlikId | int | FK → Uzmanlik |
| UserId | nvarchar(450) | FK → UserDetails |
| RandevuTarihi | datetime2 | Zorunlu |

### İlişkiler
- **Kullanıcı → Fotoğraflar**: Bire-çok (bir kullanıcı birden fazla fotoğraf yükleyebilir)
- **Fotoğraf → Öneriler**: Bire-bir (her fotoğrafa bir öneri seti atanır)

---

## 🚀 Kurulum & Çalıştırma

### Gereksinimler
- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/tr-tr/sql-server/sql-server-downloads)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) veya VS Code

### Adımlar
```bash
# 1. Repoyu klonla
git clone https://github.com/mehdi8s/Web-Programlama-odevi.git
cd Web-Programlama-odevi

# 2. Bağlantı dizesini ayarla (appsettings.json)
# "ConnectionStrings": { "DefaultConnection": "Server=...;Database=AiKesim;..." }

# 3. Veritabanı migration'larını uygula
dotnet ef database update

# 4. Uygulamayı çalıştır
dotnet run
```

Tarayıcıda `https://localhost:5001` adresini açın.

---

## 📸 Uygulama Görüntüleri

| Kayıt Ekranı | Admin Paneli | AI Saç Analizi |
|---|---|---|
| Kullanıcı kayıt formu | Çalışan & randevu yönetimi | Fotoğraf yükle & analiz et |

---

## 👨‍💻 Geliştiriciler

| İsim | Numara |
|---|---|
| Mahdi Shahrouei 
| Melih Yasak 

**Sakarya Üniversitesi** — Bilgisayar ve Bilişim Bilimleri Fakültesi, Bilgisayar Mühendisliği Bölümü

---

## 📄 Lisans

Bu proje eğitim amaçlı geliştirilmiştir.
