
[![Go](https://github.com/SadikSunbul/GO-BlockChain-Simulation/actions/workflows/go.yml/badge.svg)](https://github.com/SadikSunbul/GO-BlockChain-Simulation/actions/workflows/go.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/SadikSunbul/GO-BlockChain-Simulation)](https://goreportcard.com/report/github.com/SadikSunbul/GO-BlockChain-Simulation)
[![Version](https://img.shields.io/badge/Version-1.0-blue)]()

# IoTGo (Geliştirme Aşamasında)

Bu proje, evdeki akıllı cihazları (ışıklar, termostatlar, güvenlik kameraları, kapı kilitleri vb.) bir **mikroservis mimarisi** ile yönetmek için geliştirilmiştir. Kullanıcılar, bu cihazları **mobil uygulama** veya **web arayüzü** üzerinden kontrol edebilir. Sistem, veri güvenliği, performans izleme, zamanlama ve otomasyon gibi modern teknolojilerle desteklenmektedir.

---

## 📌 Proje Özeti

IoTGo, akıllı ev cihazlarını merkezi bir platform üzerinden yöneterek, kullanıcıların:
- Cihazların durumlarını izleme ve kontrol etmelerine,
- Zamanlama ve otomasyon ile cihazlarını programlamalarına,
- Toplanan verilerin analizini yaparak anlamlı bilgiler elde etmelerine,
- Gerçek zamanlı durum güncellemeleri ve bildirimler almasına,  
  olanak sağlar.

---

## 🚀 Temel Özellikler

### 📱 Cihaz Yönetimi
- Evdeki akıllı cihazların durumlarını kontrol etme (açma, kapama, sıcaklık ayarı vb.).
- Kullanıcıların cihazlarını uzaktan kontrol etme yeteneği.

### ⏰ Zamanlama ve Otomasyon
- Cihazların otomatik olarak belirli zamanlarda açılıp kapanması için programlama.

### 📊 Veri Toplama ve Analiz
- Akıllı cihazlardan gelen sıcaklık, nem, ışık seviyesi gibi verilerin toplanması ve analiz edilmesi.

### 🔔 Bildirimler ve Uyarılar
- Örneğin, sıcaklık çok yüksek olduğunda veya güvenlik kamerası hareket algıladığında kullanıcıya anlık bildirim gönderme.

### 🔒 Veri Güvenliği
- JWT ile kullanıcı doğrulama ve yetkilendirme.

---

## 🔧 Kullanılan Teknolojiler

| Kategori                     | Teknoloji                               | Açıklama                                       |  
|------------------------------|-----------------------------------------|-----------------------------------------------|  
| **Backend Framework**        | Fiber                                   | Hızlı ve hafif bir Go framework'ü.            |  
| **Gerçek Zamanlı İletişim**  | WebSocket                               | Cihaz durumlarını anlık iletmek için.         |  
| **Asenkron İşlemler**        | RabbitMQ, Go Channels                   | Veri akışı ve mesaj kuyruğu yönetimi.         |  
| **Veritabanı**               | SQLC, PostgreSQL                        | Güvenli ve verimli veritabanı yönetimi.       |  
| **Loglama**                  | Logrus, Zap                             | Gelişmiş loglama ve hata yönetimi.            |  
| **Güvenlik**                 | JWT                                     | Kullanıcı doğrulama ve yetkilendirme.         |  
| **Monitoring**               | Prometheus, Grafana                     | Performans izleme ve görselleştirme.          |  
| **Containerization**         | Docker                                  | Mikroservislerin bağımsız çalıştırılması.     |  

---

## 🏗️ Proje Mimarisi

IoTGo, **mikroservis mimarisi** kullanır. Her cihaz türü veya işlevsellik bağımsız bir mikroservis tarafından yönetilir.

## 🧩 Microservisler

Proje kapsamında kullanılan her bir microservis bağımsız bir repository olarak geliştirilmiştir. Aşağıda, ilgili microservislerin açıklamaları ve repo bağlantılarına ulaşabilirsiniz:

1. **Device Management Service**
    - **Açıklama**: Evdeki akıllı cihazların yönetimi, durumu, eklenmesi ve güncellenmesi.
    - **Repository**: [Device Management Service Repo](https://github.com/username/device-management-service)


2. **Scheduler and Automation Service**
    - **Açıklama**: Cihazların otomatik açılmasını ve kapanmasını sağlayan zamanlayıcı ve otomasyon işlemleri.
    - **Repository**: [Scheduler and Automation Service Repo](https://github.com/username/scheduler-automation-service)


3. **Data Analytics Service**
    - **Açıklama**: Cihazlardan toplanan verilerin analizi ve performans izleme.
    - **Repository**: [Data Analytics Service Repo](https://github.com/username/data-analytics-service)


4. **Notification and Alert Service**
    - **Açıklama**: Cihaz durumu değişiklikleri veya anormal durumlar için bildirimler gönderir.
    - **Repository**: [Notification and Alert Service Repo](https://github.com/username/notification-alert-service)


5. **API Gateway Service**
    - **Açıklama**: Dış dünyaya tek API noktası sunar ve talepleri mikroservislere yönlendirir.
    - **Repository**: [API Gateway Service Repo](https://github.com/username/api-gateway-service)


6. **Authentication Service**
    - **Açıklama**: Kullanıcı doğrulama ve yetkilendirme işlemleri.
    - **Repository**: [Authentication Service Repo](https://github.com/username/authentication-service)


7. **Service Discovery**
    - **Açıklama**: Mikroservislerin birbirini dinamik olarak keşfetmesini sağlar.
    - **Repository**: [Service Discovery Repo](https://github.com/username/service-discovery)


8. **Asynchronous Communication Service**
    - **Açıklama**: Asenkron veri iletimi ve cihazlar arası iletişim sağlar.
    - **Repository**: [Asynchronous Communication Service Repo](https://github.com/username/asynchronous-communication-service)


9. **Logging and Monitoring Service**
    - **Açıklama**: Uygulama loglarını tutar ve sistem metriklerini izler.
    - **Repository**: [Logging and Monitoring Service Repo](https://github.com/username/logging-monitoring-service)


10. **IoT Device Simulation Service**
    - **Açıklama**: Gerçek cihazlar yerine, sistemin farklı IoT cihazlarını simüle eder. Durum güncellemelerini üretir ve diğer mikroservislere sahte cihaz verileri ileterek test süreçlerini destekler.
    - **Repository**: [IoT Device Simulation Service Repo](https://github.com/username/iot-device-simulation-service)


## 📊 Monitoring ve Görselleştirme

Proje metriklerini takip etmek ve görselleştirmek için aşağıdaki araçları kullanabiliceksiniz:

- **Prometheus UI**: [http://localhost:9090](http://localhost:9090)
- **Grafana UI**: [http://localhost:3000](http://localhost:3000)

---

## 🛠️ Geliştirici Notları

### Testing
- Her mikroservis için birim testleri yazılmıştır.
- Entegrasyon testleri, API Gateway ile mikroservislerin uyumunu doğrular.

### Gelecekteki İyileştirmeler
- Kubernetes entegrasyonu ile tam otomasyon sağlanabilir.
- Makine öğrenimi algoritmaları ile cihazların davranış analizi yapılabilir.

---

## 📫 İletişim

Eğer proje ile ilgili sorularınız veya geri bildirimleriniz varsa, benimle iletişime geçebilirsiniz:

- **Email**: [jsjsqwe12@gmaik.com](mailto:jsjsqwe12@gmaik.com)
- **LinkedIn**: [Sadık Sünbül](https://www.linkedin.com/in/sadiksunbul/)  

