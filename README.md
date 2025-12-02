JalanJalan.ai — AI Agent Travel Planner

Deskripsi
- `JalanJalan.ai` adalah prototipe asisten perjalanan bertenaga AI yang membantu merancang rencana wisata di Indonesia. Proyek ini mengorkestrasi beberapa agen (weather/location, destination discovery, budget estimation, dan coordinator) untuk menghasilkan rekomendasi destinasi, itinerari singkat, serta estimasi biaya.

Fitur utama
- Rekomendasi destinasi yang mempertimbangkan cuaca dan lokasi.
- Estimasi biaya (entrance fee + biaya tambahan sederhana).
- Arsitektur multi-agent menggunakan Google ADK (contoh penggunaan `google.adk`).
- Notebook siap dijalankan di Jupyter / VS Code / Kaggle (beberapa sel menunjukkan cara memuat API key dari `.env`).

Notebook dalam repository
- `jalanjalankaggle.ipynb`: Demo dan pengenalan JalanJalan.ai, inisialisasi agen, contoh panggilan `InMemoryRunner` untuk debugging dan pengujian alur agen.
- `notebokagenttravelplaner.ipynb`: Notebook lain yang berisi versi/variasi agent initializer dan coordinator yang serupa — juga menyediakan contoh alur dan pengujian.

Persyaratan
- Python 3.8+ (virtual environment sangat direkomendasikan).
- Dependensi di `requirements.txt` (contoh: `google-adk`, `python-dotenv`, `geopy`, `pandas`, `requests`).

Instalasi (PowerShell)
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Menjalankan notebook
- Buka `jalanjalankaggle.ipynb` atau `notebokagenttravelplaner.ipynb` di Jupyter atau VS Code dan jalankan sel dari atas ke bawah.
- Jika menggunakan API nyata, buat file `.env` di folder proyek dengan variabel (contoh):
```text
GOOGLE_API_KEY=your_google_api_key_here
# (opsional) OWM_API_KEY=your_openweathermap_api_key
```

Catatan teknis
- Notebook menggunakan komponen dari `google.adk` (Agent Development Kit) termasuk `Agent`, `InMemoryRunner`, dan `google_search` sebagai contoh tool. Untuk menjalankan panggilan model dan tools yang memerlukan kredensial, pastikan API key terkait sudah tersedia di `.env` atau environment.
- Estimasi biaya di notebook bersifat sederhana; untuk akurasi, Anda bisa mengganti logika estimasi dengan tarif resmi/lookup API.

Struktur proyek
- `jalanjalankaggle.ipynb` — Notebook utama (demo + agent examples).
- `notebokagenttravelplaner.ipynb` — Notebook tambahan/variasi.
- `requirements.txt` — daftar dependency.

Danang Agung Restu Aji
https://linkedin.com/in/Profdara

