# CropCare AI

AI-powered crop disease detection and soil/weather insights for farmers. A React (Vite) frontend talks to a Flask + PyTorch (ResNet9) API that classifies 38 plant disease classes from a leaf photo.

## Features

- Leaf image upload with disease prediction and pesticide guidance
- Soil analysis insights
- Weather guidance and nearby agro-store lookup
- Multi-language UI (English, Spanish, French, Hindi)

## Run Locally

```bash
# frontend
npm install
npm run dev

# backend (separate terminal)
pip install -r requirements.txt
python api.py
```

## Build For Production

```bash
npm run build
npm run preview
```

## Deployment

- **Frontend:** GitHub Pages, deployed by GitHub Actions on every push to `main`.
- **Backend:** Render (`render.yaml`). The API needs `plant-disease-model-complete (1).pth` in the repo root.
- Set the repository variable `VITE_API_BASE_URL` to your Render URL so the built site calls the live API.

## API Endpoints

- `POST /predict` – disease detection from an uploaded image
- `POST /analyze-soil` – soil insights
- `GET /health` – health check
