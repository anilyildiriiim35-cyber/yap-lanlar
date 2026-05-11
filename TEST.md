# TESTS.md

# Manuel Test Senaryoları

---

## Test 1 - Ürün Ekleme

Önkoşul:
- Ürün yönetimi sayfası açık.

Adımlar:
1. Ürün adı alanına "Adana Kebap" yaz.
2. Fiyat alanına "250" gir.
3. Kategori olarak "Ana Yemek" seç.
4. Stok alanına "50" gir.
5. Ekle butonuna bas.

Beklenen Sonuç:
- Ürün listeye eklenir.
- localStorage içine kaydedilir.
- Sayfa yenilendiğinde ürün kaybolmaz.

---

## Test 2 - Ürün Silme

Önkoşul:
- Sistemde kayıtlı en az 1 ürün bulunmalı.

Adımlar:
1. Ürün yönetimi sayfasını aç.
2. Bir ürünün sil butonuna tıkla.

Beklenen Sonuç:
- Ürün listeden kaldırılır.
- localStorage verilerinden silinir.
- Sayfa yenilendiğinde tekrar görünmez.

---

## Test 3 - Boş Ürün Adı Validasyonu

Önkoşul:
- Ürün yönetimi sayfası açık.

Adımlar:
1. Ürün adı alanını boş bırak.
2. Fiyat gir.
3. Kategori seç.
4. Ekle butonuna bas.

Beklenen Sonuç:
- Ürün eklenmez.
- Kullanıcıya hata mesajı gösterilir.

---

## Test 4 - Negatif Fiyat Validasyonu

Önkoşul:
- Ürün yönetimi sayfası açık.

Adımlar:
1. Ürün adı gir.
2. Fiyat alanına "-100" yaz.
3. Kategori seç.
4. Ekle butonuna bas.

Beklenen Sonuç:
- Ürün eklenmez.
- Negatif fiyat kabul edilmez.
- Uyarı mesajı gösterilir.

---

## Test 5 - Kategori Ekleme

Önkoşul:
- Kategori yönetimi alanı açık.

Adımlar:
1. Yeni kategori alanına "Tatlılar" yaz.
2. Ekle butonuna bas.

Beklenen Sonuç:
- Yeni kategori listeye eklenir.
- Ürün ekleme ekranında görünür.
- Sayfa yenilendiğinde kaybolmaz.

---

## Test 6 - Menüde Ürün Listeleme

Önkoşul:
- Sistemde kayıtlı ürün bulunmalı.

Adımlar:
1. Menü sayfasını aç.

Beklenen Sonuç:
- Tüm aktif ürünler listelenir.
- Ürün adı, fiyat ve kategori bilgileri görünür.

---

## Test 7 - Menüde Arama

Önkoşul:
- Sistemde kayıtlı ürün bulunmalı.

Adımlar:
1. Menü sayfasındaki arama kutusuna "Kola" yaz.

Beklenen Sonuç:
- Sadece "Kola" içeren ürünler listelenir.
- Diğer ürünler gizlenir.

---

## Test 8 - Masa Seçimi

Önkoşul:
- Masa ekranı açık.

Adımlar:
1. Herhangi bir masa kartına tıkla.

Beklenen Sonuç:
- Seçilen masa aktif görünür.
- Sipariş paneli açılır.

---

## Test 9 - Siparişe Ürün Ekleme

Önkoşul:
- Bir masa seçilmiş olmalı.

Adımlar:
1. Menüden bir ürün seç.
2. Ürün ekle butonuna bas.

Beklenen Sonuç:
- Ürün sipariş listesine eklenir.
- Toplam tutar güncellenir.

---

## Test 10 - Siparişte Adet Artırma

Önkoşul:
- Sipariş listesinde ürün bulunmalı.

Adımlar:
1. Siparişte bulunan ürünün "+" butonuna bas.

Beklenen Sonuç:
- Ürün adedi 1 artar.
- Toplam fiyat güncellenir.

---

## Test 11 - Siparişten Ürün Silme

Önkoşul:
- Sipariş listesinde ürün bulunmalı.

Adımlar:
1. Siparişte bulunan ürünün sil butonuna bas.

Beklenen Sonuç:
- Ürün sipariş listesinden kaldırılır.
- Toplam tutar güncellenir.

---

## Test 12 - Toplam Tutar Hesaplama

Önkoşul:
- Sipariş listesinde birden fazla ürün bulunmalı.

Adımlar:
1. Farklı fiyatlarda ürünler ekle.
2. Sipariş panelini kontrol et.

Beklenen Sonuç:
- Toplam tutar doğru hesaplanır.
- Adet değiştikçe toplam güncellenir.

---

## Test 13 - Ödeme Alma

Önkoşul:
- Masada aktif sipariş bulunmalı.

Adımlar:
1. Ödeme al butonuna bas.

Beklenen Sonuç:
- Sipariş tamamlanır.
- Gün sonu raporuna satış eklenir.
- Masa durumu güncellenir.

---

## Test 14 - Ödeme Sonrası Masa Boşaltma

Önkoşul:
- Ödeme işlemi tamamlanmış olmalı.

Adımlar:
1. Ödeme sonrası masa durumunu kontrol et.

Beklenen Sonuç:
- Masa tekrar boş görünür.
- Yeni sipariş alınabilir.

---

## Test 15 - Gün Sonu Raporu

Önkoşul:
- Sistemde tamamlanmış sipariş bulunmalı.

Adımlar:
1. Gün sonu raporu sayfasını aç.

Beklenen Sonuç:
- Toplam sipariş sayısı görüntülenir.
- Toplam kazanç doğru hesaplanır.
- Satış verileri listelenir.

---

## Test 16 - Sayfa Yenileme Sonrası Veri Kalıcılığı

Önkoşul:
- Sistemde ürün ve sipariş verisi bulunmalı.

Adımlar:
1. Sayfayı yenile.
2. Ürünleri ve siparişleri kontrol et.

Beklenen Sonuç:
- localStorage verileri korunur.
- Ürünler ve siparişler kaybolmaz.

---

## Test 17 - Stok Azaltma Kontrolü

Önkoşul:
- Ürünün stok miktarı tanımlanmış olmalı.

Adımlar:
1. Bir ürün sipariş et.
2. Ürün yönetimi ekranına dön.

Beklenen Sonuç:
- Ürün stoğu sipariş kadar azalır.

---

## Test 18 - Stok Tükenme Kontrolü

Önkoşul:
- Stoğu düşük bir ürün bulunmalı.

Adımlar:
1. Ürünün tüm stoklarını sipariş ile tüket.

Beklenen Sonuç:
- Ürün pasif hale gelir.
- Menüde "Ürün Tükendi" mesajı görünür.
- Yeni siparişe eklenemez.

---

## Test 19 - Aynı Ürünü Tekrar Ekleme

Önkoşul:
- Sipariş ekranı açık.

Adımlar:
1. Aynı ürünü art arda ekle.

Beklenen Sonuç:
- Ürün tekrar satır açmak yerine adet artırır.
- Toplam tutar doğru hesaplanır.

---

## Test 20 - Boş Siparişte Ödeme Alma Engeli

Önkoşul:
- Seçili masada sipariş bulunmamalı.

Adımlar:
1. Ödeme al butonuna bas.

Beklenen Sonuç:
- Ödeme işlemi gerçekleşmez.
- Kullanıcıya uyarı mesajı gösterilir.