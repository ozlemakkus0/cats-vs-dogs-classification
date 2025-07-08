# cats-vs-dogs-classification
A CNN and MobileNetV2-based image classifier for cats and dogs using TensorFlow and Keras.
# 🐱🐶 Cats vs Dogs – CNN ile Görüntü Sınıflandırma

Bu proje, derin öğrenme kullanarak köpek ve kedi resimlerini sınıflandıran bir Convolutional Neural Network (CNN) modelini içermektedir. Google Colab üzerinde TensorFlow ile geliştirilmiş ve model `.h5` formatında kaydedilmiştir.

---

## 📌 Proje Özeti

- **Veri Seti**: [TensorFlow Cats vs Dogs](https://www.tensorflow.org/datasets/catalog/cats_vs_dogs)
- **Model Tipi**: Convolutional Neural Network (CNN)
- **Kütüphaneler**: TensorFlow, Keras, NumPy, Matplotlib
- **Çıktı**: Kedi veya köpek olarak sınıflandırma (% olasılık ile)

---

## 🧠 Kullanılan Model Özellikleri

- 3 adet `Conv2D` + `MaxPooling2D` katmanı
- `Flatten` ve `Dense` katmanları
- `Dropout` ile overfitting önleme
- Son katman: `sigmoid` aktivasyonlu `Dense(1)` → Binary classification

---

## 📓 Notebook

Modelin eğitim süreci, görselleştirme ve test adımları bu notebook dosyasındadır:  
👉 [`cats_vs_dogs_cnn_colab_duzenlenmis.ipynb`](./cats_vs_dogs_cnn_colab_ (1).ipynb)

---

## 📦 Model Ağırlıkları (`.h5`)

Eğitim tamamlandıktan sonra model `.h5` formatında kaydedildi.  
İndirmek için tıklayın:

👉 [Google Drive'dan indir (.h5)](https://drive.google.com/file/d/10cjOSZLZxKthbBQ6cZFkSGRvsCzOAiqz/view?usp=drive_link)

> Not: Bu dosya büyük olduğu için GitHub yerine Google Drive üzerinden paylaşılmıştır.

---

## 🚀 Google Colab Üzerinde Kullanım

Google Colab'da `.h5` modelini şu şekilde yükleyebilirsin:

```python
from tensorflow.keras.models import load_model
from google.colab import drive

drive.mount('/content/drive')  # Google Drive'ı bağla

# Yol: modelin bulunduğu klasöre göre düzenle
model = load_model('/content/drive/MyDrive/kedi_kopek_modeli.h5')

# Artık model ile tahmin yapabilirsin
prediction = model.predict(...)
