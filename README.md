# Agrisense: Plant Health Monitoring Application based on Multiclass Image Classification to Detect and Diagnose Diseases in Food Plants

## Project Description
Project kami bertujuan untuk mengembangkan aplikasi Plant Health Monitoring yang berfokus pada deteksi dan diagnosis penyakit pada tanaman timun, tomat, dan kentang. Pemilihan ketiga jenis tanaman ini didasarkan pada konsumsi yang tinggi di masyarakat, serta adanya masalah serius dalam pasokan dan produksi, yang dapat memberikan dampak signifikan terhadap keberlanjutan pertanian dan pangan di Indonesia.

Pertama, tanaman timun dipilih karena konsumsi mentimun di Indonesia terus meningkat setiap tahunnya, mencapai 2,10 kg per kapita pada tahun 2019. Dengan pertumbuhan konsumsi yang signifikan, perlunya pemantauan kesehatan tanaman timun menjadi sangat penting untuk menjaga ketersediaan dan kualitas pasokan.

Kedua, tanaman tomat dipilih karena konsumsi tomat per kapita mencapai 3,57 kg per tahun, sementara pasokan tomat tidak mencukupi permintaan yang ada. Dengan demikian, peningkatan produksi tomat yang sehat menjadi krusial untuk mengatasi kesenjangan antara permintaan dan pasokan, sehingga aplikasi ini dapat memberikan kontribusi positif dalam memenuhi kebutuhan konsumen.

Ketiga, tanaman kentang dipilih karena konsumsi kentang nasional per kapita meningkat dari 2282 kg pada tahun 2018 menjadi 2547 kg pada tahun 2019. Pertumbuhan konsumsi yang signifikan ini menunjukkan pentingnya meningkatkan produktivitas dan kesehatan tanaman kentang untuk memenuhi kebutuhan pangan yang terus bertambah.

Alasan utama di balik pengembangan aplikasi Plant Health Monitoring adalah untuk mengatasi masalah yang dihadapi oleh para petani dan ibu rumah tangga, yaitu serangan hama dan penyakit yang dapat mengakibatkan penurunan produksi tanaman. Dengan adanya pemantauan kesehatan tanaman yang canggih, diharapkan dapat meningkatkan hasil pertanian, mengurangi kerugian akibat penyakit tanaman, dan pada gilirannya, mendukung ketahanan pangan nasional. Oleh karena itu, penelitian ini memiliki relevansi yang tinggi dalam konteks pertanian modern yang berkelanjutan dan berkontribusi pada upaya memenuhi kebutuhan pangan yang terus berkembang di masyarakat.

## Contributor
| Full Name | Affiliation | Email | LinkedIn | Role |
| --- | --- | --- | --- | --- |
| Jessica Adelina Prameswari | Universitas Negeri Semarang | jessicadelina1709@gmail.com | [link](https://linkedin.com/in/jessica-adelina17) | Team Lead |
| Ria Novita Awalia Ramadhani | Institut Teknologi Telkom Purwokerto | rianovitaar@gmail.com | [link](https://linkedin.com/in/rianovitaar) | Team Member |
| Rakhimatulfitria Mekacahyani | Universitas Islam Sultan Agung | cahyani.pipit@gmail.com | [link](https://linkedin.com/in/rakhimatulfitria-mekacahyani-6b95b1291) |Team Member |
| Muhammad Rama Diennova Sulistyo | Universitas Sebelas Maret | RamaSulistyo@gmail.com | [link](https://linkedin.com/in/muhammad-rama-diennova-sulistyo-75b291284) | Team Member |
| Muhammad Rizky Pradhitia | Universitas Telkom | rizkypradhitia1@gmail.com | [link](https://linkedin.com/in/rizkypradhitia) | Team Member |
| Jonathan Lexi Febrian Sitohang | Universitas Sumatera Utara | jonathanlexi02@gmail.com | [link](https://linkedin.com/in/jonathanlexi) | Team Member |
| Aries Fitriawan | Startup Campus, AI Track | aries.f1991@gmail.com | [link](https://linkedin.com/in/ariesfitriawan) | Supervisor |

## Setup
### Prerequisite Packages (Dependencies)

- pandas>=1.1.4
- seaborn>=0.11.0
- python==3.9.13
- torch>=1.7.0
- torchvision>=0.8.1
- streamlit==1.29.0
- matplotlib>=3.2.2
- numpy>=1.18.5
- Pillow>=7.1.2
- PyYAML>=5.3.1
- requests>=2.23.0


### Environment
| | |
| --- | --- |
| CPU | Intel Xeon |
| GPU | Nvidia T4  |
| RAM | 51 GB |
| OS | Linux #1 SMP |

## Dataset
![Dataset](https://github.com/rianovitaa/Final-Project/assets/137513035/840f5980-b384-459d-9c37-cc0b7c7669ed)

- Link: https://drive.google.com/drive/folders/1xAsB9GOHfEk3KmAGTDCOIAWyojzmD3yD?usp=sharing

Dalam penelitian ini, dataset yang digunakan merupakan kumpulan foto daun dari tanaman timun, tomat, dan kentang, dengan sumber data berasal dari platform Kaggle. Dataset ini terdiri dari total 4000 foto yang terbagi dalam 8 kelas, masing-masing kelas memiliki 500 data foto. Kelas-kelas ini mencakup kondisi sehat dan tidak sehat pada tanaman timun, tomat, dan kentang, seperti unhealthy cucumber, healthy cucumber, healthy potato, early blight potato, late blight potato, healthy tomato, early blight tomato, dan late blight tomato.

Selanjutnya, dataset ini menjalani proses augmentasi menggunakan transformasi PyTorch, yang melibatkan pengubahan ukuran (resize) gambar menjadi 224x224 piksel, serta penerapan horizontal flip, vertical flip, random rotation, dan color jilter. Langkah ini dimaksudkan untuk memperkaya variasi data dan meningkatkan keberagaman pola yang dapat dikenali oleh model.

Proses pelatihan model dilakukan dengan menggunakan data yang telah di-augmentasi, dengan fokus pada kemampuan model untuk mengenali gambar dari berbagai arah dan kondisi cahaya, termasuk dalam situasi pencahayaan yang kurang. Model ini dilatih menggunakan data sebanyak 2400 gambar untuk training, sementara 480 gambar digunakan sebagai data testing dan 480 gambar lainnya sebagai data validation.

Hasil dari pengembangan ini diharapkan dapat menghasilkan model yang dapat secara efektif mengenali dan membedakan kondisi kesehatan tanaman timun, tomat, dan kentang. Dengan adanya augmentasi data, pelatihan model diharapkan dapat lebih tangguh dan adaptif terhadap variasi kondisi di lapangan, yang pada gilirannya dapat mendukung keberhasilan aplikasi Plant Health Monitoring dalam deteksi dan diagnosis penyakit tanaman.

## Results
### Model Performance

#### 1. Metrics
1. Presisi (Precision):
- Presisi tinggi menunjukkan bahwa model memiliki sedikit positif palsu.
Dalam hal ini:
- Presisi tertinggi: Cucumber_healty (0.99)
- Presisi terendah: Potato_early_blight (0.90)
2. Recall :
- Recall adalah rasio dari prediksi positif yang benar terhadap semua observasi pada kelas sebenarnya.
- Recall tinggi menunjukkan bahwa model memiliki sedikit negatif palsu.
Dalam hal ini:
- Recall tertinggi: Potato_early_blight (0.99)
- Recall terendah: Tomato_healthy (0.94)
3. F1-Score:

- F1-Score adalah rata-rata tertimbang dari presisi dan recall. Rentangnya dari 0 hingga 1, di mana 1 adalah F1-Score terbaik.
- Ini adalah metrik yang berguna ketika distribusi kelas tidak seimbang.
Dalam hal ini:

- F1-Score tertinggi: Cucumber_healty (0.99)
- F1-Score terendah: Potato_early_blight (0.94)
4. Support:

- Support adalah jumlah kejadian aktual dari kelas tertentu dalam dataset yang ditentukan.
5. Akurasi:

- Akurasi adalah rasio dari prediksi yang benar terhadap total observasi.
- Dalam hal ini, akurasi keseluruhan adalah 98%, menunjukkan bahwa model berkinerja baik pada dataset tersebut.

- Nilai rata-rata makro dan rata-rata berbobot keduanya sekitar 0.98, menunjukkan kinerja keseluruhan yang baik.
Secara keseluruhan, model ini tampaknya berperforma baik di berbagai kelas dengan presisi, recall, dan F1-score yang tinggi. Namun, penting untuk mempertimbangkan kebutuhan dan tujuan klasifikasi yang spesifik.
Feel free to adjust the columns in the table below.

| Model | epoch| learning_rate | Batch_size | optimizer | accuracy |
| EfficientNet | 100 | 0.0001 | | Adam | 97.73% |
| AlexNet | 100 | 0.0001 | | Adam | 87% |
| MobileNet | 100 | 0.0001 | | Adam | 65% |

#### 2. Ablation Study
Berikut arsitektur modfikasi model efficientNet pytorch : 
![Beige Colorful Minimal Flowchart Infographic Graph](https://github.com/rianovitaa/Final-Project/assets/85721522/85969263-2e97-439b-b6e6-c71678951627)

#### 3. Training/Validation Curve
Berdasarkan hasil grafik tersebut , model dapat tidak mengalami underfitting dan overfitting

![trainind and test result ](https://github.com/rianovitaa/Final-Project/assets/85721522/afddcb03-b1f9-4fb3-8b2c-370dc25a61b8)

### Testing
Berikut hasil gambar yang dapat diprediksi setelah model dilakukan pelatihan . 

![testing](https://github.com/rianovitaa/Final-Project/assets/85721522/b93d1c65-7b73-40c2-9b62-83f4655f3ae4)

## Supporting Documents
### Presentation Deck
- Link: https://drive.google.com/drive/folders/1EvTocHpmoD9gduT7jAykK9x-3tiGFG2y?usp=sharing

### Business Model Canvas
![Business Model Canvas](https://github.com/rianovitaa/Final-Project/assets/137513035/2ff02d4f-4f7d-4cf7-851b-0b1e44daafb9)


### Short Video
- Link: https://drive.google.com/drive/folders/1TTxJ99AEY8OVT8bcg0JsUmZoG1TErQw3?usp=drive_link

## References
- Link: https://iopscience.iop.org/article/10.1088/1742-6596/1693/1/012148/pdf
- Link: https://www.mdpi.com/2079-9292/10/12/1388
- Link: https://ieeexplore.ieee.org/document/8258820
- Link: https://arxiv.org/abs/1905.11946
- Link: https://catalog.ngc.nvidia.com/orgs/nvidia/models/efficientnet_b0_pyt_amp
- Link: https://pytorch.org/vision/stable/transforms.html
- Link: https://www.kaggle.com/datasets/kareem3egm/cucumber-plant-diseases-dataset
- Link: https://www.kaggle.com/datasets/farahseifeld/greenhouse-cucumber-growth-stages?select=Unhealthy+Leaves
- Link: https://www.kaggle.com/datasets/raiaone/olid-i?select=cucumber__K
- Link: https://www.kaggle.com/datasets/alinedobrovsky/plant-disease-classification-merged-dataset?select=Cucumber__diseased

## Additional Comments
Provide your team's additional comments or final remarks for this project. For example,
1. ...
2. ...
3. ...

## How to Cite
If you find this project useful, we'd grateful if you cite this repository:
```
@article{
...
}
```

## License
For academic and non-commercial use only.

## Acknowledgement
This project entitled <b>"Agrisense: Plant Health Monitoring Application based on Multiclass Image Classification to Detect and Diagnose Diseases in Food Plants"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
