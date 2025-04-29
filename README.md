---

# 💳 Bytehash Labs Assignment – Credit Card Data Extractor

This Streamlit app allows you to **scrape websites** or **upload PDFs** and automatically **extract structured credit card data**.

---

## 🚀 Features

- 🔍 Scrape content from a **website URL**
- 📄 Upload and process **PDF files**
- 🤖 Extract structured data using **Gemini 1.5 Pro**
- 📦 Output JSON in a clean, grouped format:
  - `card_name`
  - `issuing_bank`
  - `joining_fee`
  - `annual_fee`
  - `reward_structure`
  - `cashback_offers`
  - `interest_rate`
  - `credit_limit`
  - `eligibility_criteria`
  - `other_features`
- 📥 Download structured data as a JSON file

---

## 🛠 Installation

1. **Clone this repository**:
   ```bash
   git clone https://github.com/anim2403/bytehash_labs.git
   cd bytehash_labs
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🧪 Requirements

See `requirements.txt` for the full list. Main dependencies:

```txt
streamlit
requests
beautifulsoup4
PyPDF2
google-generativeai
```

---

## 🔐 Setup

1. Get your **Google Gemini API key** from:  
   👉 [https://makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey)

2. Paste the API key into the **Streamlit sidebar** when prompted.

---

## ▶️ Run the App

```bash
streamlit run main.py
```

Then open the URL shown in your terminal (typically `http://localhost:8501`).

---

## 📤 Output

The structured output is shown in the **"Structured Data"** tab and can be downloaded as a `JSON` file.

Example JSON format:
```json
{
  "cards": [
    {
      "card_name": "XYZ Platinum Card",
      "issuing_bank": "XYZ Bank",
      "joining_fee": "₹500",
      "annual_fee": "₹999",
      "reward_structure": "...",
      "interest_rate": "3.5% per month",
      "other_features": ["Lounge access", "Travel insurance"]
    }
  ]
}
```

---

## 📁 Sample Data

Sample webpages for testing:

- [Finology Credit Cards](https://select.finology.in/credit-card)
- [American Express Rewards Cards](https://www.americanexpress.com/in/credit-cards/card-types/rewards-cards/?intlink=in-en-hp-product2-pr-rewardscards-25032021)
- [Best Credit Cards in India – CardExpert](https://www.cardexpert.in/best-credit-cards-india/)

📄 A sample PDF is also available in the `sample/` folder.

---

## 📌 Notes

- Gemini API has a character limit (~30,000 tokens). Content is truncated automatically.
- Works best on clean, structured data (e.g., product listing pages or financial brochures).

---

## 📄 License

MIT License – Free to use and modify.

---

Let me know if you’d like to include usage screenshots or a GIF demo of the app!
