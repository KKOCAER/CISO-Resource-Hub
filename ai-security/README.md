# 🤖 AI Güvenliği

> Yapay zeka sistemlerinin güvenliğini sağlamak ve AI'ın yarattığı yeni tehditlere karşı korunmak için framework, standart ve best practice'ler.

---

## Kaynaklar

### NIST AI Risk Management Framework (AI RMF) ⭐ Best Practice
- **Tür**: Framework
- **Yayıncı**: NIST
- **URL**: https://www.nist.gov/system/files/documents/2023/01/26/AI%20RMF%201.0.pdf
- **Açıklama**: AI sistemleri için güven, şeffaflık, güvenlik ve dayanıklılık ilkeleri. GOVERN, MAP, MEASURE, MANAGE döngüsü. NIST CSF ile uyumlu yapı.
- **Neden önemli**: AI sistemlerini satın alan veya geliştiren organizasyonlar için risk değerlendirme çerçevesi. Regülatif baskı artıkça zorunlu referans haline geliyor.

**AI RMF Temel Fonksiyonlar:**
| Fonksiyon | Amaç |
|---|---|
| **GOVERN** | Kültür, politika ve sorumluluklar |
| **MAP** | AI riski bağlamını anlama |
| **MEASURE** | Riskleri analiz etme ve önceliklendirme |
| **MANAGE** | Riskleri tedavi etme ve izleme |

**AI Güven Özellikleri (Trustworthy AI):**
- Güvenilir & Dayanıklı (Safe & Secure)
- Açıklanabilir & Yorumlanabilir (Explainable)
- Gizlilik Koruyucu (Privacy-Enhanced)
- Adil & Önyargısız (Fair)
- Şeffaf (Transparent)
- Hesap Verebilir (Accountable)

---

### OWASP Top 10 for LLM Applications ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: OWASP
- **URL**: https://owasp.org/www-project-top-10-for-large-language-model-applications/
- **Açıklama**: Büyük Dil Modeli uygulamalarındaki en kritik 10 güvenlik riski listesi.
- **Neden önemli**: LLM tabanlı ürün ve servis geliştiren ya da kullanan her organizasyon için temel güvenlik kontrol listesi.

**OWASP LLM Top 10:**
| # | Risk | Açıklama |
|---|---|---|
| LLM01 | Prompt Injection | Zararlı talimatların modele enjekte edilmesi |
| LLM02 | Insecure Output Handling | Çıktının filtresiz kullanılması |
| LLM03 | Training Data Poisoning | Eğitim verisinin manipülasyonu |
| LLM04 | Model Denial of Service | Modelin aşırı yüklenmesi |
| LLM05 | Supply Chain Vulnerabilities | Tedarik zinciri riskleri |
| LLM06 | Sensitive Information Disclosure | Hassas veri sızdırması |
| LLM07 | Insecure Plugin Design | Güvensiz eklenti mimarisi |
| LLM08 | Excessive Agency | Gereğinden fazla yetki |
| LLM09 | Overreliance | Aşırı güven |
| LLM10 | Model Theft | Model çalınması |

---

### MITRE ATLAS (Adversarial Threat Landscape for AI)
- **Tür**: Bilgi Tabanı
- **Yayıncı**: MITRE Corporation
- **URL**: https://atlas.mitre.org/
- **Açıklama**: Makine öğrenmesi sistemlerine yönelik saldırı taktikleri ve tekniklerinin ATT&CK benzeri matrisi. Gerçek saldırı vakalarından derlendi.
- **Neden önemli**: AI güvenlik tehdit modellemesinin temeli. Kırmızı takım egzersizleri için çerçeve.

**Temel ATLAS Taktikleri:**
- Reconnaissance (Keşif)
- ML Model Access
- ML Attack Staging
- Exfiltration via ML Inference API
- Impact (Model çıktısının manipülasyonu)

---

### EU AI Act — Güvenlik Gereklilikleri
- **Tür**: Regülasyon
- **Yayıncı**: Avrupa Birliği
- **URL**: https://artificialintelligenceact.eu/
- **Açıklama**: AB'nin AI sistemleri için risk bazlı düzenleyici çerçevesi. Yüksek riskli AI sistemleri için zorunlu güvenlik, şeffaflık ve insan gözetimi gereklilikleri.
- **Neden önemli**: AB pazarına hizmet veren tüm organizasyonlar için uyum yükümlülüğü.

**Risk Sınıflandırması:**
```
Yasaklı AI ──→ Sosyal puanlama, gerçek zamanlı biyometrik gözetim
Yüksek Risk ──→ Kritik altyapı, eğitim, istihdam, kredi, yargı
Sınırlı Risk ──→ Chatbot'lar (şeffaflık zorunluluğu)
Minimum Risk ──→ Spam filtresi, oyun AI'ı
```

---

### CISA/NSA AI Security Best Practices ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: CISA + NSA + NCSC ortaklığı
- **URL**: https://www.cisa.gov/ai
- **Açıklama**: ABD ve müttefik federal ajansların AI sistemleri güvenliği için ortak yayınladığı rehber. Secure by Design AI ilkeleri ve somut uygulama adımları.
- **Neden önemli**: Devlet düzeyinde onaylanmış AI güvenlik gereklilikleri. Tedarikçi güvenlik gereksinimlerinde referans alınıyor.

---

### Adversarial ML Threat Matrix
- **Tür**: Araştırma / Framework
- **Yayıncı**: Microsoft + MITRE
- **URL**: https://github.com/mitre/advmlthreatmatrix
- **Açıklama**: Adversarial machine learning saldırı çerçevesi. Model poisoning, evasion (kaçınma), extraction ve inference saldırıları.
- **Neden önemli**: ML sistemleri kullanan güvenlik ekiplerinin test senaryoları için referans.

---

## 🏗️ AI Güvenlik Programı Best Practices

### AI Sistem Envanteri ve Risk Sınıflandırması

```
ADIM 1: Envanter
├── Dahili geliştirilen AI modeller
├── Satın alınan AI çözümleri
├── API ile tüketilen AI servisleri
└── Gömülü AI (ERP, CRM, SIEM içindeki)

ADIM 2: Risk Sınıflandırma
├── Veri hassasiyeti (kişisel veri?)
├── Karar etkisi (otomatik → insan hayatı?)
├── Dışa açıklık (iç kullanım → herkese açık?)
└── Manipülasyon riski (prompt injection?)

ADIM 3: Kontroller
├── Input validation & sanitization
├── Output filtering & monitoring
├── Model versiyonlama & rollback
└── İnsan denetimi (Human-in-the-loop)
```

### LLM Uygulamaları Güvenlik Kontrol Listesi

- [ ] Prompt injection testi yapıldı mı?
- [ ] Sistem istemi (system prompt) güvende mi?
- [ ] Çıktı filtreleme mekanizması var mı?
- [ ] API rate limiting uygulandı mı?
- [ ] PII/hassas veri LLM'e gönderilmemesi sağlandı mı?
- [ ] LLM kullanım logları saklanıyor mu?
- [ ] Plugin/tool yetkileri sınırlandırıldı mı?
- [ ] Fallback ve hata senaryoları test edildi mi?

---

## 📚 İlgili Kategoriler

- [Risk Yönetimi](../risk-management/README.md)
- [Data Security](../data-security/README.md)
- [Uyum & Regülasyon](../compliance/README.md)
