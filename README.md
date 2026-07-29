# E-Ticaret Veri Analizi Projesi

## Proje Hakkında
Bu proje, bir e-ticaret veri seti (`e_ticaret_veri_seti.csv`) üzerinde gerçekleştirilen temel veri ön işleme, veri temizleme, keşifsel veri analizi (EDA) ve görselleştirme adımlarını içeren bir Jupyter Notebook çalışmasıdır.

## Kullanılan Kütüphaneler
Projenin çalıştırılabilmesi için aşağıdaki Python kütüphanelerinin yüklü olması gerekmektedir:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

## Gerçekleştirilen İşlemler (Adım Adım)
1. **Veri Keşfi (Data Exploration):** Veri setinin boyutu, veri tipleri ve temel istatistiksel özetleri incelendi.
2. **Eksik Veri (Missing Data) Yönetimi:** 
   - Sayısal sütunlardaki eksiklikler medyan (ortanca) değeri ile dolduruldu.
   - Kategorik sütunlardaki eksiklikler mod (tepe değer) ile dolduruldu.
3. **Özellik Mühendisliği (Feature Engineering):** Sipariş tarihleri ayrıştırılarak yıl, ay, gün ve haftanın günü bilgileri çıkarıldı.
4. **Veri Temizleme:** 
   - Tekrar eden (duplicate) kayıtlar silindi.
   - Yazım farklılıkları barındıran 'sehir' ve 'kategori' sütunlarındaki metinler standartlaştırıldı.
   - Mantıksal olarak tutarsız olan hatalı kayıtlar (negatif fiyat vb.) tespit edilip temizlendi.
5. **Aykırı Değer (Outlier) Analizi:** Çeyrekler Açıklığı (IQR) yöntemi kullanılarak birim fiyatlarındaki aykırı değerler tespit edildi.
6. **Görselleştirme ve İstatistiksel Analiz:** Toplam tutar dağılımları histogram ve kutu grafikleri (box plot) ile, kategorik dağılımlar ise sütun grafikleriyle görselleştirildi.
