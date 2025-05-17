## 🛫 AI Travel Agent

The **AI Travel Agent** is a Streamlit-based application that generates **personalized travel itineraries** using **OpenAI’s GPT-4o**.  
It automates travel research, planning, and scheduling—helping you design your perfect trip with minimal effort.

---

## 🚀 Features

- 🌍 Discover travel destinations, activities, and accommodations
- 📅 Customize itineraries based on your travel duration
- 🧠 Generate intelligent, personalized plans powered by GPT-4o
- 📥 Download itineraries as a **calendar (.ics) file**
- 📆 Import plans into Google Calendar, Apple Calendar, Outlook, and more

---

### How to get Started?

1. Clone the GitHub repository

```bash
git clone https://github.com/dhvanil16/ai_data_analysis_agent.git
```
2. Install the required dependencies:

```bash
pip install -r requirements.txt
```
3. Get your OpenAI API Key

- Sign up for an [OpenAI account](https://platform.openai.com/) (or the LLM provider of your choice) and obtain your API key.

4. Get your SerpAPI Key

- Sign up for an [SerpAPI account](https://serpapi.com/) and obtain your API key.

5. Run the Streamlit App
```bash
streamlit run travel_agent.py
```

For local LLM usage (with Ollama):
```bash
streamlit run local_travel_agent.py
```

### 🔄 How it Works?

The AI Travel Agent operates through a two-stage intelligent workflow:

1. **Researcher Component**
   - Analyzes your destination and travel duration to generate targeted search queries
   - Uses SerpAPI to search the web for relevant activities, attractions, dining options, and accommodations
   - Collects comprehensive travel information from multiple sources
   - Returns curated results for the planning stage

2. **Planner Component**
   - Processes researcher findings combined with your personal preferences
   - Leverages GPT-4o to intelligently synthesize the information into a cohesive itinerary
   - Generates day-by-day activity recommendations with timing and location details
   - Creates dining suggestions and accommodation recommendations
   - Produces a ready-to-use travel plan

---

### 📥 Download Itinerary as Calendar

Convert your AI-generated itinerary into a calendar file for easy access across all your devices:

**Steps to Download:**
1. After generating your itinerary, locate the "Download Itinerary as Calendar (.ics)" button
2. Click to download the file to your computer
3. Open the .ics file with your preferred calendar application:
   - **Google Calendar**: Upload via Settings → Import & Export
   - **Apple Calendar/iCal**: Double-click the file to auto-import
   - **Outlook**: File → Open → Calendar file → Select the .ics file
   - **Other apps**: Most calendar apps support .ics format

**Benefits:**
- Each day appears as an all-day event with complete activity details
- Full itinerary details stored in event descriptions
- Access your travel plans offline on all devices
- Automatic sync across synced calendar apps

---

### 🖥️ Deployment Options: Cloud vs Local

Choose the version that best fits your needs:

| Feature | Cloud Version | Local Version |
|---------|---------------|---------------|
| **Script** | `travel_agent.py` | `local_travel_agent.py` |
| **LLM Model** | OpenAI GPT-4o | Ollama (Local) |
| **API Key Required** | OpenAI API key | None (runs locally) |
| **Data Privacy** | Sent to OpenAI | Stays on your machine |
| **Quality** | Production-grade responses | Good local performance |
| **Setup Complexity** | Simple (API key only) | Requires Ollama installation |
| **Best For** | Production use, best quality | Development, privacy-focused, offline |

**Quick Selection Guide:**
- ✅ Use **travel_agent.py** if you want the best quality itineraries and don't mind using the cloud
- ✅ Use **local_travel_agent.py** if you prefer data privacy or want to run without internet dependency