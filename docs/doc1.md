---
slug: "/"
title: Style Guide
sidebar_label: Style Guide

---








Firebase Custom Event Entegrasyon Dökümanı
Android | iOS









Firebase Custom Event İmplementasyonu
Firebase herhangi bir kurulum gerektirmeden uygulama indirmeleri, sürüm güncellemeleri, OS güncellemeleri gibi eventleri otomatik olarak takip etmektedir. Bu eventlerin bir listesine buradan ulaşabilirsiniz. Kurulumunu gerekli gördüğümüz eventlerin gönderimine dair bilgiler parametrelerin uygun veri tipleriyle birlikte aşağıdaki tabloda verilmiştir. Veri tipi belirtilmeyen parametreleri STRING veri tipinde gönderiniz. Tarih gönderim formatları (START_DATE ve END_DATE değişkenleri) yyyy-mm-dd (yıl-ay-gün) şeklindedir. USER_ID değişkeni giriş yapmış olan kullanıcılarda member ID olarak gönderilmelidir.
Sign up
Login
Listelerim Kısmı
VIEW_MAIN_LIST (Ana kategorilerin görüntülenmesi
SELECT_MAIN_LIST (Ana kategorilerin seçilmesi
VIEW_ITEM_LIST (Ana kategoriye tıklanıp gidilen ürün listesindeki ürünlerin görüntülenmesi
SELECT_ITEM (Listedeki ürünlere tıklanılması
VIEW_ITEM (Tıklanılan ürünlerin görüntülenmesi
ADD_TO_CART (Görüntülenen ürünün sepete eklenmesi
Etkinliklerim Kısmı
VIEW_SOCIAL_EVENTS (Etkinliklerim kısmına gidilmesi)
SELECT_SOCIAL_EVENTS (Etkinliklerden bir tanesinin seçilmesi)
SELECT_RECCOMENDATIONS (Önerilerden birine tıklanması)
SELECT_DETAILS (Mekan detayları girildiğinde ve güncelleye tıklandığında)
Kuponlarım Kısmı
VIEW_COUPONS (Kuponlarım kısmının görüntülenmesi)
SELECT_COUPONS (Kupon tıklamaları)
Raporlarım Kısmı
VIEW_REPORTS (Raporlar kısmının görüntülenmesi)
SELECT_REPORTS (Bir rapor kategorisinin seçilmesi)

App Eventleri (İsimlendirmeler Case Sensitive’dir.)
Tetiklenecekleri Adımlar
Parametreler (İsimlendirmeler Case Sensitive’dir.)
VIEW_MAIN_LIST
Listelerim sekmesinde  Listelerin görüntülenmesi. (Çeyiz Listesi, Balayı Listesi vs.)


USER_ID: MÜŞTERİ ID,
SCREEN_NAME: BULUNDUĞU LİSTE ADI
ITEMS: [{NAME: LİSTE SAYFASINDA BULUNAN KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)
                ITEM_ID: KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU LİSTE ADI (ÖRNEĞİN: ÇEYİZ LİSTESİ, BALAYI LİSTESİ VS.),
              VALUE: ÜRÜN EKLENDİKTEN SONRA GÖNDERİLEN DEĞER (Yatak Odası  0/3 BURADA BULUNAN KESİRLİ DEĞER)
             }]
SELECT_MAIN_LIST
Listelerim sekmesinde  görüntülenen kategorilerden birinin seçilmesi. (Yatak Odası, Mutfak vs.)
USER_ID: MÜŞTERİ ID,
ITEMS: [{NAME: LİSTE SAYFASINDA BULUNAN ALT KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)
                ITEM_ID: ALT KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU LİSTE ADI (ÖRNEĞİN: ÇEYİZ LİSTESİ, BALAYI LİSTESİ VS.),
              VALUE: ÜRÜN EKLENDİKTEN SONRA GÖNDERİLEN DEĞER (Yatak Odası  0/3 BURADA BULUNAN KESİRLİ DEĞER)
             }]
VIEW_ITEM_LIST
Seçilen kategorilerin içerisinde yer alan ürün kategorilerinin listelenmesi. (Komodin, Makyaj Masası vs.)
USER_ID: MÜŞTERİ ID,
SEARCH_TERM: LİSTEDE ARA (INPUT TERM)
ITEMS: [{NAME: ÜRÜN KATEGORİSİ (KOMODİN, MAKYAJ MASASI VS:)
                ITEM_ID: ÜRÜN KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU ALT KATEGORİ ADI (ÖRNEĞİN: YATAK ODASI, MUTFAK vs.),
              VALUE: ADET MİKTARI
             }]
SELECT_ITEM
Ürün kategorilerinden birinin seçilmesi.
USER_ID: MÜŞTERİ ID,
ITEMS: [{NAME: ÜRÜN KATEGORİSİ (KOMODİN, MAKYAJ MASASI VS:)
                ITEM_ID: ÜRÜN KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU ALT KATEGORİ ADI (ÖRNEĞİN: YATAK ODASI, MUTFAK vs.),
              VALUE: ADET MİKTARI
             }]
VIEW_ITEM
Ürünün görüntülenmesi. Örneğin; Komodin ürününün görüntülenmesi.
USER_ID: MÜŞTERİ ID,
ITEMS: [{NAME: ÜRÜN KATEGORİSİ (KOMODİN, MAKYAJ MASASI VS:)
                ITEM_ID: ÜRÜN KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU ALT KATEGORİ ADI (ÖRNEĞİN: YATAK ODASI, MUTFAK vs.),
              PRICE_MIN: EN DÜŞÜK,
               PRICE_MAX: EN YÜKSEK
             }]
ADD_TO_CART
Görüntülenen ürünün eklenmesi
USER_ID: MÜŞTERİ ID,
ITEMS: [{NAME: ÜRÜN KATEGORİSİ (KOMODİN, MAKYAJ MASASI VS:)
                ITEM_ID: ÜRÜN KATEGORİ ID,
                ITEM_CATEGORY: BULUNDUĞU ALT KATEGORİ ADI (ÖRNEĞİN: YATAK ODASI, MUTFAK vs.),
              PRICE_MIN: EN DÜŞÜK,
               PRICE_MAX: EN YÜKSEK
             }]
VIEW_SOCIAL_EVENTS
Etkinliklerim  


SELECT_SOCIAL_EVENTS


Etkinliklerim kısmına gidilmesi
SELECT_RECCOMENDATIONS




SELECT_DETAILS




VIEW_COUPONS




LOGIN
Giriş
USER_ID: MÜŞTERİ ID,
METHOD: GİRİŞ YAPARKEN KULLANILAN YÖNTEM (FACEBOOK, EMAIL VB.)
SIGN_UP
Kayıt olma
USER_ID: MÜŞTERİ ID,
METHOD: KAYIT OLUNURKEN KULLANILAN YÖNTEM (FACEBOOK, EMAIL VB.)
SELECT_COUPONS




VIEW_REPORTS







SELECT_REPORTS


















Event Kurulum Syntax Örnekleri
Android - Kotlin
Aşağıda örnek bir booking event gönderimi verilmiştir. 

NOT: Örnek gönderimde array içinde dictionary formatına uygun şekilde gönderilen ITEMS parametresini hashmap olarak (veya muadili olan uygun veri tipinde) gönderiniz. Dictionary formatı, variable key ve değerlerinin rahat okunabilirliğini sağladığı için kullanılmıştır.

firebaseAnalytics.logEvent("booking") {
    param("CURRENCY", "TRY") 
    param("VALUE", 100.00) // Ciro, double veri tipinde
    param("TRANSACTION_ID", "TRANSACTION123") // Sipariş IDsi
    param("TAX", 18.00) // Vergi, double veri tipinde
    param("USER_ID", "USER123") // Müşteri IDsi
    param("START_DATE", "2021-04-21") // Rezervasyon başlangıç tarihi
    param("END_DATE", "2021-04-23") // Rezervasyon bitiş tarihi
    param("NUMBER_OF_NIGHTS", 2) // Rezervasyon gece sayısı, flat veri tipinde
    param("NUMBER_OF_PASSENGERS", 1) // Rezervasyon müşteri sayısı, flat veri //tipinde
    param("ITEMS", [{
                      "NAME": "FOUR SEASONS ANTALYA HOTEL", // Otel/tur ismi
                      "ITEM_ID": "OTEL123", // Otel/tur IDsi
                      "PRICE": 100.00, // Otel/tur fiyatı, double veri tipinde
			   "ITEM_BRAND": "FOUR SEASONS", // Otel/tur markası
			   "ITEM_CATEGORY": "YURTİÇİ OTELLERİ", // Otel/tur //kategorisi
                      "ITEM_CATEGORY2": "ŞEHİR OTELLERİ", // Otel/tur alt //kategorisi
			   "LOCATION_ID": "KONUM123", // Otel/tur konum IDsi
			   "LOCATION": "ANTALYA", // Otel/tur konum ismi
		         "QUANTITY": 1 // Otel/tur adedi, flat veri tipinde, ASLA //null göndermeyiniz.
                   }])
}




iOS - Swift
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


```python
s = "Python syntax highlighting"
print(s)
```

    No language indicated, so no syntax highlighting.
    But let's throw in a <b>tag</b>.

```js {2}
function highlightMe() {
  console.log('This line can be highlighted!');
}
```

| App Eventleri (İsimlendirmeler Case Sensitive’dir.) | Tetiklenecekleri Adımlar                                                                        | Parametreler (İsimlendirmeler Case Sensitive’dir.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| VIEW\_MAIN\_LIST                                    | Listelerim sekmesinde  Listelerin görüntülenmesi. (Çeyiz Listesi, Balayı Listesi vs.)

<br>     | USER\_ID: MÜŞTERİ ID,

[SCREEN\_NAME](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics.Param#SCREEN_NAME): BULUNDUĞU LİSTE ADI

`ITEMS:` \[{NAME: LİSTE SAYFASINDA BULUNAN KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)

`ITEM\_ID`: KATEGORİ ID,

ITEM\_CATEGORY: BULUNDUĞU LİSTE ADI (ÖRNEĞİN: ÇEYİZ LİSTESİ, BALAYI LİSTESİ VS.),

[VALUE](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics.Param#VALUE): ÜRÜN EKLENDİKTEN SONRA GÖNDERİLEN DEĞER (Yatak Odası  0/3 BURADA BULUNAN KESİRLİ DEĞER)

             }\] |
| SELECT\_MAIN\_LIST                                  | Listelerim sekmesinde  görüntülenen kategorilerden birinin seçilmesi. (Yatak Odası, Mutfak vs.) | USER\_ID: MÜŞTERİ ID,

ITEMS: \[{NAME: LİSTE SAYFASINDA BULUNAN ALT KATEGORİNİN ADI (YATAK ODASI, MUTFAK VS.)

ITEM\_ID: ALT KATEGORİ ID,

ITEM\_CATEGORY: BULUNDUĞU LİSTE ADI (ÖRNEĞİN: ÇEYİZ LİSTESİ, BALAYI LİSTESİ VS.),

[VALUE](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics.Param#VALUE): ÜRÜN EKLENDİKTEN SONRA GÖNDERİLEN DEĞER (Yatak Odası  0/3 BURADA BULUNAN KESİRLİ DEĞER)

             }\] 