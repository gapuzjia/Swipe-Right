# Swipe Right 🎯

**Swipe Right** is a web app that helps students discover campus clubs they might be interested in — using a swipe-based interface similar to Tinder, but for student organizations at San Diego State University!  
The more you swipe, the smarter the app becomes, using machine learning to recommend better club matches based on your preferences.

## 🚀 Features
- **Swipe to Match**: Swipe right if you like a club, left if you don't.
- **Tag-Based Filtering**: Choose interests like STEM, Leadership, Arts, etc., to start with personalized club options.
- **Live Learning**: The app uses Logistic Regression to continuously learn from your swipes and improve recommendations.
- **Saved Clubs**: See a beautiful "stacked card" view of the clubs you've liked.
- **Mock Chat System**: Chat button on each liked club (demo only) for a future real messaging feature.

## 🛠️ How It Works
1. **Profile Setup**: Users first select tags that describe their interests.
2. **Swiping**: Clubs matching the selected tags are shown one by one. Swiping right records a "like," swiping left records a "dislike."
3. **Machine Learning**:
   - After each swipe, the app trains a simple **Logistic Regression model**.
   - The model learns relationships between user-selected tags and club tags.
   - Over time, it predicts new clubs the user might like based on learned patterns.
4. **Saving Preferences**: Clubs the user liked are saved and displayed at the end.

## 🧠 Technologies Used
- **Flask** — Python web framework
- **HTML/CSS/JavaScript** — Frontend design
- **Joblib** — For loading the trained logistic regression model
- **Scikit-Learn** — Machine learning (Logistic Regression)
- **CSV/JSON** — For saving training data and club info

## 📂 Project Structure
```
/static
    /images          ← swipe card images
    /style.css       ← all page styling

/templates
    profile.html     ← tag selection page
    index.html       ← swipe page
    saved.html       ← liked clubs page
    chat.html        ← mock chat overlay

app.py               ← main Flask backend
clubs.json           ← all club info
training_data.csv    ← stores user swipes for ML training
club_model.pkl       ← saved logistic regression model
train_model.py       ← retraining script
```

## ⚡ Setup Instructions
1. Install required Python packages:
   ```
   pip install flask scikit-learn joblib
   ```
2. Run the Flask app:
   ```
   python app.py
   ```
3. Open a browser and go to `http://localhost:5000/`.

## 📈 Future Improvements
- Add real-time chat functionality
- Smarter tag grouping and recommendations
- Multi-user support
- Admin dashboard for club management

## 🎉 Why It's Cool
Unlike a static directory of clubs, **Swipe Right** gets better the more you use it.  
It's fast, visual, and *personalized* — making finding a club feel less overwhelming and more fun!
