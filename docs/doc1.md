---
slug: "/"
title: Style Guide
sidebar_label: Style Guide

---
## Firebase Custom Event Entegrasyon Dökümanı

### iOS - Swift
Aşağıda örnek bir booking event gönderimi verilmiştir.

NOT: Swift, Web Analytics ekibimizin mevcut toolkiti dahilinde değildir. Bu sebeple  as NSObject kısımları ve veri tiplerinde çeşitli sorunlar yaşanabilir.

```javascript
Analytics.logEvent("booking", parameters: [
    "CURRENCY": "TRY" as NSObject,
    "VALUE": 100.00 as NSObject // Ciro, double veri tipinde
    "TRANSACTION_ID": "TRANSACTION123" as NSObject, // Sipariş IDsi
    "TAX": 18.00 as NSObject, // Vergi, double veri tipinde
    "USER_ID": "USER123" as NSObject, // Müşteri IDsi
    "START_DATE”: "2021-04-18" as NSObject, // Rezervasyon başlangıç tarihi
    "END_DATE": "2021-04-20"as NSObject, // Rezervasyon bitiş tarihi
    "NUMBER_OF_NIGHTS": 2 as NSObject, // Rezervasyon gece sayısı, flat veri //tipinde
    "NUMBER_OF_PASSENGERS": 1 as NSObject, // Rezervasyon müşteri sayısı, flat //veri tipinde
    "ITEMS": [[
              "NAME": "FOUR SEASONS ANTALYA HOTEL" as NSObject, // Otel/tur //ismi
              "ITEM_ID": "OTEL123" as NSObject, // Otel/tur IDsi
              "PRICE": 100.00 as NSObject, // Otel/tur fiyatı, double veri //tipinde
		  "ITEM_BRAND": "FOUR SEASONS" as NSObject, // Otel/tur markası
		  "ITEM_CATEGORY": "YURTİÇİ OTELLERİ" as NSObject, // Otel/tur //kategorisi
               "ITEM_CATEGORY2": "ŞEHİR OTELLERİ" as NSObject, // Otel/tur alt //kategorisi
		  "LOCATION_ID": "KONUM123" as NSObject, // Otel/tur konum IDsi
		  "LOCATION": "ANTALYA" as NSObject, // Otel/tur konum ismi
		  "QUANTITY": 1 as NSObject// Otel/tur adedi, flat veri tipinde, //ASLA null göndermeyiniz.
              ]]() as NSObject)
])
```

Kaynak: Event kurulumları ile ilgili Google’ın dokümantasyonuna buradan ulaşabilirsiniz.


`SCREEN_NAME`: BULUNDUĞU LİSTE ADI

`ITEMS:` NAME: LİSTE SAYFASINDA BULUNAN KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)

`ITEM_ID`: KATEGORİ ID

    | App Eventleri (İsimlendirmeler Case Sensitive’dir.)        |      Tetiklenecekleri Adımlar      |   Parametreler (İsimlendirmeler Case Sensitive’dir.) |
    | ------------- | :-----------: | -----: |
    | `VIEW_MAIN_LIST`     | Listelerim sekmesinde  Listelerin görüntülenmesi. (Çeyiz Listesi, Balayı Listesi vs.) | `USER_ID: MÜŞTERİ ID,
SCREEN_NAME: BULUNDUĞU LİSTE ADI
ITEMS: [{NAME: LİSTE SAYFASINDA BULUNAN KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)
                ITEM_ID: KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU LİSTE ADI (ÖRNEĞİN: ÇEYİZ LİSTESİ, BALAYI LİSTESİ VS.),
              VALUE: ÜRÜN EKLENDİKTEN SONRA GÖNDERİLEN DEĞER (Yatak Odası  0/3 BURADA BULUNAN KESİRLİ DEĞER)
             }]`
 |