# Proyek Klasifikasi Gender Menggunakan CelebA dan VGG16

Proyek ini membangun model klasifikasi gambar **Male vs Not Male** menggunakan dataset **CelebA**, arsitektur **VGG16**, dan antarmuka inferensi sederhana berbasis **Gradio**.

## Daftar Isi

- [Deskripsi Proyek](#deskripsi-proyek)
- [Tujuan Proyek](#tujuan-proyek)
- [Alur Notebook](#alur-notebook)
- [Kebutuhan Data](#kebutuhan-data)
- [Struktur Folder](#struktur-folder)
- [Dependensi](#dependensi)
- [Instalasi](#instalasi)
- [Cara Menjalankan](#cara-menjalankan)
- [Catatan Penting](#catatan-penting)
- [Output Proyek](#output-proyek)
- [File](#file)

## Deskripsi Proyek

Notebook ini dirancang untuk membangun pipeline klasifikasi gender berbasis citra wajah dengan tahapan lengkap, mulai dari:

- pemuatan data,
- eksplorasi data,
- pra-pemrosesan,
- pelatihan model,
- evaluasi,
- penyimpanan model,
- hingga inferensi menggunakan Gradio.

Model utama yang digunakan adalah **VGG16 pretrained** yang disesuaikan untuk tugas klasifikasi biner.

## Tujuan Proyek

Tujuan utama proyek ini adalah:

- memuat dan menyiapkan dataset CelebA dari file atribut dan folder gambar,
- melakukan **Exploratory Data Analysis (EDA)** untuk memahami distribusi label dan kualitas gambar,
- membagi dataset menjadi data latih dan data uji,
- melatih model klasifikasi berbasis **VGG16**,
- mengevaluasi performa model dengan metrik klasifikasi,
- menyimpan model terlatih,
- membuat demo inferensi sederhana dengan **Gradio**.

## Alur Notebook

Notebook disusun dalam urutan berikut:

1. **Persiapan environment dan import library**
2. **Path data dan file sumber**
3. **Memuat dan menyaring dataset**
4. **Exploratory Data Analysis (EDA)**  
   Meliputi:
   - distribusi label,
   - statistik dasar citra,
   - kualitas gambar,
   - bias atribut,
   - pemeriksaan duplikasi data
5. **Pembagian dataset**
6. **Dataset class dan transformasi gambar**
7. **Setup model, optimizer, dan loss function**
8. **Pelatihan model**
9. **Evaluasi model**
10. **Menyimpan model**
11. **Memuat model untuk inferensi**
12. **Demo Gradio**

## Kebutuhan Data

Get Dataset from Google Drive:

[Download from Google Drive](https://drive.google.com/drive/folders/1hiF9T5Cz-ID0GIFeQMUY48GidEHkTvip?usp=drive_link)

Setelah diunduh, siapkan:
- folder gambar wajah CelebA yang sudah disejajarkan, misalnya:
  - `img_align_celeba/`
- file atribut CelebA, misalnya:
  - `list_attr_celeba.txt`
## Struktur Folder

Contoh struktur folder proyek:

```bash
project-folder/
├── projectOne.ipynb
├── README.md
├── requirements.txt
├── model/
│   └── vgg_gender_celeba.pth
└── data/
    ├── img_align_celeba/
    └── list_attr_celeba.txt
