# turkiye-konut-fiyat-tahmini
Real estate price prediction model in Turkey using Machine Learning and Scikit-Learn.
 1. Proje: Kaliforniya Konut Fiyatı Tahmin Modeli
Amaç: Klasik makine öğrenmesi temellerini atmak ve Scikit-Learn'ün yerleşik veri seti ile doğrusal regresyon mantığını kavramiak.

Kullanılan Kütüphaneler: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn.

Yapılan Adımlar:

fetch_california_housing veri seti projeye dahil edildi.

Sütun isimleri Türkçeleştirilerek verinin yapısı incelendi.

Veri, modelin eğitimi (%80) ve testi (%20) olmak üzere train_test_split ile bölündü.

Linear Regression algoritması ile model eğitildi.

MSE (Mean Squared Error) ve R2 Skoru metrikleri ile modelin başarısı ölçüldü ve grafiksel olarak görselleştirildi.

2. Proje: Gerçek Türkiye Emlak Fiyatı Tahmin Modeli
Amaç: Hazır veri setlerinin ötesine geçerek, gerçek Türkiye emlak piyasası verileriyle çalışmak ve kategorik verileri (il, ilçe, satıcı tipi vb.) işleyerek modele uygun hale getirmek.

Kullanılan Kütüphaneler: Pandas, Scikit-Learn.

Yapılan Adımlar:

Kaggle üzerinden gerçek bir Türkiye emlak veri seti (real-estate-prices-in-turkey-2025) API aracılığıyla çekildi.

Oda_Sayisi sütunundaki metinsel ifadeler ("3+1" vb.) temizlenerek sayısal Toplam_Oda sütununa dönüştürüldü.

il, Ilce ve satici_tip gibi kategorik metin sütunları One-Hot Encoding yöntemiyle (0-1 matrisine) sayısal formata çevrildi.

Model gerçek Türkiye verileriyle eğitildi ve R2 başarı skoru hesaplandı.

Kullanıcıdan anlık il, ilçe, metrekare ve oda sayısı alarak Türk Lirası (TL) cinsinden nokta atışı fiyat tahmini yapan interaktif bir tahmin paneli yazıldı.
