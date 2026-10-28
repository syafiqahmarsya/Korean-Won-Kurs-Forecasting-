# Evaluasi Kinerja Model Time Series untuk Prediksi Nilai Jual Kurs Korean Won (KRW) terhadap Rupiah

## 📌 Project Overview

Proyek ini bertujuan untuk mengevaluasi dan membandingkan kinerja beberapa model time series dalam memprediksi nilai jual mata uang Korean Won (KRW) terhadap Rupiah Indonesia (IDR) selama periode 2015–2025.

Penelitian ini membandingkan tujuh metode peramalan, yaitu Naive, Mean, Drift, Simple Moving Average (SMA), Simple Exponential Smoothing (SES), Holt’s Linear Trend, dan ARIMA. Evaluasi dilakukan untuk mengidentifikasi model dengan tingkat kesalahan prediksi terendah.

## 🎯 Objectives

- Menganalisis karakteristik data historis nilai jual kurs KRW terhadap IDR.
- Melakukan pengujian stasioneritas data sebelum pemodelan.
- Membangun dan membandingkan tujuh model peramalan time series.
- Mengevaluasi akurasi model menggunakan Mean Squared Error (MSE) dan Mean Absolute Percentage Error (MAPE).

## 📊 Dataset

- **Source:** [Bank Indonesia](https://www.bi.go.id)
- **Currency:** Korean Won (KRW) terhadap Indonesian Rupiah (IDR)
- **Period:** Januari 2015–Maret 2025
- **Total Observations:** 2.524 data harian
- **Data Split:** 70% training data dan 30% testing data

## 🛠️ Tools & Methods

**Tools**
- R Programming Language
- Time Series Analysis
- Data Visualization

**Methods**
1. Naive Forecast
2. Mean Forecast
3. Drift Forecast
4. Simple Moving Average (SMA)
5. Simple Exponential Smoothing (SES)
6. Holt’s Linear Trend
7. ARIMA (2,1,0)

**Data Preprocessing**
- Box-Cox transformation untuk menangani ketidakstasioneran varians.
- Augmented Dickey-Fuller (ADF) dan KPSS tests untuk menguji stasioneritas mean.
- Differencing untuk membantu mencapai stasioneritas mean.
- Analisis ACF dan PACF serta kriteria informasi untuk identifikasi model ARIMA.

## 📈 Model Evaluation

| Model | MSE | MAPE |
|---|---:|---:|
| Naive | 0.2563405 | 3.585991% |
| Mean | 0.4713629 | 3.585991% |
| Drift | 0.3829380 | 4.673684% |
| SMA (n = 2) | 0.1548265 | 2.555998% |
| SES | 0.2563496 | 3.586080% |
| Holt | 0.4430470 | 5.090098% |
| ARIMA (2,1,0) | 0.2407776 | 3.433613% |

## 🏆 Key Findings

Model **Simple Moving Average (SMA) dengan parameter n = 2** menghasilkan nilai MSE dan MAPE terendah di antara model yang dibandingkan.

- **MSE:** 0.1548265
- **MAPE:** 2.555998%

Hasil ini menunjukkan bahwa SMA (n = 2) memberikan akurasi prediksi terbaik berdasarkan kedua metrik evaluasi pada eksperimen ini.
