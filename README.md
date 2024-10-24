# Fish Classification Model 

## Proje Özeti
**Bu proje**, bir balık sınıflandırma modeli oluşturmak amacıyla bir derin öğrenme yaklaşımı kullanmaktadır. Model, çeşitli balık türlerinin görüntülerini kullanarak bu türleri sınıflandırmayı hedefler. Projede, görüntü işleme, veri seti hazırlığı, model eğitimi ve model değerlendirmesi gibi adımlar yer almaktadır.

## Kullanılan Kütüphaneler
- **Pandas**: Veri analizi ve manipülasyonu için.
- **NumPy**: Sayısal hesaplamalar için.
- **Matplotlib ve Seaborn**: Görselleştirme için.
- **Scikit-learn**: Veri setinin bölünmesi, etiket kodlama ve model değerlendirme için.
- **TensorFlow/Keras**: Derin öğrenme modelinin oluşturulması ve eğitimi için.
- **Scikit-optimize**: Hiperparametre optimizasyonu için.

## Veri Seti
**Veri seti**, farklı balık türlerine ait görüntülerden oluşmaktadır. Her balık türü, belirli etiketlerle tanımlanmıştır. Görüntüler, eğitim, doğrulama ve test setlerine ayrılmadan önce karıştırılmıştır. Görüntülerin boyutu 128x128 piksel olup, siyah-beyaz formatına dönüştürülmüştür.

## Adım Adım İşlemler

### 1. Veri Hazırlama
- **Dosya Yollarının Alınması**: Veri setindeki tüm görüntü dosyalarının yolları ve etiketleri alınarak bir DataFrame'e dönüştürülmüştür.
- **Etiket Filtreleme**: 'GT' ile biten etiketler hariç tutulmuştur.
- **Karıştırma**: DataFrame, rastgele karıştırılarak eğitim, doğrulama ve test setlerine bölünmüştür.

### 2. Görüntü İşleme
- **Öznitelik Çıkarımı**: Her görüntü, siyah-beyaz formatına dönüştürülüp yeniden boyutlandırılmış ve düzleştirilmiştir.
- **Normalizasyon**: Görüntü verileri [0, 1] aralığına normalleştirilmiştir.

### 3. Etiket Kodlama
- **Label Encoding**: Etiketler sayısal değerlere dönüştürülmüştür.
- **One-Hot Encoding**: Sınıflandırma işlemi için etiketler one-hot formatına çevrilmiştir.

### 4. Model Oluşturma
- **Model Mimarisinin Tasarımı**: Birden fazla katman içeren tam bağlı bir sinir ağı oluşturulmuştur. Dropout katmanları ile aşırı öğrenme önlenmeye çalışılmıştır.
- **Hiperparametre Ayarı**: Hiperparametre optimizasyonu için Bayes arama yöntemi kullanılarak en iyi ayarlar belirlenmiştir.

### 5. Model Eğitimi
- **Eğitim Süreci**: Model, eğitim ve doğrulama verileri üzerinde eğitilmiş, en iyi performansı gösteren model kaydedilmiştir.

### 6. Model Değerlendirmesi
- **Kayıp ve Doğruluk Grafikleri**: Eğitim süreci boyunca kayıp ve doğruluk grafiklerle görselleştirilmiştir.
- **Sınıflandırma Raporu**: Modelin performansı, precision, recall ve F1-score gibi metriklerle değerlendirilmiştir.
- **Confusion Matrix**: Gerçek ve tahmin edilen sınıflar arasındaki ilişkileri gösteren bir matris oluşturulmuştur.

## Sonuçlar
**Model**, doğrulama seti üzerinde yüksek doğruluk oranı elde etmiştir. Eğitim süreci boyunca kayıp değeri sürekli azalmış, doğruluk değeri ise artmıştır. 

## Kullanım
**Proje**, Kaggle üzerinde çalışmak üzere tasarlanmıştır. Kullanıcılar, gereken kütüphaneleri yükleyerek ve kodu çalıştırarak modelin eğitimini ve değerlendirilmesini gerçekleştirebilirler.

## Kaggle
-  https://www.kaggle.com/code/siladurtas/a-large-scale-fish-ann


