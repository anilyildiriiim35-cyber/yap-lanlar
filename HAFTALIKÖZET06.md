# 📅 Haftalık Kayıt – 05.05.2026 / 06.05.2026

**Ofis Günleri:** Salı – Çarşamba
**Toplam Süre:** __ saat

---

## 🎯 Haftalık Hedefler

* Proje dosya yapısını düzenlemek
* HTML, CSS ve JavaScript kodlarını ayrıştırmak
* localStorage tabanlı veri sistemi kurmak
* Menü, sipariş ve ürün yönetimi sayfalarını birbirine bağlamak
* Stok ve masa rezervasyon sistemi geliştirmek

---

## ✅ Yapılan Çalışmalar

### 📁 Proje Düzeni & Dosya Yapısı

* Sayfa isimleri standart hale getirildi

  * `index.html`, `menu.html`, `tables.html`, `order.html`, `products.html`
* Tüm sayfalar arası linkler güncellendi
* Proje klasör yapısı düzenlendi

---

### 🎨 Frontend Düzenlemeleri

* HTML ve CSS birbirinden ayrıldı
* Tüm stiller harici `style.css` dosyasına taşındı
* Sayfalar sadeleştirildi ve temizlendi
* Navbar yapısı tüm sayfalarda ortak hale getirildi

---

### 🗄️ LocalStorage Sistemi

* `urban_products` veri yapısı oluşturuldu
* Ürün ekleme, silme ve güncelleme işlemleri geliştirildi
* Veri saklama ve çağırma sistemi kuruldu
* Tüm sayfalar localStorage üzerinden veri alacak şekilde bağlandı

---

### 🍽 Menü Sayfası

* Ürünleri localStorage’dan dinamik çekme sistemi kuruldu
* Kategori filtreleme özelliği eklendi
* Arama (search) sistemi geliştirildi
* Stokta olmayan ürünler gizlendi
* JavaScript fonksiyon hataları giderildi (`filter` → `filterMenu`)

---

### 🧾 Sipariş (Order) Sistemi

* Masa bazlı sipariş sistemi oluşturuldu
* Ürün ekleme, artırma, azaltma ve silme özellikleri eklendi
* Sipariş ile birlikte stok düşme sistemi entegre edildi
* Ödeme sistemi (nakit / kart) eklendi
* Ödeme sonrası masa sıfırlama işlemi yapıldı

---

### 🪑 Masa Yönetimi

* 12 adet masa dinamik olarak oluşturuldu
* Masa dolu / boş durumu eklendi
* Sipariş varsa masa otomatik “dolu” olarak gösterildi

---

### 📌 Masa Rezervasyon Sistemi

* Masa rezervasyon özelliği geliştirildi
* Kullanıcıdan:

  * İsim / Soyisim
  * Kişi sayısı
    bilgileri alınacak şekilde yapı kuruldu
* Rezerve edilen masa üzerinde bilgiler gösterildi
* Rezervasyon iptal butonu eklendi

---

## ⚠️ Karşılaşılan Sorunlar

* CSS dosya yolu (path) hataları
* Script sırası yanlış olduğu için veri okunamaması
* HTML ve JS fonksiyon isim uyumsuzlukları
* localStorage veri formatı farklılıkları
* Menü sayfasında ürünlerin görünmemesi

---

## 🔧 Uygulanan Çözümler

* Dosya yolları (path) düzeltildi
* Script yükleme sırası düzenlendi (`storage.js → menu.js`)
* Fonksiyon isimleri standart hale getirildi
* Veri yapısı tek tip hale getirildi
* Tüm sayfalar arasında veri senkronizasyonu sağlandı

---

## 🧠 Öğrenilenler

* localStorage ile veri yönetimi mantığı
* Sayfalar arası veri paylaşımı
* Frontend proje yapısı ve dosya organizasyonu
* JavaScript fonksiyon yönetimi ve event kullanımı
* Basit bir POS sisteminin temel çalışma yapısı

---

## 🚀 Sonraki Hedefler

* Gün sonu rapor sistemi geliştirmek
* Arayüz (UI/UX) iyileştirmeleri yapmak
* Kodları modüler hale getirmek
* Hata kontrol ve validasyon sistemleri eklemek

---
