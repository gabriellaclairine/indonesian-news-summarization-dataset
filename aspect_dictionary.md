# 📚 Aspect Keyword Dictionary

This document details the manually curated **aspect keyword dictionary** used to evaluate **Aspect Coverage** in our Indonesian news summarization experiments.

## 📌 Overview

Each aspect represents a major news domain defined by a set of **domain-specific keywords**. These keywords are used to approximate aspect-related content in news articles and summaries, enabling a **recall-based evaluation** that measures how well generated summaries preserve core thematic information.

The dictionary is designed to be **transparent, interpretable, and linguistically appropriate** for the Indonesian news context.

## 🗂 Aspect Categories

We define five aspect categories that align with common editorial sections used by major Indonesian news portals (e.g., *Detik*, *Kompas*):

1. **Ekonomi & Keuangan** (Economy & Finance)  
2. **Hukum & Kriminalitas** (Law & Crime)  
3. **Politik & Kebijakan Publik** (Politics & Public Policy)  
4. **Pembangunan & Lingkungan** (Development & Environment)  
5. **Sosial & Kemasyarakatan** (Social & Community Affairs)

## 🔍 Curation Methodology

The aspect keywords were **manually curated** following a structured validation process to ensure relevance and quality:

1. **Corpus Observation**  
   Candidate keywords were identified through manual inspection of frequently occurring terms in Indonesian news articles within each domain.

2. **Semantic Relevance**  
   Keywords were selected based on strong and unambiguous associations with their corresponding aspect (e.g., *inflasi* for economics, *korupsi* for law).

3. **Editorial Metadata Alignment**  
   Selection was informed by category labels and topical cues provided by the news source to ensure consistency with real-world news classification practices.

4. **Domain Coverage Check**  
   Keywords were verified to collectively cover core subtopics (actors, processes, policies, and outcomes) while avoiding overly generic terms.

5. **Manual Pruning**  
   Ambiguous keywords or those with high overlap across categories were removed to maintain aspect specificity.

Manual curation was preferred over automatic keyword extraction to prioritize **interpretability, control, and transparency** in the evaluation metric.

## 📖 Aspect Keyword Dictionary

The following Python dictionary can be directly used in evaluation scripts:

```python
ASPECT_KEYWORDS = {
    'Ekonomi & Keuangan': [
        'ekonomi', 'keuangan', 'rupiah', 'dollar', 'inflasi', 'bank', 'bi',
        'investasi', 'pajak', 'anggaran', 'apbn', 'apbd', 'belanja', 'harga',
        'saham', 'ihsg', 'obligasi', 'kredit', 'bunga', 'pinjaman', 'utang',
        'ekspor', 'impor', 'perdagangan', 'industri', 'manufaktur', 'umkm',
        'pengangguran', 'phk', 'gaji', 'upah', 'umr', 'subsidi', 'blt'
    ],
    'Hukum & Kriminalitas': [
        'hukum', 'kriminal', 'pidana', 'perdata', 'pengadilan', 'mahkamah',
        'jaksa', 'hakim', 'terdakwa', 'tersangka', 'saksi', 'bukti', 'vonis',
        'korupsi', 'kpk', 'tipikor', 'suap', 'gratifikasi', 'pencucian',
        'narkoba', 'narkotika', 'bnn', 'penangkapan', 'ditangkap', 'ditahan',
        'penjara', 'lapas', 'bebas', 'banding', 'kasasi', 'pk', 'eksekusi',
        'pembunuhan', 'pencurian', 'penipuan', 'penggelapan', 'kekerasan'
    ],
    'Politik & Kebijakan Publik': [
        'politik', 'kebijakan', 'pemerintah', 'negara', 'presiden', 'wakil',
        'menteri', 'kabinet', 'dpr', 'dprd', 'mpr', 'dpd', 'legislatif',
        'eksekutif', 'yudikatif', 'undang', 'peraturan', 'regulasi', 'uu',
        'pemilu', 'pilkada', 'pilpres', 'partai', 'koalisi', 'oposisi',
        'kampanye', 'suara', 'kpu', 'bawaslu', 'demokrat', 'golkar', 'pdip',
        'diplomasi', 'bilateral', 'multilateral', 'kerjasama', 'perjanjian'
    ],
    'Pembangunan & Lingkungan': [
        'pembangunan', 'infrastruktur', 'konstruksi', 'proyek', 'jalan',
        'tol', 'jembatan', 'bandara', 'pelabuhan', 'kereta', 'mrt', 'lrt',
        'lingkungan', 'alam', 'hutan', 'laut', 'sungai', 'gunung', 'pantai',
        'bencana', 'banjir', 'gempa', 'tsunami', 'longsor', 'kebakaran',
        'iklim', 'cuaca', 'bmkg', 'polusi', 'sampah', 'limbah', 'emisi',
        'energi', 'listrik', 'pln', 'pertamina', 'bbm', 'solar', 'gas'
    ],
    'Sosial & Kemasyarakatan': [
        'sosial', 'masyarakat', 'rakyat', 'warga', 'penduduk', 'komunitas',
        'pendidikan', 'sekolah', 'universitas', 'kampus', 'siswa', 'mahasiswa',
        'kesehatan', 'rumahsakit', 'puskesmas', 'dokter', 'pasien', 'obat',
        'covid', 'corona', 'vaksin', 'pandemi', 'protokol', 'masker',
        'kemiskinan', 'miskin', 'bantuan', 'bansos', 'pkh', 'bpjs',
        'keluarga', 'anak', 'perempuan', 'lansia', 'disabilitas', 'budaya'
    ]
}
```

## ⚠️ Limitations

This aspect keyword dictionary serves as a **lexical proxy** for evaluating aspect coverage. It is not intended to be exhaustive and may not capture implicit meanings, paraphrased expressions, or highly abstract representations of an aspect. In addition, the reliance on surface-form keyword matching may underestimate aspect coverage when semantically relevant content is expressed using different wording. Nevertheless, the dictionary provides a transparent and interpretable baseline for measuring domain-specific content retention in generated summaries.
