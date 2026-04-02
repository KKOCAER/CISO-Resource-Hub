# 💾 Data Security Management

> Veri keşfi, sınıflandırma, koruma ve yaşam döngüsü yönetimi için framework, standart ve best practice'ler.

---

## Kaynaklar

### NIST Privacy Framework ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: NIST
- **URL**: https://www.nist.gov/privacy-framework
- **Açıklama**: Kişisel veri riski yönetimi için NIST'in gizlilik çerçevesi. NIST CSF ile entegrasyon ve GDPR uyum haritası içerir.
- **Neden önemli**: KVKK ve GDPR gerekliliklerini tek çerçevede yönetmek için pratik araç.

**Privacy Framework Temel Fonksiyonlar:**
| Fonksiyon | Açıklama |
|---|---|
| **IDENTIFY-P** | Veri envanteri ve gizlilik riski |
| **GOVERN-P** | Politika ve risk yönetimi kararları |
| **CONTROL-P** | Veri işleme yönetimi |
| **COMMUNICATE-P** | Gizlilik uygulamalarının şeffaflığı |
| **PROTECT-P** | Veri güvenliği kontrolleri |

---

### Data Security Governance Framework ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: ISACA
- **URL**: https://www.isaca.org/resources/news-and-trends/newsletters/atisaca/2020/volume-7/governance-of-data-in-the-digital-age
- **Açıklama**: Veri sahibi atama, sınıflandırma şemaları, etiketleme ve yaşam döngüsü yönetimi. Kurumsal veri yönetişim programı kurulum rehberi.
- **Neden önemli**: Veri güvenliği programı için yönetişim temeli olmadan teknik kontroller havada kalır.

**Veri Yönetişim Rolleri:**
| Rol | Sorumluluk |
|---|---|
| Data Owner | İş birimi; veri değeri ve riski kararları |
| Data Steward | Veri kalitesi ve sınıflandırma doğruluğu |
| Data Custodian | IT; teknik koruma kontrolleri |
| Data Subject | Kişisel verisi işlenen birey |
| Privacy Officer | Regülatif uyum koordinasyonu |

---

### DSPM — Data Security Posture Management ⭐ Best Practice
- **Tür**: Best Practice / Araç Kategorisi
- **Yayıncı**: Gartner
- **URL**: https://www.gartner.com/en/information-technology/glossary/data-security-posture-management
- **Açıklama**: Yapılandırılmamış ve bulut verisi için otomatik keşif, sınıflandırma ve koruma. Cloud storage, SaaS ve veritabanlarındaki hassas veri risklerini tespit eder.
- **Neden önemli**: Bilinmeyen hassas veri (shadow data) modern ihlallerin başlıca kaynağı. DSPM görünürlük sağlar.

**DSPM Kullanım Senaryoları:**
- 🔍 S3, Azure Blob, GCS'deki gizli veri tespiti
- 🔍 SaaS uygulamalarında PII/PHI envanteri
- 🔍 Aşırı izinli veri erişiminin tespiti
- 🔍 Veri sınıflandırma politika ihlalleri
- 🔍 Eski/gereksiz veri imha tespiti

**Öne Çıkan DSPM Araçları:**
| Araç | Güçlü Yön |
|---|---|
| Varonis | NTFS/AD entegrasyonu |
| Rubrik Security Cloud | Backup entegrasyonu |
| BigID | Gizlilik odaklı |
| Cyera | Cloud-native |

---

### DLP Best Practices Rehberi ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: SANS Institute
- **URL**: https://www.sans.org/reading-room/whitepapers/dlp/
- **Açıklama**: Data Loss Prevention strateji ve uygulama kılavuzu — endpoint, network ve cloud DLP politika tasarımı.
- **Neden önemli**: DLP projeleri sık başarısız olur. Bu rehber yaygın hataları ve doğru önceliklendirmeyi gösterir.

**DLP Uygulama Yol Haritası:**
```
1. KEŞİF (Aylar 1-2)
   ├── Kritik veri türlerini tanımla (PII, PCI, ticari sır)
   ├── Veri konumlarını haritala
   └── Veri akışlarını belge et

2. POLİTİKA TASARIMI (Aylar 2-3)
   ├── Önce izleme/raporlama modunda başla
   ├── False positive oranını ölç
   └── Politikayı iş birimleriyle doğrula

3. KONTROL UYGULAMA (Aylar 3-6)
   ├── Kritik kanallardan başla (email, USB, cloud upload)
   ├── Engelleme öncesi uyarı katmanı koy
   └── İstisna yönetim sürecini tanımla

4. OLGUNLAŞTIRMA (6+ ay)
   ├── Otomatik sınıflandırma entegrasyonu
   ├── SIEM/SOAR ile entegrasyon
   └── Düzenli politika gözden geçirme
```

---

### NIST SP 800-53: Veri Güvenliği Kontrolleri
- **Tür**: Standart
- **Yayıncı**: NIST
- **URL**: https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final
- **Açıklama**: Federal bilgi sistemleri güvenlik kontrol kataloğu. AC (Access Control), AU (Audit), SC (System & Communications) ve MP (Media Protection) ailelerindeki veri kontrolleri.
- **Neden önemli**: Veri güvenliği kontrollerinin en kapsamlı ve referans alınan kataloğu.

---

### Data Classification Policy Template ⭐ Best Practice
- **Tür**: Şablon
- **Yayıncı**: SANS Institute
- **URL**: https://www.sans.org/information-security-policy/
- **Açıklama**: CISO ofisleri için hazır veri sınıflandırma politika şablonu. 4 seviyeli sınıflandırma modeli.
- **Neden önemli**: Sıfırdan politika yazmak yerine kanıtlanmış şablonla hızlı başlangıç.

---

## 🏗️ Veri Sınıflandırma Modeli

### 4 Seviyeli Veri Sınıflandırma

| Seviye | Etiket | Tanım | Örnek |
|---|---|---|---|
| 1 | 🟢 **Public** | Kamuya açık bilgi | Web sitesi içeriği, basın bültenleri |
| 2 | 🔵 **Internal** | Şirket içi kullanım | Politikalar, iç yazışmalar |
| 3 | 🟡 **Confidential** | Yetkili kişilerle sınırlı | Finansal raporlar, müşteri verileri |
| 4 | 🔴 **Restricted** | En yüksek koruma | Ticari sırlar, PCI verileri, PHI |

### Veri Koruma Kontrolleri (Seviyeye Göre)

| Kontrol | Public | Internal | Confidential | Restricted |
|---|---|---|---|---|
| Şifreleme (rest) | İsteğe bağlı | Önerilen | Zorunlu | Zorunlu + HSM |
| Şifreleme (transit) | TLS | TLS | TLS 1.2+ | TLS 1.3 |
| Erişim kaydı | — | Önerilen | Zorunlu | Zorunlu + SIEM |
| DLP politikası | — | İzleme | Engelleme uyarısı | Engelleme |
| Silme prosedürü | Standart | Güvenli silme | Sertifikalı silme | Fiziksel imha |

---

## 🔄 Veri Yaşam Döngüsü Güvenliği

```
OLUŞTURMA → Sınıflandırma etiketi atama
     ↓
DEPOLAMA  → Şifreleme + erişim kontrolü
     ↓
KULLANMA  → DLP izleme + audit log
     ↓
PAYLAŞMA  → Güvenli transfer + watermarking
     ↓
ARŞİVLEME → Uzun vadeli şifreleme + anahtar yönetimi
     ↓
İMHA      → Politikaya uygun güvenli silme
```

---

## 📚 İlgili Kategoriler

- [Identity Security](../identity-security/README.md)
- [Cloud Security](../cloud-security/README.md)
- [Uyum & Regülasyon](../compliance/README.md)
