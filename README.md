# Instagram İçerik & Büyüme Stüdyosu (Türkçe Sürüm)

Bir Instagram hesabını sıfırdan zirveye taşımak için geliştirilmiş **13 yapay zeka aracı**, bilgisayarınızda yerel çalışan **5 analiz motoru** ve tarayıcıdan anında kullanılabilen **Web Stüdyosu**.

Tamamen ücretsiz, MIT lisanslı, kayıt gerektirmez, API anahtarı istemez, Instagram şifrenizi asla talep etmez.

> Bu proje, [Jake Schincariol](https://github.com/Jakeschincariol/instagram-agent-skill) tarafından geliştirilen açık kaynaklı projenin **tamamen Türkçe konuşma diline uyarlanmış, 26 yerel açılış formülü eklenmiş ve 10 hesaba kadar destek veren Web Stüdyosu** ile zenginleştirilmiş halidir.

---

### 🌐 Canlı Web Stüdyosu (Hemen Deneyin)
Kurulum yapmadan, doğrudan tarayıcınızdan açılış cümlenizi test etmek, açıklamanızı akış simülatöründe görmek ve 26 kanca formülünü incelemek için:  
👉 **[https://asklepios0.github.io/instagram-agent-skill/](https://asklepios0.github.io/instagram-agent-skill/)**

---

## 💡 Hızlı Sözlük: Bu Terimler Ne Anlama Geliyor? (Kafanız Karışmasın)

Sosyal medyada sıkça kullanılan teknik terimleri herkesin kolayca anlayabileceği sade bir dille açıklayalım:

* **Açılış Cümlesi (Kanca / Hook):** Bir Reels videosunun ilk 2 saniyesinde söylediğiniz veya ekrana yazdığınız en can alıcı ilk cümledir. Görevi, aşağı kaydıran izleyiciyi ekranda durdurmaktır.
* **Eyleme Çağrı (CTA - Call to Action):** Takipçiye videonun veya açıklamanın sonunda ne yapacağını açıkça söylemektir. *"Yoruma MOTOR yaz"*, *"İleride lazım olursa diye kaydet"* veya *"Profilden linke tıkla"* gibi tek ve net bir eylemdir.
* **Sahne & Çekim Planı (Beat Sheet):** Senaryonuzun her cümlesinin kaç saniye süreceğini ve izleyicinin sıkılmaması için nerede kamera açısının değişmesi gerektiğini gösteren saniyelik çekim rehberidir.
* **Patlama Çarpanı (Outlier Multiple):** Bir videonun, o hesabın normal ortalama izlenmesine kıyasla kaç kat patladığıdır. Normali 10.000 izlenen bir hesabın 150.000 izlenen videosu 15 kat (15x) patlamış gerçek bir viraldir.
* **İlk 125 Karakter Kuralı:** Instagram akışında bir gönderinin altındaki "...daha fazla" butonuna basılmadan önce ekranda görünen ilk iki satırdır. İnsanların %85'i devamına basmadığı için en önemli mesaj buraya yazılmalıdır.
* **İnsanlaştırma (Humanize):** *"Dijital dünyada", "çığır açan", "unutmayın ki"* gibi robotik yapay zeka klişelerini ve kopyalama filigranlarını temizleyip samimi, doğal konuşma diline çevirme işlemidir.

---

## 🎯 Temel Felsefe: "Siz Onaylamadan Hiçbir Şey Paylaşılmaz"

Bu araç bir otomatik paylaşım botu **kesinlikle değildir**. Instagram'ın kuralları gereği harici bot yazılımları hesabınızın kısıtlanmasına (shadowban veya işlem engeli) sebep olur.

Bu yüzden sistem güvenle çalışır: **Yapay zeka analiz eder, puanlar, kurgular ve zamanlar; siz kontrol edip kendi elinizle paylaşırsınız.** Sıfır hesap riski, maksimum içerik kalitesi.

---

## 📦 13 Temel Yetenek (Komutlar)

| Komut | Ne İşe Yarar? (Sade Anlatım) |
| :--- | :--- |
| **`/ig-reel`** | Aklınızdaki ham bir fikri izleyicinin sonuna kadar izleyeceği tam bir Reel senaryosuna dönüştürür. 26 formülden 3 alternatif açılış çıkarır, bunları puanlar, ekrana yazılacak yazıları ve saniyelik sahne planını hazırlar. |
| **`/ig-viral`** | Sektörünüzde gerçekten çalışan videoları bulur; ham izlenmeye göre değil, hesabın kendi ortalamasına göre **kaç kat patladığına (patlama çarpanı)** göre sıralar. |
| **`/ig-caption`** | Gönderi açıklaması yazar ve denetler. Akışta "...daha fazla" butonundan önce görünen **ilk 125 karakteri** optimize eder. Güncel 5 hashtag kuralını uygular. |
| **`/ig-carousel`** | Kaydırmalı gönderi kurgular. Kaydırmayı tetikleyen kapak, slayt metinleri ve ekran görüntüsü aldıracak özet slaytını hazırlar. |
| **`/ig-story`** | Günlük hikaye serileri tasarlar; hangi etkileşim çıkartmasının (anket, soru kutusu vb.) nerede kullanılacağını ve takipçiyi DM'e çeken adımları belirler. |
| **`/ig-profile`** | Profilinizi (biyografi, isim alanı, link, öne çıkanlar) 12 maddelik kontrol listesiyle 100 üzerinden puanlar ve puan kaybettiren kısımları düzeltir. |
| **`/ig-plan`** | Haftalık içerik takvimini, paylaşım türlerini, zamanlamayı ve günlük etkileşime girilecek 10 hedef hesabı belirler. |
| **`/ig-human`** | Metindeki yapay zeka kokusunu, *"dijital dünyada", "çığır açan", "unutmayın ki"* gibi klişeleri, uzun tireleri ve kopyalama filigranlarını temizler. |
| **`/ig-comment`** | Başka hesapların gönderilerine atılacak 9 farklı kategoride dikkat çekici yorum üretir. Asla "🔥🔥🔥" veya boş spam yapmaz. |
| **`/ig-reply`** | Kendi gönderinizin altındaki yorumları ayıklar (müşteri adayı, soru, gürültü vb.) ve öncelik sırasına göre yanıtlar hazırlar. |
| **`/ig-dm`** | Yorumdan gelen anahtar kelime teslimatını, ilk mesajı, iş birliği teklifini ve en fazla 2 aşamalı takip (follow-up) mesajlarını yazar. |
| **`/ig-repurpose`** | 1 uzun videodan, podcast'ten veya yazıdan bir haftalık bağımsız Reels ve Carousel gönderileri türetir. |
| **`/ig-audit`** | Önceden paylaştığınız içeriklerin otopsisini yapar. İzlenme sayısı yerine erişim başına kaydetme ve paylaşım oranlarıyla analiz eder. |

---

## ⚡ Arka Planda Çalışan 5 Yerel Python Aracı

Hiçbir harici API'ye veya internet bağlantısına ihtiyaç duymaz. Tamamen sizin bilgisayarınızda yerel çalışır:

### 1. Açılış Cümlesi (Kanca) Puanlayıcı (`hookscore.py`)
```bash
python skills/ig-reel/hookscore.py --hook "18.000 TL tek bir eksik sözleşme maddesinin bana maliyetidir"
```
* Açılış cümlenizi 5 kritere göre (Uzunluk, Somutluk, Kaybetme Riski, Başa Yerleşim ve Hitap) 100 üzerinden puanlar.
* *"Selam arkadaşlar..."* gibi ölü açılışları veya *"Kaydırmayı durdur"* klişelerini **İZLEYİCİYİ KAÇIRAN HATA** olarak anında yakalar.
* Türkçe para birimlerini (TL, ₺), yazıyla yazılan sayıları ve konuşma dilini tam destekler.

### 2. Sahne & Çekim Zamanlayıcı (`beats.py`)
```bash
python skills/ig-reel/beats.py senaryo.txt --target 30
```
* Metni dakikada 165 kelime normal Türkçe konuşma hızına göre hesaplar.
* Açılışın 3 saniyeyi aşıp aşmadığını, 4 saniyeden uzun süren durgun/sıkıcı yerleri ve videonun sonunun başına bağlanıp bağlanmadığını (döngü video) denetler.

### 3. Gönderi Açıklaması Denetleyici (`caption.py`)
```bash
python skills/ig-caption/caption.py aciklama.txt
```
* Kullanıcının akışta göreceği ilk 125 karakterlik pencereyi bir kutu içinde simüle eder.
* Güncel kurala göre **en fazla 5 hashtag** sınırını denetler (30 hashtag dönemi bitti).
* Net bir eyleme çağrı (CTA: yoruma yaz, DM at, kaydet) olup olmadığını kontrol eder.

### 4. İnsanlaştırıcı & Doğallık Kontrolü (`humanize.py` & `detect.py`)
```bash
python skills/ig-human/humanize.py metin.txt --report
```
* Metindeki yapay zeka klişelerini (*"dijital dünyada", "çığır açan", "unutmayın ki", "özetle"* vb.) ve görünmez filigran karakterlerini temizler.

### 5. Viral Kıyaslama Aracı (`swipe.py`)
```bash
python skills/ig-viral/swipe.py captured.tsv
```
* Sektördeki videoları hesapların kendi ortalama (medyan) izlenmelerine kıyasla kaç kat patladığına göre sıralar ve 26 kanca formülüyle eşleştirir.

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

Bu dosya doldurulduğunda, üretilen tüm senaryolar ve metinler doğrudan **sizin ağzınızdan çıkmış gibi** doğal konuşur.

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
