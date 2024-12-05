# **IoTGo - Testing Rehberi**

Bu doküman, IoTGo projesinin test süreçlerini ve test stratejilerini açıklamaktadır. Projede kullanılan test türleri, araçlar ve yöntemler hakkında bilgi sağlar.

---

## **1. Test Stratejisi**

IoTGo projesi için kullanılan test stratejisi, sistemin her katmanında yüksek kaliteyi sağlamak amacıyla aşağıdaki aşamaları içerir:

### **1.1 Unit Testler**
- Her mikroservis içindeki fonksiyonların bağımsız olarak test edilmesi.
- Amaç: Fonksiyonel hataları erken aşamada tespit etmek.
- Araç: **`testing` paketi (Go standart test framework)**

### **1.2 Entegrasyon Testleri**
- Mikroservisler arası iletişimin doğru çalıştığını doğrulamak.
- Örneğin, API Gateway'den bir istek yapıldığında doğru mikroservise yönlendirilmesi.
- Araçlar: **`Postman`**, **`Go Test`**

### **1.3 Performans Testleri**
- Servislerin yüksek yük altında nasıl performans gösterdiğini ölçmek.
- Amaç: Sistem darboğazlarını tespit etmek.
- Araçlar: **`k6`**, **`Apache JMeter`**

### **1.4 Gerçek Zamanlı Testler**
- WebSocket bağlantılarının kesintisiz çalıştığını doğrulamak.
- Kullanıcıların cihaz durumlarını gerçek zamanlı olarak alabildiğinden emin olun.
- Araçlar: **Custom Go test scripts**, **`WebSocket test tools`**

### **1.5 Kullanıcı Kabul Testleri (UAT)**
- Kullanıcıların temel akışları test etmesi.
- Amaç: Gerçek kullanıcı deneyimini simüle etmek.
- Araçlar: **Manual testing**, **Selenium** (isteğe bağlı otomasyon)

---
