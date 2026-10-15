---
name: ig-human
description: >-
  Metindeki yapay zeka kalıntılarını (uzun tireler, AI klişeleri, görünmez filigran karakterleri)
  temizler ve metni 5 kriterli bir insanlaştırma paneliyle puanlar. Metinlerin doğal, konuşma dilinde çıkmasını sağlar.
---

# ig-human

Bu klasörde iki güçlü yerel araç bulunur:

```bash
python3 humanize.py taslak.txt --report        # Temizler ve neyin değiştiğini raporlar
python3 detect.py taslak.txt                   # 5 kontrolde insanlık puanını hesaplar
python3 detect.py once.txt sonra.txt           # Öncesi ve sonrası arasındaki farkı kanıtlar
```

Her iki araç da `slop.json` (ve `slop_tr.json`) dosyasındaki Türkçe yapay zeka klişelerini (*"dijital dünyada", "çığır açan", "unutmayın ki", "özetle", "kaydırmayı durdur"* vb.), görünmez Unicode filigranlarını ve tipografik kalıntıları okur.

## Instagram'da Neden Hayati Öneme Sahiptir?

Açıklamalar kısadır ve senaryolar kamera karşısında sesli okunur. 600 karakterlik bir açıklamada yapay zeka kokan tek bir cümle hemen sırıtır; seslendirilemeyecek kadar yapay bir senaryoda ise insan kendi yazdığı metne takılır. Buradaki asıl amaç bir yapay zeka dedektörünü atlatmak değil; takipçinin metni okurken "bunu bir marka veya bot yazmış" diyerek geçmesini engellemektir.

## Otomatik Temizlenen Unsurlar

1. **Görünmez Karakterler:** Sıfır genişlikli boşluklar (ZWSP), gizli Unicode etiketleri, yapay kopyalama filigranları. Bunlar klavyeyle üretilmez; yapay zeka çıktılarında gizlice yer alır. `humanize.py` hepsini tek seferde siler.
2. **Tipografi:** Uzun tire (—) yerine virgül veya nokta, kıvrık tırnak yerine düz tırnak, üç nokta simgesi yerine standart üç nokta.
3. **Yapay Zeka Klişeleri:** "dijital çağda", "çığır açan", "kusursuz", "kritik öneme sahip", "kaydırmayı durdurun", "bu videoda sizlere", "bunu kaydetmeyi unutma" gibi kalıplar doğal konuşma diline çevrilir veya silinir.

## 5 İnsan Kontrolü (0-100 Puan)

`detect.py` beş farklı sinyali inceler:
1. **DEĞİŞKENLİK (BURSTINESS):** Cümle uzunluklarının çeşitliliği (Robotik metinlerde her cümle aynı uzunluktadır).
2. **SOMUTLUK (SPECIFICITY):** 100 kelime başına düşen sayılar, isimler ve somut detaylar (Yapay zeka soyut isimler kullanır).
3. **KLİŞE YOĞUNLUĞU (SLOP DENSITY):** Metindeki yapay zeka kalıplarının sıklığı.
4. **FİLİGRAN (FINGERPRINT):** Görünmez karakterler ve tipografik yapaylıklar.
5. **DOĞAL SES (VOICE):** Konuşma dili, devrik cümleler ve doğrudan hitap.

GEÇER (PASS) notu için genel ortalamanın 70+ olması ve hiçbir alt kriterin 55'in altına düşmemesi gerekir.
