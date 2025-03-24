# Node-RED-Weather-Dashboard
This project is a weather monitoring dashboard built using Node-RED, integrating OpenWeather API to fetch real-time weather data. The dashboard allows users to input a location (city/country or latitude/longitude), customize update intervals, visualize weather parameters, and set warning limits for specific conditions.

---

## **Technologies Used**
- **Node-RED** – Flow-based programming tool for IoT and automation.
- **OpenWeather API** – Retrieves real-time weather data.
- **JavaScript (within Node-RED)** – Handles data processing.

---

## **Project Functionality**
This project consists of **six flows**, each handling a different aspect of the weather dashboard.

### **1. Main Flow**
- Accepts **user input** (city/country or latitude/longitude).
- Calls **OpenWeather API** to fetch weather details.
- Displays the **current location name** (not coordinates) based on user input.

### **2. Show/Hide Group Flow**
- Dynamically **shows or hides UI elements** based on user selections.
- Allows toggling between **city/country input and latitude/longitude input**.
- Helps keep the dashboard clean by showing only relevant fields.

### **3. Update Interval Flow**
- Allows users to set a **custom update interval** for fetching weather data.
- Default interval: **30 seconds**.
- Users can change the interval using a **numeric input field**.

### **4. Temperature, Humidity, Pressure & Wind Flow**
- Updates **gauges** to display:
  - **Temperature** (°C)
  - **Humidity** (%)
  - **Pressure** (hPa)
  - **Wind Speed** (km/h)
  - **Wind Direction** (Compass-style gauge)
  - **Sunrise & Sunset times**
- Displays a **speaker icon** to provide **text-to-speech weather updates**.

### **5. Charts Flow**
- Plots **temperature, humidity, and wind speed** over the past hour.
- Users can **turn charts on/off** using a switch.
- Data is updated dynamically based on the selected interval.

### **6. Warning Limits Flow**
- Allows users to **set warning thresholds** for parameters like:
  - **Temperature**
  - **Pressure**
  - **Wind Speed**
- Uses a **dropdown** to select the parameter and a **slider** to set the limit.
- When a limit is exceeded, a **warning notification** appears (e.g., *“Warning! Temperature is 30°C. Exceeds the limit by 5°C”*).

---

## **Features**
✅ **Location Input** – Accepts city/country or latitude/longitude.  
✅ **Weather Updates** – Fetches real-time data from OpenWeather API.  
✅ **Custom Update Interval** – Allows users to set refresh intervals.  
✅ **Data Visualization** – Displays temperature, humidity, pressure, and wind conditions.  
✅ **Charts** – Plots weather parameters over time.  
✅ **Warning System** – Notifies users when a parameter exceeds its threshold.  
✅ **Text-to-Speech** – Reads out weather conditions on demand.  

---

## **How to Run This Project**

### **1. Install Node-RED**
Ensure Node.js is installed, then install Node-RED:
```sh
npm install -g --unsafe-perm node-red
```

### **2. Install Required Nodes**
Inside Node-RED, install:
- `node-red-dashboard` for UI components.
- `node-red-node-openweathermap` for API access.

Or manually install via command line:
```sh
npm install node-red-dashboard node-red-node-openweathermap
```

### **3. Import Node-RED Flows**
- Open Node-RED (`http://localhost:1880`).
- Go to **Menu → Import → Clipboard**.
- Paste the JSON file containing the flows.
- Deploy the flows.

### **4. Configure OpenWeather API**
- Sign up at [OpenWeather](https://openweathermap.org/) and get an **API key**.
- Enter the API key in the **OpenWeather API node**.

### **5. Start Node-RED**
Run the server:
```sh
node-red
```
Access the dashboard at:
```
http://127.0.0.1:1880/
```

---

## **Screenshots**
(*Attach images of your dashboard and Node-RED flows here.*)

---

