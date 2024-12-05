# IoTGo (Akıllı Ev Yönetim Sistemi ) - Mimari Yapı

## 🎯 **Mimari Genel Bakış**
Proje, bir mikroservis mimarisi üzerine inşa edilmiştir. Her mikroservis, kendi alanında bağımsızdır ve API Gateway aracılığıyla dış dünyaya entegre edilir. Sistem, hem ölçeklenebilirlik hem de bakım kolaylığı göz önünde bulundurularak tasarlanmıştır.

---

## 🏛️ **Mimari Bileşenler** (Detaylar Service Documentation dosyasında)

### **1. API Gateway**
- **Görevi:**
    - Tüm istekleri bir noktada toplar ve ilgili mikroservise yönlendirir.
    - Kullanıcı doğrulama ve yetkilendirme işlemlerini yönetir.
- **Teknolojiler:**
    - **Fiber**: HTTP taleplerini yönetmek.
    - **JWT**: Kullanıcı doğrulama.

---

### **2. Mikroservisler**

| Servis Adı                  | Görevi                                                                                  | Teknolojiler                                        |
|-----------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| **Cihaz Servisi**           | Akıllı cihazların durumlarını yönetir ve kullanıcı taleplerine göre günceller.           | Fiber, SQLC, Redis                                 |
| **Zamanlayıcı Servisi**     | Cihazların belirli zamanlarda çalışmasını veya kapanmasını otomatikleştirir.             | Go Channels, RabbitMQ                              |
| **Veri Analiz Servisi**     | Cihazlardan gelen verileri toplar, analiz eder ve raporlar.                             | Prometheus, Grafana                                |
| **Bildirim Servisi**        | Gerçek zamanlı bildirimler ve uyarılar gönderir.                                        | WebSocket, RabbitMQ                                |

---

### **3. Veritabanı**
- **Görevi:**
    - Kullanıcı bilgileri, cihaz durumları ve zamanlama ayarlarını saklar.
- **Teknolojiler:**
    - **PostgreSQL**: Veritabanı yönetimi.
    - **Redis**: Oturum ve hızlı veri önbellekleme.
- **Kaç Adet Veritabanımız Olucak:**
  - Başlangıç seviyesi için 1 adet veritabanımız yetiecktir bize proje çok büyüyecek olursa yenibir düzenleme yapılıcaktır. 
---

### **4. İletişim ve Asenkron İşlemler**
- **RabbitMQ:**
    - Mikroservisler arası mesajlaşma ve asenkron işlemleri yönetir.
- **WebSocket:**
    - Cihaz durumu ve uyarıları gerçek zamanlı olarak kullanıcıya iletir.

---

### **5. İzleme ve Loglama**
- **Loglama:**
    - **Logrus** ve **Zap** ile uygulama günlükleri tutulur.
- **Performans İzleme:**
    - **Prometheus:** Sistem metriklerini toplar.
    - **Grafana:** Toplanan metrikleri görselleştirir.

---

### **6. Service Discovery**
- **Görevi:**
    - Mikroservislerin dinamik olarak birbirini keşfetmesini sağlar.
- **Teknolojiler:**
    - **Consul** veya **Eureka** kullanılabilir.

---

### **7. Testing**
- **Unit Test:** Mikroservislerin bağımsız bölümleri için.
- **Integration Test:** Mikroservisler arası iletişim ve entegrasyon için.

---

## 🔄 **Akış Diyagramı**
    ```mermaid
        graph TD;
        A[API Gateway] --> B[Cihaz Servisi];
        A --> C[Zamanlayıcı Servisi];
        A --> D[Veri Analiz Servisi];
        A --> E[Bildirim Servisi];
        B --> F[(Redis)];
        C --> G[(RabbitMQ)];
        D --> H[(Prometheus)];
        D --> I[Grafana];

---

## 🌐 **Mimari Avantajları**
- **Ölçeklenebilirlik:** Mikroservisler bağımsız olarak ölçeklenebilir.
- **Kolay Bakım:** Her servis bağımsız çalıştığı için hata tespiti ve düzeltmesi kolaydır.
- **Gerçek Zamanlılık:** WebSocket ile anlık güncellemeler sağlanır.
- **Yüksek Performans:** Prometheus ve Redis entegrasyonları ile optimize edilmiş sistem.
- **Güvenlik:** JWT kullanımıyla güvenli kullanıcı doğrulama ve yetkilendirme.