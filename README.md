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
| Aries Fitriawan | Startup Campus, AI Track | nic.dominic@icloud.com | [link](https://linkedin.com/in/ariesfitriawan) | Supervisor |

## Setup
### Prerequisite Packages (Dependencies)
- pandas==2.1.0
- openai==0.28.0
- google-cloud-aiplatform==1.34.0
- google-cloud-bigquery==3.12.0
- ...
- ...

### Environment
| | |
| --- | --- |
| CPU | Example: Apple M3 Pro 12-core CPU |
| GPU | Example: Nvidia A100 (x1) |
| ROM | Example: 1 TB SSD |
| RAM | Example: 36 GB |
| OS | Example: macOS Sonoma v14.1.1 |

## Dataset
Describe your dataset information here. Provide a screenshot for some of your dataset samples (for example, if you're using CIFAR10 dataset, then show an image for each class).
- Link: https://...

## Results
### Model Performance
Describe all results found in your final project experiments, including hyperparameters tuning and architecture modification performances. Put it into table format. Please show pictures (of model accuracy, loss, etc.) for more clarity.

#### 1. Metrics
Inform your model validation performances, as follows:
- For classification tasks, use **Precision and Recall**.
- For object detection tasks, use **Precision and Recall**. Additionaly, you may also use **Intersection over Union (IoU)**.
- For image retrieval tasks, use **Precision and Recall**.
- For optical character recognition (OCR) tasks, use **Word Error Rate (WER) and Character Error Rate (CER)**.
- For adversarial-based generative tasks, use **Peak Signal-to-Noise Ratio (PNSR)**. Additionally, for specific GAN tasks,
  - For single-image super resolution (SISR) tasks, use **Structural Similarity Index Measure (SSIM)**.
  - For conditional image-to-image translation tasks (e.g., Pix2Pix), use **Inception Score**.

Feel free to adjust the columns in the table below.

| model | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall | ... |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| vit_b_16 | 1000 |  0.0001 | 32 | Adam | 0.093 | 88.34% | 84.15% | ... |
| vit_l_32 | 2500 | 0.00001 | 128 | SGD | 0.041 | 90.19% | 87.55% | ... |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | 

#### 2. Ablation Study
Any improvements or modifications of your base model, should be summarized in this table. Feel free to adjust the columns in the table below.

| model | layer_A | layer_B | layer_C | ... | top1_acc | top5_acc |
| --- | --- | --- | --- | --- | --- | --- |
| vit_b_16 | Conv(3x3, 64) x2 | Conv(3x3, 512) x3 | Conv(1x1, 2048) x3 | ... | 77.43% | 80.08% |
| vit_b_16 | Conv(3x3, 32) x3 | Conv(3x3, 128) x3 | Conv(1x1, 1028) x2 | ... | 72.11% | 76.84% |
| ... | ... | ... | ... | ... | ... | ... |

#### 3. Training/Validation Curve
Insert an image regarding your training and evaluation performances (especially their losses). The aim is to assess whether your model is fit, overfit, or underfit.
 
### Testing
Show some implementations (demos) of this model. Show **at least 10 images** of how your model performs on the testing data.

### Deployment (Optional)
Describe and show how you deploy this project (e.g., using Streamlit or Flask), if any.

## Supporting Documents
### Presentation Deck
- Link: https://...

### Business Model Canvas
Provide a screenshot of your Business Model Canvas (BMC). Give some explanations, if necessary.

### Short Video
Provide a link to your short video, that should includes the project background and how it works.
- Link: https://...

## References
Provide all links that support this final project, i.e., papers, GitHub repositories, websites, etc.
- Link: https://...
- Link: https://...
- Link: https://...

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
This project entitled <b>"YOUR PROJECT TITLE HERE"</b> is supported and funded by Startup Campus Indonesia and Indonesian Ministry of Education and Culture through the "**Kampus Merdeka: Magang dan Studi Independen Bersertifikasi (MSIB)**" program.
