# House Price Prediction

Bu proje, konut fiyatlarını tahmin etmek için veri analizi, özellik mühendisliği ve makine öğrenmesi tekniklerini bir araya getirir. Kaggle House Prices: Advanced Regression Techniques yarışmasının veri seti kullanılmıştır.

## İçerik
- Veri temizleme ve eksik değer analizi
- Özellik mühendisliği (ordinal ve one-hot encoding)
- Korelasyon analizi ve görselleştirme
- XGBoost ile model eğitimi ve değerlendirme
- En önemli 20 feature ile alternatif model denemesi
- Tahmin sonuçlarının submission dosyası olarak kaydedilmesi

## Kullanılan Dosyalar
- `data/train.csv`: Eğitim verisi
- `data/test.csv`: Test verisi
- `data/sample_submission.csv`: Submission formatı
- `data/data_description.txt`: Veri seti açıklamaları
- `prediction.ipynb`: Tüm analiz ve modelleme adımlarını içeren Jupyter Notebook

## Adımlar

### 1. Veri Analizi ve Temizleme
- Eksik değerler incelendi ve uygun stratejilerle dolduruldu.
- Kategorik ve sayısal sütunlar için veri tipleri düzenlendi.
- Yüksek oranda eksik ve az bilgi içeren sütunlar veri setinden çıkarıldı.

### 2. Özellik Mühendisliği
- Ordinal değişkenler için sıralı mapping uygulandı.
- Nominal değişkenler için one-hot encoding ile yeni sütunlar oluşturuldu.
- Eğitim ve test setlerinde feature uyumu sağlandı.

### 3. Korelasyon Analizi
- SalePrice ile en yüksek korelasyona sahip özellikler belirlendi.
- Korelasyonlar heatmap ile görselleştirildi.

### 4. Model Eğitimi ve Değerlendirme
- XGBoost regressor ile temel model kuruldu.
- 5-fold cross-validation ile RMSE skorları hesaplandı.
- Feature importance grafiği ile en etkili özellikler incelendi.
- Sadece en önemli 20 feature ile alternatif model denemesi yapıldı.

### 5. Tahmin ve Submission
- Test seti için tahminler yapıldı.
- Sonuçlar `submission_xgb.csv` ve `submission_xgb_top20.csv` dosyalarına kaydedildi.

## Kullanılan Kütüphaneler
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

## Nasıl Kullanılır?
1. Gerekli kütüphaneleri yükleyin.
2. Notebook'u adım adım çalıştırarak veri analizi ve modelleme sürecini takip edin.
3. Tahmin dosyalarını Kaggle'a yükleyerek sonuçları değerlendirin.

## Notlar
- Notebook'ta hem tüm feature'lar hem de en önemli 20 feature ile model sonuçları karşılaştırılmıştır.
- Özellik mühendisliği ve eksik değer doldurma adımları, modelin başarısını artırmak için özenle uygulanmıştır.
- Proje, veri bilimi ve makine öğrenmesi alanında temel ve orta seviye teknikleri kapsamlı şekilde göstermektedir.

---

Her türlü öneri ve geri bildiriminiz için iletişime geçebilirsiniz.