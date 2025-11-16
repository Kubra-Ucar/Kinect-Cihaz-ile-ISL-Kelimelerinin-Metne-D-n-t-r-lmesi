# Uluslararası İşaret Dili Sözcüklerinin Kinect Cihazı ile Metne Dönüştürülmesi

Bu proje, **Kinect v2** cihazının sunduğu iskelet takibi ve el hareketi algılama özelliklerini kullanarak **Uluslararası İşaret Dili (International Sign Language – ISL)** sözcüklerini **gerçek zamanlı olarak metne dönüştürmeyi** amaçlamaktadır.

Kinect’in kemik eklem noktalarını (joints) yüksek doğrulukla algılayabilmesi sayesinde belirli sözcükler için önceden tanımlanan el ve kol pozisyonları tespit edilir ve uygun sözcük ekrana yazdırılır.

---

## 🎯 Projenin Amacı

- Uluslararası İşaret Dili (ISL) sözcüklerinin Kinect v2 ile gerçek zamanlı olarak algılanması  
- İşaret dili bilmeyen bireyler ile işaret dili kullanıcıları arasında iletişim kolaylığı sağlanması  
- Kinect’in hazır fonksiyonlarını kullanarak hızlı ve düşük maliyetli bir işaret dili çeviri sistemi sunmak  
- Tanımlanan sözcüklere karşılık gelen metni ekrana yazdırmak ve (isteğe bağlı) sesli çıktı oluşturmak  

---

## 📌 Kullanılan Teknolojiler ve Araçlar

- **Kinect v2**
- **Kinect SDK 2.0**
- **C# / WPF**
- **Body Tracking (El, kol, bilek, omuz eklemleri)**
- **Gesture / Pose tanımlayıcı fonksiyonlar**  
- Opsiyonel: Text-to-Speech (TTS) için `System.Speech` kütüphanesi

---

## 🧠 Proje Nasıl Çalışır?

1. Kinect v2 cihazı kullanıcıyı algılar.  
2. Cihazdan alınan **25 eklem noktasının koordinatları** (x, y, z) gerçek zamanlı olarak takip edilir.  
3. Her sözcük için özel pozisyon/şart kontrolleri yapılır.  
   Örneğin:
   - El açıklığı  
   - Parmak yönelimi  
   - El ile omuz arasındaki mesafe  
   - Kolun yukarı-aşağı pozisyonu  
4. Şartlar sağlandığında ilgili sözcük ekrana yazdırılır.  
5. Aynı sözcüğün sürekli tekrar edilmesini engellemek için **zaman aralığı filtresi (ör. 3 saniye cooldown)** uygulanır.  
6. İstenirse sözcük **sesli olarak da telaffuz edilir**.

---

## 📁 Proje Dosya Yapısı (Önerilen)

