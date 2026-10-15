---
name: ig-reel
description: >-
  Ham bir fikirden 26 formüle dayalı kanca seçenekleri, seslendirilecek senaryo,
  ekran yazıları ve saniyesine kadar zamanlanmış çekim planı (beat sheet) üreterek
  Reel hazırlar. Kullanıcının kendi ses tonunda yazar ve çekimden önce kancayı puanlar.
---

# ig-reel

Aklınızdaki ham bir fikri, izleyicinin sonuna kadar izleyeceği tam bir Reel senaryosuna dönüştürür.

Bu klasörde iki güçlü Python aracı yer alır ve doğrudan çalıştırılabilir:

```bash
python3 hookscore.py hooks.txt              # Kanca alternatiflerini puanlayıp sıralayın
python3 hookscore.py --hook "tek bir cümle"  # Tek bir kancayı puanlayın
python3 beats.py senaryo.txt --target 30    # Çekime başlamadan önce saniyelik çekim planı
```

## Yazmaya Başlamadan Önce

1. `templates/ses_profili.md` (veya `~/.claude/instagram/voice.md`) dosyasını okuyun. Bu dosya kullanıcının kamera karşısında nasıl konuştuğunu, hangi kelimeleri asla kullanmadığını ve kime hitap ettiğini tanımlar.
2. Bu klasördeki `hooks_tr.json` dosyasını inceleyin. Türkçe konuşma diline uyarlanmış 26 formül, şablonlar, ekran yazıları ve örnekler içerir.
3. Ham fikir zayıfsa laf kalabalığı yapmayın; tek bir somut soru sorun: Ne oldu, kimin başına geldi ve neye mâl oldu / ne kazandırdı?
4. `/ig-viral` çıktısı olan `swipe.md` varsa inceleyin. Bu dosya, kullanıcının kendi sektöründe o anda çalışan formüllerin kanıtıdır.

## Reel'in Anatomisi

Bir Reel ilk iki saniyede kazanılır ve sonraki beş saniyede elde tutulur:

```
0:00 - 0:02   KANCA (HOOK)       İddia. Konuşulan cümle ve ekran yazısı ayrı yazılır. İlk karede hareket olmalı, donuk bir yüz değil.
0:02 - 0:07   RİSK / ÇIKAR (STAKE) İzleyen kişi için bunun neden önemli olduğu. Tek bir net cümle.
0:07 - ...    GÖVDE (BODY)       Her çekimde (beat) tek bir fikir; her fikirde kamera açısı/kadraj değişir.
SON 3 SANİYE  ÖDÜL & EYLEM (PAYOFF) Kancanın vaat ettiği sonucu teslim edin, ardından tek bir eylem isteyin (CTA).
SON CÜMLE     DÖNGÜ (LOOP)       Kancadaki ilk kelimeye bağlanacak bir kelimeyle bitirin ki video başa sarıldığında kusursuz aksın.
```

Süre: 15 ile 45 saniye arası en ideal çalışma aralığıdır. 7 saniyenin altı yapay döngü şişirmesi yapar, güven vermez.

## İş Akışı

1. **Bir değil, üç kanca çıkarın.** Fikri `hooks_tr.json` üzerinden geçirin ve gerçekten uyan 3 farklı formül seçin. Aynı cümlenin 3 varyasyonu değil, 3 farklı psikolojik tetikleyici olsun.
2. **Kancaları puanlayın.** Konuşulacak 3 cümleyi `hookscore.py` ile test edin. En yüksek puan 50'nin altındaysa kanca henüz olmamıştır; senaryo yazımına geçmeyin.
3. **Senaryoyu yazın.** Kazanan kancanın üzerine senaryoyu inşa edin. Doğal Türkçe konuşma dili kullanın. Sesli okunduğunda zorlayacak devrik veya yapay cümleler yazmayın.
4. **Zamanlayın.** `beats.py senaryo.txt --target 30` çalıştırın. Kancanın 3 saniyeyi aşması, 4 saniyeden uzun durgun sahneler veya döngü eksikliği varsa düzeltin.
5. **İnsanlaştırın.** `/ig-human` üzerinden geçirerek yapay zeka kokan klişeleri ("dijital dünyada", "çığır açan" vb.) temizleyin.
6. **Kopyala-yapıştır hazır teslim edin:**

```
REEL HAZIR
kanca:       #3 Kimse Söylemiyor, 86 PUAN (GÜÇLÜ)
süre:        165 kelime/dk ile 9 sahnede 28.4 saniye
ekran yazısı: 6 kart
insanlaştırma: 4 yapay zeka kalıntısı temizlendi, İnsan Skoru 81 (GEÇTİ)
açıklama:    sıradaki komut: /ig-caption
```

7. **Asla otomatik paylaşmayın.** Bu araç senaryoyu yazar; siz çeker ve kendi elinizle paylaşırsınız.

## Ekran Yazıları Ayrı Bir Senaryodur

Her zaman ayrı yazın. Çünkü ekran yazısı duyulmadan önce okunur.

- Kart başına **en fazla 4-6 kelime**.
- Kanca yazısı **1. karede** hemen ekranda olmalıdır.
- **Güvenli alanda kalın:** 1080x1920 dikey kadrajda üstten 230 piksel, alttan 440 piksel ve sağdan 230 piksel boşluk bırakın (Instagram arayüz butonları ve açıklama bu alanları kapatır).
- Çoğu kullanıcı videoyu sessiz izlemeye başladığı için altyazıları videoya gömün.

## Fark Yaratan Kritik Kurallar

- **Reel başına tek bir ana fikir.** İki fikir varsa iki ayrı video çekin.
- **Sıfatlar yerine sayılar.** "Çok pahalıydı" yerine "18.000 TL" deyin.
- **Giriş laf kalabalığını kesin.** Selamlaşma, "bu videoda...", logo animasyonu yok. Normalde 6. saniyede söyleyeceğiniz cümleyle başlayın.
- **Her çekimde kadraj değiştirin.** 8 saniye boyunca sabit duran plan izleyicinin kaçmasına yol açar.
- **Sonunda tek bir eylem isteyin:** Ya yorumda kelime yazdırın, ya kaydettirin, ya takip ettirin. Asla hepsini birden istemeyin.
