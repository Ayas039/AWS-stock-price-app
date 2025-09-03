
# 📈 Stock Lookup Application (AWS-Deployed)

A lightweight web app that retrieves real-time U.S. stock prices using the Alpha Vantage API.  
Built with vanilla **HTML/CSS/JavaScript** and deployed on **AWS EC2**.
---

##  Project at a Glance (What I did)

- Designed a minimal, accessible UI to search by ticker (e.g., `AAPL`, `MSFT`).
- Integrated **Alpha Vantage** (Global Quote endpoint) to fetch live prices.
- Implemented input validation & clear error messaging for invalid tickers.
- Added console logging for easy debugging & demo verification.
- Deployed to **AWS EC2 (t2.micro)** and verified with screenshots of the live app + instance details.
- Documented how to run locally and how to redeploy.

## 🧩 Tech Stack

- **Frontend:** HTML, CSS, JavaScript (no frameworks)
- **API:** Alpha Vantage (Global Quote)
- **Cloud:** AWS EC2 (Windows Server in my demo; any OS works)
- **Tools:** Git/GitHub, Browser DevTools, RDP/SSH


## 🎯 Features

- Search by U.S. ticker; display current price.
- Graceful handling of invalid tickers with user-friendly messages.
- Simple, responsive layout; easy to extend.
- Console logs show request/response for verification during demos.


## 🗂️ Repository Structure
stock-lookup-app/
│── index.html # Main page (UI)
│── style.css # Styling for the app
│── app.js # API call + render + error handling
│── screenshots/ # UI, valid/invalid states, AWS proof
│── README.md # This document

---

## ⚙️ Setup & Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/stock-lookup-app.git
   cd stock-lookup-app

2.**Open the app locally**
Double-click index.html (or open it in your browser).

3. **Get an API key**
Sign up for a free key at Alpha Vantage: https://www.alphavantage.co/support/#api-key

4.**Configure the key**
In app.js, replace YOUR_API_KEY with your key:
const response = await fetch(
  `https://www.alphavantage.co/query?function=GLOBAL_QUOTE&symbol=${ticker}&apikey=YOUR_API_KEY`
);
5.**Use the app**
Enter a ticker like AAPL and click Get Stock Data.

**Deployment on AWS**

Hosted on an EC2 instance (t2.micro).

Configured security groups to allow inbound HTTP (port 80).

Uploaded source files and tested app in browser.

**Future Improvements**

Add company name, daily % change, and OHLC data.

Include stock charts using Alpha Vantage time series.

Deploy on AWS S3 + CloudFront for scalable hosting.

Add unit tests for API and UI validation.

 **Skills Demonstrated**

Frontend development (HTML, CSS, JavaScript)

API integration & error handling

Cloud deployment on AWS EC2

Debugging with browser console

Documentation & GitHub version control
