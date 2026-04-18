# 📄 CV Builder — AI-Powered Local CV Maker

> Tamamen yerel çalışan, yapay zeka destekli Türkçe/İngilizce CV oluşturucu.  
> Hiçbir sunucuya veri gönderilmez — tüm AI işlemleri kendi bilgisayarında, [Ollama](https://ollama.com) üzerinden çalışır.

---

## 📋 İçindekiler

- [Özellikler](#-özellikler)
- [CV Builder Bölümleri](#-cv-builder-bölümleri)
- [Gereksinimler](#-gereksinimler)
- [Kurulum](#-kurulum-adım-adım)
- [Desteklenen Modeller](#-desteklenen-modeller)
- [Model Seçimi](#-model-seçimi)
- [Sık Karşılaşılan Sorunlar ve Çözümleri](#-sık-karşılaşılan-sorunlar-ve-çözümleri)
- [Kullanım Kılavuzu](#-kullanım-kılavuzu)
- [Veri Güvenliği](#-veri-güvenliği)

---

## ✨ Özellikler

| Özellik | Açıklama |
|--------|----------|
| 🤖 **AI Metin Üretimi** | Deneyim görevlerini STAR formatına dönüştürme, özet yazma |
| 🌐 **TR / EN Çift Dil** | Tek tıkla Türkçe ↔ İngilizce CV çıktısı |
| 📊 **CV Analizi** | İçerik, ATS uyumluluğu, dil, yapı ve stratejik pozisyonlamaya göre 50 üzerinden puanlama |
| 🎨 **Özelleştirilebilir Şablon** | Renk paleti, font ve kolon düzeni seçimi |
| 💾 **Otomatik Kayıt** | Tüm veriler tarayıcının yerel belleğinde (localStorage) otomatik saklanır |
| 📤 **JSON Yedek/Geri Yükleme** | CV verisini dışa/içe aktar |
| 🖨️ **PDF Çıktısı** | Tarayıcının yazdır diyaloğu üzerinden seçilebilir metin içeren PDF |
| 📷 **OCR Desteği** | Sertifika görselinden otomatik metin tanıma (Tesseract.js) |
| 🔍 **Tanılama Aracı** | Ollama bağlantı sorunlarını otomatik tespit etme |
| 🔒 **Tamamen Yerel** | Hiçbir veri internete gönderilmez |

---

## 📂 CV Builder Bölümleri

CV Builder aşağıdaki sekmelere sahiptir. Her sekme CV'nin ayrı bir kısmını oluşturur:

### 1. 👤 Profil (Kişisel Bilgiler)
- Ad, soyad, e-posta, telefon (ülke kodu seçimi ile)
- Şehir ve ülke (arama destekli açılır menü)
- LinkedIn, GitHub, portföy URL'leri
- Hedef pozisyon ve hedef sektör (çoklu seçim + özel giriş)
- Profil fotoğrafı yükleme

### 2. 🎓 Eğitim
- Türkiye'deki tüm üniversiteleri kapsayan arama destekli liste
- Bölüm seçimi (dereceye göre filtrelenen liste: Lise / Ön Lisans / Lisans / Yüksek Lisans / Doktora)
- Başlangıç ve bitiş yılı, GPA girişi
- Bölüme özel önemli ders seçimi (chip arayüzü)
- Burs ve onur ödülleri seçimi

### 3. 💼 Deneyim ve Staj
- Şirket arama, pozisyon seçimi, çalışma türü (Staj / Part-time / Tam zamanlı / Gönüllü / Freelance)
- Ay/Yıl bazlı tarih seçici
- Pozisyona özgü **hızlı görev chip seçici** (önceden tanımlı sektörel görev listeleri)
- Ham nottan **AI ile STAR formatı üretimi** (Durum → Görev → Eylem → Sonuç)
- Türkçe STAR maddeleri için **otomatik İngilizce çeviri** (Ollama ile)

### 4. 🛠️ Projeler
- Proje adı, teknoloji yığını, açıklama
- GitHub / Canlı demo bağlantıları
- AI ile proje açıklaması geliştirme

### 5. 🧠 Beceriler
Kategorilere ayrılmış, arama destekli chip seçimi:
- **Programlama Dilleri** (C, C++, Python, Java, vb.)
- **Gömülü Sistemler** (STM32, ESP32, Arduino, Raspberry Pi, vb.)
- **Protokoller** (UART, SPI, I2C, CAN, Modbus, vb.)
- **EDA / Devre Tasarımı** (Altium, KiCad, LTSpice, vb.)
- **CAD / Mekanik** (SolidWorks, AutoCAD, Fusion 360, vb.)
- **IDE ve Geliştirme Ortamları**
- **Test & Ölçüm Ekipmanları**
- **DevOps / Sürüm Kontrolü**
- **İşletim Sistemleri**
- **Veritabanı**
- **Ofis Araçları**
- **Güç Elektroniği / Enerji**
- **Yabancı Diller** (seviye ile)
- **Kişisel / Sosyal Beceriler**

### 6. 📜 Sertifikalar ve Belgeler
- Sertifika görsel yükleme (JPEG, PNG, PDF)
- **OCR ile otomatik metin tanıma** (Tesseract.js)
- PDF'in ilk sayfasını görsel olarak işleme (PDF.js)
- Manuel ad, kurum, tarih ve özet düzenleme

### 7. 🤝 Gönüllülük
- Organizasyon, rol, tarih aralığı ve açıklama
- AI ile açıklama geliştirme

### 8. 📝 Özet / Hakkımda
- Türkçe ve İngilizce özet alanları
- AI ile özet üretimi (hedef pozisyon ve profil verisi kullanılarak)
- Farklı pozisyonlar için birden fazla özet varyantı kaydetme

### 🔬 CV Analizi *(Üst çubuk butonu)*
- Beş kriterde puanlama (her biri 10 üzerinden, toplam 50):
  - **İçerik Kalitesi** — nicelik, bağlam, özgünlük
  - **ATS Uyumluluğu** — anahtar kelime yoğunluğu, biçim
  - **Profesyonel Dil** — eylem fiilleri, ölçülebilir sonuçlar
  - **Yapı & Denge** — bölümlerin varlığı ve dengesi
  - **Stratejik Pozisyonlama** — hedef pozisyonla uyum
- Harf notu (A/B/C/D/F)
- Güçlü yanlar + 8–12 somut ve uygulanabilir öneri (yüksek/orta/düşük öncelikli)

---

## 📦 Gereksinimler

| Gereksinim | Versiyon | Açıklama |
|-----------|---------|----------|
| **Ollama** | En güncel | Yerel AI model sunucusu |
| **Modern Tarayıcı** | Chrome 90+ / Firefox 90+ / Edge 90+ | Safari kısmen desteklenir |
| **RAM** | En az 8 GB | Model boyutuna göre değişir (16 GB önerilir) |
| **Depolama** | 2–30 GB | İndirilen modele bağlı |
| **İnternet** | Sadece kurulum için | Modeli çektikten sonra gerekli değil |

> ⚠️ **Not:** Node.js, Python veya herhangi bir paket yöneticisi **gerekmez**. Uygulama tek bir `.html` dosyasıdır.

---

## 🚀 Kurulum (Adım Adım)

### Adım 1 — Ollama'yı İndir ve Kur

**Windows:**
1. [https://ollama.com/download](https://ollama.com/download) adresine git.
2. `OllamaSetup.exe` dosyasını indir ve çalıştır.
3. Kurulum tamamlandıktan sonra Ollama arka planda otomatik başlar.

**macOS:**
```bash
# Homebrew ile:
brew install ollama

# Veya doğrudan indirme:
# https://ollama.com/download adresinden .dmg indir
```

**Linux:**
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Kurulumu doğrulamak için terminalde:
```bash
ollama --version
```

---

### Adım 2 — Modeli İndir

Varsayılan model **Gemma 4 2B** (yaklaşık 2 GB):

```bash
ollama pull gemma4:e2b
```

> Daha güçlü bir model istiyorsan (önerilir):
> ```bash
> ollama pull gemma4:12b
> ```

İndirme tamamlandığında modeli test et:
```bash
ollama run gemma4:e2b "Merhaba, nasılsın?"
```

---

### Adım 3 — CORS Ayarını Yap (Kritik!)

CV Builder bir tarayıcıdan Ollama'ya istek gönderdiğinden CORS ayarı **zorunludur**.

**Windows (PowerShell veya CMD):**
```cmd
setx OLLAMA_ORIGINS "*"
```
Komutu çalıştırdıktan sonra **Ollama'yı yeniden başlat** (system tray → sağ tık → Quit, ardından tekrar aç).

**macOS / Linux:**
```bash
# ~/.bashrc veya ~/.zshrc dosyana ekle:
export OLLAMA_ORIGINS="*"

# Ardından terminali yeniden başlat veya:
source ~/.bashrc
```

Servisi yeniden başlat:
```bash
# macOS/Linux servis olarak çalışıyorsa:
ollama serve
```

> 💡 **Kontrol:** Tarayıcında `http://localhost:11434` adresini aç. `Ollama is running` yazısını görmelisin.

---

### Adım 4 — CV Builder'ı Çalıştır

1. `cv-builder.html` dosyasını bilgisayarına kaydet.
2. Dosyaya **çift tıkla** — tarayıcıda açılacak.
3. Sağ üst köşede `● Ollama bağlı ✓` yazısını gördüğünde hazırsın.

Herhangi bir kurulum, sunucu veya internet bağlantısı **gerekmez**.

---

## 🤖 Desteklenen Modeller

CV Builder, Ollama üzerinde çalışan **tüm** modellerle uyumludur. Yüklü modeller Ayarlar panelinde otomatik listelenir.

### 🌟 Önerilen Modeller

| Model | Komut | Boyut | Performans | Öneri |
|-------|-------|-------|-----------|-------|
| **Gemma 4 2B** *(varsayılan)* | `ollama pull gemma4:e2b` | ~2 GB | ⚡ Hızlı | RAM kısıtlıysa |
| **Gemma 4 12B** | `ollama pull gemma4:12b` | ~8 GB | 🎯 Dengeli | **Genel kullanım için önerilir** |
| **Gemma 4 27B** | `ollama pull gemma4:27b` | ~17 GB | 💎 Yüksek | Güçlü sistem için |
| **Gemma 3 12B** | `ollama pull gemma3:12b` | ~8 GB | 🎯 Dengeli | Alternatif |
| **Gemma 3 27B** | `ollama pull gemma3:27b` | ~17 GB | 💎 Yüksek | Alternatif |
| **Llama 3.2 3B** | `ollama pull llama3.2:3b` | ~2 GB | ⚡ Hızlı | Gemma alternatifi |
| **Llama 3.1 8B** | `ollama pull llama3.1:8b` | ~5 GB | 🎯 Dengeli | Alternatif |
| **Mistral 7B** | `ollama pull mistral:7b` | ~4 GB | 🎯 Dengeli | Alternatif |
| **Qwen 2.5 7B** | `ollama pull qwen2.5:7b` | ~5 GB | 🎯 Dengeli | Alternatif |

> **Not:** Gemma 4 serisi `<think>` etiketleriyle düşünce adımlarını gösterebilir. CV Builder bu etiketleri otomatik olarak temizler, yanıta yansımaz.

### Birden Fazla Model Kullanmak

Birden fazla model indirebilirsin — Ayarlar panelinden dilediğin zaman geçiş yapabilirsin:

```bash
ollama pull gemma4:e2b    # Hızlı görevler için
ollama pull gemma4:12b    # Kaliteli analiz için
```

### Hangi Modeli Seçmeliyim?

```
RAM < 8 GB   →  gemma4:e2b  veya  llama3.2:3b
RAM 8–16 GB  →  gemma4:12b  veya  mistral:7b
RAM > 16 GB  →  gemma4:27b  veya  gemma3:27b
```

---

## ⚙️ Model Seçimi

1. CV Builder'da sağ üst köşedeki **⚙ Ayarlar** butonuna tıkla.
2. **Ollama URL** alanı varsayılan olarak `http://localhost:11434` gelir — değiştirme.
3. **"Bağlan & Modelleri Listele"** butonuna tıkla.
4. Açılan **Model** açılır menüsünden istediğin modeli seç.
5. Seçim otomatik kaydedilir.

> 💡 Model yoksa önce `ollama pull <model-adı>` komutunu çalıştırıp ardından tekrar listele.

---

## 🔧 Sık Karşılaşılan Sorunlar ve Çözümleri

### ❌ "Bağlantı yok" / "CORS/Bağlantı hatası"

**Neden:** CORS ayarı yapılmamış veya Ollama çalışmıyor.

**Çözüm:**
```cmd
# Windows — CMD veya PowerShell'de çalıştır:
setx OLLAMA_ORIGINS "*"
```
Ardından Ollama'yı **tamamen kapat** (sistem tepsisi → sağ tık → Quit) ve yeniden aç.

---

### ❌ "Model bulunamadı" / HTTP 404

**Neden:** Seçili model indirilmemiş.

**Çözüm:**
```bash
ollama pull gemma4:e2b
```
Ayarlar panelinden modeli yeniden listele ve seç.

---

### ❌ "Zaman aşımı (4s)"

**Neden:** Ollama çalışıyor ama yavaş yanıt veriyor; model ilk kez yükleniyordur.

**Çözüm:** 30–60 saniye bekle, uygulama 30 saniyede bir otomatik yeniden bağlanır. Sayfada **"Yeniden Dene"** butonuna da tıklayabilirsin.

---

### ❌ AI butonları gri / devre dışı

**Neden:** Ollama bağlı değil.

**Çözüm:** Üst çubukta kırmızı uyarı bandındaki **"Tanıla"** butonuna tıkla — sorunun kaynağını gösterir. Ardından ilgili çözümü uygula.

---

### ❌ Tarayıcı dosyayı açmıyor / boş sayfa

**Neden:** Bazı tarayıcılar yerel dosyalarda `file://` protokolüyle sorun çıkarabilir.

**Çözüm — VS Code Live Server:**
```bash
# VS Code'da dosyayı aç → sağ tık → "Open with Live Server"
```

**Çözüm — Python ile basit sunucu:**
```bash
# Dosyanın bulunduğu klasörde:
python -m http.server 8080
# Tarayıcıda: http://localhost:8080/cv-builder.html
```

---

### ❌ PDF'de Türkçe karakterler bozuk

**Neden:** Tarayıcının yazdır ayarında arka plan grafikleri kapalı.

**Çözüm:** Yazdır diyaloğunda **"Arka plan grafikleri"** veya **"Background graphics"** seçeneğini etkinleştir.

---

### ❌ "Boş yanıt — model içerik üretemedi"

**Neden:** Model anlık olarak boş yanıt üretti (nadiren olur).

**Çözüm:** AI butonuna tekrar tıkla. Sorun devam ederse daha büyük bir model dene (`gemma4:12b`).

---

### ❌ OCR yanlış metin tanıdı

**Neden:** Sertifika görseli düşük çözünürlüklü veya eğik.

**Çözüm:** Yüksek çözünürlüklü, düz taranmış görsel kullan. Tanınan metni manuel olarak düzenleyebilirsin.

---

### 🔍 Tanılama Aracını Kullan

Sorunun kaynağını bulamazsan:
1. Kırmızı uyarı bandındaki **"Tanıla"** butonuna tıkla.
2. Açılan raporu kopyalayıp bir issue olarak paylaş.

---

## 📖 Kullanım Kılavuzu

### İlk Başlangıç
1. Ollama çalışıyor ve model indirilmiş olmalı (kurulum tamamlanmış).
2. `cv-builder.html` dosyasını tarayıcıda aç.
3. Sağ üstte **yeşil** `● Ollama bağlı ✓` görüyorsun — hazırsın!

### Temel Akış
```
Profil → Eğitim → Deneyim → Projeler → Beceriler → Sertifikalar → Özet → PDF
```

### Sağ Taraf — Canlı Önizleme
- CV her değişiklikte **anlık** güncellenir.
- **Renk** (altın, koyu, mavi, yeşil, bordo), **Font** ve **Kolon** (tek/çift) seçilebilir.
- **Dil** seçici (TR / EN) ile anında dil değiştirir.

### AI Özelliklerini Kullanmak
- Ollama bağlıyken sarı `✨ AI` etiketli butonlar aktif olur.
- Deneyim sekmesinde: görevi ham notlarla yaz → **"STAR Formatına Çevir"** butonuna tıkla.
- Özet sekmesinde: **"AI ile Üret"** → hedef pozisyona göre kişiselleştirilmiş özet gelir.
- **CV Analizi**: üst çubukta **"CV Analiz Et"** → 50 üzerinden puan + somut öneriler.

### PDF Kaydetme
1. Üst çubukta **"PDF (TR)"** veya **"PDF (EN)"** butonuna tıkla.
2. Tarayıcının yazdır diyaloğu açılır.
3. **Hedef:** "PDF Olarak Kaydet" seç.
4. **Arka plan grafikleri:** etkinleştir.
5. **Kaydet.**

### Yedekleme
- **Ayarlar → Dışa Aktar** → JSON dosyası indirilir.
- **Ayarlar → İçe Aktar** → JSON dosyasıyla eski CV geri yüklenir.
- Veriler aynı zamanda tarayıcının localStorage'ında otomatik tutulur.

---

## 🔒 Veri Güvenliği

- Tüm CV verisi **yalnızca kendi tarayıcında** saklanır (localStorage).
- AI işlemleri **yerel Ollama** üzerinden yapılır — hiçbir veri dışarıya gönderilmez.
- PDF üretimi tamamen istemci tarafında gerçekleşir.
- Uygulama internete yalnızca Google Fonts ve CDN kütüphaneleri (PDF.js, Tesseract.js) için bağlanır — bunlar sadece arayüz için kullanılır, CV verisi içermez.

---

## 📁 Proje Yapısı

```
cv-builder.html   ← Tek dosya, kurulum gerektirmez
README.md         ← Bu dosya
```

---

## 🐛 Sorun Bildirme

Hata veya öneri için bir **Issue** aç. Lütfen şunları ekle:

- İşletim sistemi ve tarayıcı
- Ollama versiyonu (`ollama --version`)
- Model adı
- Tanılama aracı çıktısı (uyarı bandındaki "Tanıla" butonu)

---

## 📜 Lisans

MIT License — dilediğin gibi kullanabilir, değiştirebilir ve dağıtabilirsin.

---

<div align="center">
  <sub>Yerel AI ile gizliliğini koruyarak CV hazırla 🚀</sub>
</div>
