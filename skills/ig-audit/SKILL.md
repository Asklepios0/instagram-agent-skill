---
name: ig-audit
description: >-
  Önceden paylaşılmış gönderi ve Reels videolarının otopsisini yapar: Hangi videoların
  neden tuttuğunu, hangilerinin battığını ve ne üretmeyi bırakmanız gerektiğini analiz eder.
---

# ig-audit

Bir hesap için neyin çalıştığının tek dürüst kanıtı, o hesabın kendi geçmiş verileridir. Tüm kılavuzlardaki kurallar birer varsayımdır; sizin son 30 gönderiniz ise somut delildir.

## Asıl Ölçülmesi Gereken Metrikler

Ham izlenme sayısı sayfadaki en anlamsız rakamdır; çünkü çoğunlukla zaten sizi takip edenlerin sayısına bağlıdır. Bunun yerine şu oranları hesaplayın:

| Metrik | Nasıl Hesaplanır? | Ne Anlatır? |
| --- | --- | --- |
| **Patlama Çarpanı (Outlier Multiple)** | İzlenme / Hesabın Kendi Medyan İzlenmesi | Gerçek bir viral mi yoksa sıradan bir gün mü? |
| **Takipçi Olmayanların Oranı** | Takip etmeyenlerden gelen erişim %'si | İçeriğin kendi kitlenizin dışına taşıp taşmadığı |
| **3. Saniyede Elde Tutma (Hold @ 3s)** | 3. saniyede kalan izleyiciler / Başlayanlar | Kancanın (Hook) başarı notu |
| **Ortalama İzlenme Süresi** | İstatistiklerden doğrudan alınır | Videonun gövdesinin tutup tutmadığı |
| **Erişim Başına Paylaşım (Sends / Reach)** | Paylaşım sayısı (DM) / Erişim | Algoritmaya giden en güçlü sinyal. Bir insan arkadaşına gönderiyorsa altına imzasını atıyor demektir. |
| **Erişim Başına Takipçi (Follows / Reach)** | Kazanılan takipçi / Erişim | Profilin dikkatleri takipçiye dönüştürüp dönüştüremediği |

## Aylarca Vakit Kazandıracak Hayati Ayrım

**İzlenen ama takipçi getirmeyen bir Reel başarısız bir video değildir, bir profil problemidir.** İzlenmeyen bir Reel ise kanca problemidir. Herhangi bir tavsiye vermeden önce bu ikisini mutlaka birbirinden ayırın:
- Takipçi olmayanlara erişim yüksek ama takipçi dönüşümü düşükse -> Kancaları değiştirmeyi bırakın ve `/ig-profile` ile profil biyografinizi ve sabitlenen gönderilerinizi düzeltin.
- İlk 3 saniyede izleyici kaçıyorsa -> `/ig-reel` ve `hookscore.py` ile kancayı güçlendirin.
