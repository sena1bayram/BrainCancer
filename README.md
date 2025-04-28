# 🧠 Brain Cancer MRI Classification

Bu proje, MRI görüntülerinden **beyin tümörü tiplerini** sınıflandırmak için sıfırdan oluşturulmuş bir **Convolutional Neural Network (CNN)** modeli geliştirmeyi amaçlamaktadır.

## 📚 Proje Özeti

- MRI taramalarını kullanarak **brain_glioma**, **brain_menin** ve **brain_tumor** sınıflarını ayırt etmek.
- Sıfırdan kurulan bir CNN mimarisi, **Batch Normalization**, **Data Augmentation** ve **Early Stopping** teknikleri kullanılarak optimize edilmiştir.
- Eğitim süreci ve başarı oranı grafiklerle ve confusion matrix ile desteklenmiştir.

## ⚙️ Kullanılan Teknolojiler

- Python
- TensorFlow / Keras
- Scikit-learn
- Matplotlib, Seaborn

## 🏗️ Model Mimarisi

- 4 adet Convolutional + MaxPooling bloğu
- Her Conv katmanından sonra **BatchNormalization**
- **Global Average Pooling** katmanı
- 128 nöronlu Dense + **Dropout (0.4)**
- 3 sınıflı Softmax çıkışı
- Optimizer: **Adam (learning rate = 0.0005)**

## 📈 Eğitim Özeti

- **Epoch:** 50
- **Early Stopping:** 8 patience
- **ReduceLROnPlateau:** Validation loss düştükçe learning rate azaltılır
- **Veri Artırımı:** Rotation, zoom, brightness değişimi ve yatay çevirme

## 🚀 Projeyi Çalıştırmak İçin

```bash
# Notebook'u çalıştır veya scripti çalıştır:
python train_model.py
