# Veri seti ile Lityum İyon Pil Enerji Verimlilği Analizi ile karbon Nötr Hedefi Doğrultusunda Modelleme Örneği

Bu depo, NASA Ames Prognostics Center of Excellence (PCoE) tarafından yayınlanan **B0001-B0025** serisi lityum iyon batarya veri setleri üzerinde gerçekleştirilen kapsamlı bir enerji verimliliği analizi (SoEE), dQ/dV diferansiyel kapasite teşhisi ve operasyonel karbon nötr modelleme çalışmasını içermektedir.

## 🚀 Proje Motivasyonu ve Önemi

Batarya teknolojileri, küresel enerji dönüşümünün ve karbon nötr hedeflerinin merkezinde yer almaktadır. Geleneksel batarya analizleri genellikle kapasite kaybı (**State of Health - SoH**) üzerine odaklanırken, bu çalışma operasyonel enerji verimliliği (**State of Energy Efficiency - SoEE**) ve bunun çevresel etkileri üzerine yoğunlaşmıştır.

### Temel Motivasyonlar:
*   **Gizli Verimlilik Kayıplarının Ortaya Konulması:** Kapasite kaybının ötesinde, batarya operasyonlarındaki enerji israfının ekonomik ve çevresel maliyetlerinin belirlenmesi.
*   **Karbon Nötr Hedeflerine Katkı:** Batarya sistemlerinin operasyonel karbon ayak izini doğrudan ölçen ve optimize eden yeni metrikler (**OCS** ve **ECA**) sunulması.
*   **Endüstriyel Uygulanabilirlik:** Batarya Yönetim Sistemleri (BMS) ve Dijital Batarya Pasaportu (DBP) gibi geleceğin teknolojileri için veri tabanlı, non-invazif teşhis stratejileri geliştirilmesi.

## 🔬 Bilimsel Hipotezler

Bu çalışma, aşağıdaki üç temel bilimsel hipotez üzerine inşa edilmiştir:

1.  **H1 (Yük Profili Etkisi):** Bataryanın maruz kaldığı yük profili (akım seviyesi), enerji verimliliği kaybının hızı ve büyüklüğü üzerinde doğrudan bir etkiye sahiptir.
2.  **H2 (dQ/dV Korelasyonu):** dQ/dV eğrilerindeki zirve kaymaları (peak shift), bataryanın operasyonel enerji verimliliği kaybı ile güçlü ve istatistiksel olarak anlamlı bir korelasyon gösterir.
3.  **H3 (Doğrusal Emisyon İlişkisi):** Batarya sistemlerindeki her bir birim enerji verimliliği kaybı, şebekeden çekilen ek enerji nedeniyle doğrudan ve doğrusal bir operasyonel karbon emisyonu artışına neden olur.

## ✨ Temel Özellikler ve Metrikler

*   **SoEE (State of Energy Efficiency):** Bataryanın iç direncinden kaynaklanan ısı kayıplarını hesaba katarak gerçek enerji israfını ölçen metrik.
*   **dQ/dV Teşhisi:** Savitzky-Golay filtresi ile gürültüden arındırılmış, batarya içindeki elektrokimyasal reaksiyonların faz geçişlerini temsil eden analiz yöntemi.
*   **OCS (Operasyonel Karbon Skoru):** Batarya verimlilik kaybı nedeniyle 1 GWh ölçeğinde oluşan toplam operasyonel emisyonun (Ton CO₂) nicel ifadesi.
*   **ECA (Verimlilik Katkısı):** Belirli bir verimlilik optimizasyonu ile sağlanabilecek potansiyel karbon tasarrufu.

## 📊 Öne Çıkan Bulgular

*   **Ortalama SoEE Kaybı:** 25 bataryada ortalama **%14.12** enerji verimliliği kaybı tespit edilmiştir.
*   **dQ/dV - SoEE Korelasyonu:** Zirve kayması ile verimlilik kaybı arasında **r = 0.933** (p < 0.001) gibi çok güçlü bir korelasyon bulunmuştur.
*   **Karbon Etkisi:** 1 GWh ölçeğindeki bir sistemde, verimlilik kayıpları nedeniyle oluşan toplam operasyonel emisyon **1,589 Ton CO₂** olarak hesaplanmıştır.
*   **Doğrusal İlişki:** Her %1'lik verimlilik kaybı, 1 GWh sistemde yaklaşık **4.5 Ton CO₂** ek emisyona neden olmaktadır (r = 1.000).

## 📁 Depo Yapısı

```text
├── data/                       # Analiz için kullanılan özetlenmiş batarya verileri (CSV)
│   └── battery_summary.csv
├── scripts/                    # Python analiz ve simülasyon kodları
│   └── comprehensive_analysis.py
├── matlab/                     # MATLAB Toolbox kodları
│   └── Nasa_Battery_Efficiency_Toolbox.m
├── reports/                    # Kapsamlı akademik raporlar (DOCX, PDF)
│   ├── ProjeGenelRapor.docx
│   └── ProjeGenelRapor.pdf
├── plots/                      # Analiz sonuçlarının görselleştirmeleri (PNG)
│   ├── fig1_dqdv_analysis.png
│   └── ... (diğer grafikler)
├── README.md                   # Bu dosya
└── LICENSE                     # MIT Lisans bilgileri
```

## 🛠️ Metodoloji ve Hesaplama

Proje, NASA B0001-B0025 veri setlerini temel alarak fizik tabanlı bir simülasyon altyapısı kullanır. İç direnç (R) modellemesi için **Power Law (Güç Yasası)** fonksiyonu uygulanmış, enerji hesaplamaları için **sayısal integral (trapz)** yöntemleri kullanılmıştır. dQ/dV analizinde ise **Savitzky-Golay** filtresi ile sinyal işleme teknikleri uygulanmıştır.

## 📄 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakınız.

## 👤 Yazar

**bgezer**

---
*Bu çalışma, batarya teknolojilerinin sürdürülebilir geleceği için kritik bir adım atmaktadır.*
