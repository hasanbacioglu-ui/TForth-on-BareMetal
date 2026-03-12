# TForth-on-BareMetal
Türkçe Forth ile BareMetal OS üzerinde Deterministik AI Co-Design Mimarisi
# TForth-on-BareMetal: Deterministik AI için Donanım-Yazılım Birlikte Tasarımı

## Vizyon
Bu proje, günümüzün stokastik (rastgelelik içeren) ve kara kutu yapay zeka sistemlerine bir alternatif inşa etmeyi amaçlar. Hedef, **tamamen deterministik, açıklanabilir ve bare-metal seviyesinden başlayarak birlikte tasarlanmış (co-designed)** bir AI yığını oluşturmaktır.

Temel bileşenler:
1.  **TForth:** Zig dilinin güvenliği ve modern özellikleriyle güçlendirilmiş, Türkçe anahtar kelimelere sahip bir Forth varyantı.
2.  **BareMetal OS:** Ian Seyler tarafından geliştirilen, yüksek performanslı, öngörülebilir gecikmeli 64-bit işletim sistemi.
3.  **Deterministik AI Çekirdeği:** CAA (Compositional Agentic Architecture) ilkelerine uygun, kural tabanlı ve durum makineleriyle çalışan AI ajanları.
4.  **Küresel Zeka Ağı (KZA):** "Wolf" (güçlü sunucular) ve "Mikorizal Mesh" (edge cihazlar) düğümlerinden oluşan, dağıtık hesaplama ağı.

## Neden?
Askeriye, tıp, finans ve kritik altyapı sistemleri için kararlar **izlenebilir, tekrarlanabilir ve denetlenebilir** olmalıdır. Mevcut LLM'ler ve GAN'lar bu gereksinimi karşılayamaz. Bu proje, bu boşluğu doldurmayı hedefler.

## Teknik Yol Haritası
1.  **Aşama 0 (Temel):** BareMetal OS üzerinde minimal bir Forth yorumlayıcısının (TForth çekirdeği) Zig ile yazılması.
2.  **Aşama 1 (Sistem):** TForth'a Türkçe kelimeler, AIOON (AI Oriented Object Notation) desteği ve temel donanım erişim kelimelerinin eklenmesi.
3.  **Aşama 2 (AI Çekirdek):** CAA blueprint'ine uygun, deterministik ajanların TForth kelimeleri seti olarak tanımlanması.
4.  **Aşama 3 (Ağ):** Dağıtık görev sıralayıcı ve KZA protokolünün tasarımı.

## İlk Adım: `boot.forth`
Proje, `boot.forth` dosyası ile başlar. Bu dosya, TForth yorumlayıcısı çalıştığında ilk yüklenen temel kelimeleri ve sistem mesajını içerir.
