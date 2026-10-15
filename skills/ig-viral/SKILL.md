---
name: ig-viral
description: >-
  Kullanıcının sektöründe o anda gerçekten çalışan viral Reels videolarını bulur,
  hesapların kendi ortalama izlenmesine göre kaç kat patladığına (outlier multiple)
  göre sıralar, kanca formüllerini tespit eder ve çekim için hazır bir ilham arşivi (swipe file) oluşturur.
---

# ig-viral

Pazar araştırması yeteneği. Bu paketteki diğer tüm komutlar içerik yazar; bu komut ise sektörü inceler. Her gün değil, ayda bir kez çalıştırılması önerilir; formüller sezonluktur.

Bu klasörde çalışan Python aracı:

```bash
python3 swipe.py captured.tsv --out ~/.claude/instagram/swipe.md
```

## Bu İşi Değerli Kılan Tek Temel Kural

**Ham izlenme sayısı bir kanıt değildir.** 2 milyon takipçili bir hesabın 400.000 izlenmesi sıradan, hatta durgun bir gündür. Ancak 4.000 takipçili bir hesabın 400.000 izlenmesi, orada kopyalanabilir ve formüle dökülebilir büyük bir keşif olduğunu gösterir.

Bu yüzden buradaki her şey **patlama katsayısına (outlier multiple)** göre sıralanır: Videonun izlenmesi, o hesabın son dönem medyan izlenmesine bölünür.
- **3 katı (3x) ve üzeri:** Gerçek bir viral sinyali.
- **1.5 katı (1.5x) ve altı:** Hesabın standart sıradan trafiğidir; izlenme sayısı ne kadar büyük görünürse görünsün size yeni bir formül öğretmez.

Kendi hesap boyutunuzun yaklaşık 10 katı aralığındaki hesapları inceleyin. 2 milyonluk hesabın tutturduğu formül, çoğu zaman sırf 2 milyon takipçisi olduğu için tutar.

## Adım 1: Hesapları Belirleyin

6 ile 12 arasında hedef hesap seçin:
- **4 Doğrudan Rakip:** Aynı niş, benzer hedef kitle, sizden birkaç adım önde.
- **4 Komşu Sektör:** Farklı konu, aynı kitle. Sektörünüzde henüz kimsenin denemediği formatlar buradan ödünç alınır.
- **2-4 Büyük Hesap:** Sadece görsel format ve geçiş fikirleri için; paylaşım sıklığı veya ses tonu için değil.
- Kendi **Kaydedilenler (Saved)** koleksiyonunuzu da dahil edin.

## Adım 2: İnceleyin (Kazıma Değil, Okuma)

**Asla Taviz Verilmeyecek Kurallar:**
- **Asla şifre istemez veya kullanıcı adına giriş yapmaz.** Tarayıcınızda siz açıkken incelersiniz.
- **Botla kazıma (scraping) yapılmaz.** İnsan hızında 10 hesap incelenir. Otomatik toplama botları Instagram kurallarını ihlal eder ve hesabın kısıtlanmasına yol açar.
- **Formülü kopyalayın, videoyu değil.** Kanca yapısını, video uzunluğunu ve kesme ritmini modelleyin; başkasının sesini veya hikayesini çalmayın.

Kaydedilecek bilgiler:
| Alan | Açıklama |
| --- | --- |
| account | @kullanıcıadı |
| followers | Takipçi sayısı |
| median | Son 12 Reels'ın ortanca (medyan) izlenme sayısı |
| views | İncelenen videonun izlenmesi |
| hook | Videonun ilk 2-3 saniyesindeki ilk cümle |
| on-screen | İlk karedeki ekran yazısı |
| length | Saniye cinsinden süre |
| cta | Sonundaki eyleme çağrı |

## Adım 3: Sıralayın ve Analiz Edin

`swipe.py` çalıştırıldığında videoları katlama çarpanına göre sıralar, 26 Türkçe kanca formülüyle eşleştirir ve en üst %33'lük dilimin ortak özelliklerini çıkarır.

## Çıktı

```
SWIPE ARŞİVİ · 38 Reels · 7 Hesap · Temel Çizgi: Hesap Medyanı

EN BÜYÜK PATLAMALAR (3x Üzeri)
  38.4x  kanca 86  #3  Kimse Söylemiyor   @hesap_a   412.000 (medyan 10.700)
  11.2x  kanca 79  #9  Çal ve Kullan      @hesap_c   180.000 (medyan 16.100)

ÖNE ÇIKAN ORTAK NOKTALAR:
  #3 Kimse Söylemiyor  en üst dilimde 5 kez yer aldı
  Medyan kanca uzunluğu: Üst dilimde 8 kelime, alt dilimde 19 kelime

SİZİN İÇİN UYARLANMIŞ KANCA:
  #3  "Kimse size ilk 1000 km'de kaza yapma ihtimalinizin %70 olduğunu söylemiyor."
```
