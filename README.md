#  SpeechT5 Fine-tuning for Moroccan Darija TTS

Fine-tuning [Microsoft's SpeechT5](https://huggingface.co/microsoft/speecht5_tts) 
model for **Text-to-Speech in Moroccan Darija** (Arabizi + Arabic script) 
using a custom Parquet audio dataset.

##  Features

- Loads and merges multi-part Parquet audio datasets from Google Drive
- Preprocesses Darija text (Arabic normalization, Arabizi → Arabic mapping, accent removal)
- Extracts speaker embeddings using SpeechBrain's x-vector model
- Fine-tunes SpeechT5 with Hugging Face `Seq2SeqTrainer`
- Includes a TTS evaluation system (audio quality + speech rate scoring)

##  Tech Stack

- Python, Google Colab
- Hugging Face Transformers & Datasets
- SpeechBrain
- Librosa, SoundFile
- Pandas, PyTorch

##  How to Run

1. Open `Code_TTS.ipynb` in Google Colab
2. Mount your Google Drive
3. Place your dataset Parquet files in the Drive
4. Run cells sequentially

##  Model

Base model: [`microsoft/speecht5_tts`](https://huggingface.co/microsoft/speecht5_tts)  
Vocoder: [`microsoft/speecht5_hifigan`](https://huggingface.co/microsoft/speecht5_hifigan)

## 📁 Dataset

Multi-part Parquet dataset containing Darija audio + text pairs (Arabizi and Arabic script).
