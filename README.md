# 🎵 Instant Music Recommendation System (Streamlit + Python)

An AI‑powered **Content‑Based Music Recommendation System** built with **Streamlit, scikit‑learn, NLTK, and Pandas**.  
Given a song, it recommends similar songs based on **lyrics similarity** using **TF‑IDF Vectorization** and **Cosine Similarity**.

---

## 📌 Features

- **🎧 Content‑Based Recommendation** — Finds similar songs by analyzing their lyrics.
- **🧹 Automated Preprocessing** — Cleans and tokenizes lyrics, removes stopwords, and extracts features.
- **📐 TF‑IDF + Cosine Similarity** — Measures song similarity in vector space.
- **⚡ Fast Recommendations** — Preprocessing is done offline and stored for quick lookup.
- **🌐 Streamlit Web App** — Simple browser interface for instant results.

---

## 🛠 Technology Stack

- **Python 3.10+**
- **[Streamlit](https://streamlit.io/)** – Web app framework
- **Pandas & NumPy** – Data handling
- **scikit-learn** – TF‑IDF & Cosine Similarity
- **NLTK** – Tokenization & Stopwords removal
- **Joblib** – Saving preprocessed data

---

## 📂 Project Structure

📁 music-recommendation-system/

├── app.py # Streamlit front-end app

├── preprocess.py # Dataset cleaning & TF-IDF computation

├── recommend.py # Similarity search logic

├── requirements.txt # Python dependencies

├── spotify_millsongdata.csv # Dataset (from Kaggle)

├── Music_recommendation_system.ipynb # Jupyter notebook (EDA/Experiments)

├── df_cleaned.pkl # Preprocessed dataset (generated)

├── cosine_sim.pkl # Cosine similarity matrix (generated)

└── Start_app.txt # Commands to set up and run


---

## 📊 How It Works

### 1️⃣ Data Preprocessing (`preprocess.py`)
- Loads and samples the Million Song Dataset from Kaggle.
- Cleans lyrics:
  - Removes punctuation and special characters
  - Converts to lowercase
  - Removes English stopwords
- Converts lyrics into **TF‑IDF feature vectors**.
- Computes a **Cosine Similarity matrix** between songs.
- Saves `df_cleaned.pkl`, `tfidf_matrix.pkl`, `cosine_sim.pkl` for fast loading.

### 2️⃣ Song Recommendation (`recommend.py`)
- Loads preprocessed data and similarity matrix.
- Finds the most similar songs to the user‑selected song.
- Returns **Artist & Song Name** in a nicely formatted table.

### 3️⃣ Interactive UI (`app.py`)
- User selects a song from dropdown list.
- Clicking **"Recommend"** instantly shows top similar tracks.

---

## 🚀 Installation & Setup

### 1. Clone the Repository
git clone https://github.com/ankithbalda/Music_recommendation.git

cd Music_recommendation

### 2. Install Requirements
pip install -r requirements.txt


### 3. Download & Prepare Data
- Download **Spotify Million Song Dataset** from Kaggle:  
  [https://www.kaggle.com/datasets/notshrirang/spotify-million-song-dataset](https://www.kaggle.com/datasets/notshrirang/spotify-million-song-dataset)
- Place `spotify_millsongdata.csv` in the project folder.

- Run preprocessing:
python preprocess.py


### 4. Launch Web App
streamlit run app.py

---

## 🎯 Example Usage

1. Open browser at `http://localhost:8501`.
2. Select a favorite song.
3. Click **"🚀 Recommend Similar Songs"**.
4. View a table of similar songs with artist names.

---

## 📈 Possible Improvements
- Add **Genre-based filtering** to refine recommendations.
- Enable **search by lyrics snippet**.
- Deploy the app on **Streamlit Cloud** or **Heroku**.

---

## 👨‍💻 Author
**Name:** Ankith Balda

**Email:** ankithbalda.wk@gmail.com

**LinkedIn:** https://www.linkedin.com/in/ankith-balda-812177278/

**GitHub:** https://github.com/ankithbalda

---

