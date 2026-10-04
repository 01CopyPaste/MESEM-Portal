# 🏫 MESEM Portal
**Mesleki Eğitim Merkezleri (MESEM) için Sunucusuz, Çevrimdışı Çalışabilen Koordinatörlük Yönetim Sistemi**

Bu proje, meslek liseleri ve MESEM koordinatör öğretmenlerinin sahada yaşadığı zorlukları (dosya karmaşası, adres bulamama, rotalama zorluğu) çözmek amacıyla tasarlanmış **tek dosyalık (Single HTML)** bir web uygulamasıdır. 

Sistem hiçbir arka uç (backend) veya veritabanı sunucusu gerektirmez. Tüm veriler %100 güvenli bir şekilde kullanıcının kendi tarayıcısında (Local Storage) tutulur.

## ✨ Öne Çıkan Özellikler

* 🚀 **Sıfır Kurulum & Sunucusuz Yapı:** Sadece HTML dosyasını açmanız yeterlidir. İnternet bağlantısı olmasa bile tüm liste, notlar ve kurallar çalışmaya devam eder.
* 📱 **Mobil Uygulama Desteği:** Telefon tarayıcısından açıp "Ana Ekrana Ekle" diyeyebilirsiniz. Sahada kullanım için idealdir.
* 📍 **Akıllı Bölge Otomasyonu (Regex Engine):** Adres metinlerindeki kelimeleri tarayarak (Örn: "Kadosan", "İMES") işletmeyi doğru sanayi bölgesine otomatik atar. Kurallar tamamen özelleştirilebilir.
* 📊 **Gelişmiş Çoklu Filtreleme:** Öğretmen, Bölge, Sınıf ve Dal bazlı çoklu seçim (multi-select) ile 1000+ satırlık verilerde milisaniyeler içinde süzme işlemi yapar. Sayfayı dondurmaz.
* 💾 **Akıllı Excel Yükleme:** Milli Eğitim sistemlerinden alınan Excel listelerini içeri aktarır. Aynı öğrenci numarası (Öğr.No) ile yüklenen listelerde mükerrer kayıt oluşturmaz, sadece değişen verileri günceller.
* 🗺️ **Nokta Atışı Konum:** Açık adreslerin yanı sıra enlem/boylam koordinat (Örn: `41.005, 29.164`) girişi destekler. Tek tıkla Google Haritalar'da hedefe yönlendirir.
* 🖨️ **Gelişmiş Raporlama:** Ekranda filtrelenmiş aktif listeyi saniyeler içinde **Excel** veya Türkçe karakter uyumlu **PDF** olarak dışa aktarır. Temiz A4 yazdırma (Print) moduna sahiptir.
* 🔄 **Tam Yedekleme:** Kurallar ve aktif veriler JSON formatında yedeklenip başka cihazlara tek tıkla aktarılabilir.

## 🛠️ Kurulum ve Kullanım

Sistem bağımsız bir frontend aracıdır. Kullanmak için bilgisayarınıza veya sunucuya hiçbir şey kurmanıza gerek yoktur.

1. Bu depodaki HTML dosyasını indirin.
2. Dosyaya çift tıklayarak herhangi bir tarayıcıda (Chrome, Edge, Safari vb.) açın.
3. **"Excel Yükle"** butonuna basarak elinizdeki öğrenci/işletme listesini sisteme dahil edin.

### 📱 Mobilde Kullanım
Dosyayı telefonunuza gönderin ve mobil tarayıcıda açın. Tarayıcı menüsünden **"Ana Ekrana Ekle"** seçeneğine dokunun. Uygulama telefonunuza yüklenecektir.

## 📁 Excel Veri Şablonu

İçeri aktarılacak Excel dosyasındaki başlıkların (ilk satır) sistem tarafından otomatik tanınması için aşağıdaki formatta (veya benzer varyasyonlarda) olması tavsiye edilir:

* `Öğr.No` (veya Öğrenci No, No) -> Zorunlu benzersiz anahtar
* `Ad Soyad` 
* `Sınıf` 
* `Dal`
* `Öğretmen` 
* `Firma Adı` (veya İşletme, Tespit Edilen Firma)
* `İşyeri Adresi` (veya Adres, Temiz Adres)
* `Notlar` (Opsiyonel)
* `Koordinat` (Opsiyonel)

## 💻 Kullanılan Teknolojiler
* **HTML5, CSS3, Vanilla JavaScript** (Framework kullanılmamıştır, maksimum hız hedeflenmiştir.)
* **SheetJS** - Excel içe/dışa aktarım işlemleri için.
* **jsPDF & jsPDF-AutoTable** - PDF raporlama işlemleri için.
* **FontAwesome** - Vektörel ikonlar.

## 🤝 Katkıda Bulunma
Projeyi geliştirmek, hata bildirmek veya yeni özellik önermek isterseniz Pull Request oluşturabilir veya Issues sekmesini kullanabilirsiniz. Eğitim camiasına faydalı olması dileğiyle!
