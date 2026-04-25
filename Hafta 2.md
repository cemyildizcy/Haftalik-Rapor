## 1. İşletim Sistemi Temelleri (OS Basics)

İşletim sistemi, bilgisayar donanımı ile uygulamalar arasında köprü görevi görür. Programların çalışması, belleğin kullanılması, dosyaların yönetilmesi ve donanım kaynaklarının paylaşılması işletim sistemi tarafından kontrol edilir.

### Kernel nedir?

Kernel, işletim sisteminin çekirdeğidir. Donanım ile yazılımlar arasındaki en temel iletişimi sağlar. CPU, bellek, disk, klavye, ağ kartı gibi kaynakların nasıl kullanılacağını yönetir.

Örneğin bir program dosya okumak istediğinde bunu doğrudan diske erişerek yapmaz; işletim sisteminden, yani kernel üzerinden ister. Böylece güvenlik, düzen ve kaynak paylaşımı sağlanır.

### Süreç (Process) ve iş parçacığı (Thread) farkı

Process, çalışan bir programın bellekteki bağımsız örneğidir. Her process kendi bellek alanına sahiptir. Örneğin tarayıcı, metin editörü ve müzik çalar ayrı process olarak çalışabilir.

Thread ise bir process içinde çalışan daha küçük yürütme birimidir. Aynı process içindeki thread’ler aynı belleği paylaşır. Bu nedenle thread’ler arası iletişim daha hızlıdır, ancak hatalı kullanımda veri çakışmaları oluşabilir.

Kısaca:

- Process daha bağımsız ve izoledir.
- Thread daha hafiftir ve aynı process içinde kaynak paylaşır.

### Bellek yönetimi nasıl yapılır?

Bellek yönetimi, RAM’in programlar arasında düzenli ve güvenli şekilde paylaştırılmasıdır. İşletim sistemi hangi programın ne kadar bellek kullanacağını takip eder.

Temel görevleri şunlardır:

- Programlara bellek alanı ayırmak
- Kullanılmayan belleği geri almak
- Programların birbirinin belleğine izinsiz erişmesini engellemek
- Gerektiğinde sanal bellek kullanmak

Sanal bellek sayesinde işletim sistemi, RAM yetmediğinde diskin bir bölümünü geçici bellek gibi kullanabilir. Bu işlem sistemi çalışır durumda tutar, ancak RAM’e göre daha yavaştır.

### CPU zamanlayıcıları nedir?

CPU zamanlayıcıları, işlemcinin hangi process veya thread’i ne zaman çalıştıracağını belirleyen mekanizmalardır. Çünkü genellikle aynı anda birçok program çalışmak ister, fakat CPU aynı anda sınırlı sayıda işi yürütebilir.

Zamanlayıcılar adil, hızlı ve verimli çalışma sağlamaya çalışır. Örneğin müzik çalarken aynı anda tarayıcı kullanabilmemiz, işletim sisteminin CPU zamanını bu işler arasında çok hızlı paylaştırması sayesinde olur.

Yaygın zamanlama yaklaşımlarına örnek olarak Round Robin, öncelik tabanlı zamanlama ve First-Come First-Served verilebilir.
