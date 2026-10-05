💼 MESEM Portal - Gelişmiş Koordinatörlük Sistemi

Mesleki Eğitim Merkezleri (MESEM) koordinatör öğretmenleri için geliştirilmiş, tamamen tarayıcı üzerinde çalışan, sunucusuz (serverless) ve çevrimdışı destekli (PWA) öğrenci ve işletme takip otomasyonu.

Bu proje, dışa bağımlılıkları minimumda tutarak tek bir HTML dosyası içerisinde gelişmiş bir "Single Page Application (SPA)" deneyimi sunmayı hedefler.

✨ Öne Çıkan Özellikler

🚀 Sunucusuz & Çok Hızlı: Herhangi bir veritabanı veya backend kurulumu gerektirmez. Tüm veriler tarayıcınızın localStorage alanında güvenle tutulur.

📱 PWA (Progressive Web App): Çevrimdışı (offline) çalışabilir. Telefonunuza, tabletinize veya bilgisayarınıza yerel bir uygulama gibi yüklenebilir.

📊 Excel Entegrasyonu: Yüzlerce veya binlerce öğrenci kaydını (SheetJS kullanarak) saniyeler içinde içe/dışa aktarabilirsiniz. Çift kayıtları (duplicate) akıllıca tespit eder ve günceller.

🤖 Akıllı Bölge Kural Motoru: Öğrenci/İşletme adreslerindeki metinleri Regex (Düzenli İfadeler) ile analiz ederek, öğrencileri otomatik olarak doğru "Bölgelere" atayan dinamik bir kural motoru içerir.

🔍 Gelişmiş Arama & Filtreleme: Olay Temsilciliği (Event Delegation) tabanlı yüksek performanslı arama çubuğu ve Öğretmen, Bölge, Sınıf, Dal bazlı akıllı Multi-Select filtreler.

💾 Tam Yedekleme & Arşiv: Öğrencileri silmek yerine arşivleyebilme, sistemin o anki tam durumunu (kurallar dahil) JSON formatında dışa aktarma ve geri yükleme imkanı.

🗺️ Google Maps Entegrasyonu: İşletme adreslerini veya özel koordinatları tek tıkla haritada açma.

🖨️ Özelleştirilmiş Yazdırma Görünümü: Tabloları yazdırırken gereksiz butonları ve ID'leri gizleyen temiz CSS @media print tasarımı.

🛠️ Kullanılan Teknolojiler

HTML5 & CSS3: Modern, esnek (Flexbox/Grid) ve mobil uyumlu (Responsive) arayüz.

Vanilla JavaScript (ES6+): Framework (React, Vue vb.) kullanılmadan, Closure mimarisi ve DOM optimizasyonları ile geliştirilmiş saf Javascript gücü.

SheetJS (xlsx): İstemci tarafında Excel dosyası okuma ve yazma işlemleri için.

FontAwesome: İkon setleri için.

🚀 Kurulum ve Kullanım

Bu uygulama hiçbir sunucu mimarisine ihtiyaç duymaz. Kullanmaya başlamak dünyanın en kolay işidir:

Bu depoyu klonlayın veya doğrudan repo içindeki MESEM_Portal_V24.html (veya güncel sürüm) dosyasını indirin.

İndirdiğiniz HTML dosyasına çift tıklayarak modern bir web tarayıcısında (Chrome, Edge, Safari, Firefox vb.) açın.

İşte bu kadar! Kurallarınızı oluşturmaya ve Excel'den verilerinizi yüklemeye başlayabilirsiniz.

🧠 Teknik Mimari ve Geliştirici Notları

Proje tek bir dosya olmasına rağmen "Spagetti Kod" oluşumunu engellemek için kurumsal standartlarda yazılmıştır:

Closure ve Scope Yönetimi: Tüm Javascript mantığı DOMContentLoaded içinde bir IIFE (Immediately Invoked Function Expression) benzeri yapı ile sarmalanarak global 'window' kirliliği önlenmiştir.

DOM Optimizasyonu: Yüzlerce veriyi ekrana çizerken tarayıcının donmaması için innerHTML += döngüleri yerine, HTML string'leri bir Array içerisinde (bellekte) toplanıp .join('') metoduyla tek seferde render edilmektedir (Minimize Reflow/Repaint).

Event Delegation: Tablo satırları veya liste öğeleri gibi dinamik çoğalan elementlere tek tek "event listener" eklemek yerine, kapsayıcı (parent) elementler üzerinden dinleme yapılarak yüksek performans sağlanmıştır.

🤝 Katkıda Bulunma

Eğitim kurumlarına destek olmak veya projeyi geliştirmek isterseniz pull request'lerinizi bekliyoruz! Lütfen PR göndermeden önce kodun mevcut mimarisine (Single File ve Vanilla JS) sadık kaldığınızdan emin olun.

Bu repoyu forklayın

Kendi feature branch'inizi oluşturun (git checkout -b feature/YeniOzellik)

Değişikliklerinizi commit edin (git commit -m 'Harika bir özellik eklendi')

Branch'inizi pushlayın (git push origin feature/YeniOzellik)

Bir Pull Request oluşturun.

📄 Lisans

Bu proje eğitimcilerin işini kolaylaştırmak amacıyla açık kaynak olarak geliştirilmiştir. Kendi ihtiyaçlarınıza göre özgürce değiştirebilir ve kullanabilirsiniz (MIT License).
