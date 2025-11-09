# 🎓 KOSTÜ Sınav Sistemi

<div align="center">

**Kocaeli Sağlık ve Teknoloji Üniversitesi**  
**Web Tabanlı Sınav Yönetim Sistemi**

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0.0-000000?logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-18.0-61DAFB?logo=react&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.0-646CFF?logo=vite&logoColor=white)

</div>

---

## 📖 İçindekiler

- [Özellikler](#-özellikler)
- [Ekran Görüntüleri](#-ekran-görüntüleri)
- [Teknolojiler](#️-teknolojiler)
- [Hızlı Başlangıç](#-hızlı-başlangıç)
- [Kurulum](#-kurulum)
- [Kullanım](#-kullanım)
- [Roller ve Yetkiler](#-roller-ve-yetkiler)
- [Güvenlik](#-güvenlik)
- [Katkıda Bulunma](#-katkıda-bulunma)

---

## ✨ Özellikler

### 🎯 Temel Özellikler

- ✅ **4 Rol Sistemi** - Admin, Öğretim Üyesi, Öğrenci, Bölüm Başkanı
- ✅ **Soru Havuzu Sistemi** - 20 soru ekle, rastgele 5'i sorulsun
- ✅ **Otomatik Puanlama** - Anında sonuç hesaplama
- ✅ **Ağırlıklı Not Sistemi** - Vize %40, Final %60
- ✅ **Zamanlı Sınavlar** - Belirli tarih ve saat aralığında
- ✅ **Güvenli JWT Auth** - Token tabanlı kimlik doğrulama
- ✅ **Responsive Tasarım** - Mobil uyumlu arayüz

### 🎲 Soru Havuzu Sistemi

Öğretim üyeleri istediği kadar soru ekleyebilir, sistem her öğrenciye rastgele sorular gösterir:

```
Soru Havuzu: 20 soru
Sınavda: 5 soru (rastgele)
→ Her öğrenci farklı sorular görebilir! 🎲
```

### ⏱️ Otomatik Sınav Yönetimi

- **Süre Kontrolü**: 10 dakikalık geri sayım
- **Otomatik Kaydetme**: Süre bitince otomatik gönderilir
- **Tek Giriş**: Her öğrenci sadece 1 kez sınava girebilir
- **Anlık Sonuç**: Sınav bitince anında puan hesaplanır

---

## 📸 Ekran Görüntüleri

### Giriş Ekranı
KOSTÜ teması ile modern ve güvenli giriş ekranı

### Admin Paneli
Kullanıcı, ders ve kayıt yönetimi

### Öğretim Üyesi Paneli
Test oluşturma, soru havuzu yönetimi ve sonuç görüntüleme

### Öğrenci Paneli
Sınav alma ve sonuç görüntüleme

### Bölüm Başkanı Paneli
Ders ve öğrenci istatistikleri

---

## 🛠️ Teknolojiler

### Backend
- **Flask 3.0.0** - Python web framework
- **SQLAlchemy 2.0.44** - ORM
- **Flask-JWT-Extended 4.6.0** - JWT authentication
- **PyMySQL 1.1.2** - MySQL connector
- **Flask-CORS 4.0.0** - Cross-origin resource sharing
- **Werkzeug** - Password hashing

### Frontend
- **React 18.0** - UI library (Vanilla JS - JSX kullanılmadan)
- **Vite 5.0** - Build tool
- **React Router DOM** - Client-side routing
- **Fetch API** - HTTP client

### Database
- **MySQL 8.0+** - İlişkisel veritabanı
- **utf8mb4** - Türkçe karakter desteği

---

## 🚀 Hızlı Başlangıç

### Gereksinimler

- Python 3.13+
- Node.js 18+
- MySQL 8.0+

### Tek Tuşla Başlatma

```bash
# Repository'yi klonlayın
git clone https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi.git
cd Sinav-Sistemi

# .env dosyası oluşturun
copy env.example .env
# .env dosyasını düzenleyin ve MySQL şifrenizi girin

# Bağımlılıkları yükleyin
pip install -r requirements.txt
npm install

# MySQL veritabanı oluşturun
mysql -u root -p
CREATE DATABASE exam_system CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
exit

# Sistemi başlatın
BASLAT.bat
```

Tarayıcınızda **http://localhost:3000** açın!

---

## 📦 Kurulum

### 1. Repository'yi Klonlayın

```bash
git clone https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi.git
cd Sinav-Sistemi
```

### 2. Ortam Değişkenlerini Ayarlayın

```bash
# env.example'ı kopyalayın
copy env.example .env
```

`.env` dosyasını düzenleyin:

```env
DATABASE_URL=mysql://root:YOUR_PASSWORD@localhost/exam_system
JWT_SECRET_KEY=your-secret-key-change-this
```

### 3. Python Bağımlılıklarını Yükleyin

```bash
# Virtual environment oluşturun
python -m venv venv

# Aktif edin (Windows)
.\venv\Scripts\activate

# Bağımlılıkları yükleyin
pip install -r requirements.txt
```

### 4. Node.js Bağımlılıklarını Yükleyin

```bash
npm install
```

### 5. MySQL Veritabanı Oluşturun

```sql
CREATE DATABASE exam_system CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### 6. Başlatın

**Otomatik:**
```bash
BASLAT.bat
```

**Manuel:**
```bash
# Terminal 1 - Backend
.\venv\Scripts\activate
python app.py

# Terminal 2 - Frontend
npm run dev
```

---

## 📚 Kullanım

### İlk Giriş

```
URL: http://localhost:3000
Kullanıcı: admin
Şifre: admin123
```

### Kullanım Akışı

#### 1️⃣ Admin Olarak

1. **Kullanıcılar** sekmesinde:
   - 10+ öğrenci ekleyin
   - 2+ öğretim üyesi ekleyin
   - Bölüm başkanı ekleyin

2. **Dersler** sekmesinde:
   - 4+ ders oluşturun
   - Her derse öğretim üyesi atayın

3. **Kayıtlar** sekmesinde:
   - Öğrencileri derslere kaydedin
   - Her öğrenci min. 2 derse kayıtlı olmalı

#### 2️⃣ Öğretim Üyesi Olarak

1. **Testler** sekmesinde:
   - Vize testi oluştur (Ağırlık: %40)
   - Final testi oluştur (Ağırlık: %60)
   - Sınav tarih ve saatlerini belirle
   - Kaç soru sorulacağını seç (ör: 5)

2. **Sorular** sekmesinde:
   - Soru havuzuna 5+ soru ekle
   - İstediğiniz kadar soru ekleyebilirsiniz!
   - Öğrenciye rastgele belirlenen sayıda soru gösterilir

3. **Sonuçlar**:
   - Sınav bitince öğrenci puanlarını görün
   - Sınıf ortalamasını kontrol edin

#### 3️⃣ Öğrenci Olarak

1. **Sınavlar** sekmesinde:
   - Aktif sınavları görün
   - Sınav saatinde "Sınava Başla" tıklayın

2. **Sınav**:
   - 10 dakika içinde soruları cevaplayın
   - Süre bitince otomatik kaydedilir

3. **Sonuçlar**:
   - Puanınızı görün
   - Sınıf ortalamasını kontrol edin
   - Doğru/yanlış cevapları inceleyin

#### 4️⃣ Bölüm Başkanı Olarak

- Tüm derslerin istatistiklerini görüntüleyin
- Öğrenci başarı oranlarını inceleyin
- Ders ortalamalarını takip edin

---

## 👥 Roller ve Yetkiler

### 🔑 Admin

| Yetki | Açıklama |
|-------|----------|
| ✅ Kullanıcı Yönetimi | Öğrenci, öğretim üyesi, bölüm başkanı ekle/sil |
| ✅ Ders Yönetimi | Ders oluştur, öğretim üyesi ata/değiştir, sil |
| ✅ Kayıt Yönetimi | Öğrencileri derslere kaydet |

### 👨‍🏫 Öğretim Üyesi

| Yetki | Açıklama |
|-------|----------|
| ✅ Test Oluşturma | Vize/Final testleri oluştur |
| ✅ Soru Havuzu | Sınırsız soru ekle, düzenle, sil |
| ✅ Sınav Ayarları | Tarih, saat, süre belirle |
| ✅ Sonuç Görüntüleme | Öğrenci puanları ve istatistikler |

### 👨‍🎓 Öğrenci

| Yetki | Açıklama |
|-------|----------|
| ✅ Ders Görüntüleme | Kayıtlı dersleri görüntüle |
| ✅ Sınav Alma | Belirli zaman diliminde sınava gir |
| ✅ Sonuç Görüntüleme | Puanlar ve detaylı cevaplar |

### 📊 Bölüm Başkanı

| Yetki | Açıklama |
|-------|----------|
| ✅ İstatistikler | Tüm ders ve öğrenci istatistikleri |
| ✅ Raporlama | Başarı oranları ve ortalamalar |

---

## 🔒 Güvenlik

### Uygulanan Güvenlik Önlemleri

- 🔐 **JWT Token** tabanlı kimlik doğrulama (24 saat geçerlilik)
- 🔒 **Werkzeug** ile şifre hash'leme
- 🛡️ **Role-based Authorization** - Her rol sadece yetkili işlemleri yapabilir
- 🚫 **SQL Injection** koruması (SQLAlchemy ORM)
- 🔑 **UNIQUE Constraints** - Username, email, full_name benzersiz
- 🙈 **`.env` Koruması** - Hassas bilgiler .gitignore'da
- ✅ **Input Validasyonları** - Frontend ve backend'de çift kontrol

### .env Dosyası

⚠️ **ÖNEMLİ:** `.env` dosyası şifrelerinizi içerir ve **asla GitHub'a yüklenmemelidir!**

```bash
# .env dosyası .gitignore'da olduğundan GitHub'a yüklenmez
# Her kullanıcı kendi .env dosyasını env.example'dan oluşturmalıdır
```

---

## 📁 Proje Yapısı

```
kostu-sinav-sistemi/
├── 📄 app.py                      # Flask Backend API
├── 📋 requirements.txt            # Python bağımlılıkları
├── 📦 package.json                # Node.js bağımlılıkları
├── 🚀 BASLAT.bat                  # Tek tuşla başlatma scripti
├── 🔒 .env.example                # Ortam değişkenleri şablonu
├── 📖 README.md                   # Proje dokümantasyonu
├── 📝 NASIL_KULLANILIR.txt        # Detaylı kullanım rehberi
├── 📊 PROJE_OZET.md               # Proje özeti
├── 🎨 logo.png                    # KOSTÜ logosu
├── 🌐 index.html                  # HTML template
├── ⚙️ vite.config.js              # Vite yapılandırması
│
├── 📂 src/                        # Frontend kaynak kodları
│   ├── App.js                     # Ana React bileşeni
│   ├── main.js                    # Entry point
│   ├── styles.css                 # Global stiller
│   ├── components/                # React bileşenleri
│   │   ├── Login.js
│   │   ├── AdminDashboard.js
│   │   ├── InstructorDashboard.js
│   │   ├── StudentDashboard.js
│   │   └── DepartmentHeadDashboard.js
│   ├── context/
│   │   └── AuthContext.js         # Authentication context
│   └── utils/
│       └── api.js                 # API helper fonksiyonları
│
└── 📂 public/                     # Statik dosyalar
```

---

## 🚀 Hızlı Başlangıç

### Windows'ta Tek Komut

```bash
# 1. Klonlayın
git clone https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi.git
cd Sinav-Sistemi

# 2. .env oluşturun
copy env.example .env
notepad .env  # MySQL şifrenizi girin

# 3. Kurulum ve başlatma
pip install -r requirements.txt && npm install && BASLAT.bat
```

### İlk Giriş

- **URL**: http://localhost:3000
- **Kullanıcı**: `admin`
- **Şifre**: `admin123`

---

## 📦 Detaylı Kurulum

### Adım 1: Sistem Gereksinimleri

- [Python 3.13+](https://www.python.org/downloads/)
- [Node.js 18+](https://nodejs.org/)
- [MySQL 8.0+](https://dev.mysql.com/downloads/)

### Adım 2: Repository'yi İndirin

```bash
git clone https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi.git
cd Sinav-Sistemi
```

### Adım 3: Backend Kurulumu

```bash
# Virtual environment oluşturun
python -m venv venv

# Aktif edin
.\venv\Scripts\activate  # Windows
source venv/bin/activate  # Linux/Mac

# Bağımlılıkları yükleyin
pip install -r requirements.txt
```

### Adım 4: Frontend Kurulumu

```bash
npm install
```

### Adım 5: Veritabanı Kurulumu

MySQL'e giriş yapın ve veritabanı oluşturun:

```sql
CREATE DATABASE exam_system CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### Adım 6: Ortam Değişkenlerini Ayarlayın

```bash
# env.example'ı kopyalayın
copy env.example .env
```

`.env` dosyasını düzenleyin:

```env
DATABASE_URL=mysql://root:YOUR_MYSQL_PASSWORD@localhost/exam_system
JWT_SECRET_KEY=change-this-to-a-random-secret-key
```

### Adım 7: Başlatın

**Otomatik (Önerilen):**
```bash
BASLAT.bat
```

**Manuel:**
```bash
# Terminal 1 - Backend
.\venv\Scripts\activate
python app.py

# Terminal 2 - Frontend
npm run dev
```

Tarayıcınızda **http://localhost:3000** adresini açın!

---

## 📚 Kullanım

### Admin İşlemleri

```
1. Admin ile giriş yapın (admin/admin123)
2. Kullanıcılar → 10+ öğrenci, 2+ öğretim üyesi ekleyin
3. Dersler → 4+ ders oluşturun
4. Kayıtlar → Öğrencileri derslere kaydedin
```

### Öğretim Üyesi İşlemleri

```
1. Öğretim üyesi ile giriş yapın
2. Testler → Vize (%40) ve Final (%60) oluşturun
3. Sorular → Her teste 5+ soru ekleyin (İstediğiniz kadar!)
4. Sistem sınavda rastgele soruları seçer
```

### Öğrenci İşlemleri

```
1. Öğrenci ile giriş yapın
2. Sınavlar → Aktif sınavlara girin
3. 10 dakika içinde soruları cevaplayın
4. Sonuçlar → Puanınızı ve sınıf ortalamasını görün
```

### Bölüm Başkanı İşlemleri

```
1. Bölüm başkanı ile giriş yapın
2. Tüm ders istatistiklerini görüntüleyin
3. Öğrenci başarı raporlarını inceleyin
```

---

## 🎯 Özellik Detayları

### Soru Havuzu Sistemi


✅ Soru havuzuna 20+ soru ekle
✅ Her öğrenciye rastgele 5 soru
✅ Farklı öğrenciler farklı sorular görür
✅ Kopya riski minimum
```

### Ağırlıklı Not Sistemi

```
Final Grade = (Vize × 0.40) + (Final × 0.60)

Örnek:
Vize: 70 puan  → 70 × 0.40 = 28
Final: 80 puan → 80 × 0.60 = 48
Ders Notu: 28 + 48 = 76 ✅
```

### Zaman Yönetimi

```
Sınav Saati: 10:00 - 12:00 (2 saat pencere)
Öğrenci Süresi: 10 dakika

Öğrenci 1 → 10:05'te girer → 10:15'e kadar süre
Öğrenci 2 → 10:30'da girer → 10:40'a kadar süre
Öğrenci 3 → 11:50'de girer → 12:00'a kadar süre
```

---

## 🔐 Güvenlik Önlemleri

### Kimlik Doğrulama

- **JWT Tokens** - 24 saat geçerlilik süresi
- **Werkzeug** şifre hash'leme
- **Role-based** yetkilendirme

### Veritabanı Güvenliği

- **SQLAlchemy ORM** - SQL injection koruması
- **UNIQUE Constraints** - Veri bütünlüğü
- **Foreign Keys** - İlişkisel veri tutarlılığı
- **Cascade Delete** - Veri temizliği

### Uygulama Güvenliği

- ✅ Şifreler hash'lenerek saklanır
- ✅ .env dosyası Git'e yüklenmez
- ✅ CORS politikaları
- ✅ Input validasyonları (frontend + backend)
- ✅ XSS koruması

---

## 🐛 Sorun Giderme

### Backend Başlamıyor

```bash
# MySQL servisinin çalıştığını kontrol edin
services.msc → MySQL → Start

# .env dosyasındaki şifrenin doğru olduğunu kontrol edin
notepad .env
```

### Frontend Başlamıyor

```bash
# Node.js'in yüklü olduğunu kontrol edin
node --version

# Bağımlılıkları yeniden yükleyin
npm install
```

### Sınav Başlamıyor

```bash
# Test havuzunda minimum 5 soru olmalı
# Sınav saatinin aktif olduğunu kontrol edin
# Backend terminalindeki hata mesajlarını kontrol edin
```

---

## 🤝 Katkıda Bulunma

Bu proje eğitim amaçlı geliştirilmiştir. Katkılarınızı bekliyoruz!

### Pull Request Süreci

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Commit yapın (`git commit -m 'Add some AmazingFeature'`)
4. Push edin (`git push origin feature/AmazingFeature`)
5. Pull Request açın

---



## 📞 İletişim

**Proje Sahibi:** [https://github.com/emrebgg]

**Proje Linki:** [https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi](https://github.com/KULLANICI_ADINIZ/Sinav-Sistemi)

---

## 🎊 Teşekkürler

Bu proje **Kocaeli Sağlık ve Teknoloji Üniversitesi** için geliştirilmiştir.

---

<div align="center">
