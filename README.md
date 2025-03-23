
# 🌦️ AI-Powered Weather Summary ETL Pipeline (Hugging Face + Azure)

This project is a lightweight, cloud-native ETL pipeline that extracts real-time weather data from the Weatherstack API, generates human-readable summaries using Hugging Face Transformers, and uploads the final output to Azure Blob Storage.

---

## 🔧 Tech Stack

- **Language**: Python
- **Notebook**: Google Colab (for development)
- **API**: [Weatherstack API](https://weatherstack.com/)
- **NLP Model**: Hugging Face `t5-small`
- **Cloud**: Azure Blob Storage

---

## 🔁 End-to-End Workflow

1. **Extract**  
   Fetch real-time weather data for multiple cities from Weatherstack API.

2. **Transform**  
   Clean and format the weather data into a structured format.

3. **AI Summary**  
   Use Hugging Face's `t5-small` model to generate a readable weather summary.

4. **Load**  
   Save the data as a `.csv` file and upload it to Azure Blob Storage.

---

## 📦 Output Example

| City      | Temperature (°C) | Humidity (%) | Sky Description | Weather Summary                             |
|-----------|------------------|---------------|------------------|----------------------------------------------|
| New York  | 14               | 72            | Partly cloudy     | It is partly cloudy with a temperature...    |

---

## 🧪 How to Run

1. Open the Colab notebook.
2. Set your environment variables manually inside Colab:

```python
os.environ['WEATHERSTACK_API_KEY'] = 'your_api_key'
os.environ['AZURE_STORAGE_CONNECTION_STRING'] = 'your_connection_string'
```

3. Run the notebook cells step-by-step.
4. Files will be saved locally and uploaded to your Azure Blob container.

---

## 📁 Project Structure

```
📦 AI_Weather_ETL/
├── Azure_AI_ETL_weather_summary.ipynb     # Main notebook
├── weather_summary_<city>.csv             # Output files
├── README.md                              # This file
```

---

## 🌍 Future Enhancements

- Automate daily runs using Azure Functions (Timer Trigger)
- Add scheduling and alerting based on weather patterns
- Build a Power BI dashboard using the CSVs stored in Blob

---

## 🙋‍♂️ Author

**Tirth Bhatt**  
Data Engineer | Azure Certified | Power BI Developer  
[LinkedIn](https://www.linkedin.com/in/tirthbhatt9) • [GitHub](#)

---
