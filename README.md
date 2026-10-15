# Instagram Agent Skill (Türkçe Sürüm & Web Stüdyosu)

Bir Instagram hesabını sıfırdan zirveye yönetmek için tasarlanmış **13 yapay zeka yeteneği (skill)**, bilgisayarınızda çalışan **5 yerel analiz motoru** ve tarayıcıdan anında kullanılabilen **GitHub Pages Web Stüdyosu**.

Tamamen ücretsiz, MIT lisanslı, kayıt gerektirmez, API anahtarı istemez, Instagram şifresi talep etmez.

> Bu proje, [Jake Schincariol](https://github.com/Jakeschincariol/instagram-agent-skill) tarafından geliştirilen açık kaynaklı projenin **kapsamlı Türkçe yerelleştirmesi, Türkçe konuşma diline uyarlanmış kanca formülleri ve çoklu hesap destekli Web Arayüzü** eklenmiş halidir.

---

### 🌐 Canlı Web Stüdyosu (Hemen Kullanın)
Kurulum yapmadan, doğrudan tarayıcınızdan kanca puanlamak, açıklama denetlemek ve 26 kanca formülünü incelemek için:  
👉 **[https://asklepios0.github.io/instagram-agent-skill/](https://asklepios0.github.io/instagram-agent-skill/)**

---

## 🎯 Temel Felsefe: "Siz Evet Demeden Hiçbir Şey Paylaşılmaz"

Bu araç bir otomatik paylaşım botu **değildir**. Instagram'ın resmi İçerik Yayınlama API'si dışındaki tüm botlar ve otomatik giriş yazılımları Instagram Kullanım Koşulları'nı ihlal eder ve hesabınızın kısıtlanmasına (shadowban / action-block) sebep olur.

Bu yüzden sistem şöyle çalışır: **Yapay zeka yazar, puanlar, kurgular ve zamanlar; siz onaylar ve kendi elinizle paylaşırsınız.** Sıfır ban riski, maksimum içerik kalitesi.

---

## 📦 13 Temel Yetenek (Komutlar)

| Komut | Ne İşe Yarar? |
| :--- | :--- |
| **`/ig-reel`** | Aklınızdaki ham bir fikri tam bir Reel senaryosuna dönüştürür. 26 formülden 3 alternatif kanca çıkarır, bunları puanlar, ekranda çıkacak yazıları ve saniyesine kadar zamanlanmış çekim planını (beat sheet) hazırlar. |
| **`/ig-viral`** | Sektörünüzde gerçekten çalışan videoları bulur; ham izlenmeye göre değil, hesabın kendi ortalama izlenmesine kıyasla **kaç kat patladığına (outlier multiple)** göre sıralar. |
| **`/ig-caption`** | Gönderi açıklaması yazar ve denetler. Akışta "...daha fazla" butonundan önce görünen **ilk 125 karakteri** optimize eder. Güncel 5 hashtag kuralını uygular. |
| **`/ig-carousel`** | Kaydırmalı gönderi kurgular. Kaydırmayı tetikleyen kapak, slayt metinleri ve 1080x1350 formatına uygun görsel kurgular üretir. |
| **`/ig-story`** | Günlük hikaye serileri, hangi etkileşim çıkartmasının (anket, soru vb.) ne zaman kullanılacağı ve takipçiyi DM'e çeken huniler tasarlar. |
| **`/ig-profile`** | Profilinizi (biyografi, isim alanı, link, öne çıkanlar) 12 kriterli bir rubrikle 100 üzerinden puanlar ve puan kaybettiren kısımları düzeltir. |
| **`/ig-plan`** | Haftalık içerik takvimini, paylaşım formatlarını, zamanlamayı ve günlük etkileşime girilecek 10 hedef hesabı belirler. |
| **`/ig-human`** | Metindeki yapay zeka kokusunu, *"dijital dünyada", "çığır açan", "unutmayın ki"* gibi klişeleri, uzun tireleri ve kopyalama filigranlarını temizler. |
| **`/ig-comment`** | Başka hesapların gönderilerine atılacak 9 farklı kategoride dikkat çekici yorum üretir. Asla "🔥🔥🔥" veya boş spam yapmaz. |
| **`/ig-reply`** | Kendi gönderinizin altındaki yorumları ayıklar (müşteri adayı, soru, gürültü vb.) ve öncelik sırasına göre yanıtlar hazırlar. |
| **`/ig-dm`** | Yorumdan gelen anahtar kelime teslimatını, ilk mesajı, iş birliği teklifini ve en fazla 2 aşamalı takip (follow-up) mesajlarını yazar. |
| **`/ig-repurpose`** | 1 uzun videodan, podcast'ten veya bültenden bir haftalık bağımsız Reels ve Carousel gönderileri türetir. |
| **`/ig-audit`** | Önceden paylaştığınız içeriklerin otopsisini yapar. İzlenme sayısı yerine erişim başına kaydetme ve paylaşım oranlarıyla analiz eder. |

---

## ⚡ Arka Planda Çalışan 5 Yerel Python Aracı

Hiçbir harici API'ye veya internet bağlantısına ihtiyaç duymaz. Tamamen sizin bilgisayarınızda yerel çalışır:

### 1. Kanca Puanlayıcı (`hookscore.py`)
```bash
python skills/ig-reel/hookscore.py --hook "18.000 TL tek bir eksik sözleşme maddesinin bana maliyetidir"
```
* Kancanızı 5 temel kritere göre (Uzunluk, Somutluk, Gerilim/Maliyet, Başa Yerleşim ve Hitap) 100 üzerinden puanlar.
* *"Selam arkadaşlar..."* gibi ölü açılışları veya *"Kaydırmayı durdur"* klişelerini **ÖLÜMCÜL HATA (DEALBREAKER)** olarak anında yakalar.
* Türkçe para birimlerini (TL, ₺), yazıyla yazılan sayıları ve konuşma dilini tam destekler.

### 2. Çekim Zamanlayıcı (`beats.py`)
```bash
python skills/ig-reel/beats.py senaryo.txt --target 30
```
* Metni dakikada 165 kelime Türkçe konuşma hızına göre hesaplar.
* Kancanın 3 saniyeyi aşıp aşmadığını, 4 saniyeden uzun süren durgun/sıkıcı yerleri ve videonun sonunun başına bağlanıp bağlanmadığını (loop video) denetler.

### 3. Açıklama Denetleyici (`caption.py`)
```bash
python skills/ig-caption/caption.py aciklama.txt
```
* Kullanıcının akışta göreceği ilk 125 karakterlik pencereyi bir kutu içinde simüle eder.
* Güncel kurala göre **maksimum 5 hashtag** sınırını denetler (30 hashtag dönemi bitti).
* Net bir eyleme çağrı (CTA: yoruma yaz, DM at, kaydet) olup olmadığını kontrol eder.

### 4. İnsanlaştırıcı & AI Dedektörü (`humanize.py` & `detect.py`)
```bash
python skills/ig-human/humanize.py metin.txt --report
```
* Metindeki yapay zeka klişelerini (*"dijital dünyada", "çığır açan", "unutmayın ki", "özetle"* vb.) ve görünmez filigran karakterlerini temizler.

### 5. Viral Kıyaslama Aracı (`swipe.py`)
```bash
python skills/ig-viral/swipe.py captured.tsv
```
* Sektördeki videoları hesapların kendi ortalama (medyan) izlenmelerine kıyasla kaç kat patladığına (outlier multiple) göre sıralar ve 26 kanca formülüyle eşleştirir.

---

## 📚 26 Kanıtlanmış Türkçe Kanca Formülü

`skills/ig-reel/hooks_tr.json` dosyasında Türkçe dilbilgisine, devrik ve kurallı cümle yapılarına göre uyarlanmış 26 formül yer alır:
1. **Maliyet / Hata İtirafı:** *"18.000 TL, sözleşmedeki tek bir eksik cümlenin bana maliyeti."*
2. **Olumsuz Emir:** *"Her gün video atmayı bırakın. Bunun yerine şunu yapın."*
3. **Kimse Söylemiyor:** *"Kimse size ilk 30 videonuzun batacağını söylemez."*
4. **Tasarruf / İkame:** *"Bu 300 TL'lik araç, ayda 25.000 TL ödediğim editörün yerini aldı."*
5. **Zaman Sıkıştırması:** *"Teklif hazırlamak eskiden 5 saatimi alırdı. Artık 20 dakikamı alıyor."*
6. **Rakam Masada (Fatura):** *"60 gün boyunca her gün motor sürdüm; işte gerçek servis faturam."*
... ve diğer 20 formül.

---

## 🎙️ Kendi Ses Tonunuzu Belirleme (`ses_profili.md`)

[`templates/ses_profili.md`](templates/ses_profili.md) dosyasını açıp 5 dakikada doldurun:
* Kimsiniz ve kime hitap ediyorsunuz?
* Kamera karşısındaki enerjiniz nasıl? (Hızlı, sakin, esprili, resmi)
* Hangi kelimeleri sık kullanır, hangilerini asla ağzınıza almazsınız?
* Sektörünüzde çoğu kişinin savunduğu ama sizin katılmadığınız gerçekler neler?

Bu dosya doldurulduğunda, üretilen tüm senaryolar ve metinler doğrudan **sizin ağzınızdan çıkmış gibi** konuşur.

---

## 💻 Kurulum ve Kullanım

### 1. Claude Code ile Kullanım
Depoyu klonlayın ve skilleri Claude Code klasörünüze kopyalayın:
```bash
git clone https://github.com/Asklepios0/instagram-agent-skill.git
cp -r instagram-agent-skill/skills/* ~/.claude/skills/
```

### 2. Antigravity / Gemini / Cursor ile Kullanım
Depoyu projenize ekleyin. Sohbete tek başına **`*`** (yıldız) yazdığınızda 14 maddelik Türkçe komut menüsü açılacaktır.

### 3. Doğrudan Web Üzerinden Kullanım
Hiçbir kurulum yapmadan [Canlı Web Arayüzü](https://asklepios0.github.io/instagram-agent-skill/) üzerinden tüm araçları interaktif olarak kullanabilirsiniz.

---

## 📜 Lisans & Teşekkür

* **Orijinal Proje Sahibi:** Jake Schincariol ([opusjake.ai](https://opusjake.ai) / [Orijinal Repo](https://github.com/Jakeschincariol/instagram-agent-skill))
* **Türkçe Sürüm & Web UI:** [Asklepios0](https://github.com/Asklepios0)
* **Lisans:** MIT Lisansı (Özgürce kullanılabilir, geliştirilebilir ve paylaşılabilir).
