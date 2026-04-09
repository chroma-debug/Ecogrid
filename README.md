# EcoGrid

**EcoGrid** is a zero-backend, AI-powered home energy calculator that helps users track, visualize, and reduce their carbon footprint. By leveraging Llama 3.3 and live weather data, EcoGrid delivers hyper-personalized, location-aware energy insights that turn behavioral psychology and cost-saving incentives into real-world climate action.

![EcoGrid Preview](https://via.placeholder.com/800x400.png?text=EcoGrid)

## Features
- 🌍 **Global Grid Data:** Auto-detects location via the Nominatim Geocoding API to dynamically calibrate calculations using accurate local power grid CO₂ emission factors and energy prices across 22+ countries.
- 🧠 **AI Power Estimates & Insights:** Integrates the Groq API for intelligent energy audits. The AI receives the user's appliance list and live local weather, generating tactical recommendations to reduce consumption based on current conditions.
- ⚡ **Zero-Backend Architecture:** Entirely frontend (HTML/CSS/JS). No databases or user accounts are required, meaning zero deployment overhead and maximum privacy. 
- 📤 **Shareable Eco-Grade:** Generates an instantly downloadable "Eco Report Card" grading the household against the national average, gamifying climate action.

## Quickstart

Since EcoGrid runs entirely in the browser, no installation or build steps are required. 

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ecogrid.git
   cd ecogrid
   ```
2. **Add your Groq API Key** (Required for AI insights and appliance wattage estimation). Create a new file in the root directory named `env.js` and paste your key inside:
   ```javascript
   // env.js
   window.ENV_GROQ_KEY = 'YOUR_GROQ_API_KEY_HERE';
   ```
3. Double click `index.html` to open it in your browser!

### Adding Custom API Logic
If you want to bake the API key directly into the code or use a different endpoint (e.g. standard OpenAI or a generic backend wrapper instead of Groq), simply open `index.html` and modify the config block at the bottom of the file:
```javascript
// ─── CONFIG ───────────────────────────────────────────────────────────────
const GROQ_KEY = window.ENV_GROQ_KEY || 'YOUR_GROQ_API_KEY';
const GROQ_MODEL = 'llama-3.3-70b-versatile';
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
MIT
