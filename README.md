# Acil Durum Araçları Uyarı Sistemi

![Proje Posteri](assets/poster.png)

---

## Proje Tanımı

Bu proje, ambulans, itfaiye ve polis gibi acil durum araçlarının şehir içi trafikte karşılaştığı gecikmeleri azaltmak ve sürücü farkındalığını artırmak amacıyla geliştirilen konum tabanlı bir uyarı sistemi prototipini kapsamaktadır. Geleneksel siren ve ışık uyarıları; yoğun trafik, çevresel gürültü, görüş kısıtları ve sürücü dikkat dağınıklığı gibi nedenlerle her zaman yeterli olamamaktadır. Bu durum, acil müdahale sürelerinin uzamasına ve hayati risklerin artmasına yol açabilmektedir.

Geliştirilen sistem, acil durum aracına entegre edilen hazır bir araç takip cihazından elde edilen GNSS (GPS/GLONASS) tabanlı konum verisini kullanmaktadır. Bu konum verisi, dahili SIM kart aracılığıyla bulut tabanlı bir sunucuya iletilmekte ve sunucu tarafında gerçek zamanlı olarak işlenmektedir. Sunucu üzerinde çalışan yazılım algoritması, acil durum aracının konumuna göre **100 metre menzil içerisinde bulunan** kayıtlı araçları mesafe hesaplama yöntemleriyle tespit etmektedir.

Belirlenen hedef araçlara “Acil durum aracı yaklaşıyor, yolu açın” şeklinde uyarı bildirimleri gönderilerek sürücülerin daha erken bilgilendirilmesi amaçlanmaktadır. Bu sayede acil durum araçlarının trafikte daha hızlı ve güvenli şekilde ilerlemesine katkı sağlanması hedeflenmektedir.

---

## Projenin Amacı

Bu projenin temel amacı, acil durum araçlarının trafikteki ilerleme süresini kısaltmak ve sürücü farkındalığını artırarak geçiş güvenliğini sağlamaktır. Bu doğrultuda, konum tabanlı ve dijital uyarı mekanizmalarına dayalı, altyapı bağımlılığı düşük ve ölçeklenebilir bir sistem modeli geliştirilmesi hedeflenmektedir.

---

## Hedefler

- Acil durum araçlarının konum bilgisinin gerçek zamanlı olarak alınması  
- Konum verilerinin bulut tabanlı sunucuya aktarılması  
- 100 metre menzil içerisinde bulunan araçların otomatik olarak tespit edilmesi  
- Hedef sürücülere uyarı bildirimi gönderilmesi  
- Sistem gecikme süresi ve doğruluk oranlarının ölçülmesi  
- Akademik ve teknik olarak uygulanabilir bir prototip geliştirilmesi  

---

## Yenilikçi Yönü ve Teknolojik Değeri

Bu proje, altyapı bağımlılığı gerektirmeyen, hazır araç takip cihazı kullanan ve bulut tabanlı çalışan bir mimari sunması açısından yenilikçi bir yaklaşıma sahiptir. Mevcut çalışmalarda sıklıkla kamera tabanlı, siren algılamaya dayalı veya özel donanım gerektiren çözümler öne çıkarken; bu proje daha düşük maliyetli, uygulanabilir ve yaygınlaştırılabilir bir model sunmaktadır. Ayrıca konum temelli menzil analizi ve otomatik bildirim mekanizmasının birlikte kullanılması, sistemin teknolojik değerini artırmaktadır.

---

## Sistem Mimarisi ve Bileşenler

- Hazır araç takip cihazı (GNSS + SIM)
- Bulut tabanlı sunucu altyapısı
- RESTful API (FastAPI)
- Mesafe hesaplama algoritması (Haversine)
- Bildirim modülü (Mock)
- Loglama ve test altyapısı
