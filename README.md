# 🚗 APP

This project is a Django-based backend application that calculates the most cost-effective route between two USA locations.

## 🌟 Features
* **Optimal Routing:** Uses OSRM API to find the best path between locations.
* **Fuel Cost Calculation:** Based on real fuel price data (CSV import).
* **Interactive Visualization:** Generates a route map using Folium with fuel stops markers.
* **Safety Buffer:** Fuel stops are calculated every 450 miles (for a 500-mile range vehicle).

---

## 🚀 Getting Started

### 1. Prerequisites
* Python 3.x
* A virtual environment (recommended)

### 2. Installation & Setup
Follow these steps to get the project running locally:

1. **Extract the ZIP file** and navigate to the project folder.
2. **Create a virtual environment**:
   python -m venv venv
3. **activate virtual environment**
   #### Windows:
   venv\Scripts\activate
   #### Mac/Linux:
   source venv/bin/activate
4. **Install dependencies** : pip install -r requirements.txt
5. **Apply Migrations**: 
    - python manage.py makemigrations
    - python manage.py migrate

6. **Import Fuel Data (Import prices from the provided CSV)**:
     python manage.py load_fuel.py
7. **Run the Server:** python manage.py runserver

## API Endpoint (JSON) : 
  **URL**: http://127.0.0.1:8000/api/
  
  **Method**: POST
  
  **Body (JSON)**:  
  Example : 
  {
    "start": "New York, NY",
    "finish": "Miami, FL"
  }

                      
