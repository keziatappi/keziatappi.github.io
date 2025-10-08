---
title: "Test Scenario, Test Case and Bug Report"
date: 2025-10-08
categories: [Software Testing and Quality Assurance]
tags: [Testing] 
image: /assets/images/klmpk4.png
---

#  Test Scenario, Test Case, dan Bug Report

**Test Scenario**, **Test Case**, dan **Bug Report** adalah tiga elemen penting dalam proses pengujian perangkat lunak yang saling melengkapi.  
Ketiganya membantu memastikan bahwa aplikasi berjalan **sesuai harapan**, **berfungsi dengan baik**, dan **bebas dari kesalahan** sebelum dirilis ke pengguna.

---

##  Pengertian Utama

###  Test Scenario  
Gambaran umum tentang **apa yang diuji** untuk memastikan fungsionalitas aplikasi sesuai kebutuhan.  
Biasanya berisi deskripsi skenario besar yang mewakili proses atau fitur utama dalam aplikasi.

*Contoh:* “Periksa fungsi login dengan kombinasi username dan password valid.”

###  Test Case  
Langkah-langkah **detail pengujian**, termasuk input, proses, dan hasil yang diharapkan.  
Test Case menjawab pertanyaan *“bagaimana melakukan pengujian?”*  

*Contoh:*  
1. Buka halaman login  
2. Masukkan username dan password  
3. Klik tombol “Login”  
→ **Hasil yang diharapkan:** pengguna berhasil masuk ke dashboard.

###  Bug Report  
Laporan formal tentang **kesalahan atau masalah** yang ditemukan saat pengujian, mencakup detail bug, cara mereproduksi, hasil aktual, dan hasil yang diharapkan.

---

##  Template Umum

###  Template Test Scenario
| Field | Keterangan |
|-------|-------------|
| **ID Scenario** | Nomor unik skenario |
| **Deskripsi** | Ringkasan pengujian |
| **Modul/Fitur** | Fitur atau komponen yang diuji |

---

###  Template Test Case
| Field | Keterangan |
|-------|-------------|
| **ID Test Case** | Nomor unik test case |
| **Deskripsi** | Ringkasan singkat pengujian |
| **Precondition** | Kondisi awal sebelum pengujian |
| **Test Steps** | Langkah-langkah detail pengujian |
| **Test Data** | Data yang digunakan |
| **Expected Result** | Hasil yang diharapkan |
| **Actual Result** | Hasil aktual saat diuji |
| **Status** | Pass / Fail |

---

##  Contoh Test Scenario dan Test Case  
(Aplikasi BMI – Berdasarkan Test Plan Kelompok 3)

| ID Scenario | Deskripsi | Modul/Fitur |
|--------------|------------|--------------|
| **TS001** | Periksa fungsi slider input | Input berat dan tinggi badan |
| **TS002** | Periksa hasil perhitungan & klasifikasi BMI | Perhitungan BMI |
| **TS003** | Periksa fungsi penyimpanan history BMI | History BMI |

---

###  Contoh Test Case (BMI Application)

| ID | Deskripsi | Precondition | Test Steps | Test Data | Expected Result |
|----|------------|---------------|-------------|------------|-----------------|
| **TC001** | Verifikasi slider berat | Aplikasi terbuka | Geser slider berat ke 60 kg | Berat = 60 | Label menampilkan "60 kg" |
| **TC003** | Verifikasi perhitungan BMI | Aplikasi terbuka | Masukkan tinggi 170 cm, berat 65 kg | Tinggi = 170, Berat = 65 | Hasil BMI = 22.49 |
| **TC008** | Verifikasi penyimpanan BMI ke history | Aplikasi terbuka | Tekan tombol *Simpan History* | Tinggi = 170, Berat = 65 | Data tersimpan di halaman history |

---

##  Bug Report

###  Komponen Bug Report
| Field | Keterangan |
|-------|-------------|
| **Bug ID** | Kode unik bug |
| **Bug Title** | Judul ringkas bug |
| **Steps to Reproduce** | Langkah-langkah untuk memunculkan bug |
| **Expected Result** | Hasil yang diharapkan |
| **Actual Result** | Hasil aktual yang terjadi |
| **Severity** | Dampak bug pada sistem |
| **Priority** | Tingkat urgensi perbaikan |
| **Reporter / Assignee** | Pihak yang melaporkan & memperbaiki |
| **Status** | Open / Fixed / Closed |

---

###  Tingkatan Severity
- **Low:** Tidak berdampak besar pada sistem.  
- **Medium:** Mengganggu sebagian fungsi, tetapi sistem tetap berjalan.  
- **High (Major):** Menghambat fungsi utama.  
- **Critical:** Menyebabkan sistem gagal total atau crash.

###  Tingkatan Priority
- **P1 (Urgent):** Harus segera diperbaiki.  
- **P2 (High):** Bug penting yang memengaruhi banyak pengguna.  
- **P3 (Medium):** Dapat diperbaiki di rilis berikutnya.  
- **P4 (Low):** Bug kosmetik atau minor.

---

###  Contoh Bug Report (Aplikasi BMI)
| Field | Detail |
|--------|---------|
| **Bug Title** | Perhitungan BMI salah saat input berat 60 kg & tinggi 170 cm |
| **Bug ID** | BMI-001 |
| **Steps to Reproduce** | 1. Buka aplikasi BMI<br>2. Masukkan Berat = 60<br>3. Masukkan Tinggi = 170<br>4. Klik tombol “Hitung” |
| **Expected Result** | Hasil BMI = 20.8 |
| **Actual Result** | Hasil BMI = 12.5 |
| **Severity** | Major (High) |
| **Priority** | P2 - High |
| **Build Version** | 1.0.0 |
| **Reported by** | SQA (Software Quality Assurance) |
| **Testing on** | Android |
| **Date** | 31-08-2025 |

---

##  Cara Menghindari Bug

1. **Pahami Persyaratan** – Pastikan semua kebutuhan sistem jelas bagi seluruh tim.  
2. **Unit Testing** – Lakukan pengujian sejak tahap awal.  
3. **Code Review** – Lakukan peninjauan kode antar developer.  
4. **Rencana Pengujian yang Baik** – Gunakan test plan yang komprehensif.  
5. **Automation Testing** – Gunakan alat otomatis untuk deteksi bug lebih cepat.  
6. **Kolaborasi Tim** – Bangun komunikasi efektif antara pengembang dan penguji.

---

##  Kesimpulan

Test Scenario, Test Case, dan Bug Report merupakan bagian penting dari proses **Software Testing**.  
Ketiganya membantu tim memastikan kualitas aplikasi dengan cara **terstruktur, terdokumentasi, dan efisien**, sehingga software yang dihasilkan **berfungsi dengan baik, bebas bug, dan siap digunakan oleh pengguna.**
