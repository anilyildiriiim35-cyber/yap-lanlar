# Mini POS Frontend Prototype

## Proje Tanımı

Mini POS Frontend Prototype, restoran ve kafe işletmeleri için geliştirilmiş temel seviyede bir sipariş ve masa yönetim sistemidir.  
Proje tamamen frontend tarafında çalışmaktadır ve veriler tarayıcı üzerinde `localStorage` kullanılarak saklanmaktadır.

Sistem içerisinde:

- Masa yönetimi
- Menü görüntüleme
- Sipariş oluşturma
- Ürün yönetimi
- Stok takibi
- Gün sonu raporu

gibi temel POS işlemleri bulunmaktadır.

Amaç; gerçek bir POS sisteminin çalışma mantığını frontend tarafında prototip olarak oluşturmaktır.

---

## Kullanılan Teknolojiler

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Bootstrap 5
- localStorage API

---

## Dosya Yapısı

```bash
mini-pos/
│
├── index.html
├── menu.html
├── masa.html
├── urun-yonetim.html
├── gunsonu.html
│
├── css/
│   └── style.css
│
├── js/
│   ├── app.js
│   ├── localStorage.js
│   ├── menu.js
│   ├── masa.js
│   ├── stok.js
│   └── rapor.js
│
├── assets/
│   └── images/
│
└── README.md
```

---

## Nasıl Çalıştırılır?

1. Proje klasörünü bilgisayara indiriniz.
2. Visual Studio Code ile açınız.
3. `index.html` dosyasını çalıştırınız.
4. Tarayıcı üzerinden sistemi kullanabilirsiniz.

Alternatif olarak:

- VS Code Live Server eklentisi kullanılabilir.
- `Open with Live Server` seçeneği ile proje çalıştırılabilir.

---

## Demo Akışı

1. Ürün Yönetimi sayfasından ürün eklenir.
2. Ürünlere stok miktarı atanır.
3. Menü sayfasında ürünler görüntülenir.
4. Masa seçilir.
5. Sipariş oluşturulur.
6. Sipariş verildiğinde stok miktarı azalır.
7. Stok sıfır olursa ürün pasif hale gelir.
8. Gün Sonu Raporu sayfasında satış verileri görüntülenir.

---

## localStorage Veri Modeli

### Ürünler

```json
[
  {
    "id": 1,
    "ad": "Adana Kebap",
    "fiyat": 250,
    "stok": 50,
    "kategori": "Ana Yemek",
    "aktif": true
  }
]
```

### Masalar

```json
[
  {
    "id": 1,
    "durum": "dolu",
    "siparisler": []
  }
]
```

### Siparişler

```json
[
  {
    "masaNo": 3,
    "urun": "Kola",
    "adet": 2,
    "tutar": 100,
    "tarih": "2026-05-11"
  }
]
```

### Gün Sonu Verileri

```json
{
  "toplamKazanc": 5000,
  "toplamSiparis": 42
}
```

---

## Test Senaryoları

### Senaryo 1 — Ürün Ekleme

- Yeni ürün eklenir.
- localStorage içine kaydedildiği kontrol edilir.

### Senaryo 2 — Sipariş Oluşturma

- Masa seçilir.
- Menüden ürün eklenir.
- Sipariş listesinde görüntülendiği kontrol edilir.

### Senaryo 3 — Stok Azaltma

- Sipariş verildiğinde ürün stoğu azalmalıdır.

### Senaryo 4 — Stok Tükenmesi

- Stok 0 olduğunda:
  - ürün pasif hale gelmeli
  - “Ürün Tükendi” uyarısı verilmelidir.

### Senaryo 5 — Gün Sonu Raporu

- Toplam sipariş sayısı hesaplanmalıdır.
- Toplam kazanç doğru gösterilmelidir.

---

## Bilinen Eksikler

- Backend bağlantısı bulunmamaktadır.
- Veriler gerçek veritabanında tutulmamaktadır.
- Kullanıcı giriş sistemi eksiktir.
- Çoklu kullanıcı desteği yoktur.
- Sipariş geçmişi filtreleme sistemi geliştirilmelidir.
- Responsive yapı bazı ekranlarda tam optimize değildir.
- Gerçek ödeme sistemi entegrasyonu bulunmamaktadır.