# ❓ FAQ & Panduan Dukungan

## Rules Documentation Framework

## 1. Pertanyaan Umum (FAQ)

### Q: Apakah framework ini menambah beban kerja tim Legal?

**A**: Di awal, mungkin terasa ada usaha ekstra untuk mengisi template. Namun,
ini akan mengurangi beban review manual di masa depan karena AI akan bekerja
dengan batasan yang sudah divalidasi sejak awal.

### Q: Bagaimana jika ada perubahan UU secara mendadak?

**A**: Framework mendukung **Top-Down Decomposition**. Anda hanya perlu
memperbarui file YAML di Level 1 tanpa mengubah arsitektur aplikasi inti.

### Q: Apa itu "Mail Merge" dalam konteks technical guide?

**A**: Ini adalah teknik untuk mengganti variabel dinamis (seperti nama klien
atau nilai kontrak) ke dalam aturan hukum atau pesan peringatan secara
otomatis menggunakan placeholder `{{VARIABLE}}`.

### Q: Siapa yang bertanggung jawab jika AI melanggar aturan Level 0?

**A**: Compliance Team dan System Architect. Namun, dengan
*Cross-Agent Validation*, risiko ini diminimalisir secara sistemis.

---

## 2. Saluran Komunikasi Resmi

| Channel | Fungsi | Person in Charge (PIC) |
| :--- | :--- | :--- |
| **Slack `#lh-rules-framework`** | Diskusi umum. | Architecture Lead |
| **GitHub Issues** | Pelaporan bug template. | Engineering Lead |
| **Email `compliance@lawyers-hub.ai`** | Eskalasi hukum. | Compliance Lead |

---

## 3. Mekanisme Umpan Balik (Feedback Loop)

Kami menghargai masukan Anda! Selama fase sosialisasi:

1. Gunakan formulir [Feedback Form](https://forms.lawyers-hub.ai/rules-feedback).
2. Ikuti sesi *Weekly Sync* setiap hari Jumat pukul 10:00 WIB.
3. Masukan akan ditinjau dan diintegrasikan ke versi minor berikutnya.

---

**Dukungan Anda adalah kunci kesuksesan implementasi ini.**
