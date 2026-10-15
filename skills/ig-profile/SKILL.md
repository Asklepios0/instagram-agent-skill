---
name: ig-profile
description: >-
  Instagram profilini 12 maddelik bir rubrikle 100 üzerinden puanlar ve puan kaybettiren
  kısımları (isim alanı, biyografi, link stratejisi, öne çıkanlar, sabitlenen 3 gönderi) yeniden yazar.
---

# ig-profile

Çoğu içerik üreticisi profili yanlış kurgular. Profil gezilen bir vitrin değil, **hızlı bir karar ekranıdır**. Bir Reel videosunu beğenip gelen bir ziyaretçinin tek bir sorusu vardır ve 3 saniyede cevap bekler: "Burada bundan daha fazlası var mı ve bu sayfa benim için mi?"

## Puanlama Rubriği (100 Puan)

`rubric.json` dosyasında 12 kriter yer alır:
1. **İsim Alanı (Bold Yazı - 30 Karakter):** Arama motorunun eşleştiği yerdir. Sadece isim değil, aranabilir sektör anahtar kelimesi taşır (`{İsim} | {Sektör/Hizmet}`).
2. **Biyografi 1. Satır:** Kime hitap edildiği ve takip edince ne kazanılacağı.
3. **Sabitlenen 3 Gönderi (Pinned Three):** 3 farklı görev: En büyük kanıt/sonuç, teklifin/rehberin en net hali ve en iyi tanışma videosu.
4. **Biyografi Kanıtı / Teklifi:** Kuru bir unvan yerine somut bir sonuç veya rakam.
5. **Link Stratejisi:** Biyografideki vaatle birebir örtüşen tek bir net çıkış kapısı.
6. **Öne Çıkanlar (Highlights):** Müşterinin aklındaki soruları yanıtlayan 4-6 başlık (Fiyatlar, Sonuçlar, Nasıl Çalışır, Hakkımda).
7. **Izgara / Kapak Okunabilirliği:** İlk 9 kapakta büyük, kontrastlı ve merak uyandıran 3-4 kelimelik başlıklar.
8. **Profil Fotoğrafı:** Net, yüksek kontrastlı çekim.
9. **Kullanıcı Adı (@handle):** Kısa, akılda kalıcı, Türkçe telaffuzu kolay.
10. **İletişim & Kategori Butonları:** Profesyonel araçlar aktif.
11. **Güncel Paylaşım Disiplini:** Son 7 gün içinde paylaşım yapılmış olması.
12. **Aktif Hikaye Halkası:** Profil ziyaret edildiğinde yanan renkli hikaye halkası.

## Çıktı

Dürüst puan tablosu sunulur, en çok puan kaybettiren maddeden başlanarak kopyala-yapıştır hazır Türkçe metin önerileri teslim edilir.
