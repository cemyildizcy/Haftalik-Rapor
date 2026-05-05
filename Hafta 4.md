### **4. Dosya Sistemleri ve Depolama Mantığı**

#### **NTFS – ext4 – APFS Farkları**
Dosya sistemleri, bir depolama cihazında verilerin nasıl saklandığını, organize edildiğini ve yönetildiğini belirleyen yapılardır. Farklı işletim sistemleri, kendi ihtiyaçlarına ve optimizasyonlarına uygun dosya sistemleri kullanır.
*   **NTFS (New Technology File System):** Microsoft tarafından Windows işletim sistemleri için geliştirilmiştir. Büyük dosya boyutlarını destekler, güvenlik (izinler ve şifreleme) konusunda gelişmiştir ve elektrik kesintileri gibi durumlarda veri kaybını önlemek için "journaling" (günlükleme) özelliğine sahiptir.
*   **ext4 (Fourth Extended File System):** Linux sistemlerinde en yaygın kullanılan dosya sistemidir. Yüksek performanslıdır, büyük depolama alanlarını ve dosyaları destekler. NTFS gibi journaling özelliğine sahiptir, parçalanmayı (fragmentation) en aza indirecek şekilde çalışır.
*   **APFS (Apple File System):** Apple tarafından macOS, iOS ve diğer Apple cihazları için özel olarak SSD'ler (Solid State Drives) ve flaş bellekler düşünülerek optimize edilmiştir. Kopyalama işlemlerini anında gerçekleştirme (clones), güçlü şifreleme ve hızlı alan hesaplama gibi modern özellikler sunar.

#### **Blok Yapısı Nedir?**
Depolama birimlerinde (HDD, SSD) veriler byte byte değil, "blok" (block) veya "sektör" (sector) adı verilen sabit boyutlu küçük parçalar halinde okunur ve yazılır. 
*   İşletim sistemi bir dosyayı kaydederken, o dosyayı bu bloklara böler.
*   Örneğin blok boyutu 4 KB ise ve siz 1 KB'lık bir dosya kaydederseniz, o dosya yine de diskte 4 KB'lık bir blok yer kaplar. Geriye kalan 3 KB boş kalsa da başka bir dosya için kullanılamaz (slack space).
*   Blok yapısı, diskin veriyi daha hızlı yönetmesini ve okuma/yazma işlemlerinin verimli bir şekilde yapılmasını sağlar.

#### **HDD vs SSD Çalışma Prensipleri**
Bu iki depolama teknolojisi, veriyi kaydetme ve okuma biçimleriyle birbirinden tamamen ayrılır:
*   **HDD (Hard Disk Drive):** Mekanik bir yapıya sahiptir. İçinde dönen manyetik diskler (platter) ve bu disklerin üzerinde okuma/yazma yapan hareketli bir kafa (actuator arm) bulunur. Plak çalar gibi çalışır. Veri okunacağı veya yazılacağı zaman disk döner, kafa doğru konuma gelir. Bu mekanik hareket "gecikmeye" (latency) neden olur.
*   **SSD (Solid State Drive):** Tamamen elektronik bir yapıya sahiptir. İçerisinde hareketli hiçbir parça yoktur, veriler NAND flash bellek yongalarında (mikroçiplerde) elektriksel olarak saklanır. RAM'e benzer bir mantıkla çalışır ancak gücü kestiğinizde de veriyi tutar. Hareketli parça olmadığı için veriye anında erişilebilir.

#### **Kazanç: Veri okuma/yazma hızlarının nereden geldiğini anlarsın.**
*   **HDD'lerin Yavaşlığı:** Tamamen fiziksel limitlerden kaynaklanır. Diskin dönme hızı (RPM - 5400, 7200 vb.) ve okuyucu kafanın hareket etme süresi hızın sınırını belirler. Dosyalar disk üzerinde dağınık bloklara yazılmışsa (parçalanma), kafa sürekli hareket etmek zorunda kalır ve hız performansı ciddi ölçüde düşer.
*   **SSD'lerin Hızı:** Veriye elektrik akımıyla erişildiği için fiziksel bir arama süresi yoktur. Bloklar arası geçişler mikrosaniyeler seviyesindedir. Dosya diskte ne kadar dağınık olursa olsun (fragmentation SSD'ler için sorun değildir), aynı hızda okunur. Bu yüzden işletim sisteminin açılması, programların yüklenmesi gibi işlemlerde SSD'ler, HDD'lere göre devasa hız farkları yaratır.
