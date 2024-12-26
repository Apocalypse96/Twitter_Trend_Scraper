# Twitter Trend Scraper
[Screencast from 2024-12-27 03-29-43.webm](https://github.com/user-attachments/assets/3f5860fe-c0a9-45f1-96a4-1d5eb532a30a)


Twitter Trend Scraper is a tool that automates the process of fetching the top 5 trending topics from Twitter's "What’s Happening" section using Selenium and ProxyMesh, stores the data in MongoDB, and displays the results on a webpage.

---

## Installation and Setup Guide

### Step 1: Clone the Repository

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/Apocalypse96/Twitter_Trend_Scraper.git
cd Twitter_Trend_Scraper
```

### Step 2: Install Dependencies

Use the following command to install all necessary Python dependencies:

```bash
pip install -r requirements.txt
```

### Step 3: Set Up Twitter Credentials

1. Use an existing Twitter account or create a new one.
2. Update the Selenium script (`main.py`) with your Twitter login credentials (username and password).

### Step 4: Configure ProxyMesh

1. Sign up for a ProxyMesh account.
2. Add your ProxyMesh credentials and proxy URL to the script.

### Step 5: Set Up MongoDB

1. Install MongoDB locally or use a cloud service like MongoDB Atlas.
2. Update the connection string in the script to point to your MongoDB instance.

### Step 6: Create .env file

```
MONGODB_URI=
PROXYMESH_HOST=
PROXYMESH_PORT=
TWITTER_USERNAME=
TWITTER_PASSWORD=
```

### Step 7: Run the Application

Launch the scraper using the following command:

```bash
python src/app.py
```

---

## Data Structure in MongoDB

The scraped data is stored in a MongoDB collection with the following fields:

- **unique_id**: A unique identifier for each run.
- **trend_1 to trend_5**: Names of the top 5 trending topics.
- **timestamp**: The date and time when the script finished execution.
- **ip_address**: The IP address used during the scraping process.

---

