# 🔍 Panduan Analisis Audit Trail (Grafana/ELK)

Dokumen ini menjelaskan langkah-langkah untuk memantau dan menganalisis
efektivitas aturan hukum menggunakan dashboard monitoring.

## 1. Akses Dashboard

- **Grafana**: `http://localhost:3000/dashboards`
- **Kibana (ELK)**: `http://localhost:5601/app/discover`

## 2. Filter Logs untuk Rule PRIV-RET-005

Untuk melakukan audit pada aturan retensi data dalam 24 jam terakhir:

### Di Grafana (Explore/Prometheus)

Gunakan query berikut:

```promql
# Jumlah eksekusi total
legal_rule_executions_total{rule_id="PRIV-RET-005"}

# Jumlah pelanggaran (violation)
legal_rule_violations_total{rule_id="PRIV-RET-005"}

# Rata-rata waktu eksekusi
legal_rule_duration_average_ms{rule_id="PRIV-RET-005"}
```

### Di Kibana (Logs)

1. Atur timeframe ke **Last 24 hours**.
2. Gunakan filter: `rule_id : "PRIV-RET-005"`.
3. Analisis kolom `action_type` dan `message`.

## 3. Metrik yang Harus Dipantau

| Metrik           | Deskripsi                     | Target (SLA) |
| :--------------- | :---------------------------- | :----------- |
| **Executions**   | Total pemanggilan aturan.     | N/A          |
| **Success Rate** | (Total - Violations) / Total. | > 95%        |
| **Avg Duration** | Kecepatan eksekusi.           | < 500ms      |
| **P99 Latency**  | Latensi pada persentil ke-99. | < 1000ms     |

## 4. Laporan Mingguan (Weekly Report)

Laporan harus mencakup:

1. **Ringkasan Eksekutif**: Total aturan aktif dan status kepatuhan.
2. **Top Violations**: Daftar rule yang paling sering memblokir aksi.
3. **Anomaly Detection**: Lonjakan mendadak pada pelanggaran.

## 5. Kontak Compliance

Jika ditemukan anomali data, segera hubungi:

- **Email**: <compliance-tech@lawyershub.ai>
- **Slack**: #dev-ops-compliance
