---
name: ig-caption
description: >-
  Instagram gönderi açıklaması (caption) yazar ve denetler: Akışta "...daha fazla"
  kesilmesinden önceki ilk 125 karakteri optimize eder, gövde metnini, tek bir eyleme çağrıyı (CTA),
  arama motoru kelimelerini ve en fazla 5 hashtag kuralını uygular.
---

# ig-caption

Bu klasörde çalışan Python aracı:

```bash
python3 caption.py caption.txt
python3 caption.py caption.txt --keywords "motosiklet inceleme,kask seçimi"
```

Bu araç metni Instagram akışındaki gibi görüntüler: İlk 125 karakter kutu içinde net görünür, geri kalanı ise tıklama sonrasına gizlenir. Yazdığınız diğer her şeyden önce o ilk kutuyu okuyun.

## İlk Karar: Bu Açıklamanın Görevi Ne?

Açıklamaları bozan en büyük hata bu kararı atlamaktır.

**Görev A: Video zaten izleyiciyi yakaladı.** Reel videosunun ilk 2 saniyesinde hem sesli hem ekranda güçlü bir kanca vardır. Açıklama ikinci bir kanca olmaya çalışmamalıdır; videoyla yarışırsanız ikisini de kaybedersiniz. Görevi: Eyleme çağrı (CTA), bunu anlamlı kılan bağlam ve aranan anahtar kelimelerdir.

**Görev B: Açıklamanın kendisi içeriktir.** Tek bir fotoğraf veya kaydırmalı bir görsel gönderisi. Burada ilk satır kancanın ta kendisidir: Kısa, somut ve merak uyandıran bir virgülle değil, merak zirvesinde kesilen bir cümle.

## Açıklamanın Yapısı

```
1. Satır:      125 karakterlik görünür alan.
               Görev A ise: Net eyleme çağrı veya özet.
               Görev B ise: Vurucu kanca.
               Asla selamlama, asla hashtag, ilk karakter asla emoji olmamalı.
Gövde:         Kısa paragraflar, aralarında bir satır boşluk. 2 ile 6 paragraf arası.
               Arama kelimeleri bu satırlarda doğal cümlelerle yer alır.
Eyleme Çağrı:  Tek bir tane. "DETAY yaz", "Kaydet" veya "DM at". Sadece biri.
Hashtag'ler:   En altta, ayrı bir satırda en fazla 5 adet veya hiç.
```

Karakter limiti 2.200'dür ancak neredeyse hiçbir gönderinin 2.200 karaktere ihtiyacı yoktur. Tıklamayı hak eden ve 600 karakterde değeri veren bir metin, 1.800 karakterlik laf kalabalığını ezer geçer.

## Hashtag Gerçeği

Hashtag'ler artık bir keşfet/erişim aracı değildir. Instagram, **18 Aralık 2025'te gönderi başına hashtag sınırını 30'dan 5'e indirmiştir**. Instagram yöneticisi Adam Mosseri'nin de açıkladığı gibi: Az sayıda (en fazla 5) ve konuya özel etiketler, jenerik 30 etiketten çok daha iyi çalışır.

`#viral`, `#kesfet`, `#fyp`, `#reels` gibi etiketler hiçbir konuyu tanımlamaz. Bunları çöpe atın.

## Arama Kelimeleri (Instagram SEO)

Instagram arama motoru doğrudan açıklama metnini okur. Bu yüzden bulunmak istediğiniz kelimeleri metnin içine insanların konuşacağı doğal cümleler olarak yerleştirin. En alta `#motosikletkaski` yazmak yerine, 3. satırda "Şehir içi sürüşte doğru motosiklet kaskı seçimi..." şeklinde geçirin.

## Kurallar

- **Açıklamaya tıklanamayan link koymayın.** Instagram açıklamalarındaki linkler tıklanmaz. Linki ya biyografiye ya da DM otomasyonuna yönlendirin.
- **Tek bir eyleme çağrı (CTA).** İki farklı şey istemek hiçbir şey istememekle aynıdır.
- **Anahtar kelime kolay yazılabilen tek bir kelime olsun:** `Yoruma MOTOR yaz` çalışır. `Yoruma "inceleme rehberini istiyorum" yaz` çalışmaz.
- **Emojiyi süs olarak değil, noktalama gibi kullanın.** Her 100 karaktere 4'ten fazla emoji koymayın.
