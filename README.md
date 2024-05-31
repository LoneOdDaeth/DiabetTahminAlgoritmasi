# Diyabet Tahmin Programı

Bu proje, bir kullanıcının çeşitli sağlık ölçümleri ve kişisel bilgilerini kullanarak diyabet riskini tahmin etmek için bir SVM (Destek Vektör Makinesi) modelini kullanır. Ayrıca, tahmin sonuçlarını grafik ve karmaşıklık matrisi olarak görselleştirme yeteneği sağlar.

## Proje Katılımcıları

- [Göktuğ Gökçen](https://github.com/Gktg-Gokcen)
- [Alparslan Özuygur](https://github.com/AlparslanOzuygur)
- [Selim Oğuz Şahin](https://github.com/loneoddaeth)
- [Naci Karataş](https://github.com/nacikaratas)
- [Onurcan Aşar](https://github.com/onurcanx)

## Kullanılan Kütüphaneler

- `tkinter`: Grafik kullanıcı arayüzü (GUI) oluşturmak için.
- `sklearn`: Makine öğrenimi modelleri ve veri işleme için.
  - `StandardScaler`: Verilerin standartlaştırılması için.
  - `LinearRegression`: Lineer regresyon modeli eğitimi için.
  - `SVC`: Destek Vektör Makinesi modeli eğitimi için.
  - `train_test_split`: Verileri eğitim ve test setlerine ayırmak için.
  - `confusion_matrix`, `ConfusionMatrixDisplay`: Karmaşıklık matrisi oluşturmak için.
- `pandas`: Veri yükleme ve işleme için.
- `matplotlib`: Grafik oluşturma için.

## Veri Seti

Veri seti, aynı dizinde bulunan `diabetes.csv` dosyasından yüklenir. Bu veri seti, aşağıdaki özellikleri içerir:

- **Pregnancies**: Hastanın kaç defa hamile kaldığı.
- **Glucose**: Hastanın glikoz değerleri (2 saatlik süreçte).
- **Blood Pressure**: Kan basıncı değerleri (0 ile 122 arasında).
- **Skin Thickness**: Triceps cilt kıvrım kalınlığı (0 ile 99 arasında).
- **Insulin**: 2 saatlik serum insülini (0 ile 846 arasında).
- **Body Mass Index (BMI)**: Vücut kitle indeksi.
- **Diabetes Pedigree Function**: Diyabet soyağacı işlevi (0.078 ile 2.42 arasında).
- **Age**: Hastaların yaşı (21 ile 81 arasında).

## Proje Yapısı

### `train_model` Fonksiyonu

Veri setini yükler, verileri eğitim ve test setlerine böler, verileri standartlaştırır ve SVM modelini eğitir. Ayrıca, modelin doğruluk oranını hesaplar ve tahmin sonuçlarını döndürür.

### `grafik` Fonksiyonu

Tahmin edilen sonuçlar ve gerçek sonuçlar arasında bir grafik oluşturur.

### `matris` Fonksiyonu

Karmaşıklık matrisi oluşturur ve ekranda gösterir.

### `predict_diabetes` Fonksiyonu

Kullanıcının girdiği verilerle diyabet tahmini yapar ve sonucu ekranda gösterir.

### Grafik Kullanıcı Arayüzü (GUI)

Tkinter kütüphanesi kullanılarak bir GUI oluşturulur. Kullanıcı, çeşitli sağlık ölçümlerini girer ve "Diyabeti Tahmin Et" butonuna tıkladığında sonuç ekranda gösterilir.

## Kurulum ve Kullanım

1. Gerekli kütüphaneleri yükleyin:
   ```sh
   pip install pandas scikit-learn matplotlib tk
2. Proje dosyasını ve `diabetes.csv` veri setini aynı dizine yerleştirin.
3. Aşağıdaki Python kodunu çalıştırın:
   ```sh
   python main.py
4. GUI açıldığında, gerekli verileri girin ve "Diyabeti Tahmin Et" butonuna tıklayın. Grafik ve karmaşıklık matrisi oluşturmak için ilgili butonlara tıklayın.

## Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Ayrıntılar için `LICENSE` dosyasına bakınız.

## İletişim
Herhangi bir sorunuz veya geri bildiriminiz için yukarıda listelenen katılımcılara GitHub kullanıcı adları üzerinden ulaşabilirsiniz.



---

# Diabetes Prediction Program

This project uses an SVM (Support Vector Machine) model to predict the risk of diabetes based on a user's various health metrics and personal information. It also has the capability to visualize prediction results in graphs and confusion matrices.

## Project Contributors

- [Göktuğ Gökçen](https://github.com/Gktg-Gokcen)
- [Alparslan Özuygur](https://github.com/AlparslanOzuygur)
- [Selim Oğuz Şahin](https://github.com/loneoddaeth)
- [Naci Karataş](https://github.com/nacikaratas)
- [Onurcan Aşar](https://github.com/onurcanx)

## Libraries Used

- `tkinter`: For creating the graphical user interface (GUI).
- `sklearn`: For machine learning models and data processing.
  - `StandardScaler`: For standardizing the data.
  - `LinearRegression`: For training a linear regression model.
  - `SVC`: For training the Support Vector Machine model.
  - `train_test_split`: For splitting the data into training and testing sets.
  - `confusion_matrix`, `ConfusionMatrixDisplay`: For creating confusion matrices.
- `pandas`: For loading and processing data.
- `matplotlib`: For creating graphs.

## Dataset

The dataset is loaded from the `diabetes.csv` file located in the same directory. This dataset includes the following features:

- **Pregnancies**: Number of times the patient has been pregnant.
- **Glucose**: Glucose levels (2-hour serum glucose).
- **Blood Pressure**: Blood pressure levels (0 to 122).
- **Skin Thickness**: Triceps skin fold thickness (0 to 99).
- **Insulin**: 2-hour serum insulin (0 to 846).
- **Body Mass Index (BMI)**: Body mass index.
- **Diabetes Pedigree Function**: Diabetes pedigree function (0.078 to 2.42).
- **Age**: Age of the patients (21 to 81).

## Project Structure

### `train_model` Function

Loads the dataset, splits the data into training and testing sets, standardizes the data, and trains the SVM model. It also calculates the model's accuracy and returns the prediction results.

### `grafik` Function

Creates a graph between predicted results and actual results.

### `matris` Function

Creates and displays a confusion matrix.

### `predict_diabetes` Function

Predicts diabetes based on user input and displays the result on the screen.

### Graphical User Interface (GUI)

A GUI is created using the Tkinter library. The user enters various health metrics and clicks the "Predict Diabetes" button to display the result. Buttons for generating graphs and confusion matrices are also available.

## Installation and Usage

1. Install the required libraries:
   ```sh
   pip install pandas scikit-learn matplotlib tk
2. Place the project files and `diabetes.csv` dataset in the same directory.
3. Run the following Python code
    ```sh
    python main.py
4. When the GUI opens, enter the required data and click the "Predict Diabetes" button. Click the respective buttons to generate graphs and confusion matrices.

# License
This project is licensed under the MIT License. See the LICENSE file for details.

# Contact
For any questions or feedback, you can reach out to the contributors listed above via their GitHub usernames.
