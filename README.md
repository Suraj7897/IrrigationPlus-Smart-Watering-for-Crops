# **Crop-Specific Smart Irrigation System with IoT** 🌱💧

**A smart and efficient irrigation system powered by IoT to optimize crop watering based on real-time data!**

## 📌 **Overview**
This project implements a smart irrigation system using **ESP32** microcontrollers to measure soil moisture, temperature, and rain detection in real-time. The system automatically adjusts water output based on predefined crop categories and moisture levels, ensuring efficient and automated irrigation.

Data is sent to Firebase Realtime Database, allowing for easy monitoring and control of irrigation motors. This system reduces water wastage and maximizes crop health by catering to each crop’s water requirements.

## 🔥 **Features**
- ✅ **Automated Irrigation**: Adjusts motor speed based on real-time environmental data for efficient watering.  
- ✅ **Weather-Adaptive**: Pauses irrigation if rain is detected to save water.  
- ✅ **Crop-Specific Watering**: Customizable water requirements for different crop categories.  
- ✅ **Firebase Integration**: Uses Firebase Realtime Database to upload and retrieve sensor data.  
- ✅ **Real-time Monitoring**: Tracks soil moisture, temperature, and rain status for better decision-making.

## 🛠 **Technologies Used**
- **Hardware**:
    - **ESP32 Microcontroller (2x)**
    - **DHT11 Temperature & Humidity Sensor**
    - **Soil Moisture Sensor** (Analog)
    - **Rain Sensor** (Analog)
    - **Motor Driver Module** (e.g., L298N)
    - **12V DC Motor for irrigation

- **Software**:
    - **Arduino IDE**
    - **Firebase ESP Client Library**
    - **DHT Sensor Library**
    - **Firebase Realtime Database**

- **Communication**:
    - **Wi-Fi**

## 🚀 **Getting Started**

### **1. Prerequisites**
- Install **Arduino IDE** (v1.8.13 or later)
- **ESP32** board support in Arduino IDE
- **Firebase Credentials** (API Key, Database URL)

### **2. Setup Instructions**

#### **Step 1**: Set Up Firebase Project
- Create a Firebase project in the [Firebase Console](https://console.firebase.google.com/).
- Enable **Realtime Database** and set appropriate read/write permissions for testing.
- Get your **Firebase API Key** and **Database URL**.

#### **Step 2**: Configure Arduino IDE
- Install **ESP32** board support via Arduino’s Board Manager.
- Install the following libraries via Arduino IDE:
  - **Firebase ESP Client Library**
  - **DHT Sensor Library**

#### **Step 3**: Upload Code
- Open the code files provided in this project.
- Customize the **Wi-Fi credentials**, **Firebase API Key**, and **Database URL** in the code.
- Upload the **Sensor Node Code** to the first ESP32 (to collect data).
- Upload the **Motor Control Node Code** to the second ESP32 (to control irrigation).

### **3. Usage**
- **Power on** both ESP32 modules.
- Monitor the **Serial Output** for real-time data sent/received to/from Firebase.
- The **Sensor Node** reads data from the DHT11 sensor, soil moisture sensor, and rain sensor, uploading the values to Firebase.
- The **Motor Control Node** adjusts motor speed based on crop water requirements and environmental conditions (soil moisture, temperature, and rain).

## 🧑‍🌾 **How It Works**
**Sensor Node**:
- Collects temperature from DHT11, moisture level from soil sensor, and rain status.
- Uploads data to Firebase every 10 seconds.

**Motor Control Node**:
- Reads crop category and sensor data from Firebase.
- Adjusts motor speed based on conditions:
  - **Low Moisture**: Highest motor speed
  - **Medium Moisture**: Moderate motor speed
  - **High Moisture or Rain Detected**: Stops motor

## 🌱 **Crop Categories & Water Requirements**
You can define custom crop categories in Firebase, each with specific water needs:
- **Category 1**: Low water requirement
- **Category 2**: Medium water requirement
- **Category 3**: High water requirement

![webpage](https://github.com/user-attachments/assets/62960013-aa2b-4ada-8ad9-182b9ad39e8b)
![Mobile_App](https://github.com/user-attachments/assets/36689b54-d07c-421b-a706-f1646977fff9)
![Schenmatic](https://github.com/user-attachments/assets/ae97e739-2b7c-4ba0-962f-2932c1c01ea2)
![PCB](https://github.com/user-attachments/assets/0c5786e5-6f57-4316-a5a9-0d05b85c1812)
![Sih -1 4](https://github.com/user-attachments/assets/0c5fd089-fb4a-418d-9560-72677863ee88)



## 🔮 **Future Improvements**
- **Weather Forecasting**: Integrate with online weather APIs for better watering scheduling.
- **Battery Optimization**: Implement power-saving modes to extend battery life for mobile setups.
- **Enhanced Security**: Add **user authentication** and more secure database access rules for production-ready applications.

## 🤝 **Contributing**
Contributions to improve the project are welcome! Please feel free to:
- Open issues for bugs or feature requests.
- Submit pull requests for new features or improvements.

### **To Contribute**:
1. Fork the repository.
2. Clone the forked repository.
3. Create a new branch for your feature or fix.
4. Make changes and test thoroughly.
5. Submit a pull request detailing your changes.


