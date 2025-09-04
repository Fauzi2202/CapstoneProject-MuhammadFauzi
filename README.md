# CapstoneProject-MuhammadFauzi
Capstone Project untuk program Hacktiv8 x IBM Student Developer Initiative. Proyek ini melakukan analisis sentimen komentar YouTube dengan bantuan IBM Granite LLM melalui Replicate API. Hasil analisis mengklasifikasikan komentar menjadi Positif, Negatif, dan Netral.

# 🎓 Capstone Project: Analisis Sentimen Komentar YouTube dengan IBM Granite

## 📌 Project Overview
Proyek ini bertujuan untuk menganalisis sentimen komentar pengguna pada video YouTube dengan bantuan **AI (IBM Granite via Replicate API)**.  
Dengan analisis ini, diperoleh wawasan mengenai bagaimana audiens merespons konten, pola komentar, serta rekomendasi untuk topik yang ada pada video.

## 🎯 Objectives
- Mengklasifikasikan komentar ke dalam kategori **Positif, Negatif, dan Netral**.  
- Merangkum komentar secara otomatis menggunakan IBM Granite.  
- Menyajikan visualisasi distribusi sentimen dan kata dominan.  
- Memberikan insight dan rekomendasi berdasarkan hasil analisis.  

## 📂 Dataset
- **Sumber Data**: Komentar publik dari YouTube (menggunakan YouTube Data API v3).  
- **Format**: CSV hasil scraping.  
- [📥 Link Dataset](https://docs.google.com/spreadsheets/d/1InwLGW_5STHxXLpmn4VV8_vFNLhTaFkDr7JMbim_ZVQ/edit?usp=sharing)

## 🛠️ Tools & Libraries
- **IBM Granite (Replicate API)** → klasifikasi sentimen dengan LLM.  
- **LangChain Community** → integrasi pipeline ke model.  
- **YouTube Data API** → scraping komentar YouTube.  
- **Python libraries**:  
  - `pandas` → manipulasi data  
  - `matplotlib` → visualisasi pie chart & bar chart  
  - `tqdm` → progress bar saat scraping/analisis  
  - `dotenv` → manajemen API Key  
 
  ## 🔎 Analysis Process
1. **Setup & Authentication**  
   - API Key YouTube & Replicate disimpan sebagai secret di Colab.  
   - Model default: `ibm-granite/granite-3.3-8b-instruct`.  

2. **Data Collection**  
   - Scraping komentar dari video YouTube berdasarkan `video_id`.  

3. **Preprocessing**  
   - Normalisasi teks, hilangkan duplikat.  

4. **Sentiment Analysis**  
   - Klasifikasi komentar ke **Positif, Negatif, Netral**.  
   - Prompt ketat agar tidak terlalu sering menghasilkan *Netral*.  
   - Rule-based correction: deteksi kata kunci positif/negatif untuk menghindari salah klasifikasi.  

5. **Visualization**  
   - Pie Chart → distribusi persentase sentimen.  
   - Bar Chart → jumlah komentar per kategori sentimen.
  
6. **Summarization**
   - Menggunakan IBM Granite untuk merangkum komentar secara keseluruhan
7. **Export**  
   - Semua hasil analisis disimpan ke **`hasil_sentimen.csv`**.

     ## 📊 Results
### Distribusi Sentimen
- POSITIF: 20.8%  
- NEGATIF: 76.4%  
- NETRAL: 2.8%  

### Visualisasi
*(contoh hasil chart ditampilkan di notebook)*

## 📊 Insight & Findings

Berdasarkan hasil analisis sentimen komentar, diperoleh beberapa temuan utama:

### 1. Komentar Positif
- Apresiasi terhadap AI sebagai alat bantu dalam proses kreatif.  
- Banyak audiens yang senang dengan hasil AI, khususnya di bidang seni dan animasi.  
- Pengakuan bahwa AI dapat mempercepat pekerjaan, misalnya dalam pengembangan desain dan produk.  

👉 **Insight:** AI diterima positif sebagai *supporting tool*, terutama untuk mempercepat proses kreatif.

### 2. Komentar Negatif
- Kritik keras terhadap penggunaan AI yang menggantikan karya seniman tanpa hak cipta.  
- Kekhawatiran terkait AI mengambil sumber daya seni tanpa izin atau kompensasi.  
- Rasa takut bahwa AI akan menggantikan pekerjaan kreatif manusia.  
- Kritik komersialisasi karya AI tanpa memberikan hak kepada pembuat asli.  

👉 **Insight:** Kekhawatiran utama audiens adalah isu **etika, hak cipta, dan ancaman terhadap pekerjaan kreatif manusia**.

### 3. Komentar Netral/Informasi
- Diskusi tentang regulasi & hukum hak cipta dalam seni dan animasi.  
- Pertanyaan seputar dampak AI terhadap industri kreatif.  
- Pembahasan batasan dan desain AI.  

👉 **Insight:** Ada kebutuhan mendesak akan **regulasi dan transparansi** penggunaan AI di sektor kreatif.

---

## ✅ Conclusion & Recommendations
- **Kesimpulan**: 
  1.  Penerimaan positif ada, tapi lebih banyak bersifat apresiasi terbatas (AI sebagai alat bantu, bukan pengganti).
  2.  Kekhawatiran dominan → isu etika, hak cipta, dan keamanan pekerjaan kreatif.
  3.  Audiens menuntut regulasi & transparansi terkait penggunaan AI dalam seni.
- **Rekomendasi**:  
  1. Edukasi publik tentang penggunaan AI secara etis (misalnya: AI = alat bantu, bukan pengganti).
  2. Dorong transparansi → sertakan label atau penjelasan jika sebuah karya dibuat/diolah AI.
  3. Kolaborasi manusia-AI → tunjukkan bahwa AI memperkuat, bukan menggantikan kreativitas manusia.
  4. Advokasi regulasi → ada peluang untuk riset atau usulan kebijakan mengenai hak cipta & royalti karya yang melibatkan AI.
 
## 🤖 AI Support Explanation
- **IBM Granite LLM (Replicate API)** digunakan untuk analisis sentimen dan summarization.  
- **LangChain Community** membantu pipeline integrasi LLM.  
- **Google Colab** sebagai environment analisis.

## 📎 Submission Links
- [📓 Google Colab Notebook]([./CapstoneProject_MuhammadFauzi_Final.ipynb](https://colab.research.google.com/drive/1VSD5ppiQMqcxddM0Tq2biMZL_LqSdOU1?usp=sharing))  
- [📂 Dataset Mentah](https://docs.google.com/spreadsheets/d/1InwLGW_5STHxXLpmn4VV8_vFNLhTaFkDr7JMbim_ZVQ/edit?usp=sharing)  
- [📑 Presentation Slide](https://drive.google.com/file/d/1Miojwa7pei8YB7wA1FU_V4fgjbFplwQR/view?usp=sharing)

---

### 👨‍💻 Author
Nama: **Muhammad Fauzi**  
Program: Hacktiv8 x IBM Student Developer Initiative    
