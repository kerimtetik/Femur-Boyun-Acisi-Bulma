# Femur Boyun Açısı (FBA) Ölçüm Aracı  
Pelvik X-ray görüntülerinden **femur boyun açısını** (femoral neck-shaft angle) otomatik ve tekrarlanabilir biçimde hesaplayan açık kaynak kodlu Python projesi.

---

## Projenin Amacı  
- **Klinik destek:** Ortopedi hekimleri ve radyologlara, manuel ölçüm hatalarını azaltarak olası **kalça displazisi, varus/valgus deformiteleri** ve travma sonrası açısal bozuklukları daha hızlı saptama olanağı sunmak.  
- **Araştırma altyapısı:** Görüntü işleme‐temelli kemik geometrisi çalışmalarında tekrar kullanılabilir, modüler bir çerçeve sağlamak.  
- **Eğitim:** Tıp fakültesi ve biyomedikal mühendisliği öğrencilerine, gerçek X-ray verisi üzerinde segmentasyon, özellik çıkarımı ve geometri analizini uçtan uca gösteren bir örnek proje sunmak.

---

## Temel Özellikler
- 🔍 **Ön-işleme:** Min-Max normalizasyon + CLAHE kontrast artırma  
- 🟢 **Segmentasyon:** 2 bileşenli Gaussian Mixture Model (GMM) + Otsu eşiği  
- 📏 **Geometrik Analiz:** Kontur tabanlı eksen bulma, merkez-çember yaklaşımı ile açı hesabı  
- 🩻 **CLI ve Notebook:** Komut satırı (train / predict) ve Jupyter demosu  
- 🧪 **Testler ve CI:** Pytest senaryoları, GitHub Actions ile otomatik test - lint  
- 💾 **Model Kaydetme:** Eğitilen GMM modelleri `joblib` ile saklanır  
- 🚀 **Hızlı Çalıştırma:** Tek görüntü veya klasör üzerinden toplu koşum

---

## Teknolojiler
| Python | Görüntü İşleme | ML / Yardımcı |  
|:------:|:--------------:|:-------------:|  
| 3.9+   | OpenCV         | scikit-learn, joblib|  
|        | NumPy          | tqdm, pandas |

---

## Kurulum
```bash
git clone https://github.com/<kerimtetik>/Femur-Boyun-Acisi-Bulma.git
cd Femur-Boyun-Acisi-Bulma
python -m venv venv && source venv/bin/activate        # Win: venv\Scripts\activate
pip install -r requirements.txt
