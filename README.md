# Akbank-dl-bootcamp-intel
CNN ve Transfer Learning kullanarak Intel Image Classification projesi

# Intel Image Classification – CNN & Transfer Learning

## Proje Amacı

Bu proje, **Intel Image Classification** veri seti üzerinde çok sınıflı (6 sınıf) görüntü sınıflandırması yapmayı amaçlamaktadır.  
Veri seti; *buildings*, *forest*, *glacier*, *mountain*, *sea* ve *street* olmak üzere altı farklı doğal ve yapay ortamdan oluşan yaklaşık **25.000 eğitim** ve **14.000 test** görüntüsü içerir.

Bu çalışma kapsamında:

- **Veri Hazırlığı ve Ön İşleme:** Görseller 0–1 aralığına normalize edilmiş, `ImageDataGenerator` ile **rotation, shift, zoom, horizontal flip** gibi veri çoğaltma (data augmentation) teknikleri uygulanmıştır. Böylece modelin genelleme yeteneği artırılmış ve overfitting riski azaltılmıştır.

- **CNN Tabanlı Modelleme:** Keras `Sequential` mimarisi ile 3 konvolüsyon bloğu (Conv2D → BatchNormalization → MaxPooling → Dropout) ve tam bağlantılı katmanlardan oluşan bir **temel CNN modeli** geliştirilmiş ve eğitilmiştir.

- **Transfer Learning:** Ek olarak, **VGG16** önceden eğitilmiş ağı kullanılarak transfer learning uygulanmış; temel CNN ile karşılaştırma yapılarak performans farkları gözlemlenmiştir.

- **Model Değerlendirme:** Accuracy/Loss grafikleri, `classification_report`, `confusion_matrix` ve ROC/AUC eğrileri ile model başarımı detaylı olarak incelenmiştir. Doğru ve yanlış sınıflandırılan örnekler görselleştirilmiştir.

- **Optimizasyon Denemeleri:** Adam, RMSprop ve SGD gibi farklı optimizer’lar kısa eğitimlerle test edilerek en iyi doğruluğu sağlayan optimizer belirlenmiştir.

Bu adımlar sonucunda temel CNN modeli test setinde yaklaşık **%87 doğruluk** elde etmiş, bootcamp kriterlerine uygun olarak Kaggle üzerinde paylaşılmış ve GitHub üzerinden belgelenmiştir.

## Veri Seti
- Kaynak: [Intel Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)
- 6 sınıf: Buildings, Forest, Glacier, Mountain, Sea, Street
- ~25.000 eğitim, ~14.000 test görüntüsü

## Yöntem
- CNN modeli (Conv2D + BatchNorm + Dropout)
- Transfer Learning (VGG16)
- Data Augmentation
- Optimizer karşılaştırması

## Sonuçlar
- Temel CNN doğruluk: 0.8713
- Transfer Learning doğruluk: 0.7814
- Confusion matrix ve diğer görseller için `/images` klasörüne bakınız.

## Kaggle Notebook
https://www.kaggle.com/code/hasanctn/akbank-dl-bootcamp-project-intel-image-classifica

