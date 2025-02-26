# Spelling Correction with N-grams and Beam Search

## Overview
This repository implements an advanced spelling correction system leveraging probabilistic models. It builds upon Peter Norvig's classic approach by incorporating **n-gram language models, Kneser-Ney smoothing, interpolation, and beam search** to achieve **high accuracy and efficiency**.

### Key Features:
- **Baseline (Norvig's method)**: Simple frequency-based spell correction.
- **N-gram Models (up to 5-grams)**: Context-aware corrections.
- **Add-One and Kneser-Ney Smoothing**: Improved probability estimation for unseen words.
- **Interpolation**: Combines unigram, bigram, and trigram probabilities for better accuracy.
- **Beam Search**: Efficiently finds the best possible correction sequence.

---

## Results & Analysis
### Performance Comparison
| **Model** | **Accuracy** | **Speed** | **Pros** | **Cons** |
|-----------|-------------|-----------|----------|----------|
| **Baseline (Norvig)** | 70% | Slow | Simple, frequency-based | No context awareness, slow |
| **N-grams (5) + Add-One + Beam Search** | 74% | 2× faster | Context-aware, better corrections | Requires large corpus, Add-One smoothing is naive |
| **N-grams (3) + Kneser-Ney + Interpolation + Beam Search** | **80%** | **2× faster** | Best accuracy, efficient, handles unseen words well | Still dependent on training corpus quality |

### Key Findings:
✅ **Beam Search** significantly speeds up spell correction, making all models **twice as fast** as the baseline.
✅ **Using trigrams instead of 5-grams** leads to better **data efficiency** without losing contextual accuracy.
✅ **Kneser-Ney smoothing & interpolation improve accuracy** by handling **rare words more effectively**.
✅ The **final approach (trigrams + Kneser-Ney + interpolation) is the best balance** of accuracy and efficiency.

🚀 **Next Steps:**
- Integrate **neural models (e.g., Transformers, LSTMs)** for even more accurate spell correction.
- Train on **larger and more diverse corpora** to improve generalization.
- Optimize **beam search hyperparameters** for fine-tuned accuracy-speed trade-offs.

---

## Acknowledgments
This project is inspired by **Peter Norvig’s Spelling Corrector** and leverages techniques from NLP research, particularly **Kneser-Ney Smoothing and Beam Search** for robust spelling correction.

---

## License
This project is licensed under the **MIT License**. Feel free to modify and use it in your applications.

