# IoTGo (Akıllı Ev Yönetim Sistemi ) - Kullnılıcak Teknolojiler

## 🛠️ **Teknolojiler ve Kullanım Amaçları**

| Teknoloji           | Amaç                                                                                     |
|---------------------|-----------------------------------------------------------------------------------------|
| **Fiber**           | Hızlı ve hafif HTTP servisleri oluşturmak.                                              |
| **SQLC**            | Veritabanı sorgularını güvenli ve performanslı şekilde işlemek.                         |
| **Middleware**      | Hata yönetimi, loglama, kimlik doğrulama gibi işlemleri kolaylaştırmak.                  |
| **JWT**             | Kullanıcı doğrulama ve yetkilendirme.                                                   |
| **Testing**         | Kodun doğru çalıştığından emin olmak için birim ve entegrasyon testleri.                 |
| **Docker**          | Servisleri izole etmek ve platform bağımsız çalışabilirlik sağlamak.                     |
| **Redis**           | Veri önbellekleme ve oturum yönetimi.                                                   |
| **RabbitMQ**        | Mikroservisler arası asenkron iletişim sağlamak.                                         |
| **Logrus ve Zap**   | Gelişmiş loglama ve hata takibi.                                                         |
| **WebSocket**       | Gerçek zamanlı cihaz durumu güncellemeleri sağlamak.                                     |
| **API Gateway**     | İstekleri yönlendirerek mikroservislerin güvenli ve düzenli çalışmasını sağlamak.         |
| **Service Discovery** | Mikroservislerin dinamik olarak keşfedilmesini sağlamak.                               |
| **gRPC**            | Mikroservisler arasında hızlı ve güvenli iletişim.                                       |
| **Prometheus**      | Sistem metriklerini izlemek.                                                             |
| **Grafana**         | İzlenen metrikleri görselleştirmek.                                                      |

---

## 🎯 **Mimari Yapı**

### **Mikroservisler**
- **Cihaz Servisi:** Akıllı cihazların yönetimi.
- **Zamanlayıcı Servisi:** Otomasyon ve zamanlama.
- **Veri Analiz Servisi:** Cihazlardan gelen verilerin analizi.
- **Bildirim Servisi:** Gerçek zamanlı uyarı ve bildirimler.

### **API Gateway**
- Tüm istekleri tek bir noktada toplayarak mikroservislere yönlendirir.
- Kimlik doğrulama ve yetkilendirme sağlar.

---

## 📊 **Performans İzleme**

| Araç           | Kullanım Amacı                                                                                |
|----------------|-----------------------------------------------------------------------------------------------|
| **Prometheus** | Sistemden metrikler toplayarak performans takibi.                                             |
| **Grafana**    | Performans verilerinin görselleştirilmesi.                                                    |

---

## 🧪 **Test Yaklaşımı**

- **Unit Test:** Her mikroservisin bağımsız modüllerini test etmek.
- **Integration Test:** Mikroservisler arası iletişim ve entegrasyonu doğrulamak.

---

## 🚀 **Başlangıç Adımları**

1. **Gerekli araçları kurun:**
    - Go, Docker, Redis, RabbitMQ, Prometheus, Grafana vb.
2. **Docker Compose ile tüm servisleri ayağa kaldırın.**
3. **API Gateway üzerinden istekler göndererek sistemi test edin.**
4. **Prometheus ve Grafana ile performans ve logları izleyin.**

---

## 🖥️ **Projenin Önemi**
Bu proje, modern yazılım geliştirme süreçlerinde kullanılan ileri seviye teknolojileri bir arada uygulayarak, hem teorik hem de pratik becerilerinizi geliştirmenize olanak tanır. Özellikle IoT, mikroservis mimarisi ve gerçek zamanlı sistemlere ilgi duyanlar için mükemmel bir öğrenim alanıdır.
