# ☁️ Cloud Security

> Genel ve özel bulut ortamlarını korumak için framework, standart, araç ve best practice'ler.

---

## Kaynaklar

### CSA Cloud Controls Matrix (CCM) ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: Cloud Security Alliance
- **URL**: https://cloudsecurityalliance.org/research/cloud-controls-matrix/
- **Açıklama**: 197 kontrol maddesinden oluşan cloud güvenlik matrisi. ISO 27001, NIST CSF, PCI DSS ve CIS Controls ile uyum eşlemesi içerir.
- **Neden önemli**: Bulut tedarikçi değerlendirmesi ve cloud güvenlik programı yapılandırması için endüstri standardı.

**CCM Ana Alanları:**
| Alan | Kodu | Açıklama |
|---|---|---|
| Application & Interface Security | AIS | API ve uygulama güvenliği |
| Audit & Assurance | AAC | Denetim ve güvence |
| Business Continuity | BCR | İş sürekliliği |
| Change Control | CCC | Değişiklik yönetimi |
| Data Security | DSI | Veri güvenliği ve yaşam döngüsü |
| Encryption & Key Mgmt | EKM | Şifreleme ve anahtar yönetimi |
| Identity & Access Mgmt | IAM | Kimlik ve erişim yönetimi |
| Infrastructure & Virtualization | IVS | Altyapı güvenliği |
| Threat & Vulnerability Mgmt | TVM | Tehdit ve zafiyet yönetimi |

---

### CIS Benchmarks (Cloud) ⭐ Best Practice
- **Tür**: Yapılandırma Rehberi
- **Yayıncı**: Center for Internet Security
- **URL**: https://www.cisecurity.org/cis-benchmarks
- **Açıklama**: AWS, Azure, GCP, Docker, Kubernetes ve diğer cloud platformları için sertleştirme kılavuzları. Otomatik değerlendirme araçlarıyla entegre.
- **Neden önemli**: Bulut misconfiguration — veri ihlallerinin 1 numaralı nedeni. CIS Benchmarks hızlı uygulama sağlar.

**Platform Kapsamı:**
- ☁️ AWS Foundations Benchmark
- ☁️ Microsoft Azure Benchmark
- ☁️ Google Cloud Platform Benchmark
- 🐳 Docker Benchmark
- ☸️ Kubernetes Benchmark
- 🖥️ Windows Server / Linux

---

### MITRE ATT&CK Cloud Matrix
- **Tür**: Bilgi Tabanı
- **Yayıncı**: MITRE Corporation
- **URL**: https://attack.mitre.org/matrices/enterprise/cloud/
- **Açıklama**: AWS, Azure, GCP, SaaS ve Office 365'e özgü saldırı teknikleri matrisi.
- **Neden önemli**: Cloud tehdit modelleme ve detection engineering'in temeli. SOC ekipleri için detection rule yazımında referans.

**Öne Çıkan Cloud Taktikleri:**
- T1078.004 — Valid Accounts: Cloud Accounts
- T1530 — Data from Cloud Storage
- T1537 — Transfer Data to Cloud Account
- T1580 — Cloud Infrastructure Discovery

---

### CISA SCuBA (Secure Cloud Business Applications) ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: CISA
- **URL**: https://www.cisa.gov/resources-tools/programs/secure-cloud-business-applications-scuba-project
- **Açıklama**: Microsoft 365 ve Google Workspace için federal güvenlik yapılandırma kılavuzları. ScubaGear otomatik değerlendirme aracıyla birlikte.
- **Neden önemli**: SaaS güvenlik yapılandırmasını standartlaştırır. M365 tenant hardening için pratik kontrol listesi.

---

### CSPM & CNAPP Uygulama Rehberi ⭐ Best Practice
- **Tür**: Best Practice / Araç Kategorisi
- **Yayıncı**: Gartner
- **URL**: https://www.gartner.com/en/information-technology/glossary/cloud-native-application-protection-platform-cnapp
- **Açıklama**: Cloud Security Posture Management ve Cloud-Native Application Protection Platform seçim kriterleri ve uygulama adımları.
- **Neden önemli**: CSPM → misconfiguration tespiti. CNAPP → runtime koruma + code-to-cloud görünürlüğü.

**CSPM vs CNAPP Karşılaştırması:**
| Özellik | CSPM | CNAPP |
|---|---|---|
| Kapsam | Yapılandırma | Uygulama yaşam döngüsü |
| Odak | IaaS/PaaS güvenliği | Kod → Cloud güvenliği |
| Runtime koruma | Sınırlı | Evet (CWPP dahil) |
| IaC tarama | Bazı araçlarda | Evet |
| Örnek araçlar | Prisma Cloud, Wiz | Aqua, Lacework, Wiz |

---

### NIST SP 800-144: Cloud Security Guidelines
- **Tür**: Rehber
- **Yayıncı**: NIST
- **URL**: https://csrc.nist.gov/publications/detail/sp/800-144/final
- **Açıklama**: Genel ve kamu bulutu için güvenlik ve gizlilik ilkeleri. Paylaşılan sorumluluk modeli analizi ve cloud hizmet modeli bazlı kontroller.
- **Neden önemli**: Temel kavramsal çerçeve. IaaS/PaaS/SaaS sorumluluk sınırlarını netleştirir.

---

## 🏗️ Cloud Güvenlik Mimarisi Best Practice

### Paylaşılan Sorumluluk Modeli

```
┌─────────────────────────────────────────────────┐
│                  MÜŞTERİ SORUMLULUĞU             │
├──────────────┬──────────────┬───────────────────┤
│     IaaS     │     PaaS     │       SaaS        │
│  Uygulama    │  Uygulama    │   Yapılandırma    │
│  İşletim Sis │  Veri        │   Kullanıcı Erş.  │
│  Veri        │  Kimlik      │   Veri            │
├──────────────┼──────────────┼───────────────────┤
│  Hipervizör  │  Çalışma Zam │                   │
│  Ağ          │  Ara Katman  │   Platform        │
│  Depolama    │  Ağ/Depolama │   Altyapı         │
│  Veri Merkezi│  Fiziksel    │   Güvenlik        │
│     BULUT SAĞLAYICI SORUMLULUĞU                 │
└─────────────────────────────────────────────────┘
```

### Cloud Güvenlik Program Öncelikleri

1. **Kimlik & Erişim** — MFA, Just-in-Time, Least Privilege
2. **Görünürlük** — CSPM, Cloud SIEM entegrasyonu
3. **Veri Koruma** — Şifreleme (rest/transit), DLP
4. **Ağ Segmentasyonu** — VPC tasarımı, Security Groups
5. **Güvenli Geliştirme** — IaC tarama, container güvenliği
6. **Uyum İzleme** — Sürekli CCM/CIS benchmark değerlendirme

---

## 🔧 Önerilen Araçlar

| Kategori | Açık Kaynak | Ticari |
|---|---|---|
| CSPM | Prowler, ScoutSuite | Wiz, Prisma Cloud |
| IaC Tarama | Checkov, tfsec | Bridgecrew |
| Container | Trivy, Falco | Aqua Security |
| SIEM | OpenSearch | Splunk, Sentinel |

---

## 📚 İlgili Kategoriler

- [Identity Security](../identity-security/README.md)
- [Data Security](../data-security/README.md)
- [Framework & Standartlar](../frameworks-standards/README.md)
