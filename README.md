# LexAI: Bilişim Hukukunda Yapay Zeka Destekli Asistanınız

Bu proje, İstanbul Üniversitesi - Cerrahpaşa Bilgisayar Mühendisliği bölümünde 2025 yılı Bitirme Projesi kapsamında hazırlanmıştır.  
LexAI, Türk Bilişim Hukuku özelinde geliştirilmiş, yapay zeka destekli bir hukuki araştırma ve karar destek sistemidir.
Ayrıca bu proje, **TÜBİTAK 2209-A Üniversite Öğrencileri Araştırma Projeleri Destekleme Programı** kapsamında desteklenmiştir.

## Proje Amacı

Günümüzde büyük dil modelleri (LLM), hukuki metinlerle çalışırken doğruluk, kaynak gösterme ve alan bilgisi gibi konularda yetersiz kalabilmektedir. Bu projede, Türk hukuk sistemine özel bir bilgi tabanıyla çalışan ve alana özgü fine-tune edilmiş embedding modeli kullanan gelişmiş bir Retrieval-Augmented Generation (RAG) mimarisi tasarlanmıştır.

## Proje Bileşenleri

- **Veri Tabanı**: KVKK, TCK, 5651 Sayılı Kanun, yönetmelikler ve kurul kararlarından oluşan yapılandırılmış veri kümesi
- **Gelişmiş Arama Katmanı**:
  - Anlamsal arama için FAISS
  - Anahtar kelime araması için BM25
  - Hibrit skor birleştirme ve Cross-Encoder ile yeniden sıralama
- **Model Eğitimi**:
  - `intfloat/multilingual-e5-large` modeli üzerine, bilişim hukuku verileriyle contrastive learning tabanlı fine-tuning
- **Cevap Üretimi**:
  - Meta-Llama 3.1 8B-Instruct modeli ile, gerekçeli ve kaynak gösteren yanıtlar
- **Sunum**: React tabanlı frontend ve Flask API ile çalışan bir web uygulaması

## Sonuçlar

- Fine-tuning sonrası Recall@1 değeri %10’dan fazla artmıştır.
- MRR skorlarında da anlamlı iyileşmeler gözlenmiştir.
- Sistem, hem doğruluk hem de kullanıcıya sunduğu cevapların açıklayıcılığı bakımından klasik arama motorlarının ötesine geçmektedir.

## Belgeler

- **Tez (PDF)**: [LexAI_Tez.pdf](./LexAI_Tez.pdf)
- **Proje Posteri**: [LexAI_Poster.pdf](./LexAI_Poster.pdf)

## Ekip

- Yağmur Gökçekli [LinkedIn Profili](https://www.linkedin.com/in/yagmurgokcekli/)
- Musa Berke Şengöz [LinkedIn Profili](https://www.linkedin.com/in/musaberkesengoz/)
- Danışman: Dr. Öğr. Üyesi Ramiz Görkem Birdal

## İletişim

Proje hakkında daha fazla bilgi almak isterseniz LinkedIn üzerinden iletişime geçebilirsiniz.
