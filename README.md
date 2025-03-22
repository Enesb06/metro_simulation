# metro_simulation
# Metro Ağı Projesi

 Metro Ağı Projesi
Bu proje, bir metro ağındaki istasyonlar arasındaki en kısa ve en hızlı rotaları bulmak için geliştirilmiştir. Proje, BFS (Breadth-First Search) ve A* algoritmalarını kullanarak rotaları hesaplar. Kullanıcılar, başlangıç ve hedef istasyonları belirleyerek en az aktarmalı veya en hızlı rotayı bulabilirler.

1. Kullanılan Teknolojiler ve Kütüphaneler
Projede aşağıdaki Python kütüphaneleri ve modülleri kullanılmıştır:

collections.defaultdict: Varsayılan değerlerle sözlük oluşturmak için kullanılır. Metro hatlarını ve istasyonları saklamak için kullanıldı.

collections.deque: BFS algoritmasında kuyruk veri yapısı olarak kullanıldı. FIFO (First-In-First-Out) mantığıyla çalışır.

heapq: A* algoritmasında öncelik kuyruğu (priority queue) oluşturmak için kullanıldı. En düşük maliyetli rotayı bulmak için optimize edilmiştir.

typing: Python'da tür ipuçları (type hints) sağlamak için kullanıldı. Kodun okunabilirliğini artırır.

2. Algoritmaların Çalışma Mantığı
BFS (Breadth-First Search) Algoritması
Nasıl Çalışır?

BFS, bir graf üzerinde genişleme önceliği veren bir arama algoritmasıdır.

Başlangıç düğümünden başlar ve tüm komşu düğümleri keşfeder.

Keşfedilen düğümler bir kuyruk (queue) yapısında saklanır.

Hedef düğüme ulaşıldığında, en kısa yol (en az aktarma) bulunmuş olur.

Neden Kullanıldı?

BFS, en az aktarmalı rotayı garantiler.

Metro ağı gibi ağırlıksız graflarda (veya ağırlıkların önemsiz olduğu durumlarda) etkilidir.

A* Algoritması
Nasıl Çalışır?

A*, en kısa yol problemlerini çözmek için kullanılan bir heuristic arama algoritmasıdır.

Her düğüm için bir maliyet fonksiyonu (f(n) = g(n) + h(n)) hesaplar:

g(n): Başlangıç düğümünden mevcut düğüme olan gerçek maliyet.

h(n): Mevcut düğümden hedef düğüme olan tahmini maliyet (heuristik).

Öncelik kuyruğu (priority queue) kullanarak en düşük maliyetli rotayı bulur.

Neden Kullanıldı?

A*, en hızlı rotayı bulmak için optimize edilmiştir.

Heuristic fonksiyon sayesinde BFS'ye göre daha hızlıdır ve daha az düğüm keşfeder.

3. Örnek Kullanım ve Test Sonuçları
Örnek Metro Ağı
Projede örnek bir metro ağı oluşturulmuştur. Bu ağ, üç hat (Kırmızı Hat, Mavi Hat, Turuncu Hat) ve birden fazla aktarma noktası içerir.

Test Senaryoları
AŞTİ'den OSB'ye:

En Az Aktarmalı Rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

En Hızlı Rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB (20 dakika)

Batıkent'ten Keçiören'e:

En Az Aktarmalı Rota: Batıkent -> Demetevler -> Gar -> Keçiören

En Hızlı Rota: Batıkent -> Demetevler -> Gar -> Keçiören (21 dakika)

Keçiören'den AŞTİ'ye:

En Az Aktarmalı Rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

En Hızlı Rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ (14 dakika)


4. Projeyi Geliştirme Fikirleri
Projeyi daha da geliştirmek için aşağıdaki fikirler uygulanabilir:

Grafiksel Arayüz (GUI):

Metro ağını görselleştirmek ve kullanıcıların istasyonları seçmesini sağlamak için bir GUI eklenebilir.

Gerçek Zamanlı Veri Entegrasyonu:

Gerçek dünyadaki metro hatları ve zamanlamaları projeye entegre edilebilir.

Çoklu Dil Desteği:

Proje, farklı dillerde kullanıcı arayüzü sunacak şekilde genişletilebilir.

Farklı Algoritmaların Karşılaştırılması:

Dijkstra, Bellman-Ford gibi diğer algoritmalar da eklenerek performans karşılaştırması yapılabilir.

Veritabanı Entegrasyonu:

İstasyon ve hat bilgileri bir veritabanında saklanabilir ve dinamik olarak yönetilebilir.

Mobil Uygulama:

Proje, mobil platformlarda kullanılabilecek bir uygulamaya dönüştürülebilir.
