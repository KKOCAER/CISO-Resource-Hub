# 🏭 OT / ICS Güvenliği

> Endüstriyel kontrol sistemleri, SCADA ve operasyonel teknoloji ortamlarını korumak için standart, rehber ve best practice'ler.

---

## Kaynaklar

### IEC 62443 ⭐ Best Practice
- **Tür**: Uluslararası Standart Serisi
- **Yayıncı**: IEC (International Electrotechnical Commission)
- **URL**: https://www.iec.ch/iec62443
- **Açıklama**: Endüstriyel otomasyon ve kontrol sistemleri (IACS) güvenliği için kapsamlı standart serisi. Zone/Conduit modeli, Security Level (SL) tanımları ve rol bazlı gereklilikler.
- **Neden önemli**: OT/ICS güvenlik programının omurgası. Tedarikçi, entegratör ve işletmeci için ayrı gereklilikler tanımlar.

**IEC 62443 Serisi:**
| Seri | Başlık | Hedef Kitle |
|---|---|---|
| 62443-1-x | Genel Kavramlar | Tüm paydaşlar |
| 62443-2-x | Politika & Prosedürler | İşletmeciler |
| 62443-3-x | Sistem Gereklilikleri | Sistem entegratörler |
| 62443-4-x | Bileşen Gereklilikleri | Ürün geliştiriciler |

**Security Level Tanımları:**
- **SL 1**: Kazara veya tesadüfi ihlallere karşı koruma
- **SL 2**: Kasıtlı basit araçlarla ihlale karşı koruma
- **SL 3**: Gelişmiş araç ve kaynaklarla ihlale karşı koruma
- **SL 4**: Devlet destekli aktörlere karşı koruma

---

### NIST SP 800-82 Rev.3: OT Security Guide ⭐ Best Practice
- **Tür**: Rehber
- **Yayıncı**: NIST
- **URL**: https://csrc.nist.gov/publications/detail/sp/800-82/rev-3/final
- **Açıklama**: ICS, SCADA, DCS ve PLC güvenliği için kapsamlı NIST kılavuzu. OT ağ segmentasyonu, güvenlik kontrol uygulaması ve IT/OT convergence yönetimi.
- **Neden önemli**: IT güvenlik kontrollerinin OT ortamına doğrudan uygulanamayacağını gösterir. OT'ye özgü güvenlik yaklaşımı için temel.

**OT vs IT Güvenlik Farkları:**
| Boyut | IT | OT |
|---|---|---|
| Öncelik | CIA (Gizlilik önce) | AIC (Erişilebilirlik önce) |
| Yama yönetimi | Hızlı döngü | Planlı bakım penceresi |
| Test ortamı | Mevcut | Genellikle yok |
| Protokoller | TCP/IP standart | Modbus, DNP3, Profinet |
| Ömür | 3-5 yıl | 15-25 yıl |
| Güncelleme | Düzenli | Kısıtlı / üretici bağımlı |

---

### MITRE ATT&CK for ICS
- **Tür**: Bilgi Tabanı
- **Yayıncı**: MITRE Corporation
- **URL**: https://attack.mitre.org/matrices/ics/
- **Açıklama**: Endüstriyel kontrol sistemlerine yönelik saldırı taktikleri ve tekniklerinin matrisi. Gerçek ICS saldırılarından (Triton, Industroyer, Stuxnet) derlendi.
- **Neden önemli**: OT tehdit modelleme ve ICS-CERT tavsiyelerinin pratik çerçevesi.

**Kritik ICS Saldırı Teknikleri:**
- T0816 — Device Restart/Shutdown
- T0855 — Unauthorized Command Message
- T0836 — Modify Parameter
- T0826 — Loss of Availability
- T0831 — Manipulation of Control

---

### CISA ICS Advisories
- **Tür**: Kamu Kaynağı
- **Yayıncı**: CISA (Cybersecurity and Infrastructure Security Agency)
- **URL**: https://www.cisa.gov/ics-advisories
- **Açıklama**: ICS güvenlik açıkları ve tehdit duyuruları. Enerji, su, ulaşım, sağlık gibi kritik altyapı sektörlerine yönelik.
- **Neden önemli**: Ücretsiz, gerçek zamanlı tehdit istihbaratı. ICS ürün güvenlik açıklarının takibi için temel kaynak.

---

### OT Güvenlik Programı Best Practices ⭐ Best Practice
- **Tür**: Best Practice Koleksiyonu
- **Yayıncı**: SANS ICS
- **URL**: https://www.sans.org/reading-room/whitepapers/ICS/
- **Açıklama**: IT/OT convergence güvenlik yönetimi, passive asset discovery, OT SOC kurulumu, Purdue modeli uygulama kılavuzu ve ICS güvenlik programı olgunluk değerlendirmesi.
- **Neden önemli**: Pratik uygulama rehberleri ile OT güvenlik ekibi kurmak için başlangıç noktası.

---

### NERC CIP Standartları
- **Tür**: Sektörel Standart
- **Yayıncı**: NERC (North American Electric Reliability Corporation)
- **URL**: https://www.nerc.com/pa/Stand/Pages/CIPStandards.aspx
- **Açıklama**: Kuzey Amerika elektrik altyapısı siber güvenlik standartları. Kritik altyapı CISO'ları için sektörel referans çerçeve.
- **Neden önemli**: Enerji sektörü için zorunlu uyum. Kritik altyapı koruması modellemesi için referans.

---

## 🏗️ OT Güvenlik Mimarisi Best Practice

### Purdue Model — Ağ Segmentasyonu

```
┌────────────────────────────────────────────────┐
│  Seviye 5: Enterprise Network (IT)              │
├────────────────────────────────────────────────┤
│  ══════════ DMZ / Firewall ══════════           │
├────────────────────────────────────────────────┤
│  Seviye 4: Site Business Planning               │
├────────────────────────────────────────────────┤
│  ══════════ DMZ / Data Diode ══════════         │
├────────────────────────────────────────────────┤
│  Seviye 3: Site Operations (Historian, OPC)     │
├────────────────────────────────────────────────┤
│  Seviye 2: Supervisory (SCADA, HMI, EWS)        │
├────────────────────────────────────────────────┤
│  Seviye 1: Control (PLC, DCS, RTU)              │
├────────────────────────────────────────────────┤
│  Seviye 0: Field Devices (Sensörler, Aktüatörler│
└────────────────────────────────────────────────┘
```

### OT Güvenlik Program Adımları

1. **Varlık Envanteri** — Pasif keşif araçları (Claroty, Dragos, Nozomi)
2. **Ağ Görünürlüğü** — OT trafik analizi, protokol profilleme
3. **Segmentasyon** — Purdue modeli uygulaması, DMZ tasarımı
4. **Güvenli Uzaktan Erişim** — Jump server, MFA, oturum kaydı
5. **Zafiyet Yönetimi** — Patch önceliklendirme (üretici koordinasyonu)
6. **Olay Müdahale** — OT'ye özgü IR playbook
7. **Personel Eğitimi** — OT güvenlik farkındalığı

---

## 📚 İlgili Kategoriler

- [Tehdit İstihbaratı](../threat-intelligence/README.md)
- [Olay Müdahale & BCP](../incident-response/README.md)
- [Framework & Standartlar](../frameworks-standards/README.md)
