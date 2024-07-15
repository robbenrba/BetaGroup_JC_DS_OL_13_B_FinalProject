# finalProject
Final Project, JCDSOL-013(B), Roberto Benedict & Gretty Margaretha

### Context :
Bank marketing campaigns dataset analysis - Opening a Term Deposit dataset is a dataset describing a Portugal bank marketing campaigns results. Conducted campaigns were based mostly on direct phone calls, offering bank client to place a term deposit.

**Socio-economic conditions in the campaign period: May 2008 to June 2013**
- Post global financial crisis effects in Portugal
- Bank restructuring of Banco Montepio

Due to the nature of the conditions during the period, a potential client would also have lower interest in subscribing for term deposit, which in turn would make cost of outreach or promotion cost higher to accomodate the lower interest of the clients. 

If after all marketing efforts client had agreed to place deposit - target variable marked 'yes', otherwise 'no'

Target y (term): 

* 0 : no, disagree to place deposit
* 1 : yes, agree to place deposit

### Problem Statement :

The marketing process can consume significant time and resources if the bank targets all potential clients without prior filtering or targeted marketing, resulting in wasted time and resources. The effects are more dramatic in the post global financial crisis socio-economic conditions bringing about the crucial requirement of the bank to prioritize minimizing costs due to the higher reaching out cost for new clients in the economic climate. The bank wants to increase marketing efficiency by identifying which potential clients are likely to agree to open a term deposit account.

### Goals :
1. Identify client feature patterns for the most probable potential clients:
    * Most important features correlated with the target
    * Seasonality
    * Socio-economic conditions
2. Minimize revenue loss through promotion costs minimization : How much budget allocation percentage would be minimized ?

Based on these issues, the bank aims to predict the likelihood of a client agreeing to open a term deposit account. This can support the bank in executing marketing strategies focused on clients most likely to be interested, thereby saving costs, time, and resources.

Additionally, the bank wants to understand the factors influencing a client's decision to open a term deposit account or not, enabling them to develop better plans for approaching potential clients.

## Analytic Approach
Analisis data customer akan dilakukan untuk menemukan pola tertentu yang dapat membedakan customer yang berpotensi akan churn atau tidak. Tahap selanjutnya, model klasifikasi akan dibuat untuk membantu perusahaan agar dapat melakukan prediksi kemungkinan seorang customer akan melakukan churn atau tidak.

### Goals :
1. Identify client feature patterns for the most probable potential clients:
    * Most important features correlated with the target
    * Seasonality
    * Socio-economic conditions
2. Minimize revenue loss through promotion costs minimization : How much budget allocation percentage would be minimized ?

Based on these issues, the bank aims to predict the likelihood of a client agreeing to open a term deposit account. This can support the bank in executing marketing strategies focused on clients most likely to be interested, thereby saving costs, time, and resources.

Additionally, the bank wants to understand the factors influencing a client's decision to open a term deposit account or not, enabling them to develop better plans for approaching potential clients.

### Stakeholder :
* Bank marketing division : as main the stakeholder and the user of the resulting model, marketing division will minimize promotion cost by minimizing revenue loss through lower promotion cost due to more targeted marketing.

## Machine Learning Workflow
Below is the description of the program workflow in the IPYNB file.
1. Data Cleaning
2. Data Analysis
3. Data Preparation
4. Modeling and Evaluation
5. Drawing conclusions from the insights obtained.

## Kesimpulan
Berdasarkan hasil classification report dari model, dapat disimpulkan jika model digunakan untuk prediksi list customer yang akan churn, maka model ini dapat mengurangi 93% customer yang berpotensi loyal atau tidak churn untuk tidak perusahaan fokuskan dalam alokasi biaya promosi atau bahkan bisa ditiadakan, dan model ini mendapatkan 78% customer yang churn dari seluruh customer churn berdasarkan recall.

Model ini memiliki presisi prediksi customer yang churn sebesar 70%. Hal ini berarti setiap kali model memprediksi bahwa seorang customer akan churn, kemungkinan tebakannya benar itu sebesar kurang lebih 70%. Oleh karena itu, masih ada False Positive atau akan ada customer yang sebenarnya tidak churn tetapi diprediksi model sebagai customer yang churn sebanyak 7% dari keseluruhan customer yang tidak churn berdasarkan recall.

Bila diandaikan biaya promosi per customer itu 50 USD dan jumlah customer dalam suatu kurun waktu sebanyak 200 orang di mana 100 orang churn, maka dalam kasus bisnis bisa dihitung sebagai berikut :

Tanpa Model (semua customer dianggap potensi churn dan ditawarkan promosi) :
- Total Biaya promosi = 200 x 50 USD = 10,000 USD
- Biaya yang terbuang = 100 x 50 USD = 5,000 USD
- Jumlah penghematan = 0 USD

Dengan Model (hanya customer yang diprediksi oleh model churn yang kita check dan tawarkan) :
- Total Biaya promosi = (78 x 50 USD) + (7 x 50 USD) = 3050 USD + 760 USD = 4,250 USD
- Biaya yang terbuang = (100-(78+7)) x 50 USD = 750 USD 
- Jumlah penghematan = 10,000 - 4,250 = 5,750 USD

Berdasarkan contoh hitungan sederhana tersebut, terlihat bahwa dengan menggunakan model klasifikasi dan memprediksi berapa banyak porsi customer yang kemungkina churn, maka perusahaan tersebut dapat menghemat biaya yang cukup besar tanpa mengorbankan terlalu banyak customer yang churn.


## Rekomendasi
Hal-hal yang bisa dilakukan untuk developer untuk mengembangkan proyek dan modelnya :
1. Membuat kebijakan dan sistem penjagaan input yang mendorong setiap kandidat untuk mengisi semua data yang diperlukan.
2. Memberi opsi input untuk yang memang tidak ada atau nol.
3. Menambahkan fitur baru yang kemungkinan bisa berhubungan dengan churn, seperti informasi yang terkait dengan pembayaran order dan deskripsi lain customer.
4. Mencoba algoritma ML lain dan melakukan hyperparameter tuning yang lebih advanced.
5. Mencoba grid search untuk metode fill pada cleaning.
6. Menganalisa data yang model masih salah tebak untuk mengetahui karakteristik data tersebut, yang pada akhirnya akan dialurkan untuk menambah fitur atau feature engineering lagi.

Rekomendasi terhadap stakeholder atau perusahaan :
1. Memperbanyak survey demi pengumpulan data yang lebih banyak secara volume maupun lebih beragam.
2. Menawarkan promosi atau strategi lain yang menawarkan sebuah insentif pada customer atau pelanggan agar tertarik dan tidak churn.
3. Berdasar feature importance, cashback dapat ditingkatkan untuk customer yang berpotensi untuk churn.
4. Customer yang memiliki tujuan pengiriman jauh dapat diberi promo agar dapat mengurangi churn akibat alasan terkait seperti biaya delivery mahal ataupun lamanya delivery.
5. Berdasarkan Tenure, perusahaan dapat mengadakan strategi marketing yang mendorong insentif untuk orang yang baru-baru memesan.

<br/>
Copyright &copy; 2024, Roberto Benedict & Gretty Margaretha.
