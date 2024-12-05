# IoTGo (Akıllı Ev Yönetim Sistemi ) - Proje Dokümantasyonu

## 📌 **Proje Amacı**
Bu projenin temel amacı, modern yazılım geliştirme tekniklerini ve popüler teknolojileri bir arada kullanarak bir **Akıllı Ev Yönetim Sistemi** geliştirmektir. Proje, aşağıdaki becerileri ve teknolojileri entegre etmeyi hedeflemektedir:

- **HTTP Servisleri** oluşturma ve yönetme.
- **Asenkron ve Paralel Programlama** yöntemlerini uygulama.
- Gelişmiş Go framework’ü olan **Fiber** kullanımı.
- **SQLC** ile güvenli ve verimli veritabanı işlemleri.
- **Middleware** kullanımıyla loglama, doğrulama ve hata yönetimi.
- **JWT** ile güvenli kimlik doğrulama ve yetkilendirme.
- **Testing** (Unit ve Entegrasyon) ile kod kalitesini artırma.
- **Docker** ile bağımsız çalışabilir servisler geliştirme.
- **Redis** ile hızlı veri önbellekleme ve oturum yönetimi.
- **RabbitMQ** ile asenkron veri iletimi.
- **Logrus** ve **Zap** ile gelişmiş loglama.
- **WebSocket** ile gerçek zamanlı iletişim.
- **API Gateway** ile mikroservis isteklerini yönetme.
- **Service Discovery** kullanarak dinamik servis keşfi.
- **gRPC** ile hızlı ve güvenli mikroservis iletişimi.
- **Prometheus** ile performans izleme ve **Grafana** ile görselleştirme.

---

## 🏠 **Proje Özeti**
Akıllı Ev Yönetim Sistemi, bir mikroservis mimarisi kullanarak evdeki akıllı cihazları (ışıklar, termostatlar, güvenlik kameraları vb.) kontrol etmeyi ve izlemeyi sağlar. Kullanıcılar, sistemle API'lar üzerinden etkileşim kurabilir,web veya mobil arayüzlere entegre edilebilir. Proje, veri güvenliği, performans izleme, ve gerçek zamanlı bildirim özelliklerini içermektedir.

---

## 📚 **Proje Özellikleri**

| Özellik                          | Açıklama                                                                                  |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Cihaz Yönetimi**               | Cihazların durumu izlenir ve kontrol edilir (açma/kapama, sıcaklık ayarı vb.).           |
| **Zamanlama ve Otomasyon**       | Belirli saatlerde cihazların açılıp kapanması planlanabilir.                              |
| **Gerçek Zamanlı Bildirimler**   | WebSocket ile cihaz durum değişiklikleri anlık olarak bildirilir.                        |
| **Veri Toplama ve Analiz**       | Cihaz verileri toplanır ve analiz edilir (örn. sıcaklık, nem seviyeleri).                |
| **Uyarı Sistemi**                | Kritik durumlarda (örn. aşırı sıcaklık) kullanıcıya uyarılar gönderilir.                 |
| **Veri Güvenliği**               | Kullanıcı doğrulama ve yetkilendirme **JWT** ile sağlanır.                               |

---
