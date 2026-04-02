# 🔑 Identity Security

> Kimlik doğrulama, yetkilendirme, erişim yönetimi ve Zero Trust mimarisi için standart, framework ve best practice'ler.

---

## Kaynaklar

### NIST SP 800-63: Digital Identity Guidelines ⭐ Best Practice
- **Tür**: Standart
- **Yayıncı**: NIST
- **URL**: https://pages.nist.gov/800-63-3/
- **Açıklama**: Kimlik doğrulama, federasyon ve kimlik proofing için temel rehber. IAL (Identity Assurance Level), AAL (Authentication Assurance Level) ve FAL (Federation Assurance Level) güvence seviyeleri.
- **Neden önemli**: MFA gerekliliklerinin ve kimlik doğrulama güvence seviyelerinin referans standardı.

**Güvence Seviyeleri:**
| Seviye | IAL (Kimlik) | AAL (Doğrulama) | Örnek Uygulama |
|---|---|---|---|
| 1 | Öz beyan | Tek faktör | Düşük riskli sistemler |
| 2 | Uzaktan doğrulama | MFA zorunlu | Kurumsal uygulamalar |
| 3 | Yüz yüze doğrulama | Donanım token | Kritik sistemler |

---

### Zero Trust Architecture (NIST SP 800-207) ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: NIST
- **URL**: https://csrc.nist.gov/publications/detail/sp/800-207/final
- **Açıklama**: Zero Trust ilkelerinin teknik uygulaması. Kimlik merkezli mikro-segmentasyon ve sürekli doğrulama mimarisi.
- **Neden önemli**: "Güven ama doğrula" modelinden "asla güvenme, her zaman doğrula" modeline geçişin teknik rehberi.

**Zero Trust Temel İlkeleri:**
1. Tüm veri ve servisler kaynak olarak kabul edilir
2. Ağ konumundan bağımsız erişim koruması
3. Her oturum için tek tek erişim yetkisi
4. Erişim politikası dinamik ve context-aware
5. Tüm varlıkların bütünlüğü ve güvenliği izlenir
6. Kimlik doğrulama ve yetkilendirme katı şekilde uygulanır
7. Mümkün olduğunca fazla telemetri toplanır

---

### CISA Zero Trust Maturity Model ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: CISA
- **URL**: https://www.cisa.gov/zero-trust-maturity-model
- **Açıklama**: Identity, Devices, Networks, Applications, Data boyutlarında Zero Trust olgunluk değerlendirmesi. 4 olgunluk seviyesi modeli.
- **Neden önemli**: ZTA yolculuğunda nerede olunduğunu ölçmek ve sonraki adımları önceliklendirmek için pratik araç.

**Beş ZTA Boyutu & Olgunluk Seviyeleri:**
| Boyut | Geleneksel | Başlangıç | Gelişmiş | Optimal |
|---|---|---|---|---|
| **Identity** | Statik MFA | Risk tabanlı MFA | Sürekli doğrulama | Tam otomatik |
| **Devices** | Manuel envanter | MDM + temel uyumluluk | EDR + uyumluluk politikası | Gerçek zamanlı posture |
| **Networks** | Makro-segmentasyon | Mikro-segmentasyon başlangıç | Uygulama katmanı | Tam software-defined |
| **Applications** | VPN tabanlı | Per-app VPN | ZTNA | Inline inspection |
| **Data** | Temel sınıflandırma | Etiketleme politikası | Otomatik DLP | Tam data-centric |

---

### Privileged Access Management (PAM) Best Practices ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: CyberArk / Gartner
- **URL**: https://www.cyberark.com/resources/ebooks/privileged-access-management-best-practices/
- **Açıklama**: Ayrıcalıklı hesap yönetimi — just-in-time access, session recording, credential vaulting ve break-glass prosedürleri.
- **Neden önemli**: Saldırıların %80'i ayrıcalıklı kimlik bilgilerini hedefler. PAM programı olmadan ihlal sonrası lateral movement kontrol edilemez.

**PAM Program Bileşenleri:**
```
PAM Programı
├── Keşif & Envanter
│   ├── Servis hesapları
│   ├── Lokal admin hesapları
│   └── Paylaşılan hesaplar
├── Vault & Rotasyon
│   ├── Şifre kasası (vault)
│   ├── Otomatik rotasyon
│   └── SSH key yönetimi
├── Just-in-Time Erişim
│   ├── Geçici yükseltme
│   ├── Onay akışı
│   └── Zaman sınırlı oturumlar
└── Oturum Yönetimi
    ├── Session recording
    ├── Keystroke logging
    └── Anomali tespiti
```

---

### IDSA — Identity Defined Security Alliance
- **Tür**: Topluluk / Araştırma
- **Yayıncı**: IDSA
- **URL**: https://www.idsalliance.org/
- **Açıklama**: Kimlik merkezli güvenlik stratejileri, araştırma raporları ve ücretsiz uygulama rehberleri.
- **Neden önemli**: Identity güvenliği alanında güncel araştırmalar ve pratik uygulama kılavuzları.

---

### Microsoft Entra Identity Best Practices ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: Microsoft
- **URL**: https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/security-operations-introduction
- **Açıklama**: Azure AD / Entra ID için Conditional Access, MFA zorunluluğu, PIM ve identity governance yapılandırma kılavuzu.
- **Neden önemli**: M365 ekosistemindeki organizasyonlar için spesifik yapılandırma rehberi.

---

## 🏗️ Identity Security Program Best Practices

### IAM Güvenlik Kontrol Listesi

**Temel Kontroller (IG1 seviyesi):**
- [ ] Tüm kullanıcılar için MFA zorunlu mu?
- [ ] Ayrıcalıklı hesaplar için ayrı identities var mı?
- [ ] Guest/extern hesap politikası tanımlandı mı?
- [ ] Offboarding süreci otomatik mi?
- [ ] Servis hesapları envanteri mevcut mu?

**Gelişmiş Kontroller (IG2 seviyesi):**
- [ ] Conditional Access politikaları uygulandı mı?
- [ ] Risk bazlı kimlik doğrulama aktif mi?
- [ ] PAM çözümü devrede mi?
- [ ] Identity governance (certifications) çalışıyor mu?
- [ ] Privileged Identity Management (PIM) kullanılıyor mu?

**Olgun Program (IG3 seviyesi):**
- [ ] Zero Trust mimarisi uygulandı mı?
- [ ] Passwordless authentication aktif mi?
- [ ] Identity threat detection (ITDR) devrede mi?
- [ ] JIT/JEA erişim modeli uygulandı mı?
- [ ] Cross-tenant B2B politikaları yönetiliyor mu?

### Kimlik Tehdit Senaryoları

| Senaryo | Kontrol | Tespit |
|---|---|---|
| Credential stuffing | MFA, rate limiting | SIEM login anomalisi |
| Pass-the-hash | Local admin kaldırma, PAM | EDR lateral movement |
| Token theft | Kısa token ömrü, CAE | UEBA anormallik |
| Insider threat | Least privilege, JIT | Davranışsal analiz |
| BEC (Email takeover) | MFA, login bildirimleri | İletme kuralı tespiti |

---

## 📚 İlgili Kategoriler

- [Zero Trust & Cloud Security](../cloud-security/README.md)
- [Data Security](../data-security/README.md)
- [Olay Müdahale](../incident-response/README.md)
