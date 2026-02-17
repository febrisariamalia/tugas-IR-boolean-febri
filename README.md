# Tugas IR - Boolean Retrieval Model

Implementasi sederhana **Boolean Retrieval Model** untuk tugas Information Retrieval menggunakan **Term–Document Incidence Matrix** dan operasi **AND / OR / NOT**.

## Deskripsi
Repository ini mengikuti alur pada artikel Medium:
1) Membuat token unik (vocabulary) dari dokumen  
2) Membuat **Term–Document Incidence Matrix** (0/1)  
3) Mengambil **term vector** dari incidence matrix  
4) Menjalankan operasi Boolean **AND / OR / NOT** untuk menemukan dokumen yang relevan  
5) Menjalankan query dari user dengan format sederhana

Dokumen contoh yang digunakan berupa kalimat bahasa Indonesia (3 dokumen).

## Tools
- VSCode (Remote - WSL)
- Ubuntu (WSL)
- Python 3
- Jupyter Notebook
- pandas

## Struktur File
- `incidence_boolean.ipynb` : notebook utama implementasi (sesuai Medium)
- `README.md` : penjelasan dan cara menjalankan
- `.gitignore` : agar file tidak penting (mis. `.venv/`) tidak ikut ter-upload
- `requirements.txt` : daftar library (opsional)

## Cara Menjalankan (VSCode + WSL)
1. Buka folder project ini di VSCode dalam mode **WSL: Ubuntu**.
2. Buka notebook `incidence_boolean.ipynb`.
3. Jalankan cell dari atas ke bawah (**Run All**).
4. Saat diminta input, masukkan query sesuai format.

### (Opsional) Instalasi library
Jika diperlukan, install library dari `requirements.txt`:
```bash
pip install -r requirements.txt
````

## Format Query yang Didukung

* `kata1 AND kata2`
* `kata1 OR kata2`
* `kata1 AND NOT kata2`
* `kata1 OR NOT kata2`

> Catatan: query dipisahkan dengan spasi, contoh `kopi AND NOT coding`.

## Contoh Query

* `kopi AND saya`
* `kopi AND NOT coding`
* `coding AND ujian`
* `belajar OR kopi`

## Catatan Tambahan

* Jika kata pada query tidak ada di vocabulary, hasil bisa kosong.
* Notebook menggunakan incidence matrix 0/1 seperti pada referensi Medium (bukan inverted index).

## Referensi & Acknowledgements
Proyek ini dikerjakan dengan mengikuti panduan dan referensi kode dari:

- Artikel: [Basic Information Retrieval Problem — Boolean Retrieval Model](https://bajpaihimanshu.medium.com/basic-information-retrieval-problem-boolean-retrieval-model-ed05f3d74ddc) oleh Himanshu Bajpai.
- Repositori asli: [DataScienceProjects](https://github.com/HimanshuBajpai869/DataScienceProjects) oleh Himanshu Bajpai.

_Dibuat untuk memenuhi tugas Sistem Temu Kembali Informasi._
