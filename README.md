# Akciğer Segmentasyon Projesi

Bu proje, akciğer görüntülerinin segmentasyonu için geliştirilmiş bir makine öğrenmesi projesidir. Proje, akciğer CT taramalarından segmentasyon maskeleri oluşturmak ve bu maskeleri kullanarak modeller eğitmek amacıyla tasarlanmıştır.

## 🏗️ Proje Yapısı
├── Image Masking/
│ └── Segmentation.ipynb # Görüntü maskeleme ve segmentasyon işlemleri
├── Model Training/
│ ├── lung-test image/ # Test görüntüleri
│ │ ├── 1.jpeg
│ │ ├── 2.jpeg
│ │ ├── 3.jpeg
│ │ ├── 4.jpeg
│ │ ├── 5.jpeg
│ │ └── 6.jpeg
│ ├── No Segmentation.ipynb # Segmentasyon olmadan model eğitimi
│ ├── Segmentation.ipynb # Segmentasyon ile model eğitimi
│ └── splitting_lung_data.ipynb # Veri bölme işlemleri (train/validation/test)


## 🎯 Proje Amacı

Bu proje, tıbbi görüntü işleme alanında akciğer segmentasyonu yaparak:
- Akciğer CT görüntülerinden segmentasyon maskeleri oluşturma
- Bu maskeleri kullanarak derin öğrenme modelleri eğitme
- Segmentasyonlu ve segmentasyonsuz model performanslarını karşılaştırma

## 🚀 Kullanım

### 1. Veri Hazırlama
```python
# splitting_lung_data.ipynb dosyasını çalıştırarak veriyi bölün
# Veri %70 train, %20 validation, %10 test olarak ayrılır
```

### 2. Model Eğitimi
- **Segmentasyon ile**: `Model Training/Segmentation.ipynb`
- **Segmentasyon olmadan**: `Model Training/No Segmentation.ipynb`

### 3. Görüntü İşleme
- `Image Masking/Segmentation.ipynb` ile maskeleme işlemleri

## 📋 Gereksinimler

- Python 3.7+
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib
- TensorFlow/Keras
- splitfolders (veri bölme için)

## ⚙️ Kurulum

```bash
# Gerekli kütüphaneleri yükleyin
pip install jupyter opencv-python numpy matplotlib tensorflow splitfolders

# Jupyter Notebook'u başlatın
jupyter notebook
```

## �� Veri Yapısı

Proje, aşağıdaki veri yapısını kullanır:
- **ImageData**: Orijinal akciğer görüntüleri
- **Mask**: Segmentasyon maskeleri
- **lung_data_split**: Bölünmüş görüntü verileri
- **segmentation_lung_data_split**: Bölünmüş maske verileri

## �� Lisans Bitirme Projesi

Bu proje, lisans bitirme tezi kapsamında geliştirilmiştir.

## �� Notlar

- Notebook dosyaları büyük boyutludur, bu normal bir durumdur
- Test görüntüleri `lung-test image/` klasöründe bulunmaktadır
- Veri bölme işlemi otomatik olarak %70/%20/%10 oranında yapılmaktadır

## 🔧 Kullanım Adımları

1. **Veri Hazırlama**: `splitting_lung_data.ipynb` dosyasını çalıştırın
2. **Model Eğitimi**: İstediğiniz notebook'u seçin (segmentasyonlu/segmentasyonsuz)
3. **Test**: `Image Masking/Segmentation.ipynb` ile sonuçları test edin
