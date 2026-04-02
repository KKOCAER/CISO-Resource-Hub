# 🎯 Risk Yönetimi

> Bilgi güvenliği risklerini tanımlamak, ölçmek, izlemek ve yönetmek için framework, metodoloji ve best practice'ler.

---

## Kaynaklar

### NIST Risk Management Framework (RMF)
- **Tür**: Framework
- **Yayıncı**: NIST (National Institute of Standards and Technology)
- **URL**: https://csrc.nist.gov/projects/risk-management/about-rmf
- **Referans Doküman**: NIST SP 800-37 Rev.2
- **Açıklama**: Bilgi sistemleri için 7 adımlı bütünleşik risk yönetim yaşam döngüsü. Prepare, Categorize, Select, Implement, Assess, Authorize ve Monitor adımlarından oluşur.
- **Neden önemli**: Federal ve kurumsal sistemler için uyum temeli. Güvenlik kontrollerini sistem yaşam döngüsüne entegre eder.

---

### FAIR Risk Quantification ⭐ Best Practice
- **Tür**: Metodoloji
- **Yayıncı**: FAIR Institute
- **URL**: https://www.fairinstitute.org/
- **Açıklama**: Factor Analysis of Information Risk — siber riski finansal terimlerle ölçen nicel risk analiz çerçevesi. Risk = Kayıp Olasılığı × Kayıp Büyüklüğü formülü üzerine kuruludur.
- **Neden önemli**: Yönetim kuruluna ve CFO'ya riski dolar cinsinden raporlamak için tek standartlaşmış metodoloji. Soyut tehdit anlatısından somut iş etkisine geçiş sağlar.

**FAIR Uygulama Adımları:**
1. Risk senaryosu tanımla (varlık + tehdit)
2. Tehdit frekansını tahmin et (TEF, TCap, CS)
3. Kayıp büyüklüğünü hesapla (PLM, SLM)
4. Monte Carlo simülasyonu ile risk dağılımı oluştur
5. Sonuçları risk iştahıyla karşılaştır

---

### ISO/IEC 27005: Bilgi Güvenliği Risk Yönetimi
- **Tür**: Uluslararası Standart
- **Yayıncı**: ISO/IEC
- **URL**: https://www.iso.org/standard/80585.html
- **Açıklama**: ISO/IEC 27001 BGYS kapsamında risk değerlendirme ve tedavi süreçleri için detaylı rehber. Risk tanımlama, analiz, değerlendirme ve tedavi aşamalarını kapsar.
- **Neden önemli**: ISO 27001 sertifikasyonu için pratik uygulama kılavuzu.

---

### OCTAVE Allegro
- **Tür**: Metodoloji
- **Yayıncı**: Carnegie Mellon University SEI
- **URL**: https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=8419
- **Açıklama**: Operationally Critical Threat, Asset, and Vulnerability Evaluation — bilgi varlık odaklı risk değerlendirme metodolojisi. Küçük ekiplerle harici uzman ihtiyacı olmadan uygulanabilir.
- **Neden önemli**: Pratik, workshopa dayalı yaklaşımıyla hızlı risk değerlendirmesi sağlar.

---

### Risk Appetite & Tolerance Best Practices ⭐ Best Practice
- **Tür**: Best Practice
- **Yayıncı**: ISACA
- **URL**: https://www.isaca.org/resources/isaca-journal/issues/2021/volume-4/defining-and-managing-risk-appetite
- **Açıklama**: Risk iştahı beyanı yazımı, yönetim kuruluna onaylatma ve ölçülebilir eşik belirleme rehberi.
- **Neden önemli**: Güvenlik kararlarının iş hedefleriyle hizalanması için temel yönetim aracı.

**Risk İştahı Beyanı Örnek Yapısı:**
```
[Organizasyon], müşteri verilerinin gizliliğini tehdit eden 
risklere karşı DÜŞÜK toleransa sahiptir ve bu tür riskleri 
[X] TL altında tutmayı hedefler.
```

**Key Risk Indicators (KRI) Örnekleri:**
| KRI | Eşik | Renk |
|---|---|---|
| Yama gecikmesi (kritik CVE) | > 15 gün | 🔴 |
| MFA kapsamı dışı hesaplar | > %5 | 🟡 |
| Başarısız erişim denemeleri | > 1000/gün | 🔴 |

---

## 🗺️ Risk Yönetim Süreci

```
1. KAPSAM BELİRLE          → Hangi varlıklar / süreçler?
       ↓
2. VARLIK ENVANTERİ        → Kritiklik sınıflandırması
       ↓
3. TEHDİT MODELLEME        → STRIDE / FAIR tehdit analizi
       ↓
4. RİSK DEĞERLENDİRME     → Olasılık × Etki matrisi
       ↓
5. TEDAVİ PLANI            → Kabul / Azalt / Transfer / Kaçın
       ↓
6. KONTROL UYGULAMA        → CIS Controls / ISO 27002
       ↓
7. İZLEME & RAPORLAMA     → KRI dashboard, yönetim raporu
       ↓
8. GÖZDEN GEÇİRME          → Yıllık döngü → 1. adıma dön
```

---

## 📚 İlgili Kategoriler

- [Framework & Standartlar](../frameworks-standards/README.md)
- [Uyum & Regülasyon](../compliance/README.md)
- [CISO Liderliği](../ciso-leadership/README.md)
