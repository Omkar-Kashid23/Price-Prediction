# Price Prediction Machine Learning Pipeline

An end-to-end Machine Learning project designed to predict prices based on historical data. This project is built with a highly modular, production-ready architecture, featuring automated data pipelines, comprehensive logging, exception handling, and a web interface for making real-time predictions.

## 🚀 Features

* **Modular Architecture:** Clean separation of concerns using a component-based structure (Data Ingestion, Transformation, Model Training, and Evaluation).
* **End-to-End Pipeline:** Automated training and prediction pipelines.
* **Web Interface:** A user-friendly front-end (HTML/CSS/JS) integrated with a backend web framework to serve predictions.
* **Containerization:** Fully Dockerized setup with `docker-compose` for seamless deployment across any environment.
* **Robust Tracking:** Built-in custom logging and exception handling for easy debugging and monitoring.

## 📂 Project Structure

The repository follows a standard MLOps directory structure:

```text
├── artifacts/              # Contains generated preprocessors, models, and transformed datasets
├── src/                    # Main source code directory
│   ├── components/         # Core ML modules (ingestion, transformation, trainer, pusher)
│   ├── entity/             # Data classes for configuration and artifact entities
│   ├── pipeline/           # Training and prediction pipeline logic
│   ├── exception.py        # Custom exception handling
│   ├── logger.py           # Custom logging configuration
│   └── utils.py            # Helper functions and utilities
├── static/                 # CSS and JavaScript files for the web interface
├── templates/              # HTML templates for the frontend
├── app.py                  # Main web application entry point (Flask/FastAPI)
├── main.py                 # Script to trigger the training pipeline
├── Dockerfile              # Docker image configuration
├── docker-compose.yml      # Multi-container Docker setup
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation

```

## 🛠️ Installation & Setup

### Option 1: Local Development Setup

1. **Clone the repository:**
```bash
git clone [https://github.com/Omkar-Kashid23/Price-Prediction.git](https://github.com/Omkar-Kashid23/Price-Prediction.git)
cd Price-Prediction

```


2. **Create and activate a virtual environment:**
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate

```


3. **Install dependencies:**
```bash
pip install -r requirements.txt

```



### Option 2: Docker Setup (Recommended)

If you have Docker installed, you can spin up the entire application without configuring a local Python environment.

```bash
docker-compose up --build

```

## 💻 Usage

**To train the model:**
Run the main script to trigger the data ingestion, transformation, and model training pipelines. This will generate the latest models inside the `artifacts/` folder.

```bash
python main.py

```

**To start the web application:**
Run the app server to access the user interface and generate predictions.

```bash
python app.py

```

*Once running, open your web browser and navigate to `http://localhost:5000` (or the port specified in your terminal).*

## 📊 Model & Data

* **Data Preprocessing:** Handled dynamically via `src/components/data_transformation.py`. The preprocessor object is saved as a `.joblib` file.
* **Model Training:** The best-performing model is automatically selected, saved, and pushed to the `prediction/models/` directory for inference.

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a Pull Request if you'd like to improve the model accuracy, add new features, or optimize the pipeline.

## 👤 Author

**Omkar Kashid**

* GitHub: [@Omkar-Kashid23](https://www.google.com/search?q=https://github.com/Omkar-Kashid23)
