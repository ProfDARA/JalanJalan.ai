AI Multi-Agent Trip Planner

Deskripsi
- Notebook `ai_agents.ipynb` mengimplementasikan beberapa agent: Supervisor, Weather, Places (wisata), Accommodation, dan Cost.
- Supervisor mengumpulkan laporan dari agen-agen tersebut lalu menghasilkan 3 skenario rekomendasi: `budget`, `balanced`, `premium`.

Cara pakai (singkat)
1. Pastikan Python 3.8+ terpasang. Gunakan virtualenv/venv direkomendasikan.
2. Instal dependency:

Powershell:
```
python -m pip install -r requirements.txt
```

3. (Opsional) Buat file `.env` di folder yang sama dan tambahkan API keys jika ingin data nyata:
```
OWM_API_KEY=your_openweathermap_api_key
GOOGLE_PLACES_API_KEY=your_google_places_api_key
```

4. Buka `ai_agents.ipynb` di Jupyter/VS Code dan jalankan sel-sel dari atas ke bawah. Ada sel yang mendemokan pemanggilan `run_trip_planner` yang menggunakan fallback data bila API keys tidak tersedia.

Catatan
- Jika Anda ingin saya bantu mengintegrasikan API keys Anda (contoh: tuning kueri Google Places, handling pagination, caching), beri tahu dan saya tambahkan sel-sel tersebut.
- Estimasi biaya pada notebook bersifat sederhana dan menggunakan asumsi tarif tetap yang bisa Anda sesuaikan.
