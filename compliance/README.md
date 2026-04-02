# ⚖️ Uyum & Regülasyon

> Ulusal ve uluslararası düzenleyici gereklilikleri karşılamak için regülasyon rehberleri ve uyum framework'leri.

---

## Kaynaklar

### GDPR — Teknik Gereklilikler
- **Tür**: Regülasyon
- **Yayıncı**: Avrupa Birliği
- **URL**: https://gdpr.eu/
- **Açıklama**: AB Genel Veri Koruma Yönetmeliği — DPIA (Veri Koruma Etki Değerlendirmesi), 72 saatlik ihlal bildirimi, DPO sorumlulukları ve teknik tedbirler.
- **Neden önemli**: AB vatandaşlarının verisini işleyen tüm organizasyonlar için zorunlu. İhlal cezası yıllık cironun %4'ü.

**GDPR Teknik Kontroller:**
- Encryption at rest & in transit
- Pseudonymization & anonymization
- Data minimization
- Privacy by Design & by Default
- Access control & audit logging
- Breach detection & notification capability

---

### PCI DSS v4.0
- **Tür**: Sektörel Standart
- **Yayıncı**: PCI Security Standards Council
- **URL**: https://www.pcisecuritystandards.org/
- **Açıklama**: Ödeme kartı endüstrisi veri güvenliği standardı v4.0. 12 gereklilik, 6 hedef. 2025 geçiş tarihi gereklilikleri dahil.
- **Neden önemli**: Kart işleyen tüm organizasyonlar için zorunlu. Uyumsuzluk kart markaları ile sözleşme feshi riskini doğurur.

**12 PCI DSS Gereklilik Alanı:**
1. Güvenlik duvarı kur ve yönet
2. Varsayılan şifreleri değiştir
3. Kart sahibi verisini koru
4. İletimde şifrele
5. Kötü amaçlı yazılımdan koru
6. Güvenli sistemler geliştir
7. Erişimi kısıtla
8. Kimlik doğrulama yönet
9. Fiziksel erişimi kısıtla
10. Erişimi izle ve kayıt tut
11. Güvenliği düzenli test et
12. Bilgi güvenliği politikası yönet

---

### DORA — Dijital Operasyonel Dayanıklılık (EU)
- **Tür**: Regülasyon
- **Yayıncı**: Avrupa Birliği / EIOPA
- **URL**: https://www.eiopa.europa.eu/dora
- **Açıklama**: AB finansal kurumları için ICT risk yönetimi, olay raporlama, TLPT (Threat-Led Penetration Testing) ve üçüncü taraf ICT sağlayıcı yönetimi.
- **Neden önemli**: 2025 yürürlük. AB'deki finans sektörü CISO'ları için en kapsamlı regülasyon.

---

### KVKK — Teknik Tedbirler Rehberi
- **Tür**: Ulusal Regülasyon
- **Yayıncı**: Kişisel Verileri Koruma Kurumu (Türkiye)
- **URL**: https://www.kvkk.gov.tr/
- **Açıklama**: Türkiye kişisel veri koruma mevzuatı — teknik ve idari tedbirler, veri sorumluları sicili (VERBİS), açık rıza gereklilikleri.
- **Neden önemli**: Türkiye'de faaliyet gösteren tüm kuruluşlar için yasal zorunluluk.

---

## 🗺️ Uyum Haritası

```
ISO 27001 ────── temel güvenlik kontrolleri ──────→ GDPR
    ↕                                                  ↕
NIST CSF ──── risk yönetimi ────→ PCI DSS / KVKK
    ↕                                                  ↕
CIS Controls ── teknik kontroller ──────────→ DORA
```

## 📚 İlgili Kategoriler

- [Framework & Standartlar](../frameworks-standards/README.md)
- [Risk Yönetimi](../risk-management/README.md)
- [Data Security](../data-security/README.md)
