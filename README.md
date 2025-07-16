# 🌾 Crop-Bug Detection

A full-stack web application for smart agriculture: growers can upload crop/leaf images to detect bugs/diseases and receive AI-based crop recommendations based on soil and environmental data.

![Crop-Bug Detection Screenshot](path/to/screenshot.png)

## 🚀 Features

- **Crop & Disease Detection**  
  Detect plant diseases or pest damage in uploaded images using AI-powered image recognition.

- **Crop Recommendations**  
  Get suggestions for optimal crops based on soil properties (N, P, K, pH, moisture), weather data, and geographic region.

- **Soil-Report Insights**  
  Analyze soil test reports and explain what your soil needs—based on nutrient profiles like nitrogen, phosphorus, potassium, and pH.

- **Real-Time Weather Integration**  
  Get local weather forecasts to help you plan farming activities and safeguard crops.

- **Market Price & Advisory Data**  
  Access up-to-date crop-market pricing and information on schemes and subsidies.

- **AI Chatbot Assistance**  
  Multi-lingual chatbot (English, Hindi, Marathi…) for on-the-spot help with queries and guidance.

- **Appointment Booking**  
  Schedule soil sample tests with nearby laboratories.

- **Responsive UI**  
  Clean, mobile-first interface built using shadcn/ui components.

## 🎯 Getting Started

### 1. Prerequisites

- Node.js (v16+)
- Python (3.8+) & Flask
- Jupyter Notebook (for dataset preprocessing / model training)
- `.env` file with:
  ```
  OPENWEATHER_API_KEY=your_api_key
  SOIL_API_KEY=your_api_key
  ```
- Optional: credentials or endpoints for soil testing & pricing APIs

### 2. Installation

```bash
# Clone the repo
git clone https://github.com/yourusername/crop-bug-detection.git
cd crop-bug-detection

# Frontend
cd frontend
npm install

# Backend
cd ../backend
pip install -r requirements.txt
```

### 3. Running Locally

```bash
# Frontend
cd frontend
npm run dev

# Backend
cd backend
flask run
```

Visit `http://localhost:3000` to see the app in action.

### 4. Model Training & Data

In `notebooks/crop_analysis.ipynb`, you'll find preprocessing scripts and ML model training examples. To retrain:

1. Populate `data/` folder (e.g., leaf/tissue analysis, test datasets).
2. Run notebook to output `models/*.pkl`.
3. Load into Flask API for dynamic inference.

## 🧱 Project Structure

```
/
├── frontend/         # React / Next.js UI
├── backend/          # Flask APIs for detection & advisory
|   ├── app.py
|   ├── requirements.txt
|   └── models/
│       └── crop_model.pkl
├── notebooks/        # Data preprocessing & model training
├── data/             # Raw and processed datasets
└── docs/             # Design specs, deployment guides
```

## 🔧 How It Works

### Crop/Disease Detection

1. User uploads an image via frontend.
2. Frontend sends to Flask `/predict` endpoint.
3. Flask uses a pre-trained ML model (e.g. CNN) to infer disease/pest presence.
4. Returns disease name and confidence score to the UI.

### Crop Recommendation

1. User inputs soil parameters (NPK, pH, moisture, location).
2. Frontend POSTs to `/recommend`.
3. Flask applies rule-based or trained model logic to suggest top crops.
4. Returns best-fit crops + expected yields.

## 🧠 AI Components (Simulated 🔧)

We simulated the AI logic; to add real AI:

- **Model training**  
  Use scikit‑learn/PyTorch in Jupyter notebooks.

- **Weather & Market APIs**  
  Integrate with OpenWeatherMap, AgriMarket, or local data sources.

- **Chatbot**  
  Connect with ChatGPT or any LLM via OpenAI API and embed in the frontend.

## 🗣 Languages & Transliteration

- Multi-language UI (EN, HI, MR).  
- Use `i18n/` for text translation.  
- Connect chatbot to translations for natural-language support.

## ✅ Next Steps

- Deploy real ML/DL prediction pipelines  
- Integrate external APIs (weather, market, soil labs)  
- Add authentication & farmer user profiles  
- Support more regional languages  
- Include push notifications & offline mode

## 📄 License & Contributing

This project is under the **MIT License**. Contributions, bug reports, and feature requests are welcome—simply open an issue or submit a PR!

## 🙏 Acknowledgments

- Built using Vercel, Flask, React, and shadcn/ui  
- Inspired by open-source systems like AgroFriend & Crop Guard

## 🎯 Contact

For questions or feedback, reach out at `your.email@example.com`.

**Happy farming and AI to your fields!**
