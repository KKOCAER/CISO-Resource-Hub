# 📐 Framework & Standartlar

> Siber güvenlik programının iskeletini oluşturan uluslararası çerçeveler ve standartlar.

---

## Kaynaklar

### NIST Cybersecurity Framework 2.0 ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: NIST
- **URL**: https://www.nist.gov/cyberframework
- **Açıklama**: Altı temel fonksiyon: **Govern** (yeni), Identify, Protect, Detect, Respond, Recover. Tedarik zinciri ve üçüncü taraf risk yönetimini kapsar.
- **Neden önemli**: Sektörden bağımsız, ölçeklenebilir ve GDPR/ISO 27001 ile uyumlu. ABD federal standartlarına ek olarak küresel referans.

**CSF 2.0 Fonksiyon Özeti:**
| Fonksiyon | Amaç | Temel Kategoriler |
|---|---|---|
| GOVERN | Strateji & yönetişim | Politika, roller, risk yönetimi stratejisi |
| IDENTIFY | Varlık & risk anlama | Varlık yönetimi, iş ortamı, risk değerlendirme |
| PROTECT | Koruyucu önlemler | Erişim kontrolü, farkındalık, veri güvenliği |
| DETECT | Anomali tespiti | Sürekli izleme, tespit süreçleri |
| RESPOND | Olay müdahale | Müdahale planlama, iletişim, azaltma |
| RECOVER | Kurtarma & iyileştirme | Kurtarma planlama, iyileştirme |

---

### ISO/IEC 27001:2022
- **Tür**: Uluslararası Standart
- **Yayıncı**: ISO/IEC
- **URL**: https://www.iso.org/standard/82875.html
- **Açıklama**: Bilgi Güvenliği Yönetim Sistemi (BGYS) kurulumu ve sertifikasyonu için temel uluslararası standart. 2022 güncellemesiyle cloud ve geliştirme güvenliği kontrolleri güçlendirildi.
- **Neden önemli**: Uluslararası ticaret ve tedarik zinciri ilişkilerinde güven belgesi. Müşteri denetimleri için ortak zemin.

**Annex A — Yeni 2022 Kontrolleri:**
- A.5.7 Threat intelligence
- A.5.23 Information security for use of cloud services
- A.5.30 ICT readiness for business continuity
- A.8.9 Configuration management
- A.8.10 Information deletion
- A.8.11 Data masking
- A.8.16 Monitoring activities

---

### CIS Controls v8 ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: Center for Internet Security
- **URL**: https://www.cisecurity.org/controls/v8
- **Açıklama**: 18 kritik güvenlik kontrolü, 3 uygulama grubu. Olgunluk düzeyine göre ölçeklenebilir.
- **Neden önemli**: Önceliklendirilmiş yaklaşımıyla sınırlı kaynakla maksimum etki sağlar.

**Uygulama Grupları:**
| Grup | Hedef Kurum | Kontrol Sayısı |
|---|---|---|
| IG1 | Küçük, az kaynaklı | 56 Safeguard |
| IG2 | Orta ölçek, teknik ekip | +74 Safeguard |
| IG3 | Büyük, olgun program | +23 Safeguard |

**İlk 6 Kritik Kontrol (IG1 temeli):**
1. Enterprise Asset Inventory
2. Software Asset Inventory
3. Data Protection
4. Secure Configuration
5. Account Management
6. Access Control Management

---

### MITRE ATT&CK v15
- **Tür**: Bilgi Tabanı
- **Yayıncı**: MITRE Corporation
- **URL**: https://attack.mitre.org/
- **Açıklama**: Gerçek dünya saldırılarından derlenen taktik ve tekniklerin küresel bilgi tabanı. Enterprise, ICS, Cloud ve Mobile matrislerini içerir.
- **Neden önemli**: Tehdit modelleme, kırmızı/mavi takım ve SOC detection engineering için evrensel dil.

**Kullanım Alanları:**
- 🔴 Red Team: Test edilecek tekniklerin belirlenmesi
- 🔵 Blue Team: Detection ve response kuralı yazımı
- 🟣 Purple Team: Coverage gap analizi
- 📊 CISO: Güvenlik program olgunluk değerlendirmesi

---

### SABSA Security Architecture
- **Tür**: Mimari Framework
- **Yayıncı**: SABSA Institute
- **URL**: https://sabsa.org/
- **Açıklama**: Sherwood Applied Business Security Architecture — iş riskleri temelinde güvenlik mimarisi tasarımı için kurumsal çerçeve. Zachman Framework'ün güvenlik karşılığı.
- **Neden önemli**: Güvenlik stratejisini iş hedeflerine bağlamak için en kapsamlı mimari metodoloji.

---

## 🔄 Framework Uyum Haritası

```
ISO 27001:2022 ←──────────────→ NIST CSF 2.0
      ↕                               ↕
  Annex A                      CIS Controls v8
  Kontroller ←─── eşleme ─────→ Safeguards
      ↕                               ↕
  GDPR/KVKK                    MITRE ATT&CK
  Gereklilikler                 Teknikler
```

---

## 📚 İlgili Kategoriler

- [Risk Yönetimi](../risk-management/README.md)
- [Uyum & Regülasyon](../compliance/README.md)
- [Cloud Security](../cloud-security/README.md)
