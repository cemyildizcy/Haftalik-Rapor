## 2. Ağ Temelleri (Networking)

Ağ temelleri, bilgisayarların ve yazılımların internet veya yerel ağ üzerinden nasıl iletişim kurduğunu anlamamızı sağlar. Bir web sitesine girmek, mesaj göndermek veya dosya indirmek ağ iletişimi ile gerçekleşir.

### IP, Port, DNS, TCP ve UDP nedir?

IP adresi, bir cihazın ağ üzerindeki adresidir. İnternette veya yerel ağda cihazların birbirini bulmasını sağlar.

Port, aynı cihaz üzerinde çalışan farklı uygulamaları ayırt etmek için kullanılır. Örneğin web sunucuları genellikle 80 veya 443 numaralı portları kullanır.

DNS, alan adlarını IP adreslerine çeviren sistemdir. Örneğin bir site adı yazdığımızda DNS bu adın hangi IP adresine karşılık geldiğini bulur.

TCP, güvenilir veri aktarımı sağlayan protokoldür. Verinin eksiksiz ve sıralı ulaşmasını kontrol eder. Web sayfaları, e-posta ve dosya aktarımı gibi işlemlerde sık kullanılır.

UDP ise daha hızlı ama daha az kontrollü bir protokoldür. Verinin ulaşıp ulaşmadığını TCP kadar sıkı takip etmez. Canlı yayın, online oyun ve sesli görüşme gibi hızın önemli olduğu alanlarda tercih edilir.

### Paket yapısı nasıl çalışır?

Ağ üzerinde veriler genellikle tek parça halinde gönderilmez. Bunun yerine küçük parçalara, yani paketlere bölünür. Her paketin içinde gönderilecek verinin bir kısmı ve yönlendirme için gerekli bilgiler bulunur.

Bir pakette genellikle şunlar yer alır:

- Kaynak IP adresi
- Hedef IP adresi
- Port bilgisi
- Protokol bilgisi
- Taşınan veri

Paketler ağ üzerinde farklı yollardan ilerleyebilir. Hedefe ulaştıklarında tekrar birleştirilerek anlamlı veri haline getirilir.

### Ping, traceroute ve nslookup ne işe yarar?

Ping, bir cihaza ulaşılıp ulaşılamadığını test etmek için kullanılır. Ayrıca bağlantı gecikmesini ölçer.

Traceroute, bir paketin hedefe giderken geçtiği ağ noktalarını gösterir. Bağlantı sorunlarının hangi noktada yaşandığını anlamak için faydalıdır.

Nslookup, bir alan adının hangi IP adresine karşılık geldiğini sorgulamak için kullanılır. DNS problemlerini kontrol etmekte kullanılır.

## Sonuç

İşletim sistemi temelleri, yazılımın bilgisayar üzerinde nasıl çalıştığını anlamayı sağlar. Kernel, process, thread, bellek yönetimi ve CPU zamanlama konuları bu yapının merkezindedir.

Ağ temelleri ise yazılımların internet üzerinde nasıl iletişim kurduğunu açıklar. IP, port, DNS, TCP, UDP ve ağ araçlarını bilmek, özellikle web geliştirme, sistem yönetimi ve hata ayıklama süreçlerinde büyük avantaj sağlar.

Bu iki alanı öğrenmek, yazılımın hem bilgisayar içinde hem de internet üzerinde nasıl çalıştığını daha net kavramaya yardımcı olur.
