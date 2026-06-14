# 🤖 HappyBot Backend

AI-powered chatbot backend built using Flask, TensorFlow, NLTK, and MongoDB. HappyBot understands user messages, predicts user intent using a trained neural network model, and provides intelligent responses. It also supports retrieving product information dynamically from a MongoDB database.

## 🎥 Project Demonstration

[![Watch Demo]](https://www.youtube.com/watch?v=hqYs3jjgwXI)

---

## 🚀 Features

- Intent-based chatbot responses
- Natural Language Processing (NLP)
- TensorFlow/Keras neural network model
- Product information retrieval from MongoDB
- REST API architecture
- Cross-Origin Resource Sharing (CORS) enabled
- Easy integration with web and mobile frontends

---

## 🛠️ Technology Stack

### Backend
- Python
- Flask
- Flask-CORS

### Machine Learning
- TensorFlow / Keras
- NLTK
- NumPy

### Database
- MongoDB

### Data Storage
- Pickle (.pkl) files
- JSON intents dataset

---

## 📂 Project Structure

```bash
Models/
│
├── app.py                 # Main Flask application
├── database.py            # MongoDB connection configuration
├── intents.json           # Chatbot intents and responses
├── training.py            # Model training script
├── chatbot_model.model    # Trained neural network model
├── words.pkl              # Vocabulary dataset
├── classes.pkl            # Intent classes
└── requirements.txt       # Project dependencies
```

---

## ⚙️ How It Works

### 1. User Message

The user sends a message through the frontend application.

Example:

```json
{
  "message": "Tell me about Smart Sensor"
}
```

### 2. Text Processing

The chatbot:

- Tokenizes the sentence
- Lemmatizes words using NLTK
- Converts text into a Bag-of-Words representation

### 3. Intent Prediction

The processed data is passed to a trained TensorFlow model which predicts the most likely intent.

### 4. Response Generation

#### General Conversation

The bot returns predefined responses from `intents.json`.

#### Product Information

The bot:

- Extracts the product name
- Searches MongoDB
- Returns product details such as:
  - Device Name
  - Price
  - Availability
  - Description

---

## 🗄️ Database Integration

MongoDB is used to store IoT device information.

Example document:

```json
{
  "deviceName": "Smart Sensor",
  "price": 99.99,
  "availability": "Available",
  "description": "Wireless smart monitoring device."
}
```

---

## 🔌 API Endpoint

### POST /chat

#### Request

```json
{
  "message": "Tell me about Smart Sensor"
}
```

#### Response

```json
{
  "bot_response": "Smart Sensor is available for $99.99..."
}
```

---

## 📦 Installation

### Clone Repository

```bash
git clone https://github.com/IT21224348/irwa_happybot_BackEnd.git
cd irwa_happybot_BackEnd
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

```bash
python app.py
```

Server will start at:

```bash
http://localhost:5000
```

---

## 🧠 Machine Learning Pipeline

1. Collect training data from `intents.json`
2. Preprocess text using NLTK
3. Train TensorFlow neural network
4. Save:
   - chatbot_model.model
   - words.pkl
   - classes.pkl
5. Load model during runtime

---

## 🔮 Future Improvements

- Context-aware conversations
- Multi-language support
- Voice assistant integration
- Recommendation engine
- Sentiment analysis
- User authentication
- Chat history storage

---

## 👨‍💻 Author

### H.D.S. Ravindu Sulakkana

- BSc (Hons) Information Technology – SLIIT
- Aspiring Data Engineer & AI Enthusiast
- Interested in Machine Learning, Data Engineering, and Intelligent Systems

## ⭐ Support

If you found this project useful, consider giving it a star ⭐ on GitHub.

---

## 📄 License

This project is developed for educational and research purposes.

Feel free to fork, modify, and extend this project according to your requirements.
