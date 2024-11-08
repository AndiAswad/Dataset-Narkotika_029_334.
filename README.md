# Dataset Putusan Mahkamah Agung Republik Indonesia

## Deskripsi
Dataset ini berisi 50 dokumen PDF dari Direktori Putusan Mahkamah Agung Republik Indonesia. Dokumen yang ada berfokus pada direktori Pidana Khusus Klasifikasi Narkotika dan Psikotropika dari Pengadilan Negeri Palu. 
Dataset ini berisi kumpulan putusan Pengadilan Negeri di Indonesia yang diperoleh dari Direktori Putusan Mahkamah Agung Republik Indonesia. Setiap file dalam dataset ini berbentuk PDF dan mencakup berbagai detail kasus seperti identitas terdakwa, dakwaan, bukti-bukti, saksi, serta hasil akhir putusan. Dataset ini sangat berharga untuk analisis hukum, riset di bidang pemrosesan bahasa alami, dan pelatihan model AI khusus bidang hukum.

## Struktur Dataset
- **Nama File**: Setiap file memiliki nama unik dengan format `Nomor x/Pid.Sus/yyyy/PN [Kota]`, yang mencerminkan nomor perkara, jenis pidana, tahun, dan lokasi pengadilan.
- **Konten Dokumen**:
  - **Identitas Terdakwa**: Nama lengkap, tempat lahir, usia, pekerjaan, dan alamat.
  - **Rincian Kasus**: Tanggal kejadian, tempat kejadian, deskripsi tindakan pidana, dan barang bukti yang disita.
  - **Keterangan Saksi**: Testimoni dari saksi yang diperiksa di persidangan.
  - **Putusan**: Hukuman yang dijatuhkan, termasuk pidana penjara, denda, dan barang bukti yang dimusnahkan.
  
## Contoh Penggunaan Dataset
Dataset ini dapat dimanfaatkan untuk berbagai keperluan seperti:
- **Analisis Hukum**: Mempelajari pola putusan dan alasan hakim dalam kasus tertentu.
- **Pemrosesan Bahasa Alami (NLP)**: Menggunakan data untuk melatih model QA yang dapat menjawab pertanyaan hukum berdasarkan dokumen legal.
- **Penelitian Akademik**: Menggunakan dataset ini sebagai dasar studi kasus untuk analisis tekstual dan perbandingan antar kasus.

## Contoh Ekstraksi Data
Di bawah ini adalah contoh kode sederhana untuk ekstraksi teks dari file PDF menggunakan Python:

```python
import PyPDF2

def extract_text_from_pdf(file_path):
    text = ""
    with open(file_path, "rb") as file:
        reader = PyPDF2.PdfReader(file)
        for page in reader.pages:
            text += page.extract_text()
    return text

# Contoh penggunaan
text_content = extract_text_from_pdf("Nomor 17_Pid.Sus_2024_PN_Pal.pdf")
print(text_content)


## Sumber dan Lisensi
Data ini diambil dari [Direktori Putusan Mahkamah Agung RI](https://putusan3.mahkamahagung.go.id/direktori.html) dan hanya untuk penggunaan riset. Harap mematuhi ketentuan yang berlaku.
